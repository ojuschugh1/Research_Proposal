## What Drives Score Variance in Community-Built AI Evaluations? A Structural Analysis of Weval

### Research Question

Weval's 100+ community-contributed evaluation blueprints produce scores ranging from 23% to 95% across 112+ model configurations on the same evaluations. Is this variance primarily explained by genuine differences in model capability - or by structural differences in how evaluation blueprints are designed? This proposal investigates the sources of score variance in Weval, with the goal of producing actionable guidance on what makes a community-built AI evaluation reliable, valid, and governance-relevant.

### Background and Motivation

Community-built AI evaluation platforms like Weval represent a democratic alternative to proprietary benchmarks controlled by labs. But their value as governance infrastructure depends on a question that has not yet been answered empirically: do the evaluations themselves introduce systematic variance that obscures model-level differences?

The 72-percentage-point spread in Weval scores is striking. It could reflect genuine model capability differences on socially complex tasks - a signal worth amplifying for governance purposes. Or it could reflect blueprint design choices (prompt framing, rubric structure, task complexity) that inflate or deflate scores independently of model behavior. Disentangling these two sources is foundational to using Weval as a credible evidence base for AI governance.

My background is directly relevant. I build measurement tools for AI systems: sqz instruments how models consume and discard context across real tasks; ClaimCheck audits whether agents behave as claimed. These projects have given me practical fluency in the gap between stated and actual AI behavior - precisely the gap that evaluation research must close.

### Data and Method

**Primary dataset:** Weval evaluation scores across 100+ blueprints and 112+ model configurations, including blueprint metadata (task type, rubric structure, prompt framing, social complexity category).  
**Secondary dataset:** Global Dialogues (Rounds 1-4) as an external reference frame - to test whether blueprints covering topics that publics rate as high-stakes (AI in healthcare, criminal justice, political content) show systematically different variance profiles than lower-salience domains.

**Phase 1 - Variance decomposition (Months 1-2):**  
Fit a mixed-effects model partitioning Weval score variance into model-level, blueprint-level, and interaction components. Cluster blueprints by observable design features. Measure whether blueprint cluster membership predicts score variance independently of model identity.

**Phase 2 - Design feature analysis (Months 2-3):**  
Identify which specific blueprint features (rubric granularity, prompt framing, presence of socially contested content) are most strongly associated with high inter-model variance. Produce a ranked feature importance analysis.

**Phase 3 - Governance implications (Months 4-6):**  
Cross-reference high-variance evaluation domains with Global Dialogues data on which AI governance topics publics care most about. Assess whether community contributors are building evaluations in the domains that matter most to global publics - and whether those blueprints are structurally sound.

### Impact and Novelty

No published work has applied variance decomposition to a community-built AI evaluation platform at this scale. If blueprint design choices explain a significant share of Weval's score variance, that changes how CIP should onboard contributors and weight results in governance-facing outputs. If model-level variance dominates, that strengthens Weval's credibility as a governance signal. Either finding advances CIP's mission.
