# Chapter 2 Overview: Why Randomize?
*Running Randomized Evaluations: A Practical Guide — Rachel Glennerster & Kudzai Takavarasha*

---

# Purpose of the Chapter

Chapter 2 explains **why randomized evaluations (randomized controlled trials, or RCTs)** are considered one of the most reliable methods for determining causal relationships in program evaluation.

The chapter focuses on:

- The **problem of causal inference**
- Why many common evaluation approaches produce **biased results**
- How **randomization solves the counterfactual problem**
- The **advantages and limitations of experimental evaluation methods**

Randomized evaluations help determine whether a program **actually causes an outcome**, rather than simply being correlated with it.

---

# Structure of the Chapter

The chapter is divided into several modules:

- **Module 2.1 – The Challenge of Measuring Impact**
- **Module 2.2 – Alternative Evaluation Methods and Their Limitations**
- **Module 2.3 – How Randomization Helps Infer Cause**
- **Module 2.4 – Advantages and Limitations of the Experimental Approach**

---

# Module 2.1: The Challenge of Measuring Impact

## The Counterfactual Problem

To measure the impact of a program, we need to know:

> What would have happened **if the program had not been implemented?**

This hypothetical scenario is called the **counterfactual**.

However, we can never observe both realities simultaneously for the same individual:

- Outcome **with the program**
- Outcome **without the program**

Therefore, evaluations must construct a **comparison group** that approximates this counterfactual.

---

## Example: Education Program

Suppose a tutoring program improves student test scores.

If we simply compare:

- students **who participate**
- students **who do not participate**

we may mistakenly attribute differences in scores to the program.

But the groups may already differ in important ways:

- motivation
- family support
- income
- ability

These differences introduce **selection bias**.

---

## Selection Bias

Selection bias occurs when individuals who participate in a program differ systematically from those who do not.

Examples:

- More motivated entrepreneurs enroll in business training
- Wealthier households adopt agricultural technology
- Stronger students enroll in tutoring programs

If such differences exist, we cannot determine whether the **program or preexisting characteristics** caused the observed outcomes.

---

# Module 2.2: Alternative Evaluation Methods and Their Limitations

Many evaluations attempt to estimate impact without randomization.  
The chapter examines common approaches and the assumptions they require.

---

# 1. Qualitative Impact Evaluations

Qualitative approaches rely on:

- interviews
- focus groups
- case studies

These methods assume that:

- beneficiaries or researchers can accurately determine what would have happened without the program.

However:

- perceptions are subjective
- narratives may exaggerate program impact
- the true counterfactual remains unknown.

---

# 2. Before-and-After Comparisons

This method compares outcomes **before and after program implementation**.

Example:

- Income before microcredit = $500
- Income after microcredit = $700

One might conclude the program increased income by $200.

But this assumes:

> All changes over time were caused by the program.

In reality, other factors may explain the improvement:

- economic growth
- seasonal changes
- improved infrastructure
- market price changes

---

# 3. Cross-Section Comparisons

This approach compares:

- people who participate in a program
- people who do not participate.

It assumes there are **no systematic differences between groups** other than the program. 

However, participation is rarely random, leading to **selection bias**.

---

# 4. Multivariate Regression

Regression attempts to control for differences between participants and nonparticipants.

Example variables included:

- age
- income
- education
- household size

However, regression can only control for **observable characteristics**.

Unobserved variables—such as motivation or ability—may still bias results. 

---

# 5. Difference-in-Differences (DiD)

This method compares **changes over time** between treatment and comparison groups.

It assumes that:

> Both groups would have experienced the same trend in the absence of the program. 

This assumption is called the **parallel trends assumption**.

If it is violated, the estimated impact will be incorrect.

---

# 6. Statistical Matching

Matching attempts to pair participants with nonparticipants who have similar characteristics.

Example:

Match participants and nonparticipants with similar:

- income

- education

- family size

The key assumption is that once matched, **no important differences remain** between the two groups. 

However, this assumption often fails due to unobserved variables.

---

# 7. Regression Discontinuity

Regression discontinuity uses **eligibility thresholds**.

Scholarship eligibility if income < $20,000

Example:

Researchers compare individuals just above and below the cutoff.

The method assumes that the **only difference at the threshold is program participation**. 

---

