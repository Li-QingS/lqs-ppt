# lqs-ppt · 学术科研演示制作

通用的学术汇报工作流，适用于不同学科、报告语言和研究方法。支持框架讨论、页面文案、整页图片、独立科研配图、局部修改与可编辑演示稿。

内容、术语、叙事、引用和视觉样式由本次材料、听众与要求确定，不附带领域专用知识或固定主题模板。格式不明确时先确认交付形式。可编辑制作或参考页复刻前，先确定由用户自己完成还是交给 agent；已明确选择时不重复询问。

## 安装与调用

将以下指令发送给 Codex：

```text
使用 $skill-installer 安装 https://github.com/Li-QingS/lqs-ppt/tree/main/skills/lqs-ppt
```

安装后调用：

```text
使用 $lqs-ppt，根据我提供的研究材料、听众、汇报语言和模板，先讨论这次学术汇报的框架，不生成文件。
```

```text
使用 $lqs-ppt，按照本次已确认的内容和样式生成完整页面图片。
```

使用者先安装一次，仓库更新后主动更新自己的本地副本。更新前保留需要的自定义备份，再用完整新目录替换旧版本，避免已删除的引用文件残留或混用版本。若客户端没有上述安装器，按其技能安装入口安装完整的 `skills/lqs-ppt` 目录，保留相对引用文件。

## 包含的资源

- [主流程](skills/lqs-ppt/SKILL.md)：当前任务范围、交付选择、学术叙事、证据保护与核查。
- [提示词模板](skills/lqs-ppt/references/prompt-templates.md)：整页图、独立配图、概念图局部编辑，以及证据合成、可编辑制作的任务模板，附不带领域背景的完整填写示例。
- [Checklist](skills/lqs-ppt/references/checklist.md)：共用与条件分支的勾选清单，区分通过、失败、未检查与不适用。
- [制作与验收](skills/lqs-ppt/references/production-and-qa.md)：实际文件、证据保真、局部保护和编辑性核查。
- [文案与引用](skills/lqs-ppt/references/writing-and-citations.md)：适配语言、研究方法、文献格式及修改意见。

仅按当前任务加载必要资源。提示词模板提供字段结构，示例不为新任务规定内容、颜色、字体、比例或步骤。

## 运行能力与交付

本包提供工作流与模板，不附带模型、API额度或外部工具。文本讨论只需文本能力；图片、排版和可编辑演示稿使用接收者环境中实际可用的工具。能力缺失时说明可做范围，不伪称产物已经生成或验收。

`lqs-ppt.skill` 是 ZIP 格式的分发包。可将副本后缀改为 `.zip` 后解压；技能入口仍为 `SKILL.md`。安装完整目录，不将压缩文件当作入口。

```text
skills/lqs-ppt/
├── SKILL.md
├── agents/openai.yaml
└── references/
    ├── prompt-templates.md
    ├── checklist.md
    ├── production-and-qa.md
    └── writing-and-citations.md
```

公开目录不包含聊天记录或本机依赖。当前分发方式为 GitHub 技能目录；不会自动安装到所有使用者的客户端，也不表示应用内市场上架。

仓库尚未指定开源许可证；修改后再分发的授权请与作者确认。
