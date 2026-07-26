# Chapter 9: Structured Problem Analysis and Diagnostic Frameworks

## Core Idea

Effective problem-solving requires building diagnostic frameworks before collecting data. Structure your analysis to identify root causes efficiently, avoiding the trap of collecting information first and analyzing later.

## Frameworks Introduced

### 1. **Diagnostic Framework (诊断框架)**
A structured approach to identify all possible causes of a problem before collecting data.

**Three Construction Methods:**

**Method A: Represent Physical Structure**
- Draw the system or process as it currently exists
- Identify which components could produce the problem
- Examples: Manufacturing process flow, retail customer journey, IT system architecture
- Use case: "Where in the sales process are customers dropping off?"

**Method B: Trace Causal Relationships**
Three types of causal diagrams:
1. **Financial Structure**: Trace how profit/cost factors cascade (e.g., Revenue = Volume × Price)
2. **Task Structure**: Map management responsibilities from top-level metric down to actionable tasks
3. **Action Structure**: Show what sequence of actions produces undesired result (Root cause tree)

**Method C: Classify Possible Causes**
- Group similar causes by MECE principle (Mutually Exclusive, Collectively Exhaustive)
- Use binary selection trees (yes/no choices at each branch)
- Narrows possibilities systematically

**Creating Diagnostic Framework Process:**
```
1. Define problem (R1 vs R2)
2. Identify framework structure (Physical? Causal? Classification?)
3. Break into components using MECE
4. Design yes/no questions for each branch
5. Collect data only for testable branches
```

### 2. **Logic Tree for Solutions (逻辑树)**
After diagnosis identifies root causes, use logic trees to generate solutions.

**Difference from Diagnostic Framework:**
- Diagnostic Framework: "Why does this problem exist?" (Finding root causes)
- Logic Tree: "What can we do about it?" (Finding solutions)

**Example - Cost Reduction:**
```
Reduce Direct Labor Cost
├─ Reduce hourly rate
│  ├─ Minimize overtime
│  ├─ Use lower-wage employees
│  └─ Reduce base wages
└─ Reduce hours per unit
   ├─ Fewer workers per machine
   ├─ Increase machine speed
   └─ Improve machine efficiency
```

**Example - Growth Opportunities:**
```
Expand European Business
├─ Geographic expansion
├─ Deepen customer relationships
├─ New customer segments
└─ Strategic partnerships
```

### 3. **Sequential Analysis Framework (五问法)**
The standard problem-solving sequence:
1. **Does a problem exist?** (Define it exists)
2. **Where is the problem?** (Locate it specifically)
3. **Why does it exist?** (Find root causes) ← Use Diagnostic Framework
4. **What can we do?** (Generate solutions) ← Use Logic Tree
5. **What should we do?** (Recommend optimal solution)

## Key Concepts

**MECE Principle (相互独立、完全穷尽)**
- Mutually Exclusive: Categories don't overlap
- Collectively Exhaustive: All possibilities covered
- Critical for avoiding gaps and double-counting in analysis

**Causal Structure Analysis**
- Breaks complex problems into understandable components
- Shows "if this changes, then this happens"
- Enables targeted data collection

**Hypothesis-Driven Analysis**
- Form hypotheses FIRST about what causes the problem
- Collect only data that tests these hypotheses
- Dramatically reduces wasted effort (Studies show 60% of data collection is wasted in traditional approaches)

**Data Collection Discipline**
- Don't collect "all possible information"
- Collect ONLY what's needed to test hypotheses
- Saves time and reduces analysis paralysis

## Mental Models

**Model 1: Three Analytical Approaches**

```
┌─────────────────────────────────────────┐
│ Problem: Sales down 15% YoY             │
└─────────────────────────────────────────┘
                    │
        ┌───────────┼───────────┐
        │           │           │
    STRUCTURE    CAUSALITY    CLASSIFICATION
        │           │           │
    Sales Flow   Revenue Formula  Market Segment
    → Where        → Volume/Price  → Profitable/
      drop?        → COGS          Unprofitable
    → Customer  → Opex
      journey   ┌─ If volume
    ┌─ Awareness down → check
    ├─ Consideration sales effort
    ├─ Purchase  ├─ If price
    └─ Loyalty   down → check
                pricing
                ├─ If COGS
                up → check
                supply chain
```

**Model 2: Problem-Solution Flow**

```
Problem Defined (R1→R2)
         ↓
Diagnostic Framework (Why?)
         ↓
Root Causes Identified
         ↓
Logic Tree (What can we do?)
         ↓
Solution Options Generated
         ↓
Evaluation & Selection
         ↓
Pyramid Structure (Why this one?)
```