# 8. Instrumental Variables

Instrumental variables (IV) use an external factor that predicts participation but does not directly affect the outcome.

Example:

- TV reception influenced by geographic features (mountain height).

This method relies on strong assumptions:

- the instrument affects outcomes **only through program participation**. 

If the instrument influences outcomes in any other way, the estimate becomes biased.

---

# Module 2.3: How Randomization Helps Infer Cause

Randomization addresses the central problem of causal inference.

---

## Random Assignment

In randomized evaluations:

- individuals (or schools, villages, firms) are **randomly assigned** to treatment or comparison groups.

Randomization ensures that:

- both groups are statistically similar **on average** before the intervention.

This includes both:

- observable characteristics
- unobservable characteristics such as motivation or ability. 

---

## Creating a Valid Counterfactual

Because assignment is random:

- any difference in outcomes between groups can be attributed to the program.

Thus, the comparison group represents a **valid estimate of what would have happened without the intervention**.

---

## Random Assignment vs Random Sampling

The chapter distinguishes two concepts:

| Concept | Purpose |
|------|------|
| Random Sampling | Selecting individuals to represent a population |
| Random Assignment | Allocating participants to treatment or control groups |

Randomized evaluations rely on **random assignment**, not random sampling. 

---

## Steps in Random Assignment

Typical steps include:

1. **Define the eligible population**
2. Create a complete list of units (individuals, schools, etc.)
3. Randomly assign units to:
   - treatment group
   - comparison group
4. Implement the program only for the treatment group.

---

## Imperfect Compliance

In practice:

- some people assigned to treatment may not participate
- some in the comparison group may obtain the intervention elsewhere.

However, as long as **take-up is higher in the treatment group**, impact can still be estimated statistically. 

---

# Module 2.4: Advantages and Limitations of Randomized Evaluations

## Advantages

### 1. Strong Causal Identification

Randomized evaluations provide **clear causal evidence** without requiring strong assumptions.

They eliminate selection bias because groups are comparable at baseline.

---

### 2. Transparency

Randomized designs make assumptions explicit and easily understood.

The causal logic is straightforward:

Random assignment → comparable groups → causal inference

---

### 3. Flexibility

Researchers can randomize:

- the entire program
- different program components
- alternative program designs.

This allows evaluation of **specific policy questions**. 

---

### 4. Custom Data Collection

Because evaluations are designed in advance, researchers can collect:

- baseline data
- tailored outcome measures
- long-term follow-up data.

---

## Limitations

### 1. Limited Scope

A single randomized evaluation typically answers **only a few questions**.

---

### 2. Cost

RCTs often require:

- new surveys
- baseline data collection
- monitoring systems.

These can be expensive.

---

### 3. Ethical and Practical Constraints

Randomization may not be feasible when:

- programs must be universal
- withholding treatment is unethical
- political constraints prevent random assignment.

---

### 4. External Validity

Results may depend on:

- context
- population
- institutional environment.

Findings may not generalize automatically to other settings.

---

# Historical Origins of Randomized Experiments

Randomized experimentation has roots in several disciplines.

Examples include:

- **1747 – James Lind’s scurvy experiment**, comparing citrus treatments among sailors.
- **1920s – Ronald Fisher’s agricultural experiments**, introducing modern statistical randomization.
- **1960s – Social experiments** evaluating welfare, employment, and housing policies. 

These developments laid the foundation for modern randomized impact evaluations.

---

# Key Takeaways

1. Measuring causal impact requires estimating a **counterfactual**.
2. Many evaluation methods rely on **strong assumptions** that are often unrealistic.
3. Selection bias is the central challenge in impact evaluation.
4. Randomization ensures treatment and comparison groups are **comparable on average**.
5. Randomized evaluations therefore provide **the most credible estimates of program impact**.
6. However, randomized methods also have **costs, ethical considerations, and limits to generalizability**.

---

# Summary

Chapter 2 establishes the methodological foundation for randomized impact evaluation.

It demonstrates that:

- nonexperimental methods often fail due to **selection bias and unrealistic assumptions**
- random assignment creates a **valid comparison group**
- randomized evaluations therefore provide the most reliable evidence for determining whether programs truly work.

The chapter sets the stage for later chapters, which explain **how to design, implement, and analyze randomized evaluations in practice**.

---