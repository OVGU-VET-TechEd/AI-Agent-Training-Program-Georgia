<!--

author:   Masub Makhdoom
email:    masub.makhdoom@ovgu.de
date:     29/03/2025
version:  30.0.0
language: en
narrator: UK English Female

link: https://raw.githubusercontent.com/OVGU-VET-TechEd/Integrating_AI_in_TVET_UNESCO/refs/heads/main/VorlageUN.css

repository: https://github.com/LiaScript/docs

logo:     img/logo.png

comment:  This document shall provide an entire compendium and course on the
          development of Open-courSes with [LiaScript](https://LiaScript.github.io).
          As the language and the systems grows, also this document will be updated.
          Feel free to fork or copy it, translations are very welcome...

script:   https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.js
          https://felixhao28.github.io/JSCPP/dist/JSCPP.es5.min.js

link:     https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.css

link:     https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css

import:   https://raw.githubusercontent.com/liaTemplates/ABCjs/main/README.md

link:     https://fonts.googleapis.com/css2?family=Noto+Sans+Egyptian+Hieroglyphs
          https://fonts.googleapis.com/css2?family=Noto+Sans+Ogham

font:     Noto Sans Egyptian Hieroglyphs, Noto Sans Ogham
-->

# Teaching Automation Workflow

> Audience: advanced students (Master/TVET/EdTech) who will build the workflow by themselves on a **Windows laptop**. 

> Everything includes **copy-paste ready PowerShell commands** + full file contents.

---

## Title
**Teaching Automation Workflow**  

Zero → Hero (Advanced)  

**Workshop: Build a “lesson factory” with GitHub Copilot**

---

## Why This Matters (Advanced)
You’re not learning “how to write a lesson.”  
You’re learning **how to design a system** that produces lessons consistently.

---

## Outcomes (Measurable)
By the end, you can:

- Create a production-ready repo structure
- Govern Copilot output using rules + prompts + templates
- Generate lessons with measurable objectives and testable activities
- Apply QA and peer review like a software team

---

## Prerequisites (Windows)
- Windows 10/11
- VS Code installed
- Git installed
- GitHub account
- GitHub Copilot enabled (optional but recommended)

---

## Tools Check (Windows Quick)
Open **PowerShell** and run:

```powershell
git --version
code --version
python --version
```

If `code` is not found:

- VS Code → `Ctrl+Shift+P`
- Type: **Shell Command: Install 'code' command in PATH**

---

##  Workshop Repository Goal
You will build this exact structure:

```
teaching-workflow/
├── .github/
│   └── copilot-instructions.yml
├── lessons/
│   ├── lesson-template.md
│   └── example-lesson.md
├── prompts/
│   └── teaching-guide.md
├── README.md
└── config.yaml
```

---

## The Teaching Factory Model

**Metadata** → **Rules** → **Prompts** → **Templates** → **Lessons (outputs)**

---

## Automation Maturity Model


1) Manual writing 

2) Templates  

3) AI-assisted drafting 

4) Workflow-driven consistency 

5) Continuous improvement (QA + versioning)

---

## Core Principle
**If it is not standardized, it cannot be automated.**

---

## Workshop Rules
- Copy-paste first
- Run commands exactly
- Then customize to your domain (TVET, language learning, etc.)

---

# WORKSHOP BLOCK 1 — SETUP (Slides 11–20)

---

## Create Project Folder (PowerShell)
Choose a location (Desktop example):

```powershell
cd $env:USERPROFILE\Desktop
mkdir teaching-workflow
cd teaching-workflow
```

---

##  Initialize Git (PowerShell)
```powershell
git init
```

Optional: set main branch name:
```powershell
git branch -M main
```

---

##  Open in VS Code (PowerShell)
```powershell
code .
```

---

## Create Folders (PowerShell)
```powershell
mkdir .github, lessons, prompts
```

---

## Create Empty Files (PowerShell)
```powershell
New-Item -ItemType File -Path README.md, config.yaml
New-Item -ItemType File -Path .github\copilot-instructions.yml
New-Item -ItemType File -Path prompts\teaching-guide.md
New-Item -ItemType File -Path lessons\lesson-template.md, lessons\example-lesson.md
```

---

##  Check Structure (PowerShell)
```powershell
tree /F
```

