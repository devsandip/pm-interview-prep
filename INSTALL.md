# Installation Instructions

## What's Included

This folder contains a complete PM Interview Prep System with plugin architecture.

**30 files total:**
- 1 README
- 1 config file
- 3 core system files
- 25 plugin files (8 categories × 3 files each, plus product-sense has an extra framework file)
- 8 empty question folders (for generated content)

---

## Folder Structure

```
PrepQuestions/                           ← Copy this entire folder
├── README.md                            ← Read this first
├── config.yaml                          ← Category registry (what's active)
│
├── _core/                               ← Core system (NEVER update for new categories)
│   ├── plugin-schema.md                 ← Template for creating new plugins
│   ├── master-generator.md              ← Question generator (paste into Cowork)
│   └── evaluator.md                     ← Answer evaluator (paste into Cowork)
│
├── plugins/                             ← Self-contained category plugins
│   │  ── STRATEGIC ──
│   ├── product-roadmap/
│   │   ├── framework.md                 ← MATRIX Framework
│   │   ├── generation-rules.md          ← How to generate questions
│   │   └── examples.md                  ← 6 example questions
│   │
│   ├── portfolio/
│   │   ├── framework.md                 ← Business Diagnosis Framework
│   │   ├── generation-rules.md
│   │   └── examples.md                  ← 3 example questions
│   │
│   ├── tech-application/
│   │   ├── framework.md                 ← Capabilities Matrix Framework
│   │   ├── generation-rules.md
│   │   └── examples.md                  ← 3 example questions
│   │
│   ├── conceptual/
│   │   ├── framework.md                 ← Definition-Example Framework
│   │   ├── generation-rules.md
│   │   └── examples.md                  ← 5 example questions
│   │
│   ├── product-sense/
│   │   ├── framework-milejpsr.md        ← MILEJPSR Framework (25 min)
│   │   ├── framework-circles.md         ← CIRCLES Framework (20 min)
│   │   ├── generation-rules.md
│   │   └── examples.md                  ← 6 example questions
│   │
│   │  ── ANALYTICAL ──
│   ├── goals-metrics/
│   │   ├── framework.md                 ← G.A.M.E Framework
│   │   ├── generation-rules.md
│   │   └── examples.md
│   │
│   ├── debugging/
│   │   ├── framework.md                 ← S.I.E.V.E Framework (root-cause / metric drops)
│   │   ├── generation-rules.md
│   │   └── examples.md
│   │
│   └── tradeoffs/
│       ├── framework.md                 ← T.R.A.D.E Framework
│       ├── generation-rules.md
│       └── examples.md
│
└── questions/                           ← Generated questions go here
    ├── product-roadmap/                 ← DAY-MM-DD.md, ANSWER-MM-DD.md
    ├── portfolio/
    ├── tech-application/
    ├── conceptual/
    ├── product-sense/
    ├── goals-metrics/
    ├── debugging/
    └── tradeoffs/
```

---

## Installation Steps

### Step 1: Copy to Obsidian

**Copy this entire folder to:**
```
<your-vault-path>/PrepQuestions/
```

**Result:** Your Obsidian vault should now have:
```
<your-vault-path>/
└── PrepQuestions/              ← All files from this download
    ├── README.md
    ├── config.yaml
    ├── _core/
    ├── plugins/
    └── questions/
```

---

### Step 2: Set Up Cowork Question Generator

1. **Open Cowork**
2. **Create Scheduled Task:**
   - Click "New Scheduled Task"
   - Name: `Daily PM Interview Question Generator`
   - Schedule: `Every day at 7:00 AM`
   - Instructions: **Copy & paste the ENTIRE content** from:
     ```
     PrepQuestions/_core/master-generator.md
     ```
   - Save

**What it does:**
- Runs every morning at 7 AM
- Generates 13 questions per day across 8 active categories
  (2 per strategic category × 5 = 10, plus 1 per analytical category × 3 = 3)
- Saves to `questions/{category}/DAY-MM-DD.md`

---

### Step 3: Set Up Cowork Evaluator

1. **Open Cowork**
2. **Create Project (NOT Scheduled Task):**
   - Click "New Project"
   - Name: `PM Interview Practice Arena`
   - Custom Instructions: **Copy & paste the ENTIRE content** from:
     ```
     PrepQuestions/_core/evaluator.md
     ```
   - Save

**What it does:**
- You upload `DAY-MM-DD.md` from any category
- Runs interactive interview with timer
- Evaluates your answer against framework rubric
- Generates `ANSWER-MM-DD.md` with score and feedback

---

## Daily Workflow

### Morning (Automatic)
**7:00 AM** → Cowork scheduled task runs automatically
- Generates 13 questions total (2 per strategic category, 1 per analytical category)
- Files appear in:
  - `questions/product-roadmap/DAY-MM-DD.md`
  - `questions/portfolio/DAY-MM-DD.md`
  - `questions/tech-application/DAY-MM-DD.md`
  - `questions/conceptual/DAY-MM-DD.md`
  - `questions/product-sense/DAY-MM-DD.md`
  - `questions/goals-metrics/DAY-MM-DD.md`
  - `questions/debugging/DAY-MM-DD.md`
  - `questions/tradeoffs/DAY-MM-DD.md`

