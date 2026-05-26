---
name: ad-ppt-visual-architect
description: "广告提案 PPT 视觉架构 Skill。Use when the user has proposal copy, a slide outline, page-by-page blueprint, or client pitch content and needs a visual system, page layout rules, image prompts, design handoff, industry visual conventions, or PPT visual direction. It turns text into a reusable visual Skill card and design brief without rewriting the user's copy."
---

# PPT 视觉架构

目标：把“高级、大气、科技感”这类模糊需求翻译成可执行视觉系统。不要直接改文案；先建立行业视觉公约、页面规则和设计交接稿。

## Before Working

读取 `references/style-method-library.md`，按客户类型选择风格路径。若用户提供参考图，优先分析参考图而不是凭空想象。

## Inputs

- 行业、客户类型、提案文案、逐页蓝图、参考图、品牌色、视觉禁区。
- 若文案还没整理成逐页结构，先建议调用 `$ad-proposal-narrative`。

## Workflow

1. **行业视觉公约**
   - 判断该行业“专业感”来自哪里：色彩、材质、构图、图片类型、信息密度。
   - 标注不能碰的风格误区。

2. **视觉关键词**
   - 输出 3-5 个可执行关键词，不要只写抽象词。
   - 示例：深色金融终端感、真实工厂纪实图、低饱和城市生活方式，而不是“高级感”。

3. **页面系统**
   - 封面、目录页、章节页、观点页、数据页、案例页、结尾页分别给规则。
   - 明确标题位置、内容密度、图文关系、强调方式。

4. **配图提示词**
   - 为每页输出图片描述词或素材方向。
   - 区分真实素材、AI 生成图、图标/信息图。

5. **设计交接清单**
   - 给设计师可直接执行的约束：字体倾向、色彩、留白、版式、禁区。

## Output Format

```markdown
## 视觉基调
- 行业视觉公约：
- 风格关键词：
- 禁区：

## 页面规则
| 页面类型 | 版式 | 图片规则 | 字数密度 | 强调方式 |

## 逐页视觉蓝图
| 页码 | 页面目的 | 版式建议 | 配图提示词 | 设计注意 |

## 设计交接清单
```

## Quality Bar

- 文案 100% 不乱改；如需压缩，必须单独标注为建议。
- 不说“高级、大气、科技感”这种不可执行词，除非同时解释视觉表现。
- 视觉建议必须服务客户理解，而不是只追求好看。
- 页面重点必须清晰，不能把所有元素都强调。