Expected to see `.github`, `lessons`, `prompts`, and files.

---

##  Optional: .gitignore (PowerShell)
Create `.gitignore` quickly:

```powershell
@"
.DS_Store
dist/
node_modules/
__pycache__/
*.pyc
"@ | Set-Content .gitignore -Encoding utf8
```

---

##  First Commit (PowerShell)
```powershell
git add .
git commit -m "Initialize teaching-workflow structure"
```

---

## Push to GitHub (Manual Steps)
1. GitHub → New repository → name: `teaching-workflow`
2. Do **not** add README (you already have one)
3. Copy GitHub remote URL

---

## Add Remote + Push (PowerShell)
Replace URL with your repo URL:

```powershell
git remote add origin https://github.com/YOURNAME/teaching-workflow.git
git push -u origin main
```

---

# WORKSHOP BLOCK 2 — METADATA & GOVERNANCE (Slides 21–35)

---

##  Why Metadata (config.yaml) Matters
Metadata provides **context** and ensures:

- consistent level
- consistent pedagogy
- scalable reuse across topics

---

##  Create config.yaml (Full Content)
Copy-paste into `config.yaml`:

```yaml
course:
  title: Teaching Automation Workflow
  subtitle: Zero to Hero (Advanced Workshop)
  duration_minutes: 120
  language: English

  target_audience:
    - Advanced university students
    - TVET master students
    - Instructional designers
    - EdTech developers

  learner_profile:
    assumed_skills:
      - Can use VS Code and terminal
      - Can use Git basics (commit/push)
      - Can read Markdown
    optional_skills:
      - Copilot experience
      - LiaScript or SCORM experience

  learning_outcomes:
    - Design a standardized lesson factory repository
    - Govern AI outputs using rules and prompts
    - Create lessons with measurable objectives and testable activities
    - Apply QA and peer review workflows for teaching materials

  pedagogy:
    approach:
      - Project-based learning
      - Workshop + peer review
      - Human-in-the-loop quality assurance
    lesson_requirements:
      - Objectives must be measurable (Bloom verbs)
      - Every lesson must include at least one activity with expected output
      - Keep theory short, emphasize application

  constraints:
    - Output must be Markdown
    - Avoid vague activities and filler text
    - Prefer step-by-step procedure sections
```

---

## Workshop Task (3 min)
Edit `config.yaml` to include:

- your real program name
- one domain example (e.g., “TVET AI prompting”)

---

## AI Governance Concept
**Copilot instructions** are your **policy**:

- format rules
- quality gates
- forbidden patterns

---

## Create copilot-instructions.yml (Full Content)
Copy-paste into `.github/copilot-instructions.yml`:

```yaml
role: "Teaching Assistant"

writing_style:
  tone: "clear, rigorous, workshop-friendly"
  language_level: "advanced but readable"
  format: "markdown"
  avoid:
    - "filler sentences"
    - "unverifiable claims"
    - "long theory blocks"

structure_rules:
  - "Follow lessons/lesson-template.md EXACTLY (do not remove sections)"
  - "Every lesson must include measurable Learning Objectives"
  - "Every lesson must include a Step-by-Step Procedure"
  - "Every lesson must include an Example AND an Activity"
  - "Activities must include steps + expected output + time limit"
  - "End with Summary + Reflection Question"

quality_gates:
  measurable_objectives:
    - "Use Bloom verbs: explain, compare, apply, design, evaluate"
  activity_quality:
    - "Reject vague tasks like 'think about' without output"
  length_control:
    - "Keep each section under ~10 lines unless necessary"
```

---

## Governance Rule: “Reject Vague Activities”
Example of a bad activity:

- “Discuss automation.” (no output)

Example of a good activity:

- “Write a 5-step workflow plan and submit as a markdown snippet.”

---

## Workshop Task (5 min)
Add one more strict rule to `quality_gates`, for example:

- “Common Mistakes section must include fixes.”

---

##  Why Prompts Matter (Advanced)
A prompt is not a request.
It’s a **contract** that defines how content must be produced.

---

## Create prompts/teaching-guide.md (Full Content)
Copy-paste into `prompts/teaching-guide.md`:

