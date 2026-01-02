<!--
author:   Masub Makhdoom, Sabbir Rifat
email:    masub.makhdoom@ovgu.de, a.rifat@ovgu.de
version:  3.0.0
language: en
narrator: English Female
comment:  Session 3: BMAD with Local AI (Offline) - Georgian University Workshop
logo:     https://upload.wikimedia.org/wikipedia/commons/thumb/0/04/ChatGPT_logo.svg/120px-ChatGPT_logo.svg.png

@style
.info-box {
    background-color: rgba(70, 130, 220, 0.1);
    border: 2px solid rgba(70, 130, 220, 0.4);
    border-radius: 12px;
    padding: 25px;
    margin: 20px 0;
    transition: all 0.3s ease;
}

.info-box:hover {
    transform: translateY(-8px);
    box-shadow: 0 8px 20px rgba(70, 130, 220, 0.3);
    background-color: rgba(70, 130, 220, 0.15);
}

.success-box {
    background-color: rgba(76, 175, 80, 0.1);
    border: 2px solid rgba(76, 175, 80, 0.4);
    border-radius: 12px;
    padding: 25px;
    margin: 20px 0;
    transition: all 0.3s ease;
}

.success-box:hover {
    transform: translateY(-8px);
    box-shadow: 0 8px 20px rgba(76, 175, 80, 0.3);
    background-color: rgba(76, 175, 80, 0.15);
}

.warning-box {
    background-color: rgba(255, 160, 60, 0.1);
    border: 2px solid rgba(255, 160, 60, 0.4);
    border-radius: 12px;
    padding: 25px;
    margin: 20px 0;
    transition: all 0.3s ease;
}

.warning-box:hover {
    transform: translateY(-8px);
    box-shadow: 0 8px 20px rgba(255, 160, 60, 0.3);
    background-color: rgba(255, 160, 60, 0.15);
}

.step-container {
    display: grid;
    grid-template-columns: 1fr;
    gap: 20px;
    margin: 25px 0;
}

.step-box {
    background-color: rgba(156, 39, 176, 0.1);
    border: 2px solid rgba(156, 39, 176, 0.4);
    border-radius: 12px;
    padding: 25px;
    transition: all 0.3s ease;
}

.step-box:hover {
    transform: translateX(10px);
    box-shadow: 0 8px 20px rgba(156, 39, 176, 0.3);
    background-color: rgba(156, 39, 176, 0.15);
}

.step-box h4 {
    font-size: 20px;
    color: #2c3e50;
    margin-bottom: 15px;
    font-weight: bold;
}

.comparison-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 25px;
    margin: 30px 0;
}

@media (max-width: 768px) {
    .comparison-container {
        grid-template-columns: 1fr;
    }
}

.comparison-box {
    background-color: rgba(70, 130, 220, 0.1);
    border: 2px solid rgba(70, 130, 220, 0.4);
    border-radius: 12px;
    padding: 25px;
    transition: all 0.3s ease;
}

.comparison-box:hover {
    transform: translateY(-8px);
    box-shadow: 0 8px 20px rgba(70, 130, 220, 0.3);
    background-color: rgba(70, 130, 220, 0.15);
}

.code-output {
    background-color: rgba(0, 0, 0, 0.05);
    border-left: 4px solid #4682dc;
    padding: 15px;
    border-radius: 6px;
    margin: 15px 0;
}

.platform-box-windows {
    background-color: rgba(0, 123, 255, 0.05);
    border: 2px solid rgba(0, 123, 255, 0.3);
    padding: 20px;
    border-radius: 10px;
    transition: all 0.3s ease;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

.platform-box-windows:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 16px rgba(0,123,255,0.2);
    background-color: rgba(0, 123, 255, 0.08);
}

.platform-box-mac {
    background-color: rgba(108, 117, 125, 0.05);
    border: 2px solid rgba(108, 117, 125, 0.3);
    padding: 20px;
    border-radius: 10px;
    transition: all 0.3s ease;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

.platform-box-mac:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 16px rgba(108,117,125,0.2);
    background-color: rgba(108, 117, 125, 0.08);
}

@end
-->

# Session 3: BMAD with Local AI (Offline)

> **Duration**: 1 hour 40 minutes  
> **Format**: 🎓 Hands-On Workshop  
> **Target Audience**: Georgian University Academic Staff  
> **Prerequisites**: Sessions 1 & 2 completed (understand BMAD, have GitHub Copilot)

Welcome to Session 3! After learning about Agentic AI and creating courses with GitHub Copilot, now we'll build a **completely offline** version that works without internet. This means you can create courses anywhere - even with no internet connection!

**🎯 What You'll Build Today:**

* 🔌 **15 min**: Why Offline AI? (Use cases & benefits)
* 💻 **25 min**: Install Python, Ollama & DeepSeek Model
* 🛠️ **10 min**: Create Offline Course Generator Script
* 🚀 **40 min**: Generate Your First Offline Course Together
* ✅ **10 min**: Compare Online vs. Offline Results

---

