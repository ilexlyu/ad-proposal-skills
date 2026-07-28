# Ad Proposal Skills

**A modular Agent Skill system for strategy, creative, content, and brand teams — from an ambiguous brief to a client-ready advertising proposal.**

[简体中文](README.zh-CN.md) · [Workflow](docs/workflow.en.md) · [Example brief](examples/lays-summer-brief.en.md) · [中文使用说明](https://my.feishu.cn/docx/Q95Sdsj30oEwLOxxpMDci6mKnHd)

Ad Proposal Skills turns the reasoning behind strong advertising proposals into seven composable skills. It is not a one-shot “generate a PPT” prompt. It provides a traceable workflow for framing the brief, building an evidence base, developing strategic insight, translating strategy into creative territories, structuring the pitch, directing the visual system, and reviewing the final delivery.

```text
Brief → Evidence → Insight → Creative Logic → Narrative → Visual System → Review
```

## Why it exists

Most proposal failures begin before the deck is designed: the brief is under-defined, research is copied without judgment, insights merely restate facts, and creative ideas are disconnected from the business case.

This repository gives teams a shared operating system that helps them:

- turn incomplete client input into explicit assumptions, open questions, and a work plan;
- build a source-linked evidence base instead of an untraceable research dump;
- convert facts into debatable, actionable strategic points of view;
- explain creative direction through established strategic lenses rather than generic brainstorming;
- construct a persuasion chain that clients can understand and approve;
- translate subjective visual language into executable page and design rules;
- review risk, source quality, client fit, and reusable learning before and after delivery.

## The seven-skill system

| Skill | Responsibility | Primary output |
|---|---|---|
| [`ad-proposal-orchestrator`](skills/ad-proposal-orchestrator/SKILL.md) | Frame the assignment and coordinate the workflow | Brief diagnosis, assumptions, skill sequence, deliverables |
| [`ad-research-collector`](skills/ad-research-collector/SKILL.md) | Build a credible and traceable evidence base | Cited research table with confidence and limitations |
| [`ad-insight-reviewer`](skills/ad-insight-reviewer/SKILL.md) | Generate and challenge strategic insights | Scored insight set, Top 3 recommendations, counterarguments |
| [`ad-creative-methods`](skills/ad-creative-methods/SKILL.md) | Translate strategy into persuasive creative territories | Method-led creative directions with rationale and risk |
| [`ad-proposal-narrative`](skills/ad-proposal-narrative/SKILL.md) | Turn strategy and creative into a client-ready story | Deck architecture, slide blueprint, executive summary |
| [`ad-ppt-visual-architect`](skills/ad-ppt-visual-architect/SKILL.md) | Define a visual system that serves the argument | Page rules, visual blueprint, design handoff |
| [`ad-delivery-review`](skills/ad-delivery-review/SKILL.md) | QA the proposal and capture reusable learning | Revision list, delivery risks, retrospective assets |

Each skill can run independently. For an end-to-end assignment, start with the orchestrator and call the specialist skills only when their inputs are ready.

## Install

Clone the repository and copy the skills into your Codex Skills directory:

```bash
git clone https://github.com/ilexlyu/ad-proposal-skills.git
cp -R ad-proposal-skills/skills/ad-* ~/.codex/skills/
```

Restart Codex, then invoke the orchestrator or any specialist skill by name.

## Quick start

```text
Use $ad-proposal-orchestrator

We are planning a summer campaign for Lay's aimed at younger consumers.
We want the brand to play a more visible role across travel, streaming,
friend gatherings, and other summer occasions. The campaign should feel
social rather than promotional. Budget is still open; digital is the priority,
with possible Xiaohongshu, Douyin, and offline extensions.
Help us define the strategic direction.
```

The orchestrator does not jump straight to campaign slogans. It first returns the assignment type, known inputs, critical gaps, working assumptions, recommended skill sequence, and delivery plan.

See the complete [Lay's summer brief example](examples/lays-summer-brief.en.md).

## What a complete run can produce

- **Evidence base:** category, consumer occasion, channel, competitor, and brand-asset research with source links.
- **Strategic insight:** a defensible interpretation such as “young consumers do not need another snack; they need an effortless social cue that starts the moment.”
- **Creative logic:** multiple ways to express the strategy, selected through fit, memorability, credibility, and execution risk.
- **Proposal narrative:** a slide-by-slide persuasion chain from business context to recommended action.
- **Visual system:** an executable design direction built around the sound of the crunch and the action of opening the pack.
- **Delivery review:** source, logic, page clarity, stakeholder fit, and risk checks, followed by reusable project learning.

## Example output

<p align="center">
  <img src="assets/lays-demo/乐事营销demo1.png" width="49%" alt="Lay's proposal cover: 咔嚓一下，开局了">
  <img src="assets/lays-demo/乐事营销demo4.png" width="49%" alt="Lay's strategic insight slide">
</p>
<p align="center">
  <img src="assets/lays-demo/乐事营销demo5.png" width="49%" alt="Lay's core strategy and creative platform">
  <img src="assets/lays-demo/乐事营销demo7.png" width="49%" alt="Lay's content and channel strategy">
</p>

The example demonstrates workflow output, not an official campaign or brand endorsement.

## Designed for

- agency strategy, planning, creative, copy, and account teams;
- in-house content, social, brand marketing, and ecommerce teams;
- independent strategists and creative consultants;
- teams turning proposal craft into a repeatable Agent workflow.

## Operating principles

1. **Evidence before assertion.** Material claims need a source, date, confidence level, and limitation.
2. **Judgment before ideation.** Creative exploration begins only after the strategic choice is explicit.
3. **One argument per slide.** A deck is a persuasion system, not a storage format.
4. **Execution over adjectives.** “Premium” and “youthful” must become concrete visual rules.
5. **Risk before delivery.** Challenge weak evidence, unsupported leaps, and stakeholder objections early.
6. **Learning after delivery.** Convert project-specific experience into reusable methods and references.

## Repository structure

```text
skills/      Seven installable Agent Skills and reference libraries
docs/        Workflow documentation
examples/    Example briefs and expected skill flow
assets/      Demonstration proposal visuals
```

The skills use the `SKILL.md` convention and include Codex interface metadata under `agents/openai.yaml`.

## Status

Current release: `v0.1.0`

The system is usable today and intentionally compact. Contributions that improve source quality, industry-specific references, evaluation criteria, or field-tested examples are welcome.

## License

[MIT](LICENSE)