## Worked Example

**Scenario**: Manufacturing plant inefficient; production down 12% despite stable demand

**Step 1: Structure Analysis (Diagnostic Framework)**
```
Production System
├─ Input (Raw materials)
├─ Processing
│  ├─ Labor efficiency
│  ├─ Machine availability
│  └─ Process flow
├─ Output (Finished goods)
└─ Quality (Defect rate)
```

**Step 2: Causal Analysis**
```
Production Efficiency = Output per Hour
                     = (Units Produced) / (Machine Hours × Labor Hours)

What could reduce this?
├─ Fewer units produced per hour?
│  ├─ Machine downtime?
│  ├─ Labor productivity issues?
│  └─ Process delays?
├─ More hours needed?
│  ├─ Overtime due to rush jobs?
│  ├─ Training of new workers?
│  └─ Quality rework?
```

**Step 3: Generate Yes/No Questions**
1. Has machine downtime increased? (Compare maintenance records to baseline)
2. Is labor productivity declining? (Track units/worker-hour trend)
3. Are there bottlenecks in process flow? (Map workflow vs. cycle time)
4. Has defect rate increased? (Compare scrap/rework to baseline)
5. Is staffing adequate? (Compare headcount to production volume)

**Step 4: Hypothesis-Driven Data Collection**
Rather than collecting all data about the plant, focus on questions above:
- Machine logs last 3 months
- Labor hour tracking last 3 months
- Quality reports last 3 months
- Workflow timeline studies

**Step 5: Findings & Root Cause**
- Hypothesis 1: Machine downtime ✓ CONFIRMED (Maintenance decreased 20%)
- Hypothesis 2: Labor productivity ✗ Data shows stable
- Hypothesis 3: Process bottleneck ✓ CONFIRMED (3-week wait at testing)
- Hypothesis 4: Defect rate ✓ CONFIRMED (Scrap up 40%)
- Hypothesis 5: Staffing ✗ Same headcount, but testing team at capacity

**Root Causes**: Three issues (maintenance, testing capacity, quality)

**Step 6: Solution Logic Tree**
```
Restore Production Levels
├─ Improve Machine Reliability
│  ├─ Increase preventive maintenance
│  ├─ Upgrade critical machines
│  └─ Reduce utilization rate
├─ Expand Testing Capacity
│  ├─ Add testing equipment
│  ├─ Hire/train testing staff
│  └─ Improve testing process
└─ Improve Quality
    ├─ Enhanced process controls
    ├─ Worker training
    └─ Supplier quality program
```

**Step 7: Recommendation (Pyramid)**
```
Thesis: Implement three-part quality and capacity program

Supporting Points:
1. Restore 50% production loss via preventive maintenance program
   - Cost: $200K, payback: 6 months
   
2. Restore 30% via testing capacity expansion
   - Cost: $150K, payback: 9 months
   
3. Restore 20% via quality improvement initiative
   - Cost: $100K, payback: 12 months

Total ROI: 400% in 18 months
```

## Key Takeaways

1. **Build frameworks first, collect data second** — Diagnostic framework guides data collection; avoid the trap of "collect everything then analyze"
2. **Use MECE rigorously** — Every category must be mutually exclusive and fully comprehensive
3. **Form testable hypotheses** — Hypotheses drive data collection; reduces wasted effort by 40%
4. **Match framework to problem type** — Structure problems need structural analysis; causal problems need causal trees; classification problems need categorization
5. **Keep logic trees separate** — Diagnostic frameworks find problems; logic trees find solutions (don't mix them)
6. **Leverage existing structures** — Best frameworks emerge from understanding the system/process where the problem lives
7. **Design yes/no questions** — Questions that force binary answers enable rapid elimination of hypotheses

## Anti-Patterns

- Don't collect "interesting" data that doesn't test your hypotheses
- Don't mix multiple types of trees (diagnostic + solution) without clear labels
- Don't skip the diagnostic framework and jump straight to solutions
- Don't treat logic trees as diagnostic frameworks
- Don't ignore MECE principle; gaps often hide the real problem

## Connects To

- **Ch8 (Problem Definition)**: Diagnostic framework builds from problem definition
- **Ch6-7 (Logical Order)**: Framework structure follows MECE and logical ordering principles
- **Ch10-12 (Presentation)**: Diagnostic findings become the pyramid's evidence layer
- **Ch4 (Preamble)**: Framework helps write clear, specific preambles with data-driven complications