## Quick Recap: Sessions 1 & 2 (3 minutes)

Let's review what we accomplished in the previous sessions:

### What You Already Know:

      {{0}}
<div style="background: rgba(40, 167, 69, 0.08); border: 2px solid rgba(40, 167, 69, 0.3); padding: 20px; border-radius: 10px; margin: 20px 0; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(40,167,69,0.2)'; this.style.background='rgba(40, 167, 69, 0.12)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(40, 167, 69, 0.08)';">

**✅ Session 1: Fundamentals**

- Understood Agentic AI vs. Traditional AI
- Set up VS Code + GitHub + Copilot
- Learned the BMAD Method (8 stages)
- Explored file structure and templates

</div>

      {{1}}
<div style="background: rgba(40, 167, 69, 0.08); border: 2px solid rgba(40, 167, 69, 0.3); padding: 20px; border-radius: 10px; margin: 20px 0; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(40,167,69,0.2)'; this.style.background='rgba(40, 167, 69, 0.12)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(40, 167, 69, 0.08)';">

**✅ Session 2: Implementation**

- Created complete "AI in TVET" course
- Used megaprompt for full workflow
- Saved to GitHub + local Desktop
- Generated 6,000+ words in 10 minutes

</div>

      {{2}}
**The Challenge We'll Solve Today:**

      {{2}}
<div style="background: rgba(255, 193, 7, 0.08); border: 2px solid rgba(255, 193, 7, 0.4); padding: 20px; border-radius: 10px; margin: 20px 0; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(255,193,7,0.2)'; this.style.background='rgba(255, 193, 7, 0.12)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(255, 193, 7, 0.08)';">

**⚠️ Current Limitation: Internet Required**

Sessions 1 & 2 relied on:
- ✅ GitHub Copilot (cloud-based)
- ✅ Claude AI (internet connection needed)
- ✅ Active subscription required

**What if you:**
- Work in areas with poor internet?
- Want to avoid subscription costs?
- Need data privacy (sensitive courses)?
- Travel frequently or work offline?

</div>

      {{3}}
<div style="background: rgba(40, 167, 69, 0.1); border: 2px solid rgba(40, 167, 69, 0.4); padding: 25px; border-radius: 10px; margin: 20px 0; text-align: center; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(40,167,69,0.3)'; this.style.background='rgba(40, 167, 69, 0.15)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(40, 167, 69, 0.1)';">

<span style="font-size: 1.8em; font-weight: bold;">**Solution: Local run Free AI LLM!**</span>

</div>

---

## Part 1: Why Offline AI? (15 minutes)

### Understanding the Benefits

      {{0}}
**Compare: Online vs. Offline Course Generation**

      {{0}}
<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin: 20px 0;">

<div style="background: rgba(0, 123, 255, 0.05); border: 2px solid rgba(0, 123, 255, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(0,123,255,0.2)'; this.style.background='rgba(0, 123, 255, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(0, 123, 255, 0.05)';">

#### ☁️ Online (Sessions 1 & 2)

**Pros:**

- ✅ Latest AI models (Claude)
- ✅ Easy setup
- ✅ Regular updates
- ✅ Best quality outputs

**Cons:**

- ❌ Requires internet
- ❌ Monthly subscription ($10+)
- ❌ Data sent to cloud
- ❌ Depends on service availability

**Best for:**
- Quick course creation
- Maximum quality
- Collaborative work

</div>

<div style="background: rgba(40, 167, 69, 0.05); border: 2px solid rgba(40, 167, 69, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(40,167,69,0.2)'; this.style.background='rgba(40, 167, 69, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(40, 167, 69, 0.05)';">

#### 🔌 Offline (Session 3)

**Pros:**

- ✅ Works without internet
- ✅ Completely free
- ✅ Full data privacy
- ✅ No subscriptions

**Cons:**

- ❌ Initial setup time (20-50 min)
- ❌ Requires 10GB disk space
- ❌ Slower generation (2-3x)
- ❌ Slightly lower quality

**Best for:**
- Rural/remote locations
- Budget constraints
- Sensitive course content
- Long-term independence

</div>

</div>

      {{1}}
**Real-World Use Cases:**

      {{1}}
<div style="background: rgba(23, 162, 184, 0.08); border: 2px solid rgba(23, 162, 184, 0.3); padding: 20px; border-radius: 10px; margin: 20px 0; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(23,162,184,0.2)'; this.style.background='rgba(23, 162, 184, 0.12)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(23, 162, 184, 0.08)';">

**When to Use Offline AI:**

1. **🏔️ Remote Locations:** Universities in areas with unreliable internet
2. **💰 Budget Constraints:** Avoid monthly AI subscription costs
3. **🔒 Data Privacy:** Military, healthcare, or confidential course content
4. **✈️ Travel:** Create courses during flights or field research
5. **🌍 Developing Regions:** Limited internet infrastructure
6. **📚 Large Scale:** Generate 50+ courses without API limits

</div>

      {{2}}
**What You'll Build Today:**

      {{2}}
