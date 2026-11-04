# GitHub 全球热门 Top 5 · 2026-11-04

每日 9 点自动抓取 github.com/trending 日榜，fork 存档并附中文解读。

## 1. [thedotmack/claude-mem](https://github.com/thedotmack/claude-mem)
fork 存档：https://github.com/qinshanliangengineer/claude-mem
Stars：111906 ｜ 语言：TypeScript

### 项目介绍
给每个 agent 的跨会话持久记忆：记录 agent 在会话中的全部行为，经 AI 压缩后，在未来会话中注入相关上下文。支持 Claude Code、OpenClaw、Codex、Gemini、Hermes、Copilot、OpenCode 等多种工具，用 TypeScript 构建，累计星数已突破 11 万，今日新增 1,139 星。

### 当前应用价值
已在用 Claude Code、Codex、Gemini CLI、Copilot、OpenCode 等 agent 工具的开发者可直接接入：它把每次会话的所作所为自动记录并经 AI 压缩，需要时再把相关上下文注入后续会话，适合把 agent 从「每次从零开始」变成「越用越了解你的项目」的长期助手。（注：该项目连续多日上榜，今日仍居榜首。）

### 潜在应用价值
Agent 的短板正从「会不会写代码」转向「记不记得上下文」：没有持久记忆，agent 每次都要重新熟悉项目，长期任务难以为继。claude-mem 把「记录—压缩—按需注入」做成通用层的做法，若能在隐私与成本上跑通，可能成为 agent 工具链的标准组件；但记忆的准确性与过期清理，仍是它能否真正可用的关键。

## 2. [vercel-labs/agent-desktop](https://github.com/vercel-labs/agent-desktop)
fork 存档：https://github.com/qinshanliangengineer/agent-desktop
Stars：12759 ｜ 语言：Rust

### 项目介绍
给 AI agent 用的 computer-use CLI：通过操作系统的无障碍树读取并操作桌面应用。一次快照返回 JSON，其中每个 agent 可操作的元素都有一个引用（ref），agent 对引用执行操作后再快照核对，全程不依赖像素匹配，循环逻辑仍留在你自己的 agent 里；每次 CLI 调用都在独立进程中运行。项目用 Rust 构建，累计星数 12,759，今日新增 3,791 星。

### 当前应用价值
正在做桌面自动化或 computer-use agent 的开发者可直接试用：它提供 macOS、Windows 与 Linux 的 CLI，用无障碍树快照代替像素匹配来定位可操作元素，适合把 agent 接入真实桌面应用、做跨平台自动化原型。今日新增 3,791 星，为今日榜单新增最多。

### 潜在应用价值
Computer-use 的瓶颈长期是「看得懂界面、点得准按钮」：基于截图与像素匹配的做法脆弱且昂贵。agent-desktop 把界面抽象成结构化的无障碍树快照，若能在三大桌面系统上保持稳定覆盖，有望成为 agent 操作桌面的通用底层；但快照、剪贴板与截图可能包含私人桌面内容，隐私与安全边界是落地前必须先解决的问题。

## 3. [max-sixty/worktrunk](https://github.com/max-sixty/worktrunk)
fork 存档：https://github.com/qinshanliangengineer/worktrunk
Stars：10489 ｜ 语言：Rust

### 项目介绍
面向并行 AI agent 工作流的 git worktree 管理 CLI：为每个任务创建独立的工作树，让多个 agent 可以同时在同一仓库的不同任务上工作而不互相踩脚。项目用 Rust 构建，累计星数 10,489，今日新增 438 星，话题标签覆盖 agents、Claude Code、Codex 与开发者工具。

### 当前应用价值
同时用多个 AI agent 并行改代码的开发者可直接试用：它用 git worktree 把不同任务隔离开，避免分支切换互相干扰，适合把「一人多 agent 并行开发」的工作流先规范起来。

### 潜在应用价值
多 agent 并行开发听起来美好，落地时最先撞上的往往是工作区冲突与状态混乱：worktree 本是 git 的现成隔离机制，缺的只是一个顺手的编排层。Worktrunk 若能把创建、切换、清理整条链路做顺，有望成为 agent 并行开发的标准脚手架；真正的考验在于 agent 数量上去后，合并冲突与评审成本会不会把并行收益吃掉。

## 4. [JustVugg/colibri](https://github.com/JustVugg/colibri)
fork 存档：https://github.com/qinshanliangengineer/colibri
Stars：47247 ｜ 语言：C

### 项目介绍
面向前沿 MoE（混合专家）模型的分层推理引擎：热专家驻留在 GPU（支持 CUDA 与 Vulkan），温专家放在内存，冷专家从 NVMe 流式加载。项目用 C 编写，主打「在你已有的硬件上运行」，累计星数 47,247，今日新增 802 星。

### 当前应用价值
想在自己已有的硬件上跑前沿 MoE 大模型的开发者可试用：它用分层推理把热专家放 GPU、温专家放内存、冷专家走 NVMe 流式加载，适合在单机或有限显存条件下先把大模型跑起来、再谈优化。

### 潜在应用价值
MoE 模型参数规模越做越大，显存却始终是瓶颈：全量上 GPU 不现实，全放 CPU 又太慢。colibri 的分层思路是在显存、内存与磁盘之间做动态调度，若调度开销能控制住，它可能让普通硬件也能跑起前沿大模型，降低本地推理的门槛；但专家切换的延迟与实际吞吐，仍需在真实模型与硬件组合上验证。

## 5. [mattpocock/skills](https://github.com/mattpocock/skills)
fork 存档：https://github.com/qinshanliangengineer/skills
Stars：311465 ｜ 语言：Shell

### 项目介绍
给真正的工程师的技能合集：直接取自作者自己的 .agents 目录。项目主打可直接落地的 agent 技能而非理论清单，用 Shell 构建，累计星数已高达 311,465，今日新增 1,164 星，是今日榜单中累计星数最高的项目。

### 当前应用价值
用 agent 做工程开发、想把个人工作流沉淀为可复用技能的开发者可直接参考：它来自作者真实的 .agents 目录，适合照着挑选、改造成自己的 agent 技能库，而不是从零摸索提示词与工作流写法。

### 潜在应用价值
Agent 能力正在从「模型本身」向「技能与工作流」转移：同一模型配上好的技能库，产出质量可能天差地别。一个来自真实工程实践、经得起日常使用的技能合集，若能持续更新、保持可组合性，有望成为工程师搭建个人 agent 工作流的起点；但照搬他人技能也有风险——脱离自身项目语境的技能，未必能直接复用。

PDF 下载：[digest_2026-11-04.pdf](./digest_2026-11-04.pdf)