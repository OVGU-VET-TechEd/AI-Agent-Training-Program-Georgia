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

# 🎓 <span style="color:#0B5ED7">Teaching Automation Workflow</span>
 ## 🚀 <span style="color:#198754">Zero → Hero</span>  
 

> 🧑‍💻 **Audience:** Advanced students (Master / TVET / EdTech)  
> 🪟 **Platform:** Windows (PowerShell + CMD) 
 
> 🧩 **Mode:** Copy → Paste → Do-it-yourself

---

## Welcome
<span style="color:#DC3545"><b>Today you stop writing lessons.</b></span> 

<span style="color:#198754"><b>You start building lesson factories.</b></span>

---

  ## Why This Course Exists

- 📉 Inconsistent lessons  
- 🕒 Time wasted rewriting  
- 🧑‍🤝‍🧑 Multiple instructors, different styles  

➡️ <span style="color:#0B5ED7"><b>Automation fixes this.</b></span>

---

## 🟨 Learning Outcomes
After 2 hours, you can:

- 🏗️ Design a teaching automation architecture
- 🤖 Govern AI (Copilot) behavior
- 📦 Produce reusable lessons at scale
- ✅ Apply quality assurance like software teams

---

## 🟩  Prerequisites (Windows)
✔ Windows 10 / 11 

✔ VS Code 

✔ Git 

✔ GitHub account 

✔ Copilot (recommended)

---

## 🟦  Agenda (120 Minutes)
🧠 Concepts → 🧩 Architecture → 🤖 AI Governance → 🛠️ Workshop → 🏆 Capstone

---

# 🔵 WORKSHOP 0 — Environment Check

---

## 🟪 SOpen Your Terminal
Choose your weapon:

- 🟦 PowerShell (recommended)
- 🟥 CMD

---

## 🟪 Check Git
**🟦 PowerShell**

```powershell
git --version
```

**🟥 CMD**

```bat
git --version
```

---

## 🟪  Check VS Code

**🟦 PowerShell**

```powershell
code --version
```

**🟥 CMD**

```bat
code --version
```

⚠️ If not found:  
VS Code → `Ctrl+Shift+P` → **Install 'code' command in PATH**

---

## 🟪 Target Repository
```text
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

# 🟢 WORKSHOP 1 — Create Project (Hands-on)

---

## 🟩  Create Folder
**🟦 PowerShell**

```powershell
cd $env:USERPROFILE\Desktop
mkdir teaching-workflow
cd teaching-workflow
```

**🟥 CMD**

```bat
cd %USERPROFILE%\Desktop
mkdir teaching-workflow
cd teaching-workflow
```

---

## 🟩 Initialize Git
**🟦 PowerShell**

```powershell
git init
git branch -M main
```

**🟥 CMD**

```bat
git init
git branch -M main
```

---

## 🟩 Open in VS Code
**🟦 PowerShell**

```powershell
code .
```

**🟥 CMD**

```bat
code .
```

---

## 🟩 Create Folders
**🟦 PowerShell**

```powershell
mkdir .github, lessons, prompts
```

**🟥 CMD**

```bat
mkdir .github lessons prompts
```

---

## 🟩  Create Files
**🟦 PowerShell**

```powershell
New-Item README.md, config.yaml -ItemType File
New-Item .github\copilot-instructions.yml -ItemType File
New-Item prompts\teaching-guide.md -ItemType File
New-Item lessons\lesson-template.md, lessons\example-lesson.md -ItemType File
```

**🟥 CMD**

```bat
type nul > README.md
type nul > config.yaml
type nul > .github\copilot-instructions.yml
type nul > prompts\teaching-guide.md
type nul > lessons\lesson-template.md
type nul > lessons\example-lesson.md
```

---

## 🟩  First Commit
**🟦 PowerShell**

```powershell
git add .
git commit -m "Initialize teaching automation workflow"
```

**🟥 CMD**

```bat
git add .
git commit -m "Initialize teaching automation workflow"
```

---

# 🔴 WORKSHOP 2 — AI GOVERNANCE (CRITICAL)

---

## 🔴  config.yaml (Course DNA)
Paste into `config.yaml`:

```yaml
course:
  title: Teaching Automation Workflow
  level: Advanced
  duration_minutes: 120
  language: English

  target_audience:
    - TVET Master students
    - University lecturers
    - Instructional designers

  learning_outcomes:
    - Design lesson automation systems
    - Govern AI output professionally
    - Produce measurable learning content

  constraints:
    - Markdown only
    - Measurable objectives required
    - Activities must have output
```

---

## 🔴  Copilot Instructions = AI Law
Paste into `.github/copilot-instructions.yml`:

```yaml
role: Teaching Assistant

rules:
  - Follow lesson-template.md exactly
  - Always include objectives, example, activity
  - Activities must have steps + output
  - Keep sections short and clear
```

---

## 🟠  Teaching Guide Prompt
Paste into `prompts/teaching-guide.md`:

```markdown
You are an expert educator.
Use simple language.
Follow the lesson template strictly.
Include examples and 5–10 min activities.
```

---

## 🟠 Commit Governance
**🟦 PowerShell**

```powershell
git add .
git commit -m "Add AI governance layer"
git push
```

**🟥 CMD**

```bat
git add .
git commit -m "Add AI governance layer"
git push
```

---

# 🟣 WORKSHOP 3 — TEMPLATE & LESSON FACTORY

---

## 🟣 lesson-template.md
```markdown
# Lesson Title
## Learning Objectives
## Key Concepts
## Step-by-Step Procedure
## Example
## Activity (with output)
## Common Mistakes
## Summary
## Reflection Question
```

---

## 🟣 example-lesson.md
```markdown
# Automation Basics for Teachers
## Learning Objectives
- Explain teaching automation
- Identify repetitive tasks
## Activity
Create a workflow plan and save it as a file.
```

---

## 🟣  Generate Your Own Lesson
Copilot prompt:

> Create a lesson on “Automation in Education”.  

> Follow template exactly. 

> Include PowerShell commands in the activity.

---

# 🏆 WORKSHOP 4 — CAPSTONE

---

## 🏆  Capstone Task
Create:

- 1 new lesson
- 1 measurable activity
- 1 pushed commit

---

## 🏆 Capstone Commands
**🟦 PowerShell**

```powershell
New-Item lessons\lesson-capstone.md -ItemType File
git add lessons\lesson-capstone.md
git commit -m "Add capstone lesson"
git push
```

**🟥 CMD**

```bat
type nul > lessons\lesson-capstone.md
git add lessons\lesson-capstone.md
git commit -m "Add capstone lesson"
git push
```

---

## 🟢  HERO LEVEL ACHIEVED 🎉
✔ You design systems 

✔ You govern AI


✔ You scale education      

---

## 🟢  Next Advanced Steps
- 🎯 SCORM automation
- 🎯 LiaScript integration
- 🎯 GitHub Actions validation
- 🎯 Multilingual lessons

---

## 🟢  Thank You

