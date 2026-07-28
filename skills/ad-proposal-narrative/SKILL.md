---
name: ad-proposal-narrative
description: "广告提案结构与客户叙事 Skill。Use when strategy insights and creative directions exist and the user needs a client-ready pitch structure, PPT outline, slide-by-slide proposal logic, executive summary, talk track, or persuasive narrative for marketing, branding, ecommerce, social, or campaign proposals. It turns scattered ideas into a deck flow that a client can understand and buy."
---

# 提案结构与客户叙事

目标：把策略和创意整理成客户听得懂、愿意买单的 PPT 逻辑。核心不是堆资料，而是建立“客户为什么要相信”的说服链。

## Inputs

- 洞察 Top 3、创意方向、客户背景、决策人类型、交付页数、已有资料。
- 若只有资料没有洞察，先建议调用 `$ad-insight-reviewer`。

## Workflow

1. **确定主线**
   - 用一句话说明提案要证明什么。
   - 判断客户当前最关心的是增长、品牌、转化、认知、招商、内部对齐还是风险规避。

2. **拆章节**
   - 背景：为什么现在要做。
   - 问题：客户真正要解决什么。
   - 洞察：我们如何重新解释市场/用户。
   - 策略：品牌应该怎么行动。
   - 创意：用什么传播方向承接策略。
   - 执行：怎么落地到内容、渠道、节奏。
   - 价值：为什么客户应该买单。

3. **生成逐页蓝图**
   - 每页只保留一个主判断。
   - 为每页补证据、画面建议、讲述意图和转场逻辑。

4. **写客户版摘要**
   - 用客户语言复述，而不是代理商内部术语。
   - 将复杂判断压缩成 3-5 个关键结论。

## Output Format

```markdown
## 提案主线

## 章节结构
| 章节 | 目的 | 客户要被说服的点 |

## 逐页蓝图
| 页码 | 标题 | 主判断 | 证据 | 画面建议 | 转场逻辑 |

## 客户版摘要

## 讲稿要点
```

## Quality Bar

- 每页只能有一个主判断。
- 不能只是“行业趋势、竞品分析、人群洞察”平铺；必须形成因果链。
- 必须回答：客户为什么要相信、为什么现在要做、为什么这条策略适合他。
- 说明每个章节承担的说服功能，以及它如何推动客户进入下一项判断。