<div style="background: rgba(40, 167, 69, 0.08); border: 2px solid rgba(40, 167, 69, 0.3); padding: 20px; border-radius: 10px; margin: 20px 0; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(40,167,69,0.2)'; this.style.background='rgba(40, 167, 69, 0.12)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(40, 167, 69, 0.08)';">

**🎓 Complete Offline Course Generator:**

- Python-based automation script
- Local AI model (DeepSeek-Coder)
- Automated YAML & Markdown generation
- Works 100% offline after setup
- Same BMAD workflow as Sessions 1 & 2
- Generate unlimited courses for free!

</div>

---



# Part 2: Check Your System (5 minutes)

## System Requirements Check


**Before We Begin - Everyone Check This:**

<div class="warning-box">

**⚠️ SYSTEM REQUIREMENTS:**

**Minimum Specs:**

- **RAM:** 8 GB (16 GB recommended)
- **Storage:** 10 GB free space for AI model
- **CPU:** Any modern processor (2015 or newer)
- **OS:** Windows 10/11 OR macOS 10.15+

**Internet:** Needed ONLY for initial download (~4 GB)

**After setup:** Works 100% offline forever!


</div>

---



# Part 3: Install Required Software (25 minutes)

## Step 1: Open Terminal (3 minutes)

      {{0}}
**👉 EVERYONE DO THIS NOW:**

We need to open the command-line terminal to install software.

<div class="comparison-container">

<div class="platform-box-windows">

**🪟 Windows Users:**

**Quickest Method:**
1. Press `Win + X`
2. Select "Windows PowerShell"

**Alternative:**
- Press `Win` key
- Type `powershell`
- Press Enter

</div>

<div class="platform-box-mac">

**🍎 Mac Users:**

**Quickest Method:**
1. Press `⌘ + Space`
2. Type `Terminal`
3. Press Enter

**Alternative:**
- Open Applications
- Go to Utilities
- Double-click Terminal

</div>

</div>

      {{1}}
<div class="success-box">

**✋ CHECKPOINT:** Can everyone see a terminal/command window open?

**Windows users:** Should see `PS C:\Users\YourName>`

**Mac users:** Should see `YourName@Computer ~ %`

**✅ If yes → Great! Keep this window open!**

</div>

## Step 2: Install Python, Git & Ollama (15 minutes)

      {{0}}
**👉 NOW WE'LL INSTALL 3 PROGRAMS:**

<div class="info-box">

**What We're Installing:**

1. **Python** - Programming language (needed to run our script)
2. **Git** - Version control (useful for saving course versions)
3. **Ollama** - Local AI engine (runs the AI model on your computer)



**Installation time:** 10-15 minutes

</div>

---

### Windows Installation

      {{0}}
**👉 WINDOWS USERS - Follow These Steps:**

<div class="step-container">

<div class="step-box">
<h4>Step 2a: Download Python</h4>

1. Open browser → Go to: `https://www.python.org/downloads/`
2. Click the big **"Download Python 3.x.x"** button
3. **IMPORTANT:** When installer opens:
   - ✅ **CHECK** "Add Python to PATH"
   - Click "Install Now"
4. Wait for installation (2-3 minutes)
5. Click "Close" when done

</div>

<div class="step-box">
<h4>Step 2b: Download Ollama</h4>

1. Open browser → Go to: `https://ollama.com/download`
2. Click **"Download for Windows"** button
3. Run `OllamaSetup.exe` when downloaded
4. Follow installation wizard (default settings OK)
5. Ollama starts automatically in background

</div>

<div class="step-box">
<h4>Step 2c: Download Git</h4>

1. Open browser → Go to: `https://git-scm.com/download/win`
2. Download will start automatically
3. Run installer with **default settings**
4. Click "Next" through all screens
5. Click "Install" → "Finish"

</div>

</div>

      {{1}}
**Verify Windows Installation:**

{{1}}
<div class="step-box">
<h4>📝 Test in PowerShell:</h4>

**Close and reopen PowerShell**, then type these commands:

```powershell
python --version
ollama --version
git --version
```

**Expected output:**

```
Python 3.12.x
ollama version 0.x.x
git version 2.x.x
```

</div>

      {{2}}
<div class="success-box">

**✋ WINDOWS CHECKPOINT:** Do you see all 3 version numbers?

**✅ If YES → Perfect! Wait for Mac users to catch up**

**❌ If NO → Raise your hand for help!**

</div>

---

### macOS Installation

      {{0}}
**👉 MAC USERS - Follow These Steps:**

<div class="step-container">

<div class="step-box">
<h4>Step 2a: Install Homebrew (Package Manager)</h4>

**In Terminal, paste this command:**

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Press Enter and wait (3-5 minutes)

**Then add Homebrew to your PATH:**

```bash
echo 'eval "$(/usr/local/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/usr/local/bin/brew shellenv)"
```

**Verify:**

```bash
brew --version
```

Should show: `Homebrew 4.x.x`

</div>

<div class="step-box">
<h4>Step 2b: Install Python, Git & Ollama</h4>

