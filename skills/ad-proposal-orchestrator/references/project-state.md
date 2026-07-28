# Proposal Project State

Use this contract to preserve context between specialist Skills. Keep it in the workspace when writes are allowed; otherwise maintain the same fields in the conversation. Omit empty optional fields rather than inventing values.

## State Template

```yaml
project:
  name:
  mode: full-proposal
  proposal_type:
  decision_maker:
  business_objective:
  communication_objective:
  audience:
  channels: []
  budget:
  deadline:
  deliverables: []
  approval_mode: automatic

constraints: []
open_questions: []

assumptions:
  - id: A01
    statement:
    impact: low
    status: working

evidence:
  - id: E01
    claim:
    source_url:
    source_date:
    data_period:
    accessed_at:
    confidence: high
    limitation:

decisions:
  - id: D01
    statement:
    based_on: [E01]
    confidence: medium
    status: proposed

artifacts:
  - stage: research
    path_or_url:
    status: draft

gates:
  gate_0_intake: pending
  gate_1_evidence: pending
  gate_2_insight: pending
  gate_3_creative: pending
  gate_4_narrative_visual: pending
  gate_5_delivery: pending
```

Use stable IDs. Never reuse an ID for a different claim. Mark superseded assumptions or decisions instead of silently deleting them.

## Stage Gates

| Gate | Pass condition | Failure action |
|---|---|---|
| 0 Intake | Objective, audience, decision maker, deliverable and material constraints are known or explicitly assumed | Ask only for direction-changing gaps; record the rest as assumptions |
| 1 Evidence | Critical claims have traceable sources, dates, confidence and limitations | Return to research; downgrade unsupported claims to hypotheses |
| 2 Insight | Selected insight has a point of view, evidence, counterargument and action implication | Generate stronger candidates or return to missing evidence |
| 3 Creative | Recommended direction clearly translates the strategy and specifies audience response, format and risk | Rework the direction or select a better-scoring alternative |
| 4 Narrative/Visual | The argument is causal, each page has one job, and visual choices improve comprehension | Return to the first broken chapter or page rule |
| 5 Delivery | Sources, logic, client fit, page clarity, risks and requested file formats pass review | Fix critical findings and rerun delivery review |

## Handoff Contract

Every specialist handoff must report:

```markdown
## Stage Handoff
- Stage:
- Inputs used:
- Evidence/decision IDs:
- Outputs and artifact paths:
- Assumptions and confidence:
- Unresolved questions:
- Gate result: pass / fail / provisional
- Next action:
```

`provisional` is allowed only when the remaining uncertainty is visible and does not change the recommended direction. A downstream stage must not convert a provisional claim into a fact.
