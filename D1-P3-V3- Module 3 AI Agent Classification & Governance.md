<!--
author:   Mahwish Kanwal, Sabbir Rifat
email:    mahwish.kanwal@ovgu.de, a.rifat@ovgu.de
version:  3.0.0
language: en
narrator: US English Female
comment:  Module 3: AI Agent Classification & Governance Framework - Master the 7-dimension framework and practical risk assessment

@style
.dimension-card {
    background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
    color: white;
    padding: 25px;
    margin: 20px 0;
    border-radius: 15px;
    box-shadow: 0 8px 16px rgba(0,0,0,0.2);
}

.classification-box {
    background: linear-gradient(135deg, #E3F2FD 0%, #BBDEFB 100%);
    padding: 25px;
    margin: 20px 0;
    border-radius: 12px;
    border-left: 5px solid #1976D2;
    line-height: 1.9;
}

.example-card {
    background: #ffffff;
    border: 2px solid #e0e0e0;
    padding: 20px;
    margin: 15px 0;
    border-radius: 10px;
    box-shadow: 0 6px 12px rgba(0,0,0,0.15);
}

.spectrum-box {
    background: linear-gradient(90deg, #ffebee 0%, #fff9e6 50%, #e8f5e9 100%);
    padding: 20px;
    margin: 15px 0;
    border-radius: 12px;
}

.interactive-exercise {
    background: linear-gradient(135deg, #fff3e0 0%, #ffe0b2 100%);
    padding: 25px;
    margin: 20px 0;
    border-radius: 15px;
}

.key-insight {
    background: linear-gradient(135deg, #E8F5E9 0%, #C8E6C9 100%);
    padding: 20px;
    margin: 20px 0;
    border-radius: 12px;
    border-left: 5px solid #4CAF50;
    font-size: 1.15em;
}

.warning-box {
    background: linear-gradient(135deg, #FFEBEE 0%, #FFCDD2 100%);
    padding: 20px;
    margin: 15px 0;
    border-radius: 12px;
}

.governance-card {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 25px;
    margin: 20px 0;
    border-radius: 15px;
    box-shadow: 0 8px 16px rgba(0,0,0,0.2);
}

.task-box {
    background: linear-gradient(135deg, #ffeaa7 0%, #fdcb6e 100%);
    padding: 25px;
    margin: 20px 0;
    border-radius: 15px;
    border: 3px solid #e17055;
}

.solution-box {
    background: linear-gradient(135deg, #dfe6e9 0%, #b2bec3 100%);
    padding: 20px;
    margin: 15px 0;
    border-radius: 10px;
    border-left: 5px solid #2d3436;
}

.preview-card {
    background: linear-gradient(135deg, #a29bfe 0%, #6c5ce7 100%);
    color: white;
    padding: 30px;
    margin: 25px 0;
    border-radius: 15px;
    box-shadow: 0 10px 20px rgba(0,0,0,0.3);
}

/* ========================================
   TASK 1: MODULE ROADMAP STYLES
   Transparent blue boxes with hover effect
   ======================================== */
.roadmap-container {
    max-width: 900px;
    margin: 30px auto;
}

.roadmap-header {
    background: linear-gradient(135deg, #2196F3 0%, #1976D2 100%);
    color: white;
    padding: 25px;
    border-radius: 12px 12px 0 0;
    text-align: center;
    font-size: 1.3em;
    font-weight: bold;
    box-shadow: 0 4px 12px rgba(33, 150, 243, 0.3);
}

.roadmap-box {
    background: rgba(33, 150, 243, 0.08);
    border: 2px solid rgba(33, 150, 243, 0.3);
    border-radius: 12px;
    padding: 25px;
    margin: 20px 0;
    transition: all 0.3s ease;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.roadmap-box:hover {
    transform: translateY(-8px);
    box-shadow: 0 12px 24px rgba(33, 150, 243, 0.25);
    background: rgba(33, 150, 243, 0.12);
    border-color: rgba(33, 150, 243, 0.5);
}

.part-title {
    color: #1976D2;
    font-size: 1.25em;
    font-weight: bold;
    margin-bottom: 15px;
    display: flex;
    align-items: center;
}

.time-badge {
    background: #2196F3;
    color: white;
    padding: 4px 12px;
    border-radius: 20px;
    font-size: 0.75em;
    margin-left: auto;
}

.roadmap-item {
    margin: 10px 0 10px 20px;
    color: #333;
    line-height: 1.8;
}

.exercise-box {
    background: rgba(255, 152, 0, 0.1);
    border-left: 4px solid #FF9800;
    padding: 15px 20px;
    margin: 15px 0;
    border-radius: 8px;
}

/* ========================================
   TASK 2: SIDE-BY-SIDE BOXES STYLES
   Challenge and Solution transparent boxes
   ======================================== */
.side-by-side-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 25px;
    margin: 30px 0;
}

.challenge-box {
    background: rgba(244, 67, 54, 0.08);
    border: 2px solid rgba(244, 67, 54, 0.3);
    border-radius: 12px;
    padding: 25px;
    transition: all 0.3s ease;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.challenge-box:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 16px rgba(244, 67, 54, 0.2);
    background: rgba(244, 67, 54, 0.12);
}

.solution-box-new {
    background: rgba(76, 175, 80, 0.08);
    border: 2px solid rgba(76, 175, 80, 0.3);
    border-radius: 12px;
    padding: 25px;
    transition: all 0.3s ease;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.solution-box-new:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 16px rgba(76, 175, 80, 0.2);
    background: rgba(76, 175, 80, 0.12);
}

.box-title {
    font-size: 1.3em;
    font-weight: bold;
    margin-bottom: 18px;
    padding-bottom: 10px;
    border-bottom: 2px solid currentColor;
}

.challenge-box .box-title {
    color: #D32F2F;
}

.solution-box-new .box-title {
    color: #388E3C;
}

.box-content {
    line-height: 1.9;
    color: #333;
}

/* ========================================
   TASK 3: SEQUENTIAL BOXES STYLES
   Boxes appear one by one with Next button
   ======================================== */
.sequential-container {
    max-width: 800px;
    margin: 30px auto;
}

.sequential-box {
    background: rgba(103, 58, 183, 0.08);
    border: 2px solid rgba(103, 58, 183, 0.3);
    border-radius: 12px;
    padding: 25px;
    margin: 20px 0;
    display: none;
    opacity: 0;
    transition: opacity 0.5s ease;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.sequential-box.active {
    display: block;
    opacity: 1;
}

.next-button {
    background: linear-gradient(135deg, #673AB7 0%, #512DA8 100%);
    color: white;
    border: none;
    padding: 12px 30px;
    border-radius: 25px;
    font-size: 1.1em;
    font-weight: bold;
    cursor: pointer;
    margin: 20px auto;
    display: block;
    transition: all 0.3s ease;
    box-shadow: 0 4px 12px rgba(103, 58, 183, 0.3);
}

.next-button:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 16px rgba(103, 58, 183, 0.4);
    background: linear-gradient(135deg, #512DA8 0%, #4527A0 100%);
}

.next-button:disabled {
    background: #9E9E9E;
    cursor: not-allowed;
    transform: none;
    box-shadow: none;
}

.progress-indicator {
    text-align: center;
    color: #673AB7;
    font-weight: bold;
    margin: 15px 0;
}

.scenario-title {
    color: #673AB7;
    font-size: 1.2em;
    font-weight: bold;
    margin-bottom: 15px;
}

/* ========================================
   TASK 4: FRAMEWORK VISUALIZATION STYLES
   Enhanced 7-Dimension Framework display
   ======================================== */
.framework-container {
    max-width: 900px;
    margin: 40px auto;
    padding: 20px;
}

.framework-header {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 30px;
    border-radius: 15px;
    text-align: center;
    font-size: 1.5em;
    font-weight: bold;
    box-shadow: 0 8px 20px rgba(102, 126, 234, 0.3);
    margin-bottom: 30px;
}

.dimension-category {
    background: linear-gradient(135deg, #E3F2FD 0%, #BBDEFB 100%);
    border-radius: 15px;
    padding: 30px;
    margin: 25px 0;
    box-shadow: 0 6px 15px rgba(0, 0, 0, 0.1);
}

.category-header {
    color: #1565C0;
    font-size: 1.4em;
    font-weight: bold;
    text-align: center;
    margin-bottom: 10px;
}

.category-subtitle {
    color: #1976D2;
    text-align: center;
    font-style: italic;
    margin-bottom: 25px;
}

.dimension-item {
    background: white;
    border-left: 5px solid #2196F3;
    border-radius: 10px;
    padding: 20px;
    margin: 15px 0;
    transition: all 0.3s ease;
    box-shadow: 0 3px 8px rgba(0, 0, 0, 0.08);
}

.dimension-item:hover {
    transform: translateX(10px);
    box-shadow: 0 5px 15px rgba(33, 150, 243, 0.2);
}

.dimension-number {
    background: linear-gradient(135deg, #2196F3 0%, #1976D2 100%);
    color: white;
    width: 40px;
    height: 40px;
    border-radius: 50%;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    font-size: 1.2em;
    font-weight: bold;
    margin-right: 15px;
    vertical-align: middle;
}

.dimension-name {
    color: #1976D2;
    font-size: 1.2em;
    font-weight: bold;
    display: inline;
}

.dimension-question {
    color: #555;
    font-style: italic;
    margin: 10px 0 0 55px;
}

.flow-arrow {
    text-align: center;
    font-size: 2em;
    color: #2196F3;
    margin: 10px 0;
}

.emergent-box {
    background: linear-gradient(135deg, #FFF3E0 0%, #FFE0B2 100%);
    border-radius: 15px;
    padding: 30px;
    margin: 25px 0;
    box-shadow: 0 6px 15px rgba(255, 152, 0, 0.2);
    border: 3px solid #FF9800;
}

.emergent-header {
    color: #E65100;
    font-size: 1.4em;
    font-weight: bold;
    text-align: center;
    margin-bottom: 20px;
}

.emergent-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 15px;
}

.emergent-item {
    background: white;
    padding: 15px;
    border-radius: 8px;
    border-left: 4px solid #FF9800;
    font-weight: 500;
}

/* ========================================
   TASK 5: RISK MATRIX STYLES
   Enhanced color-coded risk matrix
   ======================================== */
.risk-matrix-container {
    max-width: 900px;
    margin: 40px auto;
    padding: 20px;
}

.risk-matrix-header {
    background: linear-gradient(135deg, #F44336 0%, #D32F2F 100%);
    color: white;
    padding: 20px;
    border-radius: 12px 12px 0 0;
    text-align: center;
    font-size: 1.3em;
    font-weight: bold;
}

.risk-matrix-grid {
    display: grid;
    grid-template-columns: 150px repeat(5, 1fr);
    gap: 2px;
    background: #333;
    border-radius: 0 0 12px 12px;
    overflow: hidden;
}

.matrix-cell {
    padding: 18px 12px;
    text-align: center;
    font-weight: 600;
    min-height: 70px;
    display: flex;
    align-items: center;
    justify-content: center;
}

.matrix-header-col {
    background: linear-gradient(135deg, #455A64 0%, #37474F 100%);
    color: white;
    font-size: 0.9em;
}

.matrix-header-row {
    background: linear-gradient(135deg, #455A64 0%, #37474F 100%);
    color: white;
    font-size: 0.85em;
    writing-mode: horizontal-tb;
}

.matrix-corner {
    background: linear-gradient(135deg, #263238 0%, #1C2831 100%);
    color: rgba(255,255,255,0.5);
    font-size: 0.75em;
}

.risk-vlow {
    background: linear-gradient(135deg, #C8E6C9 0%, #A5D6A7 100%);
    color: #1B5E20;
}

.risk-low {
    background: linear-gradient(135deg, #FFF9C4 0%, #FFF59D 100%);
    color: #F57F17;
}

.risk-med {
    background: linear-gradient(135deg, #FFE082 0%, #FFD54F 100%);
    color: #E65100;
}

.risk-high {
    background: linear-gradient(135deg, #FFAB91 0%, #FF8A65 100%);
    color: #BF360C;
}

.risk-vhigh {
    background: linear-gradient(135deg, #EF9A9A 0%, #E57373 100%);
    color: #B71C1C;
}

.risk-critical {
    background: linear-gradient(135deg, #E57373 0%, #EF5350 100%);
    color: white;
    font-weight: 800;
}

.risk-legend {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
    gap: 15px;
    margin: 25px 0;
}

.legend-item {
    padding: 12px;
    border-radius: 8px;
    text-align: center;
    font-weight: 600;
    box-shadow: 0 3px 8px rgba(0, 0, 0, 0.15);
}

table {
    border-collapse: collapse;
    width: 100%;
    margin: 20px 0;
    box-shadow: 0 4px 8px rgba(0,0,0,0.15);
}

th {
    background: linear-gradient(135deg, #2C3E50 0%, #34495E 100%);
    color: white;
    padding: 15px;
    text-align: left;
    font-weight: bold;
}

td {
    padding: 15px 18px;
    border-bottom: 2px solid #E0E0E0;
}

tr:nth-child(even) {
    background-color: #f8f9fa;
}

tr:hover {
    background-color: #e3f2fd;
    transition: background-color 0.3s;
}

@media (max-width: 768px) {
    .side-by-side-container {
        grid-template-columns: 1fr;
    }
    .risk-matrix-grid {
        font-size: 0.8em;
    }
}
@end

-->

# Module 3: AI Agent Classification & Governance
> **The 7-Dimension Framework & Practical Risk Assessment**
>
> *Systematic Approaching, Evaluating & Governing AI Agents*
>
> Duration: 90 minutes | Interactive Classification & Governance Workshop

---

## 🎯 Learning Objectives

By the end of this module, you will be able to:

- [X] Master all seven classification dimensions and their importance
- [X] Apply the framework to classify real-world AI agents
- [X] Identify risk factors based on dimensional profiles
- [X] Compare agents systematically across dimensions
- [X] Conduct comprehensive agent risk assessments
- [X] Design proportionate governance mechanisms
- [X] Make informed governance decisions using classification data
- [X] Recognize interaction effects between dimensions

---

## 📊 Module Roadmap

<div class="roadmap-container">

<div class="roadmap-header">
📊 MODULE 3: CLASSIFICATION & GOVERNANCE - 90 MIN
</div>

{{1}}
<div class="roadmap-box">
<div class="part-title">
Part 1: CLASSIFICATION FRAMEWORK
<span class="time-badge">40 min</span>
</div>
<div class="roadmap-item">🎯 Why Classification Matters </div>
<div class="roadmap-item">📐 The 7-Dimension Framework Overview </div>
<div class="roadmap-item">🔗 Dimensional Interactions</div>
<div class="roadmap-item">📊 Detailed Dimensions 1-7 </div>
</div>

{{2}}
<div class="exercise-box">
<strong>👥 GROUP EXERCISE: Classification Practice (10 min)</strong>
</div>

{{3}}
<div class="roadmap-box">
<div class="part-title">
Part 2: RISK ASSESSMENT & GOVERNANCE
<span class="time-badge">25 min</span>
</div>
<div class="roadmap-item">🔍 Risk Assessment Framework </div>
<div class="roadmap-item">🛡️ Governance Mechanisms </div>
</div>

{{4}}
<div class="roadmap-box">
<div class="part-title">
Part 3: REAL-WORLD APPLICATIONS
<span class="time-badge">10 min</span>
</div>
<div class="roadmap-item">🌍 Case Studies & Examples </div>
</div>

{{5}}
<div class="exercise-box">
<strong>👤 INDIVIDUAL EXERCISE: Risk & Governance (5 min)</strong>
</div>

</div>

---

## Part 1: Classification Framework

### Why Classification Matters 🎯

<div class="side-by-side-container">

<div class="challenge-box">
<div class="box-title">❌ The Challenge</div>
<div class="box-content">

Without a systematic framework, organizations struggle to:

• Compare different AI agent solutions objectively  
• Assess risk profiles consistently  
• Design appropriate governance mechanisms  
• Communicate requirements clearly to vendors/developers  
• Make informed build-vs-buy decisions

</div>
</div>

<div class="solution-box-new">
<div class="box-title">✅ The Solution</div>
<div class="box-content">

A structured classification framework provides:

• **Common Language** for discussing agent capabilities  
• **Risk Assessment Foundation** based on dimensional profiles  
• **Governance Guidance** scaled to agent characteristics  
• **Comparison Baseline** across vendors and solutions  
• **Documentation Standard** for organizational AI inventories

</div>
</div>

</div>

---

#### Real-World Impact: Classification in Action


<div class="scenario-title">**Scenario:** Your company evaluates three chatbot vendors</div>

<div class="sequential-box active" id="box1">
<h4>Without Framework: Vague Claims</h4>

```
Vendor A: "Our AI is advanced and autonomous"
Vendor B: "We use cutting-edge machine learning"
Vendor C: "Our bot is smarter and more reliable"

→ Vague claims, no basis for comparison
```

<p style="color: #D32F2F; font-weight: bold; margin-top: 15px;">
❌ Result: No objective way to compare solutions
</p>
</div>

{{1}}
<div style="background: rgba(200, 255, 200, 0.1); border: 1px solid rgba(100, 255, 100, 0.2); border-radius: 8px; padding: 20px; margin: 20px 0;">

**With 7-Dimension Framework: Clear Comparison**

| Dimension | Vendor A | Vendor B | Vendor C |
|-----------|----------|----------|----------|
| **Function** | Support | Support | Sales |
| **Role** | Autonomous | Collaborative | Advisory |
| **Predictability** | Medium | High | Medium |
| **Autonomy** | High | Medium | Low |
| **Authority** | Tier 1-3 | Tier 1-2 | Tier 1 |
| **Use Case** | Customer Service | Technical Support | Lead Generation |
| **Environment** | Digital | Hybrid | Digital |

<p style="color: #388E3C; font-weight: bold; margin-top: 15px;">
✅ Result: Clear, objective comparison enables informed decision
</p>

</div>

{{2}}
<div style="background: rgba(200, 220, 255, 0.1); border: 1px solid rgba(100, 150, 255, 0.2); border-radius: 8px; padding: 20px; margin: 20px 0;">

**Decision Outcome**

<div style="background: linear-gradient(135deg, #E8F5E9 0%, #C8E6C9 100%); padding: 20px; border-radius: 8px; border-left: 5px solid #4CAF50; margin: 15px 0;">

**Based on Classification Analysis:**

✅ **Vendor B selected** for customer service needs because:

- High predictability reduces risk
- Collaborative role aligns with support workflow  
- Medium autonomy balances efficiency with oversight
- Proven technical support experience

🔍 **Risk Profile:** Medium-Low (manageable with standard governance)

📋 **Governance Plan:** Human-on-the-loop monitoring, weekly performance reviews

</div>

<p style="text-align: center; margin-top: 20px; font-size: 1.1em; color: #1976D2;">
💡 <strong>Framework enables data-driven decisions, not marketing claims</strong>
</p>

</div>

---


### The 7-Dimension Framework Overview 📐

<div class="framework-container">

<div class="framework-header">
🎯 7-DIMENSION CLASSIFICATION FRAMEWORK
</div>

<div class="dimension-category">
<div class="category-header">AGENT CHARACTERISTICS</div>
<div class="category-subtitle">(Internal Properties)</div>

<div class="dimension-item">
<span class="dimension-number">1</span>
<span class="dimension-name">FUNCTION</span>
<div class="dimension-question">What does the agent do?</div>
</div>

<div class="flow-arrow">↓</div>

<div class="dimension-item">
<span class="dimension-number">2</span>
<span class="dimension-name">ROLE</span>
<div class="dimension-question">How does it interact with users/systems?</div>
</div>

<div class="flow-arrow">↓</div>

<div class="dimension-item">
<span class="dimension-number">3</span>
<span class="dimension-name">PREDICTABILITY</span>
<div class="dimension-question">How consistent/stable are outputs?</div>
</div>

<div class="flow-arrow">↓</div>

<div class="dimension-item">
<span class="dimension-number">4</span>
<span class="dimension-name">AUTONOMY</span>
<div class="dimension-question">How independently does it operate?</div>
</div>

<div class="flow-arrow">↓</div>

<div class="dimension-item">
<span class="dimension-number">5</span>
<span class="dimension-name">AUTHORITY</span>
<div class="dimension-question">What decisions can it make?</div>
</div>

</div>

<div class="dimension-category">
<div class="category-header">OPERATIONAL CONTEXT</div>
<div class="category-subtitle">(External Factors)</div>

<div class="dimension-item">
<span class="dimension-number">6</span>
<span class="dimension-name">USE CASE</span>
<div class="dimension-question">Which domain/industry/application?</div>
</div>

<div class="flow-arrow">↓</div>

<div class="dimension-item">
<span class="dimension-number">7</span>
<span class="dimension-name">ENVIRONMENT</span>
<div class="dimension-question">Physical, digital, or hybrid context?</div>
</div>

</div>

<div class="flow-arrow">⬇ ⬇ ⬇ ⬇</div>

<div class="emergent-box">
<div class="emergent-header">⚡ EMERGENT PROPERTIES</div>
<div class="emergent-list">
<div class="emergent-item">📊 Overall Risk Profile</div>
<div class="emergent-item">⚖️ Governance Requirements</div>
<div class="emergent-item">📜 Regulatory Considerations</div>
<div class="emergent-item">👥 Stakeholder Impact</div>
</div>
</div>

</div>

<div class="key-insight">
💡 <strong>Core Principle:</strong> Classification defines an agent's characteristics and operational context to guide evaluation, risk assessment, and governance decisions. 

Without classification, oversight risks becoming inconsistent, reactive, or disconnected from an agent's actual capabilities and environment.
</div>

---


### Dimensional Interactions 🔗

Dimensions don't operate in isolation—they interact to create compound effects:

#### High-Risk Combinations

<div class="warning-box">

**⚠️ Red Flags: Dangerous Dimensional Combinations**

1. **High Autonomy + High Authority + Low Predictability**
   - Example: Trading algorithm with full buy/sell authority
   - Risk: Unpredictable high-stakes decisions
   - Mitigation: Mandatory human approval for transactions > threshold

2. **Physical Environment + Medium Predictability + High Autonomy**
   - Example: Delivery robot in crowded urban area
   - Risk: Safety incidents from unexpected behavior
   - Mitigation: Geo-fencing, constant telemetry, emergency stop

3. **High Authority + Specialist Function + Critical Use Case**
   - Example: Medical diagnosis agent with treatment authority
   - Risk: Errors in specialized high-stakes context
   - Mitigation: Human-in-the-loop, extensive validation, liability insurance

</div>

#### Dimensional Synergies

<div class="example-card">

**✅ Positive Combinations**

1. **Low Autonomy + Advisory Role + High Predictability**
   - Example: Grammar checking tool
   - Risk: Minimal
   - Governance: Minimal oversight required

2. **Medium Autonomy + Collaborative Role + Bounded Use Case**
   - Example: Research assistant for literature review
   - Risk: Low to Medium
   - Governance: Standard testing and monitoring

3. **High Predictability + Specialist Function + Digital Environment**
   - Example: Form validation agent
   - Risk: Low
   - Governance: Basic logging and error tracking

</div>

---

## Detailed Dimensions

### 1️⃣ Function: What Does It Do?

<div class="dimension-card">

**DIMENSION 1: FUNCTION**

**Definition:** The specific role, purpose, or set of tasks the agent is designed to perform.

**Key Question:** What does the agent do in practice, independent of the environment it's deployed in?

</div>

{{1}} 
<div class="dimension-card">

**Function Categories & Examples**

<div style="overflow-x: auto;">

| Category | Description | Examples |
|----------|-------------|----------|
| <span style="color: #FF4444; font-weight: bold; font-size: 1.1em;">Data Processing</span> | <span style="color: #1A1A1A; font-weight: 500;">Analyze, transform, aggregate information</span> | <span style="color: #2C2C2C;">SQL query agent, ETL pipeline</span> |
| <span style="color: #00D9FF; font-weight: bold; font-size: 1.1em;">Content Generation</span> | <span style="color: #1A1A1A; font-weight: 500;">Create text, images, code, designs</span> | <span style="color: #2C2C2C;">Copywriting assistant, code generator</span> |
| <span style="color: #00FFB3; font-weight: bold; font-size: 1.1em;">Customer Service</span> | <span style="color: #1A1A1A; font-weight: 500;">Support, troubleshooting, inquiries</span> | <span style="color: #2C2C2C;">Helpdesk chatbot, ticket router</span> |
| <span style="color: #FF6B9D; font-weight: bold; font-size: 1.1em;">Decision Support</span> | <span style="color: #1A1A1A; font-weight: 500;">Recommendations, analysis, insights</span> | <span style="color: #2C2C2C;">Credit risk analyzer, hiring screener</span> |
| <span style="color: #B794F6; font-weight: bold; font-size: 1.1em;">Automation</span> | <span style="color: #1A1A1A; font-weight: 500;">Execute repetitive tasks</span> | <span style="color: #2C2C2C;">Invoice processor, email sorter</span> |
| <span style="color: #FFB3D9; font-weight: bold; font-size: 1.1em;">Monitoring</span> | <span style="color: #1A1A1A; font-weight: 500;">Surveillance, anomaly detection</span> | <span style="color: #2C2C2C;">Security monitor, fraud detector</span> |
| <span style="color: #FFE66D; font-weight: bold; font-size: 1.1em;">Planning</span> | <span style="color: #1A1A1A; font-weight: 500;">Scheduling, resource allocation</span> | <span style="color: #2C2C2C;">Meeting scheduler, logistics optimizer</span> |
| <span style="color: #4ECDC4; font-weight: bold; font-size: 1.1em;">Coordination</span> | <span style="color: #1A1A1A; font-weight: 500;">Orchestrate workflows, manage tasks</span> | <span style="color: #2C2C2C;">Project manager bot, workflow engine</span> |

</div>

</div>

{{2}}
<div class="spectrum-box">

**Function Spectrum: Specialist ← → Generalist**

```ascii
SPECIALIST                HYBRID                GENERALIST
    ↓                       ↓                       ↓
┌──────────┐          ┌───────────┐            ┌──────────┐
│ Tax      │          │ Financial │            │ Personal │
│ Filing   │          │ Assistant │            │   AI     │
│ Agent    │          │ (Budget+  │            │Assistant │
│          │          │  Tax+     │            │ (Open-   │
│ One task │          │  Invest)  │            │  ended)  │
└──────────┘          └───────────┘            └──────────┘

High Precision          Balanced              High Flexibility
Low Flexibility       Moderate Precision     Variable Precision
```

**Trade-offs:**
- **Specialists:** More accurate, less flexible, easier to govern
- **Generalists:** More versatile, potentially less reliable, harder to govern

</div>

---

### 2️⃣ Role: How Does It Interact?

<div class="dimension-card">

**DIMENSION 2: ROLE**

**Definition:** The breadth of tasks an agent can perform, ranging from highly specialized to generalist capabilities.

**Key Question:** How does the agent interact with users, systems, and other agents?

</div>

{{1}}
<div class="classification-box">
__**Four Primary Roles**__
</div>

{{1}}
<div class="classification-box">

**1. SPECIALIST**
- Narrowly focused on specific domains
- Optimized for particular task types
- High accuracy within scope
- Limited adaptability outside domain

**Examples:**
- Tax filing agent (only prepares tax returns)
- Medical image classifier (only analyzes X-rays)
- Grammar checker (only corrects text)

</div>

{{2}}
<div class="classification-box">

**2. GENERALIST**
- Adapts across multiple domains
- Broader task range
- More flexible but potentially less accurate
- Handles diverse challenges

**Examples:**
- Personal AI assistant (scheduling, email, research, planning)
- Digital personal assistant (manages multiple aspects of life/work)
- General-purpose coding assistant

</div>

{{3}}
<div class="classification-box">

**3. COLLABORATIVE PARTNER**
- Works alongside humans
- Augments human capabilities
- Requires human input/oversight
- Handles subtasks while human manages overall process

**Examples:**
- Design co-pilot (suggests ideas, human makes final decisions)
- Research assistant (finds sources, human synthesizes)
- Code completion tool (suggests lines, developer reviews/accepts)

</div>

{{4}}
<div class="classification-box">

**4. AUTONOMOUS OPERATOR**
- Functions independently
- Minimal human intervention
- Self-directed task execution
- Reports results but doesn't require approval

**Examples:**
- Warehouse inventory robot
- Automated trading system
- Spam filter (silently processes emails)

</div>

{{5}}
<div class="classification-box">
**Role Comparison Matrix**

| Dimension | Specialist | Generalist | Collaborative | Autonomous |
|-----------|------------|------------|---------------|------------|
| **Task Breadth** | Very Narrow | Broad | Varies | Task-Specific |
| **Human Interaction** | Minimal | Frequent | Constant | Minimal |
| **Adaptability** | Low | High | Medium | Low |
| **Error Impact** | Contained | Variable | Shared | Full Responsibility |
| **Governance Need** | Focused | Comprehensive | Shared | High Oversight |

</div>

---

### 3️⃣ Predictability: Output Consistency?

<div class="dimension-card">

**DIMENSION 3: PREDICTABILITY**

**Definition:** The stability and repeatability of agent behavior—how consistent outputs are given the same inputs.

**Key Question:** How much can we trust the agent to produce consistent, reproducible results?

</div>

{{1}}
<div class="spectrum-box">
__**Predictability Spectrum**__
</div>

{{1}}
<div class="spectrum-box">

```ascii
  DETERMINISTIC             PROBABILISTIC            NON-DETERMINISTIC
    100%                      Variable                       0%
  ┌──────────┐              ┌──────────┐               ┌──────────┐
  │ Rule-    │              │ ML Model │               │ Creative │
  │ Based    │              │ (Temp=0) │               │ LLM      │
  │ System   │              │          │               │(Temp=1.0)│
  └──────────┘              └──────────┘               └──────────┘

         Same input  →  Same input   →    Same input  →
        Same output    Similar output    Variable output
        Every time     Most of the time  Each time different
```
</div>

{{2}}
<div class="spectrum-box">
**Examples by Predictability Level:**

| Level | Agent Type | Behavior |
|-------|------------|----------|
| **High (Deterministic)** | SQL query executor | Query "SELECT * FROM users WHERE id=5" always returns same result |
| **Medium-High** | Sentiment analyzer | "This is great!" consistently classified as positive |
| **Medium** | Recommendation engine | Suggests similar but not identical items each time |
| **Medium-Low** | Conversational chatbot | Varies phrasing while maintaining intent |
| **Low (Creative)** | Story generator | Each generation uniquely different |

</div>

{{3}}
<div class="spectrum-box">
**Why Predictability Matters**
</div>

{{3}}
<div class="key-insight">

**Governance Implications:**

**High Predictability = Lower Oversight**
- Easier to validate behavior
- Simpler testing procedures
- Predictable failure modes
- Clearer accountability

**Low Predictability = Higher Oversight**
- Requires extensive testing
- Need for ongoing monitoring
- Unpredictable edge cases
- Shared human-AI accountability

</div>

---

### 4️⃣ Autonomy: Independence Level?

<div class="dimension-card">

**DIMENSION 4: AUTONOMY**

**Definition:** The degree to which an agent can define and pursue objectives with minimal human guidance.

**Key Question:** How independently does the agent operate after deployment?

</div>

{{1}}
<div class="dimension-card">

**Autonomy Levels Framework**

Based on automotive industry standards (SAE International), adapted for AI agents:

```ascii
┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃              AUTONOMY SPECTRUM                        ┃
┗━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┛

LEVEL 0: NO AUTONOMY
├─ Human does everything
├─ Agent provides information only
└─ Example: Static calculator, lookup table

LEVEL 1: ASSISTANCE
├─ Agent makes suggestions
├─ Human approves/rejects all actions
└─ Example: Autocomplete, spell-check suggestions

LEVEL 2: PARTIAL AUTONOMY
├─ Agent executes simple tasks independently
├─ Human oversight for complex decisions
└─ Example: Email sorting (auto-files routine emails)

LEVEL 3: CONDITIONAL AUTONOMY
├─ Agent handles most tasks independently
├─ Requests human input in ambiguous cases
└─ Example: Customer service bot (escalates complex issues)

LEVEL 4: HIGH AUTONOMY
├─ Agent operates fully independently within domain
├─ Human monitors but rarely intervenes
└─ Example: Fraud detection (auto-blocks transactions)

LEVEL 5: FULL AUTONOMY
├─ Agent operates without human oversight
├─ Self-monitoring and self-correcting
└─ Example: Theoretical AGI (doesn't exist yet)
```
</div>

{{2}}
<div class="dimension-card">
**Autonomy vs. Authority**
</div>

{{2}}
<div class="warning-box">

**⚠️ Critical Distinction:**

**Autonomy** = CAN it act independently?  
**Authority** = SHOULD it act independently?

**Example Scenarios:**

| Autonomy | Authority | Interpretation |
|----------|-----------|----------------|
| High | Low | Can do complex reasoning but must ask permission |
| Low | High | Simple rule-based system with high-stakes decision power |
| High | High | ⚠️ HIGH RISK - Independent AND impactful decisions |
| Low | Low | ✅ LOW RISK - Limited capability and limited power |

</div>

---

### 5️⃣ Authority: Decision-Making Scope?

<div class="dimension-card">

**DIMENSION 5: AUTHORITY**

**Definition:** The actions an agent is permitted to take, from read-only access to full administrative control.

**Key Question:** What decisions can the agent make, and what is the potential impact?

</div>

{{1}}
<div class="key-insight">

**Authority Spectrum**

```ascii
┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃             AUTHORITY LEVELS & IMPACT                   ┃
┗━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┛

TIER 0: NO AUTHORITY (Read-Only)
├─ Can only read/observe data
├─ No ability to modify state
├─ Zero direct impact
└─ Examples: Analytics dashboard, report generator

TIER 1: ADVISORY (Recommendations Only)
├─ Suggests actions but cannot execute
├─ Human reviews and decides
├─ Indirect impact through influence
└─ Examples: Hiring screener, investment advisor bot

TIER 2: LOW-STAKES EXECUTION
├─ Executes minor tasks with limited impact
├─ Typically reversible actions
├─ Low financial/safety risk
└─ Examples: Email drafting, calendar scheduling

TIER 3: MODERATE-STAKES EXECUTION
├─ Meaningful business impact
├─ Some irreversibility
├─ Medium financial risk ($100s-$1000s)
└─ Examples: Customer refunds up to $500, order fulfillment

TIER 4: HIGH-STAKES EXECUTION
├─ Significant business impact
├─ Often irreversible
├─ High financial risk ($10,000s+)
└─ Examples: Procurement approvals, loan decisions

TIER 5: CRITICAL EXECUTION
├─ Business-critical or safety-critical
├─ Irreversible with severe consequences
├─ Very high financial/legal/safety risk
└─ Examples: Emergency medical decisions, power grid control
```
</div>


{{2}}
<div style="background: rgba(173, 216, 230, 0.15); border: 1px solid rgba(135, 206, 250, 0.3); border-radius: 8px; padding: 20px; margin: 20px 0;">

**Authority Dimensions Matrix**

<div style="overflow-x: auto;">

| Dimension | Low Authority | Medium Authority | High Authority |
|-----------|---------------|------------------|----------------|
| <span style="color: #2E86DE; font-weight: bold;">Data Access</span> | <span style="color: #1A1A1A;">Public data</span> | <span style="color: #1A1A1A;">Internal data</span> | <span style="color: #1A1A1A;">Sensitive/PII</span> |
| <span style="color: #2E86DE; font-weight: bold;">System Access</span> | <span style="color: #1A1A1A;">Read-only</span> | <span style="color: #1A1A1A;">Write specific tables</span> | <span style="color: #1A1A1A;">Admin privileges</span> |
| <span style="color: #2E86DE; font-weight: bold;">User Impact</span> | <span style="color: #1A1A1A;">Self only</span> | <span style="color: #1A1A1A;">Team</span> | <span style="color: #1A1A1A;">Organization/Public</span> |
| <span style="color: #2E86DE; font-weight: bold;">Reversibility</span> | <span style="color: #1A1A1A;">Fully reversible</span> | <span style="color: #1A1A1A;">Partially reversible</span> | <span style="color: #1A1A1A;">Irreversible</span> |
| <span style="color: #2E86DE; font-weight: bold;">Time Sensitivity</span> | <span style="color: #1A1A1A;">No urgency</span> | <span style="color: #1A1A1A;">Moderate</span> | <span style="color: #1A1A1A;">Real-time critical</span> |

</div>

</div>

---

### 6️⃣ Use Case: Application Domain?

<div class="dimension-card">

**DIMENSION 6: USE CASE**

**Definition:** The domain and environment where the agent performs its distinct function for stakeholders.

**Key Question:** In which industry, domain, or application area does the agent operate?

</div>


{{1}}
<div class="key-insight">
**Major Use Case Categories**

| Domain | Characteristics | Risk Profile | Examples |
|--------|----------------|--------------|----------|
| **Customer Service** | High volume, routine queries | Low-Medium | Support chatbots, FAQ bots |
| **Healthcare** | High stakes, regulated | High | Diagnosis assistants, drug interaction checkers |
| **Finance** | Regulated, fraud risk | High | Trading bots, credit scoring |
| **Legal** | High accuracy required | High | Contract analysis, case research |
| **Manufacturing** | Physical safety concerns | Medium-High | Quality control, predictive maintenance |
| **Marketing** | Creative, subjective | Low-Medium | Content generation, ad targeting |
| **HR** | Bias concerns, regulated | Medium-High | Resume screening, interview scheduling |
| **Education** | Long-term impact | Medium | Tutoring systems, grading assistants |
| **Research** | Accuracy critical | Medium | Literature review, data analysis |
| **IT Operations** | System availability | Medium | Log analysis, incident response |

</div>

{{2}}
<div class="warning-box"> 
**Use Case Risk Assessment**
</div>

{{2}}
<div class="classification-box">

**Four Risk Factors by Domain:**

1. **Regulatory Intensity**
   - Heavy: Healthcare, Finance, Legal
   - Medium: HR, Education
   - Light: Marketing, General productivity

2. **Error Consequences**
   - Severe: Medical diagnosis, financial trading
   - Moderate: Legal research, hiring
   - Minor: Email drafting, content recommendations

3. **Bias Potential**
   - High: Hiring, lending, criminal justice
   - Medium: Education, marketing
   - Low: Data processing, scheduling

4. **Explainability Requirements**
   - Critical: Legal, Healthcare, Credit decisions
   - Important: HR, Education
   - Optional: Content generation, routine automation

</div>

---

### 7️⃣ Environment: Operating Context?

<div class="classification-box">

**DIMENSION 7: ENVIRONMENT**

**Definition:** The operating conditions the agent functions under, ranging from simple/predictable to complex/uncertain contexts.

**Key Question:** Where and under what conditions does the agent operate?

</div>

{{1}}
<div style="background: rgba(173, 216, 230, 0.15); border: 1px solid rgba(135, 206, 250, 0.3); border-radius: 8px; padding: 20px; margin: 20px 0;">

__**Three Environmental Categories**__

</div>

{{2}}
<div style="background: rgba(173, 216, 230, 0.15); border: 1px solid rgba(135, 206, 250, 0.3); border-radius: 8px; padding: 20px; margin: 20px 0;">

**1. PHYSICAL ENVIRONMENT**

**Characteristics:**
- Real-world interaction with objects/people
- Safety-critical considerations
- Sensor-based perception
- Irreversible physical actions

**Examples:**
- Autonomous vehicles (high complexity)
- Warehouse robots (medium complexity)
- Robotic vacuum cleaners (low complexity)

</div>

{{3}}
<div style="background: rgba(173, 216, 230, 0.15); border: 1px solid rgba(135, 206, 250, 0.3); border-radius: 8px; padding: 20px; margin: 20px 0;">

**2. DIGITAL ENVIRONMENT**

**Characteristics:**
- Software-only interaction
- API and data-based operations
- Reversible actions (usually)
- Lower physical safety risk

**Examples:**
- Chatbots (low complexity)
- Trading algorithms (high complexity)
- Email assistants (low complexity)

</div>

{{4}}
<div style="background: rgba(173, 216, 230, 0.15); border: 1px solid rgba(135, 206, 250, 0.3); border-radius: 8px; padding: 20px; margin: 20px 0;">

**3. HYBRID ENVIRONMENT**

**Characteristics:**
- Combines physical and digital
- Cyber-physical systems
- Complex failure modes
- Multi-modal sensing and action

**Examples:**
- Smart home systems
- Connected medical devices
- Industrial IoT controllers

</div>

---

## 👥 Group Exercise: Classification Practice

### Classify an AI Agent Across All 7 Dimensions

<div class="task-box">

**Scenario:** Your organization is considering deploying an **AI-Powered Resume Screening Agent**

**Agent Description:**
- Reviews job applications automatically
- Scores candidates based on qualifications (skills, experience, education)
- Recommends top 10 candidates to hiring manager for interview
- Uses machine learning trained on past successful hires
- Operates through HR information system
- Processes 100+ applications per job posting
- Does NOT make final hiring decisions

**Your Task (10 minutes):**

**Step 1:** Form groups of 3-4 people

**Step 2:** Classify this agent across all 7 dimensions using the framework:

| Dimension | Your Classification | Justification |
|-----------|---------------------|---------------|
| **1. Function** | What does it do? | |
| **2. Role** | Specialist/Generalist/Collaborative/Autonomous? | |
| **3. Predictability** | High/Medium/Low? | |
| **4. Autonomy** | Level 0-5? | |
| **5. Authority** | Tier 0-5? | |
| **6. Use Case** | Which domain? | |
| **7. Environment** | Physical/Digital/Hybrid? | |

**Step 3:** Discuss within your group:
- Which dimensional combinations might create risks?
- Is this a low, medium, or high-risk agent overall?
- What makes this agent different from a fully autonomous hiring system?

**Step 4:** Be ready to share your classification with the class

</div>

#### Discussion Prompts for Groups

<details>
<summary>💡 Click for guiding questions</summary>

**Function & Role:**
- Is this purely screening, ranking, or decision-making?
- Does it make final decisions or just recommendations?
- How specialized is it (only hiring vs. broader HR tasks)?

**Predictability:**
- Will it rank candidates consistently?
- Could ML introduce variability?
- Is the scoring transparent and reproducible?

**Autonomy & Authority:**
- Can it reject candidates automatically or just recommend?
- Does a human review every decision?
- What level of independence does it have?

**Use Case & Environment:**
- What industry/domain does this fall under?
- What are the regulatory considerations (e.g., anti-discrimination laws)?
- Is it purely digital or does it interface with physical processes?

**Risk Thinking:**
- What if the model is biased against certain demographics?
- What are the legal implications?
- How would errors impact candidates and the company?
- Which dimensional combinations raise red flags?

</details>

<span style="font-size: 1.4em; font-weight: bold;">Sample Classification</span>

<details>
<summary>✅ Click to see example classification</summary>

<div class="solution-box">

| Dimension | Classification | Justification |
|-----------|----------------|---------------|
| **1. Function** | Specialist - Decision Support | Focused specifically on candidate screening and ranking |
| **2. Role** | Advisory/Collaborative | Recommends candidates; hiring manager makes final decision |
| **3. Predictability** | Medium | ML-based scoring may vary slightly; not fully deterministic |
| **4. Autonomy** | Level 2 (Partial) | Executes screening independently but escalates to human for final decision |
| **5. Authority** | Tier 1 (Advisory) | Only makes recommendations; cannot reject or hire candidates |
| **6. Use Case** | HR/Recruitment | Human resources domain with regulatory considerations |
| **7. Environment** | Digital | Operates through HR software system |

**Overall Risk Profile:** **MEDIUM-HIGH**

**Why?**
- Medium-High risk despite advisory role due to:
  - High bias potential (protected characteristics)
  - Regulatory intensity (employment discrimination laws)
  - Significant impact on people's livelihoods
  - Medium predictability (ML variability)

**Key Risk Factors:**
- Discriminatory screening against protected classes
- Lack of transparency in scoring decisions
- Training data bias from historical hiring patterns
- Legal compliance (EEOC, GDPR Article 22)

**Required Governance:**
- Bias testing and fairness audits
- Explainability of scoring criteria
- Human review of all recommendations
- Regular model retraining and validation
- Legal compliance review

</div>

</details>

---

## Part 2: Risk Assessment & Governance

### Risk Assessment Framework 🔍

<div class="governance-card">

**Risk assessment is the foundation of proportionate governance.**

Effective agent evaluation rests on three principles:

1. **Contextualization** - Reflect the specific environment
2. **Multidimensional Assessment** - Consider all factors holistically  
3. **Temporal Monitoring** - Track performance over time

</div>

#### Multidimensional Risk Assessment

<div class="warning-box">

**Dangerous Dimensional Combinations:**

🚨 **Profile 1: The Unpredictable Authority**  
High Autonomy + Low Predictability + High Authority  
Example: AI trading system with full market access  
Risk: Unexpected high-impact decisions

⚠️ **Profile 2: The Physical Wildcard**  
Physical Environment + Medium Predictability  
Example: Delivery drone in urban area  
Risk: Safety incidents from environmental complexity

⚠️ **Profile 3: The Specialist with Power**  
Specialist Function + High Authority + Critical Domain  
Example: Medical diagnosis system with auto-prescribe  
Risk: Errors in specialized high-stakes context

</div>

#### 📊 Risk Scoring Matrix


<div style="display: flex; align-items: center; justify-content: center; gap: 15px;">

  <div style="writing-mode: vertical-rl; text-orientation: mixed; font-weight: bold; font-size: 1.5em; color: #7C3AED; border-right: 3px solid #E5E7EB; padding-left: 10px; height: 400px; text-align: center;">
    CATASTROPHIC ⬅️

  </div>

  <div style="flex: 1; max-width: 1000px;">
    
    <div style="text-align: center; font-weight: bold; font-size: 1.1em; color: #1E40AF; margin-bottom: 10px; letter-spacing: 2px; margin-left: 16.66%;">
      LIKELIHOOD ➡️
    </div>

    <table style="width: 100%; margin: 0 auto; border-collapse: collapse; text-align: center; font-size: 0.9em; table-layout: fixed;">
      <thead>
        <tr>
          <th style="background: #1E40AF; color: #FFFFFF; padding: 12px 8px; border: 2px solid #3B82F6; font-weight: bold; width: 16.66%; vertical-align: middle;">IMPACT</th>
          <th style="background: #1E40AF; color: #FFFFFF; padding: 12px 8px; border: 2px solid #3B82F6; font-weight: bold; width: 16.66%; vertical-align: middle;">RARE</th>
          <th style="background: #1E40AF; color: #FFFFFF; padding: 12px 8px; border: 2px solid #3B82F6; font-weight: bold; width: 16.66%; vertical-align: middle;">LOW</th>
          <th style="background: #1E40AF; color: #FFFFFF; padding: 12px 8px; border: 2px solid #3B82F6; font-weight: bold; width: 16.66%; vertical-align: middle;">MEDIUM</th>
          <th style="background: #1E40AF; color: #FFFFFF; padding: 12px 8px; border: 2px solid #3B82F6; font-weight: bold; width: 16.66%; vertical-align: middle;">HIGH</th>
          <th style="background: #1E40AF; color: #FFFFFF; padding: 12px 8px; border: 2px solid #3B82F6; font-weight: bold; width: 16.66%; vertical-align: middle;">V.HIGH</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td style="background: #7C3AED; color: #FFFFFF; padding: 12px 8px; border: 2px solid #A78BFA; font-weight: bold;">CATASTROPHIC</td>
          <td style="background: #FCD34D; color: #000000; padding: 12px 8px; border: 2px solid #F59E0B; font-weight: bold;">MEDIUM</td>
          <td style="background: #FB923C; color: #000000; padding: 12px 8px; border: 2px solid #F97316; font-weight: bold;">HIGH</td>
          <td style="background: #EF4444; color: #FFFFFF; padding: 12px 8px; border: 2px solid #DC2626; font-weight: bold;">V.HIGH</td>
          <td style="background: #991B1B; color: #FFFFFF; padding: 12px 8px; border: 2px solid #7F1D1D; font-weight: bold;">CRITICAL</td>
          <td style="background: #7F1D1D; color: #FFFFFF; padding: 12px 8px; border: 2px solid #450A0A; font-weight: bold;">CRITICAL</td>
        </tr>
        <tr>
          <td style="background: #7C3AED; color: #FFFFFF; padding: 12px 8px; border: 2px solid #A78BFA; font-weight: bold;">SEVERE</td>
          <td style="background: #86EFAC; color: #000000; padding: 12px 8px; border: 2px solid #4ADE80; font-weight: bold;">LOW</td>
          <td style="background: #FCD34D; color: #000000; padding: 12px 8px; border: 2px solid #F59E0B; font-weight: bold;">MEDIUM</td>
          <td style="background: #FB923C; color: #000000; padding: 12px 8px; border: 2px solid #F97316; font-weight: bold;">HIGH</td>
          <td style="background: #EF4444; color: #FFFFFF; padding: 12px 8px; border: 2px solid #DC2626; font-weight: bold;">V.HIGH</td>
          <td style="background: #991B1B; color: #FFFFFF; padding: 12px 8px; border: 2px solid #7F1D1D; font-weight: bold;">CRITICAL</td>
        </tr>
        <tr>
          <td style="background: #7C3AED; color: #FFFFFF; padding: 12px 8px; border: 2px solid #A78BFA; font-weight: bold;">MODERATE</td>
          <td style="background: #86EFAC; color: #000000; padding: 12px 8px; border: 2px solid #4ADE80; font-weight: bold;">LOW</td>
          <td style="background: #86EFAC; color: #000000; padding: 12px 8px; border: 2px solid #4ADE80; font-weight: bold;">LOW</td>
          <td style="background: #FCD34D; color: #000000; padding: 12px 8px; border: 2px solid #F59E0B; font-weight: bold;">MEDIUM</td>
          <td style="background: #FB923C; color: #000000; padding: 12px 8px; border: 2px solid #F97316; font-weight: bold;">HIGH</td>
          <td style="background: #EF4444; color: #FFFFFF; padding: 12px 8px; border: 2px solid #DC2626; font-weight: bold;">V.HIGH</td>
        </tr>
        <tr>
          <td style="background: #7C3AED; color: #FFFFFF; padding: 12px 8px; border: 2px solid #A78BFA; font-weight: bold;">MINOR</td>
          <td style="background: #D1FAE5; color: #000000; padding: 12px 8px; border: 2px solid #86EFAC; font-weight: bold;">V.LOW</td>
          <td style="background: #86EFAC; color: #000000; padding: 12px 8px; border: 2px solid #4ADE80; font-weight: bold;">LOW</td>
          <td style="background: #86EFAC; color: #000000; padding: 12px 8px; border: 2px solid #4ADE80; font-weight: bold;">LOW</td>
          <td style="background: #FCD34D; color: #000000; padding: 12px 8px; border: 2px solid #F59E0B; font-weight: bold;">MEDIUM</td>
          <td style="background: #FB923C; color: #000000; padding: 12px 8px; border: 2px solid #F97316; font-weight: bold;">HIGH</td>
        </tr>
        <tr>
          <td style="background: #7C3AED; color: #FFFFFF; padding: 12px 8px; border: 2px solid #A78BFA; font-weight: bold;">NEGLIGIBLE</td>
          <td style="background: #D1FAE5; color: #000000; padding: 12px 8px; border: 2px solid #86EFAC; font-weight: bold;">V.LOW</td>
          <td style="background: #D1FAE5; color: #000000; padding: 12px 8px; border: 2px solid #86EFAC; font-weight: bold;">V.LOW</td>
          <td style="background: #86EFAC; color: #000000; padding: 12px 8px; border: 2px solid #4ADE80; font-weight: bold;">LOW</td>
          <td style="background: #86EFAC; color: #000000; padding: 12px 8px; border: 2px solid #4ADE80; font-weight: bold;">LOW</td>
          <td style="background: #FCD34D; color: #000000; padding: 12px 8px; border: 2px solid #F59E0B; font-weight: bold;">MEDIUM</td>
        </tr>
      </tbody>
    </table>

    <div style="margin-top: 25px; text-align: center;">
      <p style="font-size: 1.05em; margin-bottom: 15px;"><strong>Risk Level Color Legend:</strong></p>
      <div style="display: flex; flex-wrap: wrap; gap: 12px; justify-content: center;">
        <span style="background: #D1FAE5; color: #000000; padding: 8px 15px; border-radius: 5px; font-weight: bold; border: 2px solid #86EFAC;">■ VERY LOW</span>
        <span style="background: #86EFAC; color: #000000; padding: 8px 15px; border-radius: 5px; font-weight: bold; border: 2px solid #4ADE80;">■ LOW</span>
        <span style="background: #FCD34D; color: #000000; padding: 8px 15px; border-radius: 5px; font-weight: bold; border: 2px solid #F59E0B;">■ MEDIUM</span>
        <span style="background: #FB923C; color: #000000; padding: 8px 15px; border-radius: 5px; font-weight: bold; border: 2px solid #F97316;">■ HIGH</span>
        <span style="background: #EF4444; color: #FFFFFF; padding: 8px 15px; border-radius: 5px; font-weight: bold; border: 2px solid #DC2626;">■ VERY HIGH</span>
        <span style="background: #991B1B; color: #FFFFFF; padding: 8px 15px; border-radius: 5px; font-weight: bold; border: 2px solid #7F1D1D;">■ CRITICAL</span>
      </div>
    </div>

  </div>
</div>


**Risk Level Actions:**

| Risk Rating | Action Required | Timeline |
|-------------|----------------|----------|
| **Critical** | Immediate mitigation or suspend deployment | 24-48 hours |
| **Very High** | Urgent action required | 1 week |
| **High** | Priority mitigation | 1 month |
| **Medium** | Standard controls | 1 quarter |
| **Low** | Monitor | As resources permit |

---

### Governance Mechanisms 🛡️

<div class="governance-card">

**Core Principle:** Scale oversight intensity proportionally to agent autonomy, authority, and operational complexity.

**Higher Risk = Stronger Governance**

</div>

#### Key Governance Practices

**1️⃣ Access Control 🔐**

<div class="classification-box">

**Purpose:** Prevent agents from accessing unnecessary data, systems, or tools

**Key Actions:**
- Enforce least-privilege access
- Define clear task boundaries
- Implement role-based access control (RBAC)
- Regular access audits

**Example:**
- Customer service bot: Read-only access to customer data, write access only to ticket system
- Trading bot: API access limited to specific trading pairs, capped transaction sizes

</div>

**2️⃣ Testing & Validation 🧪**

<div class="classification-box">

**Purpose:** Validate expected behavior, detect errors, prevent untested code from affecting live systems

**Testing Types:**
- Sandbox testing (all agents)
- Pilot testing (medium+ risk)
- A/B testing (significant changes)
- Regression testing (every update)
- Adversarial testing (high-risk agents)

</div>

**3️⃣ Monitoring & Logging 📈**

<div class="classification-box">

**Purpose:** Maintain traceability, enable early detection, support incident response

**Essential Logs:**
- Action log (every decision/action)
- Input log (user queries, system events)
- Output log (agent responses)
- Error log (exceptions, failures)
- Performance log (latency, resource usage)

**Monitoring Frequency by Risk:**

| Risk Level | Real-Time | Periodic Review | Governance Review |
|------------|-----------|-----------------|-------------------|
| Critical | Every action | Daily | Weekly |
| High | Key metrics | Weekly | Monthly |
| Medium | Sampled | Monthly | Quarterly |
| Low | Basic | Quarterly | Annual |

</div>

**4️⃣ Human Oversight 👁️**

<div class="classification-box">

**Purpose:** Ensure critical decisions have human review

**Oversight Models:**
- **Human-in-the-loop:** Human approves every decision (high-stakes)
- **Human-on-the-loop:** Human monitors and can intervene (medium-stakes)
- **Human-over-the-loop:** Periodic audits and reviews (low-stakes)

</div>

---

## Part 3: Real-World Applications

### Case Studies: Agents in Action 🌍

#### Example 1: Customer Service Chatbot

<div class="example-card">

**Agent Profile:**

| Dimension | Rating | Details |
|-----------|--------|---------|
| Function | Specialist | Customer support only |
| Role | Collaborative | Works with human agents |
| Predictability | Medium-High | Mostly consistent responses |
| Autonomy | Medium | Handles routine, escalates complex |
| Authority | Low-Medium | Can issue refunds up to $100 |
| Use Case | Customer Service | E-commerce support |
| Environment | Digital | Web chat interface |

**Risk Assessment:**
- Overall Risk: **MEDIUM**
- Key Risks: Incorrect refunds, poor customer experience, data privacy

**Governance Applied:**
- ✅ Access Control: Read customer data, limited write to support tickets
- ✅ Testing: Sandbox with test scenarios, pilot with 5% of traffic
- ✅ Monitoring: Track refund rate, customer satisfaction, escalation rate
- ✅ Human Oversight: Human-on-the-loop for refunds >$100

</div>

#### Example 2: Autonomous Warehouse Robot

<div class="example-card">

**Agent Profile:**

| Dimension | Rating | Details |
|-----------|--------|---------|
| Function | Specialist | Package movement |
| Role | Autonomous | Operates independently |
| Predictability | High | Consistent navigation |
| Autonomy | High | Self-directed within warehouse |
| Authority | Medium | Controls own movement |
| Use Case | Manufacturing/Logistics | Warehouse operations |
| Environment | Physical | Structured warehouse |

**Risk Assessment:**
- Overall Risk: **MEDIUM-HIGH**
- Key Risks: Collisions, package damage, system downtime

**Governance Applied:**
- ✅ Access Control: Limited to designated zones
- ✅ Testing: Extensive safety testing, collision avoidance validation
- ✅ Monitoring: Real-time position tracking, obstacle detection logs
- ✅ Human Oversight: Human-on-the-loop via control center, emergency stop

</div>

#### Example 3: Medical Diagnosis Assistant

<div class="example-card">

**Agent Profile:**

| Dimension | Rating | Details |
|-----------|--------|---------|
| Function | Specialist | Medical diagnosis suggestions |
| Role | Advisory | Recommends, doctor decides |
| Predictability | Medium | ML-based, some variability |
| Autonomy | Low | Provides information only |
| Authority | Low | Advisory only, no prescribing |
| Use Case | Healthcare | Clinical decision support |
| Environment | Digital | Hospital information system |

**Risk Assessment:**
- Overall Risk: **HIGH** (healthcare domain)
- Key Risks: Misdiagnosis, bias in recommendations, patient harm

**Governance Applied:**
- ✅ Access Control: Read patient data, no treatment authorization
- ✅ Testing: Clinical validation, bias testing, regulatory approval
- ✅ Monitoring: Track diagnostic accuracy, edge cases, doctor override rate
- ✅ Human Oversight: Human-in-the-loop (doctor makes all final decisions)
- ✅ Compliance: HIPAA, medical device regulations, clinical trials

</div>

---

## 👤 Individual Exercise: Risk Assessment & Governance Design

### Apply Risk Assessment & Governance to an AI Agent

<div class="task-box">

**Scenario:** You're the AI Governance Lead at a retail company. Your team has built a **Dynamic Pricing Agent** that adjusts product prices in real-time.

**Agent Classification (Already Completed):**

| Dimension | Rating |
|-----------|--------|
| Function | Specialist (Price Optimization) |
| Role | Autonomous Operator |
| Predictability | Medium (ML-based) |
| Autonomy | Level 4 (High) |
| Authority | Tier 3-4 (Moderate-High Stakes) |
| Use Case | Retail/E-commerce |
| Environment | Digital |

**Agent Capabilities:**
- Automatically changes prices every 15 minutes based on:
  - Competitor prices
  - Inventory levels
  - Customer demand patterns
  - Time of day
  - Customer browsing history
- Can adjust prices ±30% from base price
- Affects 5,000+ products
- No human approval required for price changes
- Uses machine learning to optimize revenue

**Your Task (5 minutes):**

**Part A: Risk Identification (2 minutes)**

Identify 3 major risks and rate them:

| Risk Description | Likelihood (Rare/Low/Med/High/V.High) | Impact (Negl/Minor/Mod/Severe/Cata) | Overall Rating |
|------------------|---------------------------------------|-------------------------------------|----------------|
| 1. | | | |
| 2. | | | |
| 3. | | | |

**Part B: Governance Design (3 minutes)**

For your highest-rated risk, design 2 governance mechanisms:

**Risk:**

**Mechanism 1:**
- Type (Access Control/Testing/Monitoring/Human Oversight):
- Implementation:
- Expected outcome:

**Mechanism 2:**
- Type:
- Implementation:
- Expected outcome:

**Overall Deployment Decision:** Should this agent be deployed? (Yes/Yes with conditions/No)

</div>

---

### 📋 Individual Exercise - Solution Guide

<details>
<summary>✅ Click to reveal sample solution</summary>

<div class="solution-box">

**Part A: Classification**

| Dimension | Rating | Justification |
|-----------|--------|---------------|
| **Function** | Specialist | Focused solely on price optimization |
| **Role** | Autonomous Operator | Makes decisions without human input |
| **Predictability** | Medium | ML-based with some variability |
| **Autonomy** | Level 4 (High) | Operates fully independently within pricing domain |
| **Authority** | Tier 3-4 (Moderate-High) | Direct revenue impact, ±30% price changes |
| **Use Case** | Retail/E-commerce | Commercial pricing domain |
| **Environment** | Digital | E-commerce platform |

**Overall Risk Profile:** ⚠️ **HIGH RISK**

---

**Part B: Risk Identification**

| Risk Description | Likelihood | Impact | Overall Rating |
|------------------|------------|--------|----------------|
| **1. Pricing Errors** - Agent sets unreasonably high/low prices losing sales or revenue | High | Severe | **CRITICAL** |
| **2. Discriminatory Pricing** - Uses customer data in ways that discriminate against protected groups | Medium | Catastrophic | **CRITICAL** |
| **3. Competitive Race to Bottom** - Price wars with competitors erode margins | Medium | Severe | **HIGH** |
| **4. Customer Trust Loss** - Frequent price changes frustrate customers, damage brand | High | Moderate | **HIGH** |

---

**Part C: Governance Mechanisms**

**1. Access Control & Constraints**
   - **Control type:** Technical constraints
   - **Implementation:**
     - Set hard limits: prices cannot exceed ±20% (narrower than ±30%)
     - Implement price floors to prevent loss-making sales
     - Require human approval for price changes on high-value items (>$500)
     - Rate limiting: maximum 1 price change per hour per product
   - **Risk(s) addressed:** Pricing Errors, Competitive Race to Bottom

**2. Monitoring & Alerting**
   - **Control type:** Continuous monitoring
   - **Implementation:**
     - Real-time dashboard tracking: price changes, revenue impact, margin
     - Automated alerts if:
       - Any product price changes >15% in one adjustment
       - Margin drops below threshold (e.g., <20%)
       - Customer complaints spike
       - Competitor prices diverge significantly
     - Daily report of all price changes to pricing team
   - **Risk(s) addressed:** All risks (early detection)

**3. Bias Testing & Compliance Review**
   - **Control type:** Testing & validation, legal compliance
   - **Implementation:**
     - Monthly bias audit: analyze if pricing varies inappropriately by customer demographics
     - Legal review of pricing algorithm for discrimination risk
     - Fairness testing: same product should show same price to similar customers (remove personalized pricing based on protected characteristics)
     - Document pricing logic for regulatory compliance
   - **Risk(s) addressed:** Discriminatory Pricing

**Additional Recommended Controls:**

4. **Human Oversight (Human-on-the-loop)**
   - Pricing manager reviews daily report
   - Can pause or override agent at any time
   - Weekly review meeting to assess performance

5. **Testing & Validation**
   - Pilot with limited product set (100 products) for 2 weeks
   - A/B testing: compare agent pricing vs. static pricing
   - Simulate edge cases: what if competitor drops prices 50%?

6. **Customer Communication**
   - Transparency: inform customers about dynamic pricing in ToS
   - Provide price history to customers
   - Honor prices shown at checkout time (prevent bait-and-switch)

**Expected Outcome:**
- Residual Risk: **MEDIUM** (with controls)
- Deployment Decision: ✅ **APPROVE with conditions**
  - Start with limited pilot
  - Implement all critical controls
  - Monthly governance review for first 6 months
  - Annual independent audit

</div>

</details>

---

## 🔮 Looking Ahead: Day 2 Preview

<div class="preview-card">

### **Day 2: AI Workflows, Automation & BMAD Framework**

Tomorrow we transition from **understanding** AI agents to **implementing** them responsibly in organizational workflows.

---

#### 📚 What We'll Cover:

**AI Workflows & Automation**

- 🔄 Designing end-to-end AI agent workflows
- ⚙️ Automation strategies and best practices
- 🔗 Integrating agents into existing systems
- 📊 Measuring workflow performance

**BMAD Framework**

- 🎯 **B**usiness Alignment - Connecting agents to proper goals
- 📏 **M**etrics & Measurement - Defining success criteria
- 🎨 **A**rchitecture & Design - Building robust agent systems
- 🚀 **D**eployment & Delivery - Responsible rollout strategies

---


#### 💡 The BMAD Advantage:

**"Use the BMAD workflow to SHOW how AI Agents can be introduced responsibly and clearly."**

**Get ready to transform today's theory into tomorrow's practice.**

</div>

---

## Key Takeaways

<div class="key-insight">

**What We Learned Today:**

1️⃣ **Classification Framework**
- The 7-dimension framework provides a common language for evaluating AI agents
- Dimensions interact—combinations matter more than individual scores
- Classification guides proportionate governance

2️⃣ **Risk Assessment**
- Systematic risk assessment prevents oversights
- Higher-risk dimensional profiles require stronger controls
- Continuous monitoring is essential (agents evolve over time)

3️⃣ **Governance Mechanisms**
- Governance should scale with risk level
- Key controls: Access, Testing, Monitoring, Human Oversight
- Documentation and transparency are critical

4️⃣ **Practical Application**
- Every agent should be classified before deployment
- Risk assessment informs governance design
- Real-world examples show framework in action

</div>

---


## 📚 Additional Resources


**Governance & Classification Frameworks:**

- World Economic Forum (2025) - "AI Agents in Action: Foundations for Evaluation and Governance"
- Global Future Council on AGI (2025) - "Preparing for Artificial General Intelligence: Global Risks and International Coordination"


**Enterprise Implementation & Strategy:**

- Ransbotham (2025) - "The Emerging Agentic Enterprise: How Leaders Must Navigate a New Age of AI"
- QuantumBlack McKinsey (2025) - "The State of AI in 2025: Agents, Innovation and Transformation"


---

## Thank You! 🙏

**Questions? Discussion? Feedback?**

*Let's make AI agents work responsibly for everyone.*

---

**Module 3 Complete** ✅  
**Day 1 Complete** ✅  
**Ready for Day 2** 🚀