```markdown
# Teaching Guide (Base Prompt)

You are an expert educator and instructional designer.

## Mission
Generate lessons that are consistent, testable, and workshop-ready.

## Audience
Advanced learners (Master/TVET/EdTech) who can follow terminal commands and produce deliverables.

## Output Format
- Markdown only
- Follow lessons/lesson-template.md exactly

## Pedagogical Rules (Non-negotiable)
- Start with measurable learning objectives (Bloom verbs)
- Explain concepts in short, dense bullets (no long essays)
- Include a realistic example linked to the domain
- Include a 5–10 minute activity with steps + expected output
- Include common mistakes + fixes
- End with summary + reflection

## Cognitive Load Limits
- Keep each section compact
- Prefer checklists and procedures
- Avoid repeating the same point

## Quality Self-Check
Before finalizing:

- Are objectives measurable?
- Is the activity testable with an output?
- Does procedure include actionable steps?
- Are mistakes and fixes included?
```

---

##  Prompt Pattern (Reusable)
When you want a new lesson, use this pattern:

- Topic + level + constraints + domain example + expected output

---

## Workshop Task (5 min)
Update the Audience line in `teaching-guide.md` to your group, e.g.:
- “OVGU ITVET Master students building micro-credentials.”

---

## Commit Your Governance Layer
```powershell
git add .
git commit -m "Add metadata, Copilot governance, and teaching guide"
git push
```

---

##  Quick QA Checkpoint
If your team clones this repo, they should instantly understand:

- what to generate
- how to generate
- what “good” means

---

## Anti-Pattern Warning
Do NOT “fix” bad AI output by rewriting the whole lesson.
Fix:

- rules
- template
- prompts
Then regenerate.

---

## Transition
Now we build the **template** and produce **high-quality outputs**.

---

# WORKSHOP BLOCK 3 — TEMPLATE & OUTPUT PRODUCTION (Slides 36–55)

---

## Create lessons/lesson-template.md (Advanced Template)
Copy-paste into `lessons/lesson-template.md`:

```markdown
# Lesson Title

## Learning Objectives
By the end of this lesson, learners will be able to:
- Objective 1 (measurable)
- Objective 2 (measurable)
- Objective 3 (measurable)

## Key Concepts
- Concept 1 (1–2 lines)
- Concept 2 (1–2 lines)
- Concept 3 (1–2 lines)

## Step-by-Step Procedure
1. Step 1 (action)
2. Step 2 (action)
3. Step 3 (action)
4. Step 4 (action)

## Example (Realistic Scenario)
Write one scenario that matches the topic and learner context.

## Activity (5–10 minutes)
**Task:** What learners must do.  
**Steps:**
1. ...
2. ...
3. ...
**Expected Output:** A clear deliverable (text, file, checklist, commands run).  
**Time Box:** 5–10 minutes.

## Common Mistakes & Fixes
- Mistake 1 → Fix
- Mistake 2 → Fix
- Mistake 3 → Fix

## Summary
- Key takeaway 1
- Key takeaway 2
- Key takeaway 3

## Reflection Question
One open-ended question for discussion or journaling.
```

---

##  — Why This Template Works
It forces:

- outcomes
- procedure
- evidence of learning (activity output)
- feedback loop (mistakes/fixes)

---

##  Create lessons/example-lesson.md (Full Example)
Copy-paste into `lessons/example-lesson.md`:

```markdown
# GitHub Workflow for Teaching Content (Advanced)

## Learning Objectives
By the end of this lesson, learners will be able to:
- Explain how version control improves teaching material quality
- Apply a review workflow using branches and pull requests
- Design a “lesson review checklist” for AI-generated content

## Key Concepts
- Version control: tracking changes over time with history and collaboration
- Pull request (PR): a review mechanism for changes before merging
- Quality gate: a rule that must pass before content is accepted

## Step-by-Step Procedure
1. Create a new branch for a lesson change.
2. Edit the lesson using the template and Copilot rules.
3. Commit changes with a clear message.
4. Push the branch and open a Pull Request.
5. Review using the lesson checklist, then merge.

## Example (Realistic Scenario)
A program has three instructors. Each writes lessons differently. By forcing PR reviews and using a template, the team catches missing objectives and weak activities before learners see the content.

## Activity (5–10 minutes)
**Task:** Create a review checklist and apply it to one lesson.  
**Steps:**
1. Write a checklist with 6–8 items (objectives, activity output, procedure, etc.).
2. Open `lessons/example-lesson.md` and check each item.
3. Write one improvement suggestion and implement it.
**Expected Output:** A checklist + one committed improvement.  
**Time Box:** 10 minutes.

## Common Mistakes & Fixes
- Mistake: objectives are vague → Fix: use Bloom verbs (apply, compare, evaluate)
- Mistake: activities have no output → Fix: require a file/snippet/checklist deliverable
- Mistake: long theory blocks → Fix: convert into bullets + procedure

## Summary
- Git enables collaboration and quality control for teaching materials
- PR reviews create consistent standards across instructors
- Templates and checklists reduce variability and missing parts

## Reflection Question
What quality rules should be non-negotiable in your teaching materials?
```

