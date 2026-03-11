# Field Experiments (Harrison & List, 2004) — Detailed Overview
*Glenn W. Harrison & John A. List. Journal of Economic Literature, Vol. 42(4), Dec. 2004, pp. 1009–1055.*

---

## 1) What the article is trying to do

Harrison and List position **field experiments** as a bridge between:
- **laboratory experiments**, which excel at *control* and *internal validity* but can be criticized for limited realism, and
- **observational econometrics**, which often studies naturally occurring variation but must defend *exogeneity* and *identification* assumptions.

Their core claim is that the “lab vs. field” distinction is not a simple binary. Instead, experiments differ along several *dimensions* (subject pool, context, stakes, etc.). Once those dimensions are made explicit, researchers can (i) classify what kind of field experiment they are running, (ii) better interpret divergences between lab and field results, and (iii) use field evidence to design better lab tests.

---

## 2) Introduction: why “field experiments” matter

### 2.1 The counterfactual and the appeal of experimentation
The authors frame field experiments as a way to **construct credible counterfactuals** via controlled variation, without giving up the possibility of studying behavior in environments that look like the real economic settings economists care about.

### 2.2 “Sterility” is not a flaw—unless it’s all you have
They defend the laboratory’s “sterility” as a feature: it produces sharp inference about treatment effects. The problem arises only when laboratory evidence is used *in isolation* to predict field behavior without checking whether the relevant behavioral margins “travel” from the lab to the field.

---

## 3) Defining field experiments as multidimensional (Section 2)

### 3.1 What does “field” mean?
They lean on the ordinary-language idea that “field” refers to the **natural environment** rather than the lab/office setting, but argue that “natural environment” is itself multidimensional across the components of an experiment.

### 3.2 Six defining factors (a checklist for “fieldness”)
The paper proposes **six factors** to locate any experiment on a lab–field spectrum:

1. **Subject pool** (students vs. nonstandard/target populations)
2. **Information subjects bring** (experience, market knowledge, heuristics)
3. **Commodity** (abstract/induced values vs. real goods/services)
4. **Task / trading rules** (familiar field tasks vs. artificial tasks)
5. **Stakes** (levels and salience relative to real-world decisions)
6. **Environment** (context cues, norms, and naturally occurring setting)

A key methodological point is that these dimensions are often correlated, but separating them helps explain why a field result may differ from a lab result.

### 3.3 A proposed taxonomy (four canonical categories)
They introduce a widely used taxonomy:

| Category | What changes relative to a conventional lab experiment? | Core idea |
|---|---|---|
| **Conventional lab** | students + abstract framing + imposed rules | maximum control, minimal natural context |
| **Artefactual field experiment** | *nonstandard* subjects (but still “lab-like”) | change the subject pool first |
| **Framed field experiment** | add *field context* in commodity/task/info | context may activate field heuristics |
| **Natural field experiment** | subjects in their natural environment and **unaware** they are in an experiment | minimize experimenter demand / selection into “being studied” |

The authors stress this taxonomy is not exhaustive, and that running **multiple versions** can identify what feature is driving results.

---

## 4) Field experiments in the broader identification toolkit (Section 3)

The authors embed experiments in the broader set of strategies for identifying **treatment effects** when counterfactual outcomes are missing.

They contrast:
- **Controlled experiments** (lab + field): direct randomization constructs the control group.
- **Natural experiments**: exploit naturally occurring “as-if random” events; identification hinges on assumptions.
- **Propensity score matching**: tries to make observational data “look like” experimental data; relies on selection-on-observables.
- **Instrumental variables**: requires strong exclusion restrictions; instruments are scarce and fragile.
- **Structural modeling**: relies on deeper functional-form and equilibrium assumptions; useful for simulation but heavy on identifying restrictions.

The key message: field experiments are valuable because they retain the **logic of controlled experimentation** while relaxing some of the lab’s artificial constraints.

---

## 5) Artefactual field experiments (Section 4): “real people” in controlled designs

### 5.1 Why move beyond students?
A central critique of lab experiments is that student subjects may not represent the target population. Artefactual field experiments respond by **changing the subject pool** while keeping much of the controlled experimental structure.

### 5.2 Sample selection and recruitment biases
The authors emphasize that selection is not magically solved by “going to the field.” Key issues include:
- **Recruitment effects** (who volunteers) and how fees/compensation can shift the recruited sample.
- **Attrition** once an experiment begins (especially outside controlled lab settings).
- The possibility that randomization itself attracts participants with certain traits (e.g., lower risk aversion).

### 5.3 Are students behaviorally different?
They review evidence that the “student problem” may be less about students being intrinsically different and more about **restricted variation in covariates** (age, income, experience). With a good behavioral model, one can sometimes reweight/predict to a target population, but extrapolation beyond the student support (e.g., predicting behavior of older adults from 19–27-year-olds) can be unreliable.

### 5.4 Partial matching can backfire
They discuss a methodological warning: matching subjects on some observables can induce bias if the matched groups differ in variance or in unobservables that map into outcomes (drawing on critiques of paired-audit studies of discrimination).

### 5.5 Takeaway for artefactual field experiments
Artefactual field experiments are a **first step** toward relevance, but they inherit many lab-like selection issues because subjects still select into “being in the experiment.”

