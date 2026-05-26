# Ad Proposal Skills

一套面向广告新人、策略/创意/内容团队的 Agent Skills。

中文使用说明页：[广告提案 Agent Skills：从模糊 Brief 到完整提案工作流](https://my.feishu.cn/docx/Q95Sdsj30oEwLOxxpMDci6mKnHd)

它不是一个“帮我生成 PPT”的 prompt，而是一套从模糊 brief 到完整提案工作流的可复用方法：

```text
Brief -> 资料 -> 洞察 -> 创意解释 -> 提案结构 -> 视觉架构 -> 交付复盘
```

## 解决什么问题

广告提案最难的地方，往往不是写 PPT，而是面对一个模糊 brief 时不知道从哪里开始。

这套 Skills 试图把广告人的隐性经验显性化：

- 先拆 brief，而不是直接打开 PPT。
- 先找可信资料，而不是复制一堆截图。
- 把事实改写成有判断的洞察。
- 用华与华、奥美/Deck of Brilliance、麦肯锡、群玉山等方法解释策略。
- 把策略和创意整理成客户听得懂的 PPT 逻辑。
- 把“年轻化、高级、夏日感”翻译成可执行视觉规则。
- 交付后复盘，把经验沉淀成下一次可复用资产。

## Skills

| Skill | 作用 |
|---|---|
| `ad-proposal-orchestrator` | 提案总控：拆 brief、识别缺失信息、规划后续 Skill 调用顺序 |
| `ad-research-collector` | 行业资料搜集：规定资料源、可信度、输出资料表 |
| `ad-insight-reviewer` | 洞察生成与评审：把事实变成有立场的策略判断 |
| `ad-creative-methods` | 创意方法论：用机构方法论解释策略，而不是泛泛发散点子 |
| `ad-proposal-narrative` | 提案结构叙事：把策略和创意变成客户可理解的 PPT 逻辑 |
| `ad-ppt-visual-architect` | PPT 视觉架构：生成视觉系统、页面规则和设计交接稿 |
| `ad-delivery-review` | 交付质检与复盘：检查风险，并沉淀可复用资产 |

## 安装

把 `skills/ad-*` 复制到你的 Codex Skills 目录：

```bash
cp -R skills/ad-* ~/.codex/skills/
```

重新打开 Codex / Agent 后，即可通过 `$ad-proposal-orchestrator` 或其他 Skill 名称调用。

## 快速示例

可以先用一个模糊 brief 测试总控：

```text
Use $ad-proposal-orchestrator

我们是乐事薯片，今年暑期想做一波年轻人向的传播。
夏天大家出去玩、宅家追剧、朋友聚会都挺多的，我们希望乐事能更有存在感。
不想只是做促销，也不想太硬广，最好能有一点社交传播性。
预算还没完全定，线上为主，可能会结合小红书、抖音和一些线下场景。
你们先帮我们想想方向。
```

总控会把 brief 拆成项目判断、缺失信息、后续 Skill 调用顺序和交付物清单。

完整示例见 [`examples/lays-summer-brief.md`](examples/lays-summer-brief.md)。

## 示例成果

用这套流程跑完乐事暑期 brief 后，可以产出：

- 资料表：行业、场景、渠道、竞品和品牌资产。
- 洞察：例如“年轻人不是缺零食，而是缺一个能自然开局的社交道具”。
- 创意解释：华与华找符号，奥美戏剧化问题，麦肯锡讲客户逻辑，群玉山补公共叙事。
- PPT 主线：让乐事成为年轻人的夏日开局道具。
- 视觉方向：用“咔嚓声波”和“开袋动作”串联追剧、露营、朋友局、夜宵。

部分生成示例图在 [`assets/lays-demo`](assets/lays-demo)。

## 适合谁

- 广告公司新人、策略、创意、文案。
- 内容团队、品牌市场部、电商运营团队。
- 想把自己的提案方法沉淀成 Agent Skill 的个人创作者。
- 想训练团队提案 SOP 的中小公司。

## 版本

当前版本：`v0.1.0`

这是第一版可用结构。后续可以继续补：

- 更多行业案例。
- 安装脚本。
- 视频教程。
- 飞书/Notion 使用说明页。
- 更多机构方法论 reference。

## License

MIT