---

## Commit Template + Example
```powershell
git add lessons\lesson-template.md, lessons\example-lesson.md
git commit -m "Add advanced lesson template and example lesson"
git push
```

---

## How to Generate a New Lesson (Copilot)
Create a new file: `lessons/lesson-automation-basics.md`

Then ask Copilot (in VS Code chat):

> Generate a lesson titled “Automation Basics for Teachers (Advanced)”.  

> Follow lessons/lesson-template.md exactly.  

> Use the teaching guide constraints. 

> Include a PowerShell-based activity with expected output.

---

## If You Don’t Have Copilot (Manual Method)
You can still do it:

1. Copy the template into a new file
2. Fill each section yourself
3. Use the checklist to validate

---

##  Workshop: Generate 1 Lesson (10 min)
Deliverable:

- a complete lesson file in `lessons/`
- activity includes Windows commands and an output

---

## Quality Checklist (Must Pass)
- [ ] Objectives measurable (Bloom verbs)
- [ ] Procedure is actionable steps
- [ ] Example is realistic and aligned
- [ ] Activity has steps + expected output + time box
- [ ] Mistakes include fixes
- [ ] No filler or repeated statements

---

##  Debugging Copilot Output (System Fix)
If Copilot ignores structure:

- paste the template first
- ask it to fill section-by-section:

  - “Fill Learning Objectives only.”
  - “Fill Key Concepts only.”

---

## Add Windows Command Standards
Rule for your team:

- Use **PowerShell** blocks for Windows
- Keep commands tested and minimal

---

##  Workshop: Add a “Commands” Section (Optional)
If you want, extend template with:

- “Commands (Windows)”
- “Commands (macOS/Linux)”

(For this workshop we keep Windows only.)

---

##  Versioning Teaching Materials
Use semantic commits:

- `feat:` new lesson
- `fix:` corrections
- `refactor:` structure changes

Example:
```powershell
git commit -m "feat: add lesson on automation basics"
```

---

## Peer Review Like a Software Team (Workshop)
Pair up:

- Student A reviews Student B lesson using checklist
- Student B reviews Student A lesson
Deliverable: 2 review comments + 1 improvement commit

---

## Review Comments Template
- ✅ Strength:

- ⚠ Issue:
- 🛠 Fix suggestion:
- 🔁 Regenerate or edit? (system decision)

---

## Optional Advanced: PR Workflow (GitHub)
Commands:

```powershell
git checkout -b lesson/new-automation-basics
# edit lesson file
git add .
git commit -m "feat: add automation basics lesson"
git push -u origin lesson/new-automation-basics
```
Then open GitHub → create Pull Request → review → merge.

---

##  Why PRs Matter
PRs enforce:

- review culture
- shared standards
- traceable changes

---

## Advanced QA: Rubric (Scoring)
Score each lesson 0–2 per item:

- objectives measurable
- activity output
- procedure clarity
- example relevance
- mistakes + fixes

Total /10 → publish threshold ≥ 8

---

## Workshop: Apply Rubric (5 min)
Score your lesson.
Improve the lowest scoring item.

---

##  Troubleshooting Table
| Problem | Cause | Fix |
|---|---|---|
| too long | no constraints | cap section length in instructions |
| vague activity | missing output requirement | require expected output |
| wrong level | missing audience info | tighten config + teaching guide |
| inconsistent headings | template not enforced | regenerate section-by-section |

---

## Commit Your New Lesson
```powershell
git add lessons
git commit -m "feat: add new generated lesson"
git push
```

