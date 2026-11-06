# LQS 科研 PPT Skill

用于中文科研论文与平台展示的框架讨论、整页图片、独立配图，以及按参考图进行可编辑复刻。

技能名与调用名为 `lqs-ppt`、`$lqs-ppt`。`lqs-ppt.skill` 是 ZIP 格式的下载分发包；技能入口仍叫 `SKILL.md`。

## 安装到 Codex

本仓库为 `Li-QingS/lqs-ppt`，默认分支为 `main`，技能位置为 `skills/lqs-ppt`。

将这段话发送给 Codex：

```text
使用 $skill-installer 安装这个 GitHub 技能：
https://github.com/Li-QingS/lqs-ppt/tree/main/skills/lqs-ppt
```

安装成功后，在 Codex 中调用：

```text
使用 $lqs-ppt，阅读我提供的论文和参考PPT，先讨论成果展示的结构，不生图、不修改原PPT。
```

```text
使用 $lqs-ppt，沿用这份参考页的学术风格，生成下一页的完整图片，只交PNG。
```

如果接收者的客户端没有 `$skill-installer`，让其按自身客户端的技能安装入口安装 `skills/lqs-ppt` 目录。不要只复制 `SKILL.md`，四份 `references/` 文件也需要保留。

## 下载包方式

如果收到 `lqs-ppt.skill` 文件，可把副本后缀改为 `.zip`，解压得到 `lqs-ppt/`。将该目录安装到接收者实际使用的 Codex 技能目录，再调用 `$lqs-ppt`。本包不假设所有版本的技能目录位置相同。

发布仓库并不会自动把该技能装入所有人的 Codex。接收者先安装一次，再在自己的对话中调用。

## 运行能力

框架讨论、文案与检查清单可以只用文本能力。生成图片需要接收者环境提供图像生成工具；输出 PPTX 需要可用的演示文稿制作与渲染工具。本包不附带这些工具、API 额度或硬件服务。

若环境提供 `imagegen` 或演示文稿技能，按其指引使用；若工具名称不同，保持相同的证据保真与验收要求。环境无法生成指定文件时，应明确说明能力缺口。

默认科研风格源于 LQS 的制作习惯，当前使用者的要求与模板优先。波形平台及 GMI 内容只在相关任务中按需读取。

## 仓库内容

```text
README.md
skills/
└── lqs-ppt/
    ├── SKILL.md
    ├── agents/openai.yaml
    └── references/
        ├── production-and-qa.md
        ├── project-context.md
        ├── source-ledger.md
        └── writing-and-citations.md
```

公开版不包含私人聊天全文、会话编号、本机路径或录音位置。完整制作与科学内容仍须根据用户实际材料验证。

## 版本与共享

将安装链接发给接收者即可。更新后需要使用者自行更新本地安装；仓库文件变化不代表所有本地副本已同步。

下载附件在发布者提供的 Release 中获取。单独技能目录安装不依赖附件。

此仓库尚未指定开源许可证；如需修改后再分发，请先与作者确认授权。

该方式是 GitHub 分发。应用内市场的搜索发现及安装需遵循相应插件和市场规则。

## 核验依据

核读日期：2026-11-06。

- [OpenAI skill-installer 实现](https://github.com/openai/skills/blob/main/skills/.system/skill-installer/SKILL.md)：支持自选 GitHub 目录安装。该仓库目前标记为弃用，因此这里引用的是可核读的安装器实现，不将旧精选清单的投稿方式作为当前上架流程。
- [OpenAI 当前插件示例仓库](https://github.com/openai/plugins/blob/b767f8fa3be1a22b093127dd59956c91ecffca9d/README.md)：供后续插件封装参考。独立目录安装这一路线不需要先增加插件清单。

本次官方开发文档页面返回403，未确认应用内市场的投稿资格、审核过程或上架范围；本说明不对此作承诺。
