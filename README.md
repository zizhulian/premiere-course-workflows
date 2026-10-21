# PR课程工作流 · premiere-course-workflows

一个面向 Codex 的中文 Premiere Pro 剪辑 skill，将课程方法整理成可执行的剪辑流程、操作说明与案例配方。

## 能做什么

- 根据素材、目标时长和交付要求组织内容、音乐、声音与剪辑节奏。
- 辅助处理 PR 序列、时间线、剪辑工具、关键帧、蒙版、变速、字幕和导出问题。
- 查阅胶片、缩进、破碎、切割、人物出场、换装、水滴、移动与万花筒九类案例。
- 通过分P链接和大致时间位置回查课程依据。

skill 提供任务指导。实际操作 PR 需要当前环境具备可用的应用控制或集成；本仓库没有 PR 自动化接口。

## 安装与使用

可以在有权限访问本仓库的 Codex 环境中发出安装请求：

```text
请使用 skill-installer，从 https://github.com/zizhulian/premiere-course-workflows
安装 premiere-course-workflows，技能文件位于仓库根目录。
```

也可以将仓库完整目录放入当前 Codex 使用的 skills 目录，保持目录名为 `premiere-course-workflows`，且 `SKILL.md` 直接位于其中。私有仓库需要相应的 GitHub 访问权限。安装后，在识别到该 skill 的会话中使用：

```text
请使用 $premiere-course-workflows，根据我的素材制定一个60秒竖屏剪辑方案。
保留完整人声，给出各段画面、音乐、音效与转场安排，并注明课程依据。
```

安装方式参考 [Codex 官方技能文档](https://developers.openai.com/codex/skills/)。Codex 会自动识别技能变化；若未出现，可重启后检查。

## 文件导航

| 文件 | 内容 |
|---|---|
| [SKILL.md](SKILL.md) | 触发条件、任务判断、工作流程和验收要求 |
| [editorial-and-sound.md](references/editorial-and-sound.md) | 剪辑结构、节奏、音乐与声音 |
| [premiere-operations.md](references/premiere-operations.md) | PR 基础与常用操作 |
| [transition-recipes.md](references/transition-recipes.md) | 九类案例的条件、步骤与检查点 |
| [source-index.md](references/source-index.md) | 40个分P、回查入口与验证范围 |
| [agents/openai.yaml](agents/openai.yaml) | Codex 界面元数据与默认提示词 |

## 来源与验证范围

来源为剪辑圈彭于晏发布的 [Bilibili 课程 BV1Nb421H77B](https://www.bilibili.com/video/BV1Nb421H77B/)。本项目为个人整理，与课程作者及 Adobe 无隶属关系。

截至 **2026-10-21**，原页面标题宣传“全289集”，该链接实际目录提供 **40个分P**，显示时长合计 **7:06:05**。本 skill 依据这40P整理，没有覆盖标题所称的289集。

整理过程包括40课完整音轨的本地转写与逐课阅读、120张代表画面和27张细节画面的核对，以及 P02/P03 联系表查看。它不等于连续逐秒观看全部音画；也尚未在 PR 中逐课复现或导出验证。基础演示主要使用 PR 2024，部分案例画面使用 PR 2023。

部分案例依赖 `BCC 3D Extruded Image Shatter` 或 `BCC Halftone`。仓库不附带插件、安装程序或课程素材。

本仓库仅包含重新组织和撰写的工作流说明、元数据及公开来源链接，不包含课程视频、音频、截图、逐字转写、账号信息或签名媒体地址。详细依据见 [source-index.md](references/source-index.md)。