---

# WORKSHOP BLOCK 4 — CAPSTONE & EXTENSIONS (Slides 56–68)

---

##  Capstone Goal
Build a lesson that teaches **repo workflow itself**:

- “Teaching Workflow: From Topic to Published Lesson”

---

## Capstone Requirements
Your capstone lesson must include:

- PowerShell commands in the activity
- a deliverable file output
- peer review checklist reference

---

##  Capstone Prompt (Copy)
Use this in Copilot chat:

> Create a lesson titled “From Topic to Published Lesson (Workflow Capstone)”.  
> Follow the template exactly.  
> Activity must include PowerShell commands to create a new lesson file, commit, and push.  
> Expected output: a pushed commit and a new lesson file.

---

## Capstone Activity Commands (PowerShell Example)
Students should include commands like these in their lesson activity:

```powershell
# 1) Create a new lesson file from template (manual copy in VS Code) OR create empty file:
New-Item -ItemType File -Path lessons\lesson-my-topic.md

# 2) Stage and commit
git add lessons\lesson-my-topic.md
git commit -m "feat: add lesson my topic"

# 3) Push
git push
```

---

## Advanced Extension: Add GitHub Actions (Concept)
Later you can automate checks:

- validate template headings
- block merge if missing sections

(We focus on repo workflow today.)

---

## Advanced Extension: LiaScript
Markdown → LiaScript → interactive teaching content.

---

##  Advanced Extension: SCORM
Markdown → build pipeline → SCORM zip → LMS

---

##  Ethics & Governance
Rules + review protect against:

- hallucinations
- bias
- wrong pedagogy

---

## Final Quality Checklist (Non-Negotiable)
- [ ] measurable objectives
- [ ] activity output exists
- [ ] steps are runnable on Windows
- [ ] example is realistic
- [ ] mistakes have fixes

---

## Final Commit (PowerShell)
```powershell
git add .
git commit -m "chore: finalize workshop outputs"
git push
```

---

## What “Hero Level” Means
Hero level is not “I can generate content.”  
Hero level is: **I can govern and scale content creation responsibly.**

---

## Next Steps for Master-Level Work
- Add PR-based review policy
- Add CI checks for structure
- Add publishing pipeline (Pages / SCORM)
- Add multilingual lesson generation

---

## Thank You
Questions, discussion, and next improvements.

---

# APPENDIX A — Copy-Paste File Contents (Full Pack)

Use these if someone wants to recreate everything quickly.

## A1) config.yaml
```yaml
course:
  title: Teaching Automation Workflow
  subtitle: Zero to Hero (Advanced Workshop)
  duration_minutes: 120
  language: English

  target_audience:
    - Advanced university students
    - TVET master students
    - Instructional designers
    - EdTech developers

  learner_profile:
    assumed_skills:
      - Can use VS Code and terminal
      - Can use Git basics (commit/push)
      - Can read Markdown
    optional_skills:
      - Copilot experience
      - LiaScript or SCORM experience

  learning_outcomes:
    - Design a standardized lesson factory repository
    - Govern AI outputs using rules and prompts
    - Create lessons with measurable objectives and testable activities
    - Apply QA and peer review workflows for teaching materials

  pedagogy:
    approach:
      - Project-based learning
      - Workshop + peer review
      - Human-in-the-loop quality assurance
    lesson_requirements:
      - Objectives must be measurable (Bloom verbs)
      - Every lesson must include at least one activity with expected output
      - Keep theory short, emphasize application

  constraints:
    - Output must be Markdown
    - Avoid vague activities and filler text
    - Prefer step-by-step procedure sections
```

## A2) .github/copilot-instructions.yml
```yaml
role: "Teaching Assistant"

writing_style:
  tone: "clear, rigorous, workshop-friendly"
  language_level: "advanced but readable"
  format: "markdown"
  avoid:
    - "filler sentences"
    - "unverifiable claims"
    - "long theory blocks"

structure_rules:
  - "Follow lessons/lesson-template.md EXACTLY (do not remove sections)"
  - "Every lesson must include measurable Learning Objectives"
  - "Every lesson must include a Step-by-Step Procedure"
  - "Every lesson must include an Example AND an Activity"
  - "Activities must include steps + expected output + time limit"
  - "End with Summary + Reflection Question"

quality_gates:
  measurable_objectives:
    - "Use Bloom verbs: explain, compare, apply, design, evaluate"
  activity_quality:
    - "Reject vague tasks like 'think about' without output"
  length_control:
    - "Keep each section under ~10 lines unless necessary"
```

