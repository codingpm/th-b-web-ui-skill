# TH B Web UI Skill

`th-b-web-ui-skill` 是一个面向企业后台原型生成的 skill。

它的目标是把内部系统常见的页面结构、命名习惯、组件语义和界面风格提炼成一套可复用规则，让 AI 生成出来的原型更像内部业务系统。

## 适合做什么

- 生成后台列表页原型
- 生成配置页或审批页原型
- 生成带抽屉的快速编辑流程
- 生成详情页、状态页、运营页
- 生成更贴近内部组件体系的 Figma 提示词
- 生成更像内部后台风格的 Vue、React、HTML 原型代码

## 这个 Skill 的核心价值

它会引导 AI 优先采用更像内部系统的设计语言，例如：

- 基础组件族风格的页面结构
- 业务组件族风格的领域选择器和业务模块
- 标准化区块风格的配置式区域
- 列表页常见的“筛选区 + 操作区 + 表格 + 分页”结构
- 表单页常见的“卡片分组 + 表单区 + 底部固定操作栏”结构
- 抽屉式编辑、标签状态、标准表格、固定底部操作栏等后台模式

它生成的结果会更克制、更规整、更像企业后台，而不是消费级产品页面或营销落地页。

## 不做什么

这个 skill 不追求复刻某一套具体技术实现，而是优先沉淀：

- 页面结构规则
- 命名和组件语义
- 企业后台常见布局模式
- 更贴近内部系统的界面风格

它更适合做“规范约束”和“原型生成”，而不是绑定某种具体实现。

## 推荐使用方式

最简单的调用方式：

```text
请用 $th-b-web-ui-skill 生成一个后台页面原型，要求贴近企业后台设计规范和标准化页面结构。
```

更推荐的调用方式：

```text
请用 $th-b-web-ui-skill 生成一个资源管理列表页原型。

要求：
- 页面结构贴近内部后台系统
- 顶部使用基础表单式或标准筛选区式结构
- 中间使用标准数据表格式区域
- 状态使用标签式或状态指示式方式表达
- 操作区保持企业后台风格，紧凑、规整、克制
- 不要做成消费级产品页面
```

## 适合补充给 AI 的信息

为了让结果更准，建议补充：

- 页面类型：列表页、详情页、编辑页、抽屉页、配置页、审批页
- 主要业务对象：资源、组织、地点、分类、对象、记录
- 筛选字段
- 表格列
- 操作按钮
- 弹窗或抽屉的用途
- 是否需要生成代码
- 是否需要更贴近基础组件族、业务组件族或标准化区块的某一类模式

## 目录说明

- [SKILL.md](/Users/mashaoguang/.codex/skills/th-b-web-ui-skill/SKILL.md)
  skill 的核心规则定义
- [openai.yaml](/Users/mashaoguang/.codex/skills/th-b-web-ui-skill/agents/openai.yaml)
  skills 平台展示信息和默认 prompt
- [page-patterns.md](/Users/mashaoguang/.codex/skills/th-b-web-ui-skill/references/page-patterns.md)
  常见页面类型模板
- [internal-mapping.md](/Users/mashaoguang/.codex/skills/th-b-web-ui-skill/references/internal-mapping.md)
  内部命名语义和组件映射方式
- [publishing-kit.md](/Users/mashaoguang/.codex/skills/th-b-web-ui-skill/references/publishing-kit.md)
  对外发布文案和示例 prompt

## 一句话总结

如果你的目标是“让 AI 生成出来的后台原型更像成熟的企业后台设计体系”，那就用 `th-b-web-ui-skill`。