---

## 6) Framed field experiments (Section 5): adding context that activates field behavior

Framed field experiments keep experimental control but incorporate **field context** in one or more dimensions.

### 6.1 Information & experience
Field subjects may bring experience-based heuristics to tasks (e.g., auction or bargaining settings). The authors highlight the question of whether such heuristics **travel** to other contexts or disappear when stripped of context.

### 6.2 Commodity realism
Replacing induced values with real goods/services can shift behavior. The authors treat this not as a nuisance but as diagnostic:
- if theory fails when commodities are real, then the theory’s domain of applicability is limited (or the theory is wrong).

### 6.3 Task and rules
Field-relevant parameterizations and familiar tasks can change behavior. One can also import estimated field parameters into lab designs to test theory in a *field-relevant* domain.

### 6.4 Stakes
They address the criticism that lab stakes are “trivial.” Stakes can matter, and the relationship between stake levels, salience, and behavior is itself an empirical question.

### 6.5 Environment
Context can provide cues about norms, strategies, and attention. Rather than treating these as uncontrolled confounds, framed field experiments can make them **controlled objects of study**.

### 6.6 Takeaway for framed field experiments
Framed field experiments are explicitly about testing whether adding context changes behavior and whether lab results generalize when key aspects of the field setting are restored.

---

## 7) Natural field experiments (Section 6): minimal invasiveness and reduced demand effects

Natural field experiments combine:
- naturally occurring settings and tasks, and
- the critical feature that **subjects do not know they are in an experiment**.

### Why this matters
Not knowing one is studied can reduce:
- **experimenter demand effects**
- role-playing and “being a subject” behaviors
- selection into the experiment itself (although subjects still select into the underlying market/setting).

The authors treat natural field experiments as closest to the “ideal” of observing natural behavior under controlled variation—though the ability to randomize and maintain clean controls can be harder.

They also discuss *minimally invasive* designs that exploit institutional features to create experimental variation with minimal disruption (e.g., manipulating temporary bets in markets where cancellations are possible).

---

## 8) Social experiments (Section 7): randomized policy as experimentation

Social experiments are **government-run randomized changes** to policy implementation.

### Typical applications
They note social experiments’ role in areas such as:
- employment and training programs
- discrimination detection and enforcement

### Key methodological lessons
- Recruitment and compliance can be difficult, especially when administrators and participants perceive ethical/political stakes.
- Substitution can undermine clean counterfactuals if control-group subjects can access close substitutes outside the experimental protocol.
- Experimenter and implementer effects can be hard to avoid in politicized settings.

The authors argue that debates over social experiments contain transferable lessons for the design of field experiments.

---

## 9) Natural experiments (Section 8): “as-if random” events with weaker control

Natural experiments exploit naturally occurring shocks that resemble random assignment.

### Benefits
- Can speak to large-scale, naturally occurring economic activity.

### Costs
- Less direct control means heavier reliance on identification assumptions.
- Instruments/events are scarce, so researchers often face limited opportunities to replicate or triangulate.

The authors advocate complementarity: use natural experiments where feasible, but recognize what is gained/lost relative to controlled field experimentation.

---

## 10) Thought experiments and neuroeconomics (Section 9): experiments “of the mind”

### 10.1 Thought experiments
They treat thought experiments as related to the logic of experimentation, especially when theorists posit “what if” scenarios. A key methodological issue is that theoretical predictions typically do not come with explicit “instructions” for statistical testing—particularly **error specifications** and heterogeneity.

They discuss how debates over expected utility theory illustrate that different stochastic error assumptions can yield very different inferences about what is “broken.”

### 10.2 Neuroeconomic evidence
They briefly locate neuroeconomics as providing new measurement technologies that can be paired with artefactual experimental settings (e.g., lab tasks with brain measurements), raising questions about interpretation and external validity.

---

## 11) Practical synthesis: how to use the paper

### 11.1 Use the six-factor checklist to diagnose differences
When lab and field results differ, ask systematically:
- Is it the subject pool?
- Experience/information?
- Commodity realism?
- Task familiarity/rules?
- Stakes?
- Environment/context cues?

### 11.2 Treat lab and field as complements, not substitutes
The paper repeatedly emphasizes a **cycle**:
1. use labs to isolate mechanisms with clean control,
2. use framed/natural field experiments to test whether mechanisms generalize,
3. bring anomalies back to the lab to refine theory and isolate neglected features.

---

## 12) Key takeaways (exam-ready)

1. “Fieldness” is multidimensional; do not classify experiments with a single binary label.
2. Field experiments preserve the experimental logic of counterfactual construction while increasing realism along selected dimensions.
3. The Harrison–List taxonomy (conventional / artefactual / framed / natural) is a practical way to describe experimental designs.
4. Selection, recruitment, attrition, and substitution threats remain central—even in the field.
5. Natural field experiments reduce “being-studied” effects but can be harder to control.
6. The best evidence often comes from **triangulation**: multiple experiments across lab/field contexts plus complementary nonexperimental methods.

---

## Reference
Harrison, G. W., & List, J. A. (2004). *Field experiments*. **Journal of Economic Literature, 42**(4), 1009–1055.