**Now install all 3 programs with one command:**

```bash
brew install python3 git ollama
```

Press Enter and wait (5-35 minutes)

This downloads and installs all three automatically!

</div>

</div>

      {{1}}
**Verify Mac Installation:**


{{1}}
<div class="step-box">
<h4>📝 Test in Terminal:</h4>

**Type these commands:**

```bash
python3 --version
ollama --version
git --version
```

**Expected output:**

```
Python 3.12.x
ollama version 0.x.x
git version 2.x.x
```

</div>

      {{2}}
<div class="success-box">

**✋ MAC CHECKPOINT:** Do you see all 3 version numbers?

**✅ If YES → Perfect! You're caught up with Windows users!**

**❌ If NO → Raise your hand for help!**

</div>

---

      {{3}}
<div class="success-box">

**🎉 EVERYONE - Installation Complete!**

**You now have:**
- ✅ Python (to run automation scripts)
- ✅ Git (to save course versions)
- ✅ Ollama (to run local AI)

**Next:** Start Ollama and download the AI model!

</div>

---

# **Step 2: Configure AI Model**

## **2.1 Start Ollama Service**
Ollama must run as a background service to handle AI requests.

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin: 20px 0;">

<div style="background: rgba(0, 123, 255, 0.05); border: 2px solid rgba(0, 123, 255, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(0,123,255,0.2)'; this.style.background='rgba(0, 123, 255, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(0, 123, 255, 0.05)';">

**🪟 Windows**

**Start Ollama:**

```powershell
ollama serve
```

**Or run in background:**

```powershell
Start-Process "ollama" -ArgumentList "serve" -WindowStyle Hidden
```

**Verify it's running:**

```powershell
ollama list
```

> **💡 Tip:** Keep terminal open or run as background process.

</div>

<div style="background: rgba(108, 117, 125, 0.05); border: 2px solid rgba(108, 117, 125, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(108,117,125,0.2)'; this.style.background='rgba(108, 117, 125, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(108, 117, 125, 0.05)';">

**🍎 macOS**

**Start as background service:**

```bash
brew services start ollama
```

**Verify status:**

```bash
brew services list
```

**Expected output:**

```
Name   Status  User
ollama started <username>
```

> **💡 Tip:** Service auto-starts on system boot.

</div>

</div>

---

## **2.2 Download AI Model**

Download DeepSeek-Coder, a specialized code generation model.

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin: 20px 0;">

<div style="background: rgba(0, 123, 255, 0.05); border: 2px solid rgba(0, 123, 255, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(0,123,255,0.2)'; this.style.background='rgba(0, 123, 255, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(0, 123, 255, 0.05)';">

**🪟 Windows**

**Download model:**

```powershell
ollama pull deepseek-coder

```

**Download progress:**

```
pulling manifest
pulling 8934d96d3f08... 100% ▕████████▏ 3.8 GB
pulling 8c17c2ebb0ea... 100% ▕████████▏ 7.0 KB
pulling 7c23fb36d801... 100% ▕████████▏ 4.8 KB
pulling 2e0493f67d0c... 100% ▕████████▏   59 B
pulling fa8235e5b48f... 100% ▕████████▏  491 B
verifying sha256 digest
writing manifest
success
```

**Test the model:**

```powershell
ollama run deepseek-coder "Write a hello world in Python"
```

</div>

<div style="background: rgba(108, 117, 125, 0.05); border: 2px solid rgba(108, 117, 125, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(108,117,125,0.2)'; this.style.background='rgba(108, 117, 125, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(108, 117, 125, 0.05)';">

**🍎 macOS**

**Download model:**

```bash
ollama pull deepseek-coder

```

**Download progress:**

```
pulling manifest
pulling 8934d96d3f08... 100% ▕████████▏ 3.8 GB
pulling 8c17c2ebb0ea... 100% ▕████████▏ 7.0 KB
pulling 7c23fb36d801... 100% ▕████████▏ 4.8 KB
pulling 2e0493f67d0c... 100% ▕████████▏   59 B
pulling fa8235e5b48f... 100% ▕████████▏  491 B
verifying sha256 digest
writing manifest
success
```

**Test the model:**

```bash
ollama run deepseek-coder "Write a hello world in Python"
```

</div>

</div>

> **⏱️ Time:** Download takes 5-35 minutes (3.8 GB model size).
>
> **💾 Disk Space:** Ensure you have at least 10 GB free.

---

# **Step 3: Create Project Structure**

## **3.1 Set Up Project Folder**

Create a dedicated directory for your course generator.

**First, open your Documents folder in VS Code:**

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin: 20px 0;">

<div style="background: rgba(0, 123, 255, 0.05); border: 2px solid rgba(0, 123, 255, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(0,123,255,0.2)'; this.style.background='rgba(0, 123, 255, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(0, 123, 255, 0.05)';">

**🪟 Windows**

**Open VS Code:**

1. Open VS Code
2. Click `File` → `Open Folder`
3. Navigate to `Documents`
4. Click "Select Folder"

