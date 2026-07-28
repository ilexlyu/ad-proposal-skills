---
name: ad-proposal-orchestrator
description: "面向策略、创意、内容与品牌团队的广告提案总控 Skill。Use when the user gives an advertising, marketing, branding, ecommerce, social campaign, launch, or client brief and wants to start a proposal, pitch deck, PPT outline, campaign plan, or AI/Agent Skill workflow. Use to clarify the brief, identify missing inputs, split work into research, insight, creative, narrative, visual, and delivery-review steps, and recommend which ad-proposal Skills to call next."
---

# 广告提案总控

目标：把一个模糊 brief 拆成可执行提案任务图，并调度专项 Skill。不要直接跳去写 PPT；先确定“缺什么信息、先做什么、哪些判断还不能下”。

## Core Workflow

1. **识别提案类型**
   - 品牌定位/年度策略/新品上市/电商增长/社媒内容/整合营销/招商或销售提案。
   - 标注决策人：老板、市场部、品牌部、电商负责人、代理商比稿、内部汇报。

2. **抽取输入**
   - 品牌/产品、行业、目标人群、传播目标、预算级别、交付形式、截止时间、已有材料。
   - 如果缺关键字段，列成“必须补充/可以边做边查/暂时假设”三类。

3. **拆解任务**
   - 资料：调用 `$ad-research-collector`。
   - 洞察：调用 `$ad-insight-reviewer`。
   - 创意：调用 `$ad-creative-methods`。
   - 结构：调用 `$ad-proposal-narrative`。
   - 视觉：调用 `$ad-ppt-visual-architect`。
   - 质检/复盘：调用 `$ad-delivery-review`。

4. **输出任务地图**
   - 项目判断：这是什么类型的提案。
   - 缺失信息：现在不能下的判断。
   - Skill 顺序：建议调用哪些 Skill，按什么顺序。
   - 交付物：资料表、洞察表、创意方向、PPT 大纲、视觉蓝图、质检清单。

## Output Format

```markdown
## 项目判断
- 提案类型：
- 决策人：
- 核心目标：

## 当前输入
- 已有信息：
- 缺失信息：
- 暂定假设：

## Skill 调用顺序
1. ...

## 交付物清单
- ...

## 暂时不能下的判断
- ...
```

## Quality Bar

- 必须先解释“为什么按这个顺序做”。
- 不要把 brief 直接改写成 PPT 大纲，除非资料、洞察和创意已经充分。
- 明确每一步的专业职责：资料建立事实基础，洞察形成策略判断，创意负责策略转译，结构建立说服链，视觉提升理解效率，质检控制风险并沉淀资产。
