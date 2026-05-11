# Do Community AI Evaluations Cover What Global Publics Actually Care About?

## Research Question

Global Dialogues data shows that unsupervised AI systems draw the highest and fastest-growing public concern globally (+5.6pp between GD3 and GD4), while trust in AI companies sits near the bottom of the institutional hierarchy at ~35%. Weval hosts 100+ community-built evaluation blueprints spanning a wide range of AI behaviors. The question this proposal investigates: do those blueprints concentrate in the domains global publics flag as high-stakes - or is there a systematic gap between what communities choose to evaluate and what the public actually worries about?

## Background and Motivation

Community-built evaluation platforms like Weval represent a democratic alternative to proprietary benchmarks. But their value as governance infrastructure depends on two things being true: the evaluations must be structurally sound (not just reflecting blueprint design artifacts), and they must cover the domains that matter to the publics AI will affect. Neither has been tested empirically.

The 72-percentage-point spread in Weval scores is the entry point. It could reflect genuine model capability differences on socially complex tasks - a signal worth amplifying for governance purposes. Or it could reflect blueprint design choices that inflate or deflate scores independently of model behavior. Disentangling these is foundational to using Weval as credible governance evidence.

My background is directly relevant. I build measurement tools for AI systems: sqz instruments how models consume context across real tasks; ClaimCheck audits whether agents behave as claimed. These projects have given me practical fluency in the gap between stated and actual AI behavior - precisely the gap evaluation research must close.

## Data and Method

**Primary dataset:** Global Dialogues (Rounds 1-4), specifically the governance Indicator questions - institutional trust, societal impact by technology, and AI governance preferences. I have already built a cross-round analysis of these using the public data (notebook: [governance_concern_map_gd3_gd4.ipynb](https://github.com/ojuschugh1/global-dialogues/blob/governance-concern-map/tools/notebooks/governance_concern_map_gd3_gd4.ipynb)).

**Secondary dataset:** Weval evaluation scores across 100+ blueprints and 112+ model configurations, including blueprint metadata.

### Phase 1 - Governance concern map (Months 1-2)

Use Global Dialogues Indicator questions to identify which AI domains global publics rate as highest-stakes, segmented by country and round. This is the reference frame for everything that follows.

### Phase 2 - Variance decomposition (Months 2-3)

Fit a mixed-effects model partitioning Weval score variance into model-level, blueprint-level, and interaction components. Cluster blueprints by design features. Measure whether blueprint cluster membership predicts score variance independently of model identity.

### Phase 3 - Coverage gap analysis (Months 4-6)

Cross-reference the governance concern map from Phase 1 with Weval blueprint coverage. Assess whether community contributors are building evaluations in the domains that matter most to global publics - and whether those blueprints are structurally sound enough to be used as governance evidence.

## Impact and Novelty

No published work has applied variance decomposition to a community-built AI evaluation platform at this scale, or cross-referenced evaluation coverage against longitudinal public opinion data. Either finding - coverage gap or structural soundness - advances CIP's mission directly.