**Open Terminal in VS Code:**

- Click `View` → `Terminal`
- Or press `` Ctrl + ` ``

**Create project folder:**

```powershell
cd $HOME\Documents
mkdir CourseProjectTool
cd CourseProjectTool
```

**Verify location:**

```powershell
pwd
```

**Expected output:**

```
Path
----
C:\Users\YourName\Documents\CourseProjectTool
```

</div>

<div style="background: rgba(108, 117, 125, 0.05); border: 2px solid rgba(108, 117, 125, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(108,117,125,0.2)'; this.style.background='rgba(108, 117, 125, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(108, 117, 125, 0.05)';">

**🍎 macOS**

**Open VS Code:**

1. Open VS Code
2. Click `File` → `Open Folder`
3. Navigate to `Documents`
4. Click "Open"

**Open Terminal in VS Code:**

- Click `View` → `Terminal`
- Or press `` Ctrl + ` ``

**Create project folder:**

```bash
cd ~/Documents
mkdir CourseProjectTool
cd CourseProjectTool
```

**Verify location:**

```bash
pwd
```

**Expected output:**

```
/Users/YourName/Documents/CourseProjectTool
```

</div>

</div>

---

## **3.2 Create Python Script File**

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin: 20px 0;">

<div style="background: rgba(0, 123, 255, 0.05); border: 2px solid rgba(0, 123, 255, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(0,123,255,0.2)'; this.style.background='rgba(0, 123, 255, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(0, 123, 255, 0.05)';">

**🪟 Windows**

**Create file:**

```powershell
New-Item -Path "smart_course_project.py" -ItemType File

```

**Open in VS Code:**

```powershell
code smart_course_project.py

```

</div>

<div style="background: rgba(108, 117, 125, 0.05); border: 2px solid rgba(108, 117, 125, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(108,117,125,0.2)'; this.style.background='rgba(108, 117, 125, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(108, 117, 125, 0.05)';">

**🍎 macOS**

**Create file:**

```bash
touch smart_course_project.py

```

**Open in VS Code:**

```bash
code smart_course_project.py

```

</div>

</div>

> **📝 Note:** VS Code will open automatically. If prompted to install Python extension, click "Install".

---
# **Step 4: Implement the Generator**

## **4.1 Copy Python Code**

Copy the complete script below into your `smart_course_project.py` file.

```python
import subprocess
from pathlib import Path

BASE_PATH = Path.home() / "Documents" / "Mini_Workshop_Course_Development"
COURSE_NAME = "Mini Workshop Course Development"
MODEL = "deepseek-coder"

def ollama_generate(prompt: str) -> str:
    result = subprocess.run(
        ["ollama", "run", MODEL],
        input=prompt.encode("utf-8"),
        stdout=subprocess.PIPE,
        stderr=subprocess.PIPE,
    )
    return result.stdout.decode("utf-8", errors="ignore")

def save_yaml(folder: str, filename: str, content: str):
    path = BASE_PATH / folder
    path.mkdir(parents=True, exist_ok=True)
    with open(path / filename, "w", encoding="utf-8") as f:
        f.write(content)
    print(f"[OK] saved {folder}/{filename}")

def create_ai_course():
    sections = {
        "personality": "Define learners, tone, and course context.",
        "structure": "Outline units, structure, and sequence.",
        "activities": "List tasks, discussions, reflections.",
        "output": "Describe learning outcomes and assessment."
    }

    print(f"[AI] Generating course: {COURSE_NAME}\n")

    for section, desc in sections.items():
        filename = f"{section}.yaml"
        target_file = BASE_PATH / section / filename
        if target_file.exists():
            print(f"[skip] {section}.yaml already exists")
            continue
        prompt = f"Create a YAML file for the {section} part of a course titled '{COURSE_NAME}'. Focus on: {desc}."
        print(f"[AI] Generating {section}.yaml ...")
        content = ollama_generate(prompt)
        save_yaml(section, filename, content)

    summary_md = BASE_PATH / f"{COURSE_NAME.replace(' ', '_')}.md"
    prompt_summary = f"""
Generate a Markdown summary for '{COURSE_NAME}' including:
- Course description
- Learning objectives
- Section overview
- Expected outcomes
- Final message
"""
    print("[AI] Generating Markdown summary...")
    summary_content = ollama_generate(prompt_summary)

    with open(summary_md, "w", encoding="utf-8") as f:
        f.write(summary_content)

    print(f"\n✅ Course '{COURSE_NAME}' created at {BASE_PATH}")

if __name__ == "__main__":
    create_ai_course()
```

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin: 20px 0;">

<div style="background: rgba(0, 123, 255, 0.05); border: 2px solid rgba(0, 123, 255, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(0,123,255,0.2)'; this.style.background='rgba(0, 123, 255, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(0, 123, 255, 0.05)';">

**🪟 Windows**

**Save the file:**

1. Press `Ctrl + S`
2. Confirm the filename is `smart_course_project.py`
3. Ensure it's in `Documents\CourseProjectTool`

