<!--
author:   Mahwish Kanwal
email:    mahwish.kanwal@ovgu.de
version:  3.0.0
language: en
narrator: US English Female
comment:  Module 2: Functional Classification of AI Agents - Master the 7-dimension framework for systematic agent evaluation

@style
.dimension-card {
    background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
    color: white;
    padding: 30px;
    border-radius: 15px;
    margin: 25px 0;
    box-shadow: 0 8px 16px rgba(0,0,0,0.2);
}

.classification-box {
    background: linear-gradient(135deg, #E3F2FD 0%, #BBDEFB 100%);
    border-left: 10px solid #1976D2;
    padding: 30px;
    margin: 25px 0;
    border-radius: 12px;
    font-size: 1.1em;
    line-height: 1.9;
}

.example-card {
    background: #ffffff;
    border: 3px solid #4CAF50;
    padding: 25px;
    margin: 20px 0;
    border-radius: 12px;
    box-shadow: 0 6px 12px rgba(0,0,0,0.15);
}

.spectrum-box {
    background: linear-gradient(90deg, #ffebee 0%, #fff9e6 50%, #e8f5e9 100%);
    border: 3px solid #757575;
    padding: 25px;
    margin: 25px 0;
    border-radius: 12px;
}

.comparison-table {
    background: white;
    box-shadow: 0 4px 8px rgba(0,0,0,0.15);
    border-radius: 8px;
    overflow: hidden;
}

.interactive-exercise {
    background: linear-gradient(135deg, #fff3e0 0%, #ffe0b2 100%);
    border: 4px dashed #FF9800;
    padding: 30px;
    margin: 25px 0;
    border-radius: 15px;
}

.key-insight {
    background: linear-gradient(135deg, #E8F5E9 0%, #C8E6C9 100%);
    border-left: 10px solid #4CAF50;
    padding: 25px;
    margin: 25px 0;
    border-radius: 12px;
    font-weight: bold;
    font-size: 1.15em;
}

.warning-box {
    background: linear-gradient(135deg, #FFEBEE 0%, #FFCDD2 100%);
    border-left: 10px solid #E53935;
    padding: 25px;
    margin: 25px 0;
    border-radius: 12px;
}

table {
    border-collapse: collapse;
    width: 100%;
    margin: 25px 0;
    box-shadow: 0 4px 8px rgba(0,0,0,0.15);
}

th {
    background: linear-gradient(135deg, #2C3E50 0%, #34495E 100%);
    color: white;
    padding: 18px;
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
@end

-->

# Module 2: Functional Classification
> **The 7-Dimension Framework for AI Agent Evaluation**
>
> *Systematic Approach to Understanding, Comparing & Assessing AI Agents*
>
> Duration: 75 minutes | Hands-On Classification Workshop

---

## 🎯 Learning Objectives

By the end of this module, you will be able to:

- [X] Explain all seven classification dimensions and their importance
- [X] Apply the framework to classify real-world AI agents
- [X] Identify risk factors based on dimensional profiles
- [X] Compare agents systematically across dimensions
- [X] Make informed governance decisions using classification data
- [X] Conduct comprehensive agent evaluations
- [X] Recognize interaction effects between dimensions

---

## 📊 Module Roadmap

```ascii
╔═══════════════════════════════════════════════════════════════╗
║     MODULE 2: FUNCTIONAL CLASSIFICATION - 75 MIN             ║
╠═══════════════════════════════════════════════════════════════╣
║                                                               ║
║  Part 1: FRAMEWORK FOUNDATION (20 min)                        ║
║  ├─ 🎯 Why Classification Matters              (5 min)       ║
║  ├─ 📐 The 7-Dimension Framework Overview      (8 min)       ║
║  └─ 🔗 Dimensional Interactions                (7 min)       ║
║                                                               ║
║  Part 2: DETAILED DIMENSIONS (30 min)                         ║
║  ├─ 1️⃣ Function (What does it do?)            (4 min)       ║
║  ├─ 2️⃣ Role (How does it interact?)           (4 min)       ║
║  ├─ 3️⃣ Predictability (Output consistency?)   (5 min)       ║
║  ├─ 4️⃣ Autonomy (Independence level?)         (5 min)       ║
║  ├─ 5️⃣ Authority (Decision-making scope?)     (5 min)       ║
║  ├─ 6️⃣ Use Case (Application domain?)         (4 min)       ║
║  └─ 7️⃣ Environment (Operating context?)       (3 min)       ║
║                                                               ║
║  Part 3: PRACTICAL APPLICATION (25 min)                       ║
║  ├─ 🌍 Real-World Agent Examples               (10 min)      ║
║  ├─ 🎮 Interactive Classification Exercise     (10 min)      ║
║  └─ 📊 Comparative Analysis Workshop           (5 min)       ║
║                                                               ║
╚═══════════════════════════════════════════════════════════════╝
```

---

## Part 1: Framework Foundation

### Why Classification Matters 🎯

<div class="classification-box">

**The Challenge:** Without a systematic framework, organizations struggle to:

❌ Compare different AI agent solutions objectively
❌ Assess risk profiles consistently
❌ Design appropriate governance mechanisms
❌ Communicate requirements clearly to vendors/developers
❌ Make informed build-vs-buy decisions

**The Solution:** A structured classification framework provides:

✅ **Common Language** for discussing agent capabilities
✅ **Risk Assessment Foundation** based on dimensional profiles
✅ **Governance Guidance** scaled to agent characteristics
✅ **Comparison Baseline** across vendors and solutions
✅ **Documentation Standard** for organizational AI inventories

</div>

#### Real-World Impact: Classification in Action

**Scenario:** Your company evaluates three chatbot vendors

**Without Framework:**
```
Vendor A: "Our AI is advanced and autonomous"
Vendor B: "We use cutting-edge machine learning"
Vendor C: "Our bot is smarter and more reliable"

→ Vague claims, no basis for comparison
```

**With 7-Dimension Framework:**
```
Dimension        Vendor A    Vendor B    Vendor C
─────────────────────────────────────────────────
Function         Support     Support     Sales
Role             Autonomous  Collab      Advisory
Predictability   Medium      High        Medium
Autonomy         High        Medium      Low
Authority        Tier 1-3    Tier 1-2    Tier 1
Use Case         Customer    Technical   Lead Gen
Environment      Digital     Hybrid      Digital

→ Clear, objective comparison enables informed decision
```

---

### The 7-Dimension Framework Overview 📐

The World Economic Forum's classification framework consists of seven interconnected dimensions:

```ascii
┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃           7-DIMENSION CLASSIFICATION FRAMEWORK              ┃
┗━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┛

┌──────────────────────────────────────────────────────────────┐
│                  AGENT CHARACTERISTICS                       │
│                  (Internal Properties)                       │
├──────────────────────────────────────────────────────────────┤
│                                                              │
│  1️⃣ FUNCTION                                                │
│     What does the agent do?                                  │
│     ↓                                                        │
│  2️⃣ ROLE                                                    │
│     How does it interact with users/systems?                 │
│     ↓                                                        │
│  3️⃣ PREDICTABILITY                                          │
│     How consistent/stable are outputs?                       │
│     ↓                                                        │
│  4️⃣ AUTONOMY                                                │
│     How independently does it operate?                       │
│     ↓                                                        │
│  5️⃣ AUTHORITY                                               │
│     What decisions can it make?                              │
│                                                              │
└──────────────────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────────────────┐
│                  OPERATIONAL CONTEXT                         │
│                  (External Factors)                          │
├──────────────────────────────────────────────────────────────┤
│                                                              │
│  6️⃣ USE CASE                                                │
│     Which domain/industry/application?                       │
│     ↓                                                        │
│  7️⃣ ENVIRONMENT                                             │
│     Physical, digital, or hybrid context?                    │
│                                                              │
└──────────────────────────────────────────────────────────────┘

        ↓           ↓           ↓           ↓
  
┌──────────────────────────────────────────────────────────────┐
│              EMERGENT PROPERTIES                             │
├──────────────────────────────────────────────────────────────┤
│  • Overall Risk Profile                                      │
│  • Governance Requirements                                   │
│  • Regulatory Considerations                                 │
│  • Stakeholder Impact                                        │
└──────────────────────────────────────────────────────────────┘
```

<div class="key-insight">
💡 **Core Principle:** Classification defines an agent's characteristics and operational context to guide evaluation, risk assessment, and governance decisions. 

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
   - Risk: Unpredictable high-value decisions without oversight
   - Mitigation: Mandatory human approval for transactions > threshold

2. **Physical Environment + Medium Predictability + High Autonomy**
   - Example: Delivery robot in crowded urban area
   - Risk: Unpredictable real-world interactions, safety concerns
   - Mitigation: Geo-fencing, constant telemetry, emergency stop

3. **High Authority + Specialist Function + Critical Use Case**
   - Example: Medical diagnosis agent with treatment authority
   - Risk: Specialized errors in high-stakes domain
   - Mitigation: Human-in-the-loop, extensive validation, liability insurance

</div>

#### Dimensional Synergies

<div class="example-card">

**✅ Positive Combinations**

1. **Low Autonomy + Advisory Role + High Predictability**
   - Example: Grammar checking tool
   - Benefit: Safe, reliable assistance without execution risk
   - Governance: Minimal oversight required

2. **Medium Autonomy + Collaborative Role + Bounded Use Case**
   - Example: Research assistant for literature review
   - Benefit: Productivity gains with human verification
   - Governance: Standard testing and monitoring

3. **High Predictability + Specialist Function + Digital Environment**
   - Example: Form validation agent
   - Benefit: Reliable, efficient, low-risk automation
   - Governance: Basic logging and error tracking

</div>

---

## Part 2: Detailed Dimensions

### 1️⃣ Function: What Does It Do?

<div class="dimension-card">

**DIMENSION 1: FUNCTION**

**Definition:** The specific role, purpose, or set of tasks the agent is designed to perform.

**Key Question:** What does the agent do in practice, independent of the environment it's deployed in?

</div>

#### Function Categories & Examples

| Category | Description | Examples |
|----------|-------------|----------|
| **Data Processing** | Analyze, transform, aggregate information | SQL query agent, ETL pipeline |
| **Content Generation** | Create text, images, code, designs | Copywriting assistant, code generator |
| **Customer Service** | Support, troubleshooting, inquiries | Helpdesk chatbot, ticket router |
| **Decision Support** | Recommendations, analysis, insights | Credit risk analyzer, hiring screener |
| **Automation** | Execute repetitive tasks | Invoice processor, email sorter |
| **Monitoring** | Surveillance, anomaly detection | Security monitor, fraud detector |
| **Planning** | Scheduling, resource allocation | Meeting scheduler, logistics optimizer |
| **Coordination** | Orchestrate workflows, manage tasks | Project manager bot, workflow engine |

<div class="spectrum-box">

**Function Spectrum: Specialist ← → Generalist**

```ascii
SPECIALIST                 HYBRID                  GENERALIST
    ↓                        ↓                         ↓
┌─────────┐           ┌──────────┐             ┌──────────┐
│ Tax      │          │ Financial │            │ Personal │
│ Filing   │          │ Assistant │            │   AI     │
│ Agent    │          │ (Budget+  │            │Assistant │
│         │          │  Tax+     │            │ (Open-   │
│ One task│          │  Invest)  │            │  ended)  │
└─────────┘           └──────────┘             └──────────┘

High Precision            Balanced              High Flexibility
Low Flexibility           Moderate Precision    Variable Precision
```

**Trade-offs:**
- **Specialists:** More accurate, less flexible, easier to govern
- **Generalists:** More versatile, potentially less reliable, harder to govern

</div>

#### Function Documentation Template

```ascii
┌─────────────────────────────────────────────────────────┐
│              AGENT FUNCTION PROFILE                     │
├─────────────────────────────────────────────────────────┤
│ Primary Function: _________________________________     │
│                                                         │
│ Sub-functions:                                          │
│ • ________________________________________________     │
│ • ________________________________________________     │
│ • ________________________________________________     │
│                                                         │
│ Input Types:                                            │
│ □ Natural language    □ Structured data                │
│ □ Images/video        □ Sensor data                    │
│ □ Other: __________________________________________    │
│                                                         │
│ Output Types:                                           │
│ □ Text responses      □ Data transformations           │
│ □ Actions/commands    □ Predictions/scores             │
│ □ Other: __________________________________________    │
│                                                         │
│ Frequency of Use:                                       │
│ □ Continuous   □ Hourly   □ Daily   □ On-demand       │
│                                                         │
│ Specialist or Generalist: __________________________   │
└─────────────────────────────────────────────────────────┘
```

---

### 2️⃣ Role: How Does It Interact?

<div class="dimension-card">

**DIMENSION 2: ROLE**

**Definition:** The breadth of tasks an agent can perform, ranging from highly specialized to generalist capabilities.

**Key Question:** How does the agent interact with users, systems, and other agents?

</div>

#### Four Primary Roles

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

#### Role Comparison Matrix

| Dimension | Specialist | Generalist | Collaborative | Autonomous |
|-----------|------------|------------|---------------|------------|
| **Task Breadth** | Very Narrow | Broad | Varies | Task-Specific |
| **Human Interaction** | Minimal | Frequent | Constant | Minimal |
| **Adaptability** | Low | High | Medium | Low |
| **Error Impact** | Contained | Variable | Shared | Full Responsibility |
| **Governance Need** | Focused | Comprehensive | Shared | High Oversight |

---

### 3️⃣ Predictability: Output Consistency?

<div class="dimension-card">

**DIMENSION 3: PREDICTABILITY**

**Definition:** The stability and repeatability of agent behavior—how consistent outputs are given the same inputs.

**Key Question:** How much can we trust the agent to produce consistent, reproducible results?

</div>

#### Predictability Spectrum

<div class="spectrum-box">

```ascii
DETERMINISTIC                PROBABILISTIC             NON-DETERMINISTIC
    100%                      Variable                       0%
     │                           │                           │
     ↓                           ↓                           ↓
┌──────────┐              ┌──────────┐               ┌──────────┐
│ Rule-    │              │ ML Model │               │ Creative │
│ Based    │              │ (Temp=0) │               │ LLM      │
│ System   │              │          │               │(Temp=1.0)│
└──────────┘              └──────────┘               └──────────┘

Same input  →  Same input   →    Same input  →
Same output    Similar output    Variable output
Every time     Most of the time  Each time different
```

**Examples by Predictability Level:**

| Level | Agent Type | Behavior |
|-------|------------|----------|
| **High (Deterministic)** | SQL query executor | Query "SELECT * FROM users WHERE id=5" always returns same result |
| **Medium-High** | Sentiment analyzer | "This is great!" consistently classified as positive |
| **Medium** | Recommendation engine | Suggests similar but not identical items each time |
| **Medium-Low** | Conversational chatbot | Varies phrasing while maintaining intent |
| **Low (Creative)** | Story generator | Each generation uniquely different |

</div>

#### Why Predictability Matters

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

#### Measuring Predictability

**Quantitative Approaches:**

1. **Consistency Score**
   ```
   Run same input 100 times
   Measure output variance
   Score = (Identical outputs / Total runs) × 100
   ```

2. **Semantic Similarity**
   ```
   For text outputs:
   Calculate embedding distance between outputs
   Low distance = High predictability
   ```

3. **Determinism Test**
   ```
   Set random seed (if possible)
   Compare outputs with/without seed
   Fully deterministic = Seed controls all variation
   ```

---

### 4️⃣ Autonomy: Independence Level?

<div class="dimension-card">

**DIMENSION 4: AUTONOMY**

**Definition:** The degree to which an agent can define and pursue objectives with minimal human guidance.

**Key Question:** How independently does the agent operate after deployment?

</div>

#### Autonomy Levels Framework

Based on automotive industry standards (SAE International), adapted for AI agents:

```ascii
┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃              AUTONOMY SPECTRUM                          ┃
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

#### Autonomy vs. Authority

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

#### Autonomy Assessment Checklist

```ascii
┌──────────────────────────────────────────────────────────┐
│           AUTONOMY ASSESSMENT QUESTIONNAIRE              │
├──────────────────────────────────────────────────────────┤
│                                                          │
│ 1. Can the agent determine its own goals?               │
│    □ Yes (High)  □ Partially (Medium)  □ No (Low)       │
│                                                          │
│ 2. Does it require human approval before acting?        │
│    □ Never (High)  □ Sometimes (Medium)  □ Always (Low) │
│                                                          │
│ 3. Can it handle unexpected situations?                 │
│    □ Yes (High)  □ Some (Medium)  □ No (Low)            │
│                                                          │
│ 4. Does it learn from experience without retraining?    │
│    □ Yes (High)  □ Limited (Medium)  □ No (Low)         │
│                                                          │
│ 5. Can it operate for extended periods unattended?      │
│    □ Yes (High)  □ Partially (Medium)  □ No (Low)       │
│                                                          │
│ 6. Does it self-monitor for errors?                     │
│    □ Yes (High)  □ Basic (Medium)  □ No (Low)           │
│                                                          │
│ SCORING:                                                 │
│ Mostly "High" → Level 4-5 Autonomy                      │
│ Mostly "Medium" → Level 2-3 Autonomy                    │
│ Mostly "Low" → Level 0-1 Autonomy                       │
└──────────────────────────────────────────────────────────┘
```

---

### 5️⃣ Authority: Decision-Making Scope?

<div class="dimension-card">

**DIMENSION 5: AUTHORITY**

**Definition:** The actions an agent is permitted to take, from read-only access to full administrative control.

**Key Question:** What decisions can the agent make, and what is the potential impact?

</div>

#### Authority Spectrum

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

#### Authority Dimensions Matrix

Authority operates across multiple dimensions simultaneously:

| Dimension | Low Authority | Medium Authority | High Authority |
|-----------|---------------|------------------|----------------|
| **Financial** | <$100 | $100-$10K | >$10K |
| **Data Access** | Public data | Internal data | Sensitive/PII |
| **System Access** | Read-only | Write specific tables | Admin privileges |
| **User Impact** | Self only | Team | Organization/Public |
| **Reversibility** | Fully reversible | Partially reversible | Irreversible |
| **Time Sensitivity** | No urgency | Moderate | Real-time critical |

<div class="example-card">

**Example: Customer Service Agent Authority Levels**

**Level 1: Advisory**
- Suggests responses to agent (human sends)
- Recommends refund amount (manager approves)

**Level 2: Low-Stakes**
- Sends pre-approved response templates
- Issues refunds up to $50 automatically

**Level 3: Moderate-Stakes**
- Processes returns up to $500
- Offers account credits
- Escalates to supervisor if >$500

**Level 4: High-Stakes** (Rarely given to AI)
- Approves refunds of any amount
- Modifies account contracts
- Represents company legally

</div>

---

### 6️⃣ Use Case: Application Domain?

<div class="dimension-card">

**DIMENSION 6: USE CASE**

**Definition:** The domain and environment where the agent performs its distinct function for stakeholders.

**Key Question:** In which industry, domain, or application area does the agent operate?

</div>

#### Major Use Case Categories

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

#### Use Case Risk Assessment

<div class="classification-box">

**Four Risk Factors by Domain:**

1. **Regulatory Intensity**
   - Heavy: Healthcare, Finance, Legal
   - Moderate: HR, Education
   - Light: Marketing, General productivity

2. **Error Consequences**
   - Severe: Medical diagnosis, financial trading
   - Moderate: Contract review, hiring decisions
   - Minor: Email drafting, content recommendations

3. **Bias Potential**
   - High: Hiring, lending, criminal justice
   - Medium: Marketing targeting, insurance pricing
   - Low: Data processing, scheduling

4. **Explainability Requirements**
   - Critical: Legal, Healthcare, Credit decisions
   - Important: HR, Education
   - Optional: Content generation, routine automation

</div>

---

### 7️⃣ Environment: Operating Context?

<div class="dimension-card">

**DIMENSION 7: ENVIRONMENT**

**Definition:** The operating conditions the agent functions under, ranging from simple/predictable to complex/uncertain contexts.

**Key Question:** Where and under what conditions does the agent operate?

</div>

#### Three Environmental Categories

<div class="classification-box">

**1. PHYSICAL ENVIRONMENT**

**Characteristics:**
- Real-world interaction with objects/people
- Safety-critical considerations
- Sensor-based perception
- Irreversible physical actions

**Complexity Factors:**
- Obstacle density
- Environmental unpredictability (weather, lighting)
- Human interaction frequency
- Safety margins

**Examples:**
- Autonomous vehicles (high complexity)
- Warehouse robots (medium complexity)
- Robotic vacuum cleaners (low complexity)

</div>

<div class="classification-box">

**2. DIGITAL ENVIRONMENT**

**Characteristics:**
- Software-only interaction
- API and data-based operations
- Reversible actions (usually)
- Lower physical safety risk

**Complexity Factors:**
- Data quality and availability
- System integration complexity
- API reliability
- Data privacy requirements

**Examples:**
- Chatbots (low complexity)
- Trading algorithms (high complexity)
- Email assistants (low complexity)

</div>

<div class="classification-box">

**3. HYBRID ENVIRONMENT**

**Characteristics:**
- Combines physical and digital
- Cyber-physical systems
- Complex failure modes
- Multi-modal sensing and action

**Complexity Factors:**
- Physical-digital synchronization
- Multi-system dependencies
- Mixed failure modes
- Broader attack surface

**Examples:**
- Smart home systems
- Connected medical devices
- Industrial IoT controllers

</div>

#### Environmental Complexity Scoring

```ascii
┌──────────────────────────────────────────────────────────┐
│         ENVIRONMENT COMPLEXITY ASSESSMENT                │
├──────────────────────────────────────────────────────────┤
│                                                          │
│ SIMPLE ENVIRONMENT (1-2 points)                          │
│ □ Controlled setting                                     │
│ □ Predictable conditions                                 │
│ □ Complete information available                         │
│ □ Static or slow-changing                                │
│ □ Few actors or variables                                │
│                                                          │
│ MODERATE ENVIRONMENT (3-4 points)                        │
│ □ Some variability                                       │
│ □ Incomplete information                                 │
│ □ Dynamic but bounded changes                            │
│ □ Multiple interacting systems                           │
│ □ Some uncertainty                                       │
│                                                          │
│ COMPLEX ENVIRONMENT (5-6 points)                         │
│ □ Highly unpredictable                                   │
│ □ Incomplete/noisy information                           │
│ □ Rapidly changing conditions                            │
│ □ Many interacting actors                                │
│ □ High uncertainty                                       │
│ □ Continuous adaptation required                         │
│                                                          │
│ SCORING INTERPRETATION:                                  │
│ • 1-2: Simple → Lower oversight needed                   │
│ • 3-4: Moderate → Standard governance                    │
│ • 5-6: Complex → Enhanced monitoring required            │
└──────────────────────────────────────────────────────────┘
```

---

## Part 3: Practical Application

### Real-World Agent Examples 🌍

Let's apply the 7-dimension framework to diverse AI agents:

#### Example 1: Robot Vacuum Cleaner 🤖

<div class="example-card">

| Dimension | Rating | Explanation |
|-----------|--------|-------------|
| **Function** | Specialist | Floor cleaning only |
| **Role** | Autonomous Operator | Minimal human interaction |
| **Predictability** | High | Consistent cleaning patterns |
| **Autonomy** | Medium | Navigates independently, returns to base |
| **Authority** | Low | Limited to movement and suction |
| **Use Case** | Residential/Commercial Cleaning | Home maintenance domain |
| **Environment** | Physical (Low Complexity) | Indoor, mapped spaces |

**Risk Profile:** ✅ LOW RISK
- Limited authority, predictable behavior, controlled environment

**Governance Needs:** Minimal—basic safety testing, user manual warnings

</div>

---

#### Example 2: Medical Diagnosis Assistant 🏥

<div class="example-card">

| Dimension | Rating | Explanation |
|-----------|--------|-------------|
| **Function** | Specialist | Disease diagnosis from symptoms/images |
| **Role** | Collaborative Partner | Assists physicians, doesn't replace |
| **Predictability** | Medium-High | Consistent for known patterns, variable for edge cases |
| **Autonomy** | Medium | Analyzes independently, recommendations only |
| **Authority** | Advisory | Cannot prescribe or treat |
| **Use Case** | Healthcare (Diagnostic Support) | Clinical decision support |
| **Environment** | Digital (Medical Records) | Structured + unstructured medical data |

**Risk Profile:** ⚠️ MEDIUM-HIGH RISK
- High-stakes domain, potential for diagnostic errors, regulatory oversight

**Governance Needs:**
- Extensive pre-deployment validation
- Ongoing performance monitoring
- Regulatory compliance (FDA, CE Mark)
- Human physician always in loop
- Explicit documentation of AI role to patients

</div>

---

#### Example 3: Automated Trading System 📈

<div class="example-card">

| Dimension | Rating | Explanation |
|-----------|--------|-------------|
| **Function** | Specialist | Buy/sell securities based on market data |
| **Role** | Autonomous Operator | Executes trades without human approval |
| **Predictability** | Low-Medium | Stochastic market conditions |
| **Autonomy** | High | Real-time decision-making |
| **Authority** | High | Financial transactions up to preset limits |
| **Use Case** | Finance (Algorithmic Trading) | Investment management |
| **Environment** | Digital (High Complexity) | Dynamic, multi-factor, global markets |

**Risk Profile:** 🚨 HIGH RISK
- High autonomy + High authority + Unpredictable environment
- Significant financial exposure

**Governance Needs:**
- Stringent testing (backtesting, stress tests)
- Kill switches and circuit breakers
- Position limits and loss caps
- Continuous monitoring
- Regulatory compliance (SEC, FINRA)
- Regular audits
- Catastrophic risk insurance

</div>

---

#### Example 4: Email Drafting Assistant ✉️

<div class="example-card">

| Dimension | Rating | Explanation |
|-----------|--------|-------------|
| **Function** | Specialist | Composes emails from prompts |
| **Role** | Collaborative Partner | Drafts for user review |
| **Predictability** | Medium | Consistent style, variable creativity |
| **Autonomy** | Low | Requires user prompt and approval |
| **Authority** | Advisory | User decides to send |
| **Use Case** | Productivity (Communication) | Business/personal correspondence |
| **Environment** | Digital (Low Complexity) | Email platforms, text editors |

**Risk Profile:** ✅ LOW RISK
- Low autonomy, advisory only, user maintains control

**Governance Needs:** Minimal
- Basic quality testing
- Privacy policy for data handling
- User education on reviewing outputs

</div>

---

### 🎮 Interactive Classification Exercise

<div class="interactive-exercise">

**🎯 HANDS-ON CHALLENGE: Classify Your Own Agent**

**Scenario:** Your organization is deploying an **AI-Powered Contract Review Agent** that:
- Analyzes vendor contracts for legal compliance
- Identifies non-standard clauses
- Flags potential risks
- Suggests redlines (edits)
- Sends findings to legal team for approval

**Your Task:** Classify this agent across all 7 dimensions

</div>

#### Exercise Template

```ascii
┌──────────────────────────────────────────────────────────┐
│        CONTRACT REVIEW AGENT CLASSIFICATION              │
├──────────────────────────────────────────────────────────┤
│                                                          │
│ 1️⃣ FUNCTION:                                            │
│    □ Specialist  □ Generalist  □ Other: _____________   │
│    Specific task: ___________________________________   │
│                                                          │
│ 2️⃣ ROLE:                                                │
│    □ Specialist  □ Generalist                           │
│    □ Collaborative  □ Autonomous                        │
│                                                          │
│ 3️⃣ PREDICTABILITY:                                      │
│    □ High  □ Medium  □ Low                              │
│    Reasoning: _______________________________________   │
│                                                          │
│ 4️⃣ AUTONOMY:                                            │
│    Level: □ 0-1  □ 2-3  □ 4-5                           │
│    Explanation: _____________________________________   │
│                                                          │
│ 5️⃣ AUTHORITY:                                           │
│    Tier: □ 0  □ 1  □ 2  □ 3  □ 4  □ 5                   │
│    What can it do: __________________________________   │
│                                                          │
│ 6️⃣ USE CASE:                                            │
│    Domain: __________________________________________   │
│    Regulatory concerns: _____________________________   │
│                                                          │
│ 7️⃣ ENVIRONMENT:                                         │
│    □ Physical  □ Digital  □ Hybrid                      │
│    Complexity: □ Simple  □ Moderate  □ Complex         │
│                                                          │
├──────────────────────────────────────────────────────────┤
│ OVERALL RISK PROFILE:                                    │
│ □ Low  □ Medium  □ High  □ Critical                     │
│                                                          │
│ KEY GOVERNANCE REQUIREMENTS:                             │
│ 1. _______________________________________________       │
│ 2. _______________________________________________       │
│ 3. _______________________________________________       │
└──────────────────────────────────────────────────────────┘
```

#### Sample Solution

<details>
<summary>💡 Click to see suggested classification</summary>

**Contract Review Agent Classification:**

1️⃣ **FUNCTION:** Specialist
   - Specific task: Legal contract analysis and compliance checking

2️⃣ **ROLE:** Collaborative Partner
   - Assists legal team, doesn't make final decisions

3️⃣ **PREDICTABILITY:** Medium-High
   - Consistent for standard clauses
   - May vary on novel contract types

4️⃣ **AUTONOMY:** Level 2-3 (Conditional Autonomy)
   - Analyzes contracts independently
   - Flags issues for human review
   - Cannot execute contract changes

5️⃣ **AUTHORITY:** Tier 1 (Advisory)
   - Makes recommendations only
   - Legal team approves all actions

6️⃣ **USE CASE:** Legal (Contract Management)
   - High accuracy requirements
   - Regulatory/compliance implications
   - Potential liability concerns

7️⃣ **ENVIRONMENT:** Digital (Moderate Complexity)
   - PDF documents, contract databases
   - Varied contract formats and structures

**RISK PROFILE:** ⚠️ MEDIUM RISK
- Legal domain with accuracy requirements
- Advisory role limits direct risk
- Human-in-loop provides safety net

**GOVERNANCE REQUIREMENTS:**
1. Pre-deployment validation on test contracts
2. Regular accuracy audits vs. human lawyer reviews
3. Clear documentation of AI limitations to users
4. Logging of all recommendations for audit trail
5. Periodic retraining on new legal precedents
6. Error escalation procedures

</details>

---

### 📊 Comparative Analysis Workshop

#### Group Exercise: Compare Three Agents

Compare these three customer-facing agents:

**Agent A: FAQ Chatbot**
- Answers common questions from knowledge base
- No ability to access customer accounts
- Provides information only

**Agent B: Account Management Bot**
- Answers questions + Can update customer profiles
- Can process simple requests (address changes)
- Requires customer authentication

**Agent C: Full-Service Virtual Agent**
- All of Agent B's capabilities
- Can process refunds up to $1000
- Can schedule service appointments
- Has access to full customer history

<div class="interactive-exercise">

**🎯 Task:** Use the comparison matrix to analyze governance needs

| Dimension | Agent A (FAQ) | Agent B (Account) | Agent C (Full-Service) |
|-----------|---------------|-------------------|------------------------|
| Function | Information retrieval | Account updates | Comprehensive service |
| Role | ? | ? | ? |
| Predictability | ? | ? | ? |
| Autonomy | ? | ? | ? |
| Authority | ? | ? | ? |
| Use Case | Customer service | Customer service | Customer service |
| Environment | Digital | Digital | Digital |
| **Risk Profile** | ? | ? | ? |
| **Governance** | ? | ? | ? |

**Discussion Points:**
1. How does risk scale from Agent A → Agent B → Agent C?
2. What governance mechanisms should differ between them?
3. At what point would you require human approval?
4. How would monitoring requirements differ?

</div>

---

## 📚 Module 2 Summary

<div class="key-insight">

### Key Takeaways

✅ **7-Dimension Framework** provides systematic approach to agent classification:
   - Function, Role, Predictability, Autonomy, Authority, Use Case, Environment

✅ **Dimensions interact** to create compound risk profiles—watch for dangerous combinations

✅ **Classification drives governance** decisions—higher risk dimensions require stronger controls

✅ **Use case context matters**—same agent type has different risk profiles in different domains

✅ **Holistic assessment required**—never evaluate a single dimension in isolation

✅ **Documentation is critical**—maintain classification records for all organizational agents

</div>

---

## 🎯 Self-Assessment Quiz

1. **Which dimension describes what the agent is permitted to do?**
   - [ ] Autonomy
   - [X] Authority
   - [ ] Function
   - [ ] Role

2. **An agent that makes recommendations but cannot execute actions has:**
   - [ ] High Authority, Low Autonomy
   - [ ] High Autonomy, High Authority
   - [X] Low/Advisory Authority, Variable Autonomy
   - [ ] No classification needed

3. **Which combination represents the HIGHEST risk?**
   - [ ] Low Autonomy + High Predictability + Advisory Authority
   - [X] High Autonomy + Low Predictability + High Authority
   - [ ] Medium Autonomy + High Predictability + Low Authority
   - [ ] Low Autonomy + Low Predictability + Medium Authority

4. **A robot vacuum cleaner operates in which type of environment?**
   - [X] Physical - Low Complexity
   - [ ] Digital - Low Complexity
   - [ ] Physical - High Complexity
   - [ ] Hybrid - Medium Complexity

5. **True or False: An agent with high autonomy necessarily requires high authority.**
   - [ ] True
   - [X] False (Autonomy = CAN act, Authority = ALLOWED to act)

---

## 🔗 Bridge to Module 3

In the next module, we'll explore:

🛡️ **Evaluation & Governance** - How to assess risk and design proportionate governance mechanisms

**Preview Questions:**
- How do we systematically assess agent risks?
- What governance mechanisms scale with risk?
- How do we monitor agents over time?

---

## 📖 Additional Resources

**Reference Documents:**
- World Economic Forum (2025) - "AI Agents in Action: Classification Framework"
- IEEE Standards for AI System Classification
- ISO/IEC 23053 - Framework for AI System Using ML

**Tools:**
- Agent Classification Template (downloadable)
- Risk Assessment Matrix
- Governance Mapping Worksheet

---

> **🎓 Congratulations on completing Module 2!**
>
> You can now systematically classify AI agents across seven dimensions.
>
> **Continue to Module 3: Evaluation & Governance** →
