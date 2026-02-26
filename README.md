
# In-Class Group Assignment  

## Designing a Multivariate A/B Testing Architecture

- **Duration:** 25–30 minutes  
- **Group Size:** 4-5 students  

## Scenario

Your startup is testing **4 checkout page designs**:

- Control (A)
- Design B
- Design C
- Design D

**Goal:** Increase conversion rate.

**Traffic:** 40,000 visitors per week.

You are the analytics team. Your task is to design the **system architecture and experimental flow** for this multivariate test.

You are not required to compute statistics.  
You must design the system.


## Deliverables

**Each group must produce:**

1. A flowchart of the experiment logic (miro, draw.io, mermaid diagram) 
2. A system architecture diagram  
3. A clear statistical decision protocol  

## STEP 1 | Experimental Logic Flowchart

**Draw a flowchart that includes at minimum:**

- User visit
- Random assignment
- Variant delivery (A/B/C/D)
- Exposure logging
- Event tracking (conversion)
- Data storage
- Statistical testing
- Multiple testing correction
- Decision rule
- Deployment or continuation

Your flowchart must clearly show how data moves from user visit to final decision.


## Phase 2 | System Architecture Design 

Design the architecture components required to run this experiment in production.

You must define:

1. **Randomization Layer**
    - Equal allocation or weighted?
    - Where is assignment stored?
    - How do you prevent reassignment?

2. **Data Layer**
   - Exposure table (user_id, variant, timestamp)
   - Conversion table (user_id, converted, timestamp)
   - Experiment metadata table

3. **Analytics Layer**
   - Sample size calculation module
   - Hypothesis testing module
   - Multiple comparison correction module
   - Monitoring dashboard

4. **Decision Engine**
   - What triggers analysis?
   - Who approves deployment?
   - What are stopping conditions?

Draw the architecture diagram clearly.



## Phase 3 | Multiple Testing Logic

**There are 4 variants.**

1. How many pairwise comparisons are there?
2. How will you control Type I error?
   - Bonferroni
   - Holm
   - False Discovery Rate
3. What significance level will you use?

**Explain your reasoning.**


## Phase 4 | Decision Rule 

You observe the following results:

| Variant | Conversion Rate |
|----------|-----------------|
| A        | 10.0%           |
| B        | 11.5%           |
| C        | 10.8%           |
| D        | 12.1%           |

Some comparisons are significant without correction, but not after adjustment.

**Define:**

- When do you declare a winner?
- Do you rerun the test?
- Do you eliminate weak variants?
- Do you move to a second-stage test?

>Write your final deployment policy clearly.



## Evaluation Criteria (10 Points)

| Component | Points |
|------------|--------|
| Clear experiment flowchart | 2 |
| Sound architecture design | 2 |
| Proper logging/data design | 2 |
| Correct multiple testing logic | 2 |
| Clear and rational decision rule | 2 |