</div>

<div style="background: rgba(108, 117, 125, 0.05); border: 2px solid rgba(108, 117, 125, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(108,117,125,0.2)'; this.style.background='rgba(108, 117, 125, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(108, 117, 125, 0.05)';">

**🍎 macOS**

**Save the file:**

1. Press `⌘ + S`
2. Confirm the filename is `smart_course_project.py`
3. Ensure it's in `Documents/CourseProjectTool`

</div>

</div>

---

# **Step 5: Generate Your First Course**

## **5.1 Open Integrated Terminal**

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin: 20px 0;">

<div style="background: rgba(0, 123, 255, 0.05); border: 2px solid rgba(0, 123, 255, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(0,123,255,0.2)'; this.style.background='rgba(0, 123, 255, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(0, 123, 255, 0.05)';">

**🪟 Windows**

**In VS Code:**

1. Click `New Terminal`
2. Or press `` Ctrl + ` ``

**Check PowerShell is selected** in terminal dropdown

**Navigate to project:**

```powershell
cd $HOME\Documents\CourseProjectTool

```

</div>

<div style="background: rgba(108, 117, 125, 0.05); border: 2px solid rgba(108, 117, 125, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(108,117,125,0.2)'; this.style.background='rgba(108, 117, 125, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(108, 117, 125, 0.05)';">

**🍎 macOS**

**In VS Code:**

1. Click `New Terminal`
2. Or press `` Ctrl + ` ``

**Check bash/zsh is selected** in terminal dropdown

**Navigate to project:**

```bash
cd ~/Documents/CourseProjectTool

```

</div>

</div>

---
## **5.2 Run the Generator**

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin: 20px 0;">

<div style="background: rgba(0, 123, 255, 0.05); border: 2px solid rgba(0, 123, 255, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(0,123,255,0.2)'; this.style.background='rgba(0, 123, 255, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(0, 123, 255, 0.05)';">

**🪟 Windows**

**Execute:**

```powershell
python smart_course_project.py

```

**Duration:** 4-10 minutes

</div>

<div style="background: rgba(108, 117, 125, 0.05); border: 2px solid rgba(108, 117, 125, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(108,117,125,0.2)'; this.style.background='rgba(108, 117, 125, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(108, 117, 125, 0.05)';">

**🍎 macOS**

**Execute:**

```bash
python3 smart_course_project.py

```

**Duration:** 4-10 minutes

</div>

</div>



**Expected Output (Both Systems):**

```
======================================================================
  🎓 AI Course Generator
  📚 Course: Mini Workshop Course Development
  📁 Location: ~/Documents/Mini_Workshop_Course_Development
======================================================================

📝 Section: PERSONALITY
   Purpose: Define target learners...
  🤖 AI is thinking... ✓
  💾 Saved: personality/personality.yaml

📝 Section: STRUCTURE
   Purpose: Outline units, modules...
  🤖 AI is thinking... ✓
  💾 Saved: structure/structure.yaml

📝 Section: ACTIVITIES
   Purpose: List learning activities...
  🤖 AI is thinking... ✓
  💾 Saved: activities/activities.yaml

📝 Section: OUTPUT
   Purpose: Describe learning outcomes...
  🤖 AI is thinking... ✓
  💾 Saved: output/output.yaml

📝 Section: SUMMARY
   Purpose: Create course overview
  🤖 AI is thinking... ✓
  💾 Saved: Mini_Workshop_Course_Development.md

======================================================================
  ✅ Course generation complete!
  📂 Open folder: ~/Documents/Mini_Workshop_Course_Development
======================================================================
```

> **⏱️ Note:** The AI model generates each section sequentially. This is normal and ensures quality output.

---

## **5.3 View Generated Files**

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin: 20px 0;">

<div style="background: rgba(0, 123, 255, 0.05); border: 2px solid rgba(0, 123, 255, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(0,123,255,0.2)'; this.style.background='rgba(0, 123, 255, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(0, 123, 255, 0.05)';">

**🪟 Windows**

**Open in File Explorer:**

```powershell
explorer "$HOME\Documents\Mini_Workshop_Course_Development"

```

**Or via VS Code:**

```powershell
code "$HOME\Documents\Mini_Workshop_Course_Development"

```

**Expected structure:**

```
Mini_Workshop_Course_Development/
├── personality/
│   └── personality.yaml
├── structure/
│   └── structure.yaml
├── activities/
│   └── activities.yaml
├── output/
│   └── output.yaml
└── Mini_Workshop_Course_Development.md

```

</div>

<div style="background: rgba(108, 117, 125, 0.05); border: 2px solid rgba(108, 117, 125, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(108,117,125,0.2)'; this.style.background='rgba(108, 117, 125, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(108, 117, 125, 0.05)';">

**🍎 macOS**

**Open in Finder:**

```bash
open ~/Documents/Mini_Workshop_Course_Development

```

**Or via VS Code:**

```bash
code ~/Documents/Mini_Workshop_Course_Development

```

**Expected structure:**

