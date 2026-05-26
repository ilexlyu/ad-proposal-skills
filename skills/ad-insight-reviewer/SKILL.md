---
name: ad-insight-reviewer
description: "广告策略洞察生成与评审 Skill。Use when research materials, fact tables, consumer data, competitor notes, or client inputs are ready and the user needs strategic insights, POVs, campaign angles, pitch strategy, or a judged Top 3 insight set. It turns facts into opinionated strategic statements with evidence, counterarguments, fit, and action implications."
---

# 洞察生成与评审

目标：从事实里提炼有立场的策略判断。洞察不是事实复述，而是对事实的重新解释。

## Inputs

- 资料表或事实清单。
- 产品卖点、目标用户、客户诉求、竞争环境。
- 如果资料不足，先列“需要补证据的问题”，不要强行产出结论。

## Workflow

1. **事实分组**：用户、人群、品类、竞品、渠道、文化情绪、购买阻力。
2. **寻找张力**：新旧变化、说法与行为不一致、用户想要但不愿承认、竞品都忽略的角度。
3. **生成候选洞察**：输出 10 条，每条必须是判断句。
4. **逐条评分**：按 4 个维度评分 1-5。
5. **选择 Top 3**：说明为什么值得客户相信，以及会改变什么动作。

## Scoring Dimensions

| 维度 | 问题 |
|---|---|
| 重新解释事实 | 它是否不是事实复述，而是给事实换了一个解释？ |
| 明确立场 | 它是否允许被反驳，而不是永远正确的废话？ |
| 行动影响 | 它是否能改变产品定位、传播方向或渠道选择？ |
| 证据/反证 | 它是否有证据支撑，也看过可能反驳？ |

## Output Format

```markdown
## 候选洞察 10 条
| 洞察 | 支持事实 | 可能反证 | 行动影响 | 评分 |

## 推荐 Top 3
### 1. 洞察
- 策略句：
- 为什么成立：
- 客户为什么会相信：
- 会改变的动作：
- 风险：
```

## Quality Bar

- 禁止输出“年轻人越来越注重情绪价值”“消费者更关注健康”等事实复述。
- 必须改写成有判断的策略句，例如“消费者不是更关注健康，而是更害怕自己看起来不健康”。
- 对新人解释为什么某条洞察只是事实，为什么另一条更像策略。