### Practice Session (Manual)
1. **Open** today's question file (e.g., `questions/product-roadmap/DAY-05-22.md`)
2. **Review** the recommended framework
3. **Upload** file to Cowork project "PM Interview Practice Arena"
4. **Answer** the question interactively (25 min with timer)
5. **Receive** evaluation with score and feedback
6. **Download** `ANSWER-05-22.md` from Cowork
7. **Save** to `questions/product-roadmap/ANSWER-05-22.md`

---

## Active Categories

Currently generating questions for:

**Strategic (5 categories — 10 questions/day):**

| Category | Questions/Day | Time | Framework |
|----------|---------------|------|-----------|
| Product Roadmap | 2 | 25 min | MATRIX |
| Portfolio (CEO) | 2 | 20 min | Business Diagnosis |
| Tech Application | 2 | 20 min | Capabilities Matrix |
| Conceptual | 2 | 5 min | Definition-Example |
| Product Sense | 2 | 20-25 min | MILEJPSR or CIRCLES |

**Analytical (3 categories — 3 questions/day):**

| Category | Questions/Day | Time | Framework |
|----------|---------------|------|-----------|
| Goals & Metrics | 1 | 25 min | G.A.M.E |
| Debugging & Diagnosis | 1 | 20 min | S.I.E.V.E |
| Trade-offs | 1 | 20 min | T.R.A.D.E |

**Total: 13 questions per day**

---

## Customization

### To disable a category:
1. Open `config.yaml`
2. Find the category (e.g., `product-sense`)
3. Change `active: true` to `active: false`
4. Save

Next day's generation will skip that category.

### To change question frequency:
1. Open `config.yaml`
2. Find the category
3. Change `questions_per_day: 2` to `questions_per_day: 1` (or 3)
4. Save

---

## Adding New Categories

**Example: Adding RCU (Execution) questions**

See `_core/plugin-schema.md` for complete instructions.

**Quick steps:**
1. Create `plugins/execution/` folder
2. Create 3 files: `framework.md`, `generation-rules.md`, `examples.md`
3. Update `config.yaml`:
   ```yaml
   - id: execution
     active: true
     questions_per_day: 1
   ```
4. Done! Generator and evaluator auto-detect it.

**Full RCU example included in plugin-schema.md**

---

## Verification

After installation, verify:

### ✅ Folder structure exists:
```bash
ls -la <your-vault-path>/PrepQuestions/
```

Should show: `README.md`, `config.yaml`, `_core/`, `plugins/`, `questions/`

### ✅ Cowork scheduled task created:
- Open Cowork
- Check Scheduled Tasks
- Should see "Daily PM Interview Question Generator"

### ✅ Cowork project created:
- Open Cowork
- Check Projects
- Should see "PM Interview Practice Arena"

### ✅ Questions generate:
- Wait until 7:01 AM next day
- Check `questions/product-roadmap/` folder
- Should see `DAY-MM-DD.md` files

---

## Troubleshooting

### Questions not generating?
1. Check Cowork scheduled task exists
2. Check scheduled task has content from `_core/master-generator.md`
3. Check `config.yaml` has categories with `active: true`

### Evaluation not working?
1. Check Cowork project exists (not scheduled task)
2. Check project has content from `_core/evaluator.md`
3. Check question file has correct frontmatter
4. Check framework file exists at path specified in question

### Framework not loading?
1. Verify path in question file matches actual file location
2. Check framework has required sections (see plugin-schema.md)
3. Verify rubric totals 10 points

---

## File Sizes Reference

| File | Size |
|------|------|
| README.md | 13 KB |
| config.yaml | 2.6 KB |
| _core/plugin-schema.md | 20 KB |
| _core/master-generator.md | 8 KB |
| _core/evaluator.md | 13 KB |
| **Each framework.md** | 13-24 KB |
| **Each generation-rules.md** | 6-13 KB |
| **Each examples.md** | 6-9 KB |

**Total system size:** ~200 KB

---

## Support

**Full documentation:** `README.md`  
**Create new plugins:** `_core/plugin-schema.md`  
**Questions:** Reference README troubleshooting section

---

**System Version:** 1.0 (Plugin Architecture)  
**Installation Date:** May 2026  
**Ready to Use:** Yes ✅

---

## Quick Start Checklist

- [ ] Copied entire folder to Obsidian vault
- [ ] Created Cowork Scheduled Task with master-generator.md
- [ ] Created Cowork Project with evaluator.md
- [ ] Verified folder structure exists
- [ ] Waited until 7 AM for first question generation (or manually triggered)
- [ ] Opened a generated question file
- [ ] Uploaded to Cowork project and practiced
- [ ] Received evaluation feedback

**Once all checked → System is fully operational! 🎉**