```
Mini_Workshop_Course_Development/
├── personality/
│   └── personality.yaml
├── structure/
│   └── structure.yaml
├── activities/
│   └── activities.yaml
├── output/
│   └── output.yaml
└── Mini_Workshop_Course_Development.md

```

</div>

</div>

---

# **Step 6: Customize & Regenerate**

## **6.1 Edit Manually**

You can refine any generated section by hand.

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin: 20px 0;">

<div style="background: rgba(0, 123, 255, 0.05); border: 2px solid rgba(0, 123, 255, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(0,123,255,0.2)'; this.style.background='rgba(0, 123, 255, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(0, 123, 255, 0.05)';">

**🪟 Windows**

**Open specific file:**

```powershell
code "$HOME\Documents\Mini_Workshop_Course_Development\structure\structure.yaml"

```

**Edit → Save → Done**

- Press `Ctrl + S` to save
- Changes are preserved

</div>

<div style="background: rgba(108, 117, 125, 0.05); border: 2px solid rgba(108, 117, 125, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(108,117,125,0.2)'; this.style.background='rgba(108, 117, 125, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(108, 117, 125, 0.05)';">

**🍎 macOS**

**Open specific file:**

```bash
code ~/Documents/Mini_Workshop_Course_Development/structure/structure.yaml

```

**Edit → Save → Done**

- Press `⌘ + S` to save
- Changes are preserved

</div>

</div>

---

## **6.2 Regenerate Specific Sections**

If you want AI to recreate a section with fresh content.

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin: 20px 0;">

<div style="background: rgba(0, 123, 255, 0.05); border: 2px solid rgba(0, 123, 255, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(0,123,255,0.2)'; this.style.background='rgba(0, 123, 255, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(0, 123, 255, 0.05)';">

**🪟 Windows**

**Delete the section file:**

```powershell
Remove-Item "$HOME\Documents\Mini_Workshop_Course_Development\activities\activities.yaml"

```

**Rerun the generator:**

```powershell
python smart_course_project.py

```

**Result:** Only the deleted section regenerates

</div>

<div style="background: rgba(108, 117, 125, 0.05); border: 2px solid rgba(108, 117, 125, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(108,117,125,0.2)'; this.style.background='rgba(108, 117, 125, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(108, 117, 125, 0.05)';">

**🍎 macOS**

**Delete the section file:**

```bash
rm ~/Documents/Mini_Workshop_Course_Development/activities/activities.yaml

```

**Rerun the generator:**

```bash
python3 smart_course_project.py

```

**Result:** Only the deleted section regenerates

</div>

</div>

> **💡 Smart Skip:** The script automatically detects existing files and skips them, saving time.

---

## **6.3 Create Different Courses**

Modify the script to generate completely new courses.

**Step 1: Open your script**

```python
code smart_course_project.py

```

**Step 2: Change these lines (around line 8-9):**

```python
# FROM:
BASE_PATH = Path.home() / "Documents" / "Mini_Workshop_Course_Development"
COURSE_NAME = "Mini Workshop Course Development"

# TO:
BASE_PATH = Path.home() / "Documents" / "Quantitative_Research_Methods"
COURSE_NAME = "Quantitative Research Methods"

```

**Step 3: Save and run**

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin: 20px 0;">

<div style="background: rgba(0, 123, 255, 0.05); border: 2px solid rgba(0, 123, 255, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(0,123,255,0.2)'; this.style.background='rgba(0, 123, 255, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(0, 123, 255, 0.05)';">

**🪟 Windows**

```powershell
python smart_course_project.py

```

</div>

<div style="background: rgba(108, 117, 125, 0.05); border: 2px solid rgba(108, 117, 125, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(108,117,125,0.2)'; this.style.background='rgba(108, 117, 125, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(108, 117, 125, 0.05)';">

**🍎 macOS**

```bash
python3 smart_course_project.py

```

</div>

</div>

**Result:** A new course folder is created with fresh AI-generated content!

---


# **Step 7: Advanced Customization**

## **7.1 Modify AI Prompts**

You can fine-tune how the AI generates content.

**Edit the `sections` dictionary in your Python script:**

```python
sections = {
    "personality": {
        "desc": "Your custom description here",
        "prompt": """Your enhanced prompt here.
        
Add specific requirements:
- Must include X
- Should focus on Y
- Format as Z
        """
    },
    # ... more sections
}
```

**Example: Make structure more detailed**

```python
"structure": {
    "desc": "Detailed unit breakdown with time estimates",
    "prompt": """Create a YAML file for the structure section of '{COURSE_NAME}'.

Requirements:
- 8-12 units minimum
- Each unit must have:
  * Title
  * Learning objectives (3-5 per unit)
  * Topics covered (detailed list)
  * Estimated time (in hours)
  * Prerequisites
  * Resources needed
  
Format as valid YAML with proper indentation."""
}
```

---

## **7.2 Change the AI Model**

DeepSeek-Coder is optimized for code, but you can use other models.

**Some available models:**

