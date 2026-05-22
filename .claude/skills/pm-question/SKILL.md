---
name: pm-question
description: Generate a single PM interview practice question from this repo's plugin library, then evaluate the user's answer when they reply. Triggers on "ask me a PM question", "give me a practice question", "ask me a product roadmap question", "/pm-question", "PM question please", or any request for one practice question. Accepts optional category (e.g., product-roadmap, portfolio, debugging) and difficulty (easy/medium/hard).
---

# pm-question

Generate one PM interview practice question from the repo, present it to the user, and evaluate their answer when they reply.

## Resolving the repo root

The repo root is the directory containing `config.yaml`. Find it via:

1. If `$CLAUDE_PROJECT_DIR` is set and contains `config.yaml`, use that.
2. Else run `git rev-parse --show-toplevel`. If `config.yaml` is at that root, use it.
3. Else walk up from cwd looking for `config.yaml`.
4. If none found, tell the user: "Run this from inside the pm-interview-prep repo so I can find `config.yaml`."

All paths below are relative to that root.

## Step 1: Collect inputs

The user may have already specified category and/or difficulty in their message.

- **Category** (optional): one of the active category ids in `config.yaml`. Examples: `product-roadmap`, `portfolio`, `tech-application`, `conceptual`, `product-sense`, `goals-metrics`, `debugging`, `tradeoffs`. If not specified, pick a random active category.
- **Difficulty** (optional): `easy`, `medium`, or `hard`. Default: `medium`.

If the user invoked you without specifying difficulty, ask in one short message:

> "What difficulty? (easy / medium / hard — default medium)"

Don't ask about category if they didn't specify one; pick randomly. Random selection is intentional for unspecified categories.

If category is specified but invalid (not in config or has `active: false`), tell the user and list the valid active categories.

## Step 2: Load plugin files

Read `config.yaml` to confirm the category is active and get its `framework`, `time_limit`, and `folder`.

Then read:
- `<root>/plugins/<category>/generation-rules.md`
- `<root>/plugins/<category>/examples.md`

If the category has multiple framework files (e.g., `product-sense` has `framework-milejpsr.md` and `framework-circles.md`), pick one at random unless the question naturally fits one better.

## Step 3: Generate one question

Generate **exactly one** question following:
- The structure in `generation-rules.md` (selection pools, question template, required context)
- Style of the examples in `examples.md`
- The chosen difficulty:
  - **easy**: well-known product, fewer constraints, clearer scope. Lower stakes.
  - **medium**: standard difficulty per the plugin's `generation-rules.md`.
  - **hard**: complex constraints, ambiguous scope, multi-stakeholder tradeoffs, or a niche product.

Apply variety rules from `generation-rules.md`: don't reuse products that appear in the most recent files in `<root>/questions/<category>/`.

## Step 4: Save the question file

Filename: `ON_DEMAND-DAY-MM-DD-HHMM.md` where MM-DD is today's date and HHMM is 24-hour local time. If that exact filename already exists, suffix with `-2`, `-3`, etc.

Write to `<root>/questions/<category>/<filename>` with this frontmatter:

```yaml
---
date: YYYY-MM-DD
category: <category-id>
category_name: "<Display Name>"
framework: <framework_name>
framework_path: <absolute path to framework file>
time_limit: <minutes>
difficulty: <easy | medium | hard>
generated_by: pm-question
generated_at: <ISO 8601 timestamp>
---

# <Category Name> Question - <Day, Month DD, YYYY>

<Question text following the template from generation-rules.md, with all required context: current state, constraint, competitive landscape, strategic opportunity, etc.>

**Time Limit:** <X> minutes
**Framework:** <framework name>
**Framework location:** plugins/<category>/<framework-file>.md
```

## Step 5: Present and wait

Show the user in chat:
- The question (full text, not just "see the file")
- Framework name + repo-relative path
- Time limit
- Where the file was saved (repo-relative path)
- One closing line: "Reply with your answer when ready — paste it here, give me a local file path, or share a Google Drive link."

## Step 6: Evaluate the answer

When the user replies with their answer, follow the procedure in `.claude/skills/pm-evaluate/SKILL.md`. Pass the path to the question file you just created so the evaluator can load the right framework.

## Notes

- Difficulty levels for the user are easy/medium/hard. The existing Cowork-generated files use `medium / hard / very_hard`. Don't mix these vocabularies in the frontmatter you write — stick to easy/medium/hard.
- Never overwrite an existing file.
- Use absolute paths in `framework_path` (so pm-evaluate can load it directly).