## A3) prompts/teaching-guide.md
```markdown
# Teaching Guide (Base Prompt)

You are an expert educator and instructional designer.

## Mission
Generate lessons that are consistent, testable, and workshop-ready.

## Audience
Advanced learners (Master/TVET/EdTech) who can follow terminal commands and produce deliverables.

## Output Format
- Markdown only
- Follow lessons/lesson-template.md exactly

## Pedagogical Rules (Non-negotiable)
- Start with measurable learning objectives (Bloom verbs)
- Explain concepts in short, dense bullets (no long essays)
- Include a realistic example linked to the domain
- Include a 5–10 minute activity with steps + expected output
- Include common mistakes + fixes
- End with summary + reflection

## Cognitive Load Limits
- Keep each section compact
- Prefer checklists and procedures
- Avoid repeating the same point

## Quality Self-Check
Before finalizing:
- Are objectives measurable?
- Is the activity testable with an output?
- Does procedure include actionable steps?
- Are mistakes and fixes included?
```

## A4) lessons/lesson-template.md
```markdown
# Lesson Title

## Learning Objectives
By the end of this lesson, learners will be able to:
- Objective 1 (measurable)
- Objective 2 (measurable)
- Objective 3 (measurable)

## Key Concepts
- Concept 1 (1–2 lines)
- Concept 2 (1–2 lines)
- Concept 3 (1–2 lines)

## Step-by-Step Procedure
1. Step 1 (action)
2. Step 2 (action)
3. Step 3 (action)
4. Step 4 (action)

## Example (Realistic Scenario)
Write one scenario that matches the topic and learner context.

## Activity (5–10 minutes)
**Task:** What learners must do.  
**Steps:**
1. ...
2. ...
3. ...
**Expected Output:** A clear deliverable (text, file, checklist, commands run).  
**Time Box:** 5–10 minutes.

## Common Mistakes & Fixes
- Mistake 1 → Fix
- Mistake 2 → Fix
- Mistake 3 → Fix

## Summary
- Key takeaway 1
- Key takeaway 2
- Key takeaway 3

## Reflection Question
One open-ended question for discussion or journaling.
```

## A5) lessons/example-lesson.md
```markdown
# GitHub Workflow for Teaching Content (Advanced)

## Learning Objectives
By the end of this lesson, learners will be able to:
- Explain how version control improves teaching material quality
- Apply a review workflow using branches and pull requests
- Design a “lesson review checklist” for AI-generated content

## Key Concepts
- Version control: tracking changes over time with history and collaboration
- Pull request (PR): a review mechanism for changes before merging
- Quality gate: a rule that must pass before content is accepted

## Step-by-Step Procedure
1. Create a new branch for a lesson change.
2. Edit the lesson using the template and Copilot rules.
3. Commit changes with a clear message.
4. Push the branch and open a Pull Request.
5. Review using the lesson checklist, then merge.

## Example (Realistic Scenario)
A program has three instructors. Each writes lessons differently. By forcing PR reviews and using a template, the team catches missing objectives and weak activities before learners see the content.

## Activity (5–10 minutes)
**Task:** Create a review checklist and apply it to one lesson.  
**Steps:**
1. Write a checklist with 6–8 items (objectives, activity output, procedure, etc.).
2. Open `lessons/example-lesson.md` and check each item.
3. Write one improvement suggestion and implement it.
**Expected Output:** A checklist + one committed improvement.  
**Time Box:** 10 minutes.

## Common Mistakes & Fixes
- Mistake: objectives are vague → Fix: use Bloom verbs (apply, compare, evaluate)
- Mistake: activities have no output → Fix: require a file/snippet/checklist deliverable
- Mistake: long theory blocks → Fix: convert into bullets + procedure

## Summary
- Git enables collaboration and quality control for teaching materials
- PR reviews create consistent standards across instructors
- Templates and checklists reduce variability and missing parts

## Reflection Question
What quality rules should be non-negotiable in your teaching materials?
```