| Model | Size | Best For |
|-------|------|----------|
| `deepseek-coder` | 3.8 GB | Code generation, technical courses |
| `llama3.2` | 2 GB | General education, humanities |
| `phi3` | 2.3 GB | Faster, lighter, good for quick generation |

**To change:**

1. Download new model:

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin: 10px 0;">

<div style="background: rgba(0, 123, 255, 0.05); border: 2px solid rgba(0, 123, 255, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(0,123,255,0.2)'; this.style.background='rgba(0, 123, 255, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(0, 123, 255, 0.05)';">

**🪟 Windows**

```powershell
ollama pull llama3.2

```

</div>

<div style="background: rgba(108, 117, 125, 0.05); border: 2px solid rgba(108, 117, 125, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(108,117,125,0.2)'; this.style.background='rgba(108, 117, 125, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(108, 117, 125, 0.05)';">

**🍎 macOS**

```bash
ollama pull llama3.2

```

</div>

</div>

2. Edit your script (line 9):

```python
MODEL = "llama3.2"  # Changed from deepseek-coder

```

3. Regenerate course

---

## **7.3 Add More Sections**

Expand your course structure with custom sections.

**Example: Add "Resources" section**

```python
sections = {
    # ... existing sections ...
    
    "resources": {
        "desc": "Course materials, tools, and references.",
        "prompt": """Create a YAML file for the resources section of '{COURSE_NAME}'.
        
Include:
- required_textbooks: (with ISBN, authors)
- optional_readings: (articles, papers)
- software_tools: (applications needed)
- online_resources: (websites, videos)
- datasets: (if applicable)

Format as valid YAML."""
    }
}
```

---





# **Appendix: Quick Reference**

## Command Cheat Sheet

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin: 20px 0;">

<div style="background: rgba(0, 123, 255, 0.05); border: 2px solid rgba(0, 123, 255, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(0,123,255,0.2)'; this.style.background='rgba(0, 123, 255, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(0, 123, 255, 0.05)';">

**🪟 Windows**

**Essential Commands:**

```powershell
# Navigate
cd $HOME\Documents\CourseProjectTool

# Run generator
python smart_course_project.py

# Start Ollama
ollama serve

# List models
ollama list

# Pull new model
ollama pull <model-name>

# Open in VS Code
code .

# View files
explorer .

# Check Python
python --version

# Update packages
choco upgrade all -y

```

</div>

<div style="background: rgba(108, 117, 125, 0.05); border: 2px solid rgba(108, 117, 125, 0.3); padding: 20px; border-radius: 10px; transition: all 0.3s ease; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 8px 16px rgba(108,117,125,0.2)'; this.style.background='rgba(108, 117, 125, 0.08)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 8px rgba(0,0,0,0.1)'; this.style.background='rgba(108, 117, 125, 0.05)';">

**🍎 macOS**

**Essential Commands:**

```bash
# Navigate
cd ~/Documents/CourseProjectTool

# Run generator
python3 smart_course_project.py

# Start Ollama
brew services start ollama

# List models
ollama list

# Pull new model
ollama pull <model-name>

# Open in VS Code
code .

# View files
open .

# Check Python
python3 --version

# Update packages
brew upgrade

```

</div>

</div>

---

## File Structure Reference

```
Documents/
└── CourseProjectTool/
    └── smart_course_project.py          # Main generator script

Documents/
└── Mini_Workshop_Course_Development/    # Generated course
    ├── personality/
    │   └── personality.yaml             # Learner & teaching style
    ├── structure/
    │   └── structure.yaml               # Units & organization
    ├── activities/
    │   └── activities.yaml              # Tasks & exercises
    ├── output/
    │   └── output.yaml                  # Outcomes & assessment
    └── Mini_Workshop_Course_Development.md  # Summary document
```

---


## 🎉 Congratulations!

<div style="background: rgba(255,255,255,0.15); padding: 25px; border-radius: 12px; margin: 20px 0; backdrop-filter: blur(10px);">

**You've successfully completed the Agentic AI Workshop!**

</div>

<div style="background: rgba(255,255,255,0.1); border-left: 5px solid #ffd700; padding: 20px; border-radius: 8px; margin: 25px 0; font-style: italic; text-align: left;">

*"The integration of Agentic AI in TVET is not about replacing educators; it's about empowering them to focus on what matters most: inspiring learners, fostering critical thinking, and preparing the workforce of tomorrow. Technology amplifies our potential; it is our wisdom and compassion that give it purpose."*

<div style="text-align: right; margin-top: 15px; font-weight: bold; color: #ffd700;">
**— The Future of Education is in Your Hands**
</div>

</div>


<div style="background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%); padding: 30px; border-radius: 15px; box-shadow: 0 8px 25px rgba(245,87,108,0.4); margin: 30px 0; color: white; transition: transform 0.3s ease;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'">


<div style="text-align: center; font-size: 1.8em; margin-top: 20px; text-shadow: 2px 2px 4px rgba(0,0,0,0.3);">

**Happy Course Creating! 🎓✨**

</div>

</div>

