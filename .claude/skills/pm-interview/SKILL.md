---
name: pm-interview
description: Run a mock PM interview — multiple questions in sequence, with evaluation after each. Triggers on "run a mock interview", "set up a PM interview", "give me N questions", "/pm-interview", "let's do a mock", or any request to practice multiple questions in one session. Asks the user for question count, categories, and difficulty.
---

# pm-interview

Run a mock PM interview: N questions across one or more categories, sequential generate-answer-evaluate loop.

## Resolving the repo root

Same as `.claude/skills/pm-question/SKILL.md` — find the directory containing `config.yaml`.

## Step 1: Collect interview parameters

Ask the user in **one combined message**:

> "Mock interview setup. Three quick questions:
> 1. How many questions? (default 5)
> 2. Which categories? (one id, comma-separated list, or 'all')
> 3. Difficulty? (easy / medium / hard / mixed — default medium)
> 
> Or just say 'default' and I'll go with 5 questions, all categories, medium."

Valid category ids are the active ones in `config.yaml`: `product-roadmap`, `portfolio`, `tech-application`, `conceptual`, `product-sense`, `goals-metrics`, `debugging`, `tradeoffs`.

Validate the inputs before continuing. If the user gives an invalid category, list the valid ones and re-ask.

## Step 2: Plan the interview

Compute a question plan (list of `{category, difficulty}` tuples of length N).

- **Single category specified**: all N questions from that category.
- **List of categories**: distribute roughly evenly across them in randomized order.
- **"all"**: pick N categories at random from active ones (with replacement if N > number of active categories).
- **Difficulty = "mixed"**: roll per question — roughly 30% easy, 50% medium, 20% hard.

Avoid scheduling the same product twice across the interview (you'll check this at generation time in step 3).

Show the user the plan in one line and wait for "start" / "go" / "ready":

> "Plan: 5 questions — product-roadmap (medium), debugging (medium), goals-metrics (medium), product-sense (medium), tradeoffs (medium). Say 'go' when ready."

## Step 3: Run the loop

For each question in the plan:

1. **Announce** which question this is: "Question 1 of 5 — Product Roadmap (medium)."
2. **Generate** the question following steps 2-4 of `.claude/skills/pm-question/SKILL.md` (load plugin files, generate one question, save to `ON_DEMAND-DAY-MM-DD-HHMM.md`). Check earlier questions in this interview to avoid product collisions.
3. **Present** the question in chat (full text). Include framework name and time limit.
4. **Wait** for the user's answer (pasted text, local file path, or Google Drive link).
5. **Evaluate** following the full procedure in `.claude/skills/pm-evaluate/SKILL.md`. Save the answer file.
6. **Short result line** in chat: "Q1: 8/10 — Strong. Moving to Q2." Don't dump full feedback in chat — it's in the answer file.
7. **Offer a break** between questions (Q2 onward): "Want a 1-minute break before Q2? Say 'ready' or just give me your next answer." Skip this offer on the last question.

## Step 4: Final summary

After all N questions:

In chat, give:
- **Total score**: average across all N questions, e.g., "Average: 7.4/10 across 5 questions."
- **Per-category breakdown** (only if multi-category): "Product Roadmap: 8/10. Debugging: 6/10. Goals & Metrics: 8/10."
- **Top 2 strengths** synthesized across the answer files.
- **Top 2 improvement areas** synthesized across the answer files.
- **File pointer**: "All questions saved to `questions/<category>/ON_DEMAND-DAY-*.md`, all answers in `ON_DEMAND-ANSWER-*.md`."

## State

Keep interview state in conversation context. No scratch session file. If the user walks away mid-interview, the question and answer files already on disk are the durable record — pick up by reading those if asked later.

## Notes

- If the user wants to stop early, save what's been done and give a partial summary covering the questions completed.
- Don't generate two questions on the same product within one interview. If a collision happens, regenerate with a different product.
- Stick to the single chosen difficulty across the interview unless `mixed` was selected.
- All evaluation logic lives in `.claude/skills/pm-evaluate/SKILL.md`. Don't duplicate it here — follow that file.
