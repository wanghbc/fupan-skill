# Fupan — Evidence-based Retrospective | 复盘

**Goals → Results → Gaps and root causes → Verifiable improvements**

**Based on Lenovo's management philosophy, personally organized and adapted into an AI skill by EDGAR WANG ([@wanghbc](https://github.com/wanghbc)). References and reuse are welcome.**

This is the author's independent adaptation, not an official Lenovo publication or endorsed product. This attribution describes the author's intellectual foundation; it does not claim exclusive Lenovo origin for the broader practice of retrospectives. The instructions are the author's formulation, not quotations from a Lenovo manual.

[English](#english) · [中文](#中文)

## English

### Purpose

Fupan guides AI assistants through retrospectives of projects, business initiatives, personal actions and completed tasks. It examines success as well as failure, distinguishing repeatable practices from favorable circumstances.

| Step | Question | Output |
|---|---|---|
| 1. Goals | What was originally intended? | Original objectives, criteria, deadlines and constraints |
| 2. Results | What actually happened? | Verifiable outcomes, costs and completion status |
| 3. Gaps and root causes | Why did outcomes exceed or fall short of goals? | Causal analysis, evidence, alternatives and uncertainty |
| 4. Improvements | What should change? | Actions, owners, dates, acceptance criteria and follow-up |

It preserves original goals, separates facts from hypotheses, avoids treating activity as achievement, and checks effectiveness before closing actions.

### Installation

The installable unit is **`skills/fupan/`**. Copy the entire folder and keep the folder name `fupan`.

| Environment | Personal installation | Project installation | Invocation |
|---|---|---|---|
| Local Codex | `~/.agents/skills/fupan/` | `.agents/skills/fupan/` | `$fupan` |
| Local Claude Code | `~/.claude/skills/fupan/` | `.claude/skills/fupan/` | `/fupan` |

`~` means your user home directory. On Windows, use your actual user profile folder. Compare or back up an existing `fupan` installation before replacing it. Restart the session if the skill is not discovered and check the locations supported by your installed version.

If your Codex environment provides `$skill-installer`, you can instead ask:

```text
Use $skill-installer to install skills/fupan from the GitHub repository wanghbc/fupan-skill.
```

Hosted ChatGPT/Work environments may require a plugin or another product-specific route. Publishing on GitHub does not automatically install a skill there. Other tools supporting Agent Skills should follow their own installation documentation. In a chat app without skill installation, provide `SKILL.md` as instructions for the current task; this does not establish persistent installation.

### Usage

```text
Use $fupan to review this project against its original goals. Use the original
plan, execution records and previous action list. Separate confirmed causes
from hypotheses and propose improvements with verifiable acceptance criteria.
```

In Claude Code, replace `Use $fupan` with `/fupan`.

Fictional example: a two-week pilot targeted 10 completed customer interviews and 3 paid trials. The records show 8 interviews and 1 paid trial; 2 other customers expressed interest but have not paid. Supply the original plan, interview log and payment records. The retrospective should not count expressions of interest as paid trials or infer root causes without evidence.

### Compatibility and limits

- Uses the Agent Skills structure, with English instructions followed by Chinese instructions. Responds in the user's requested language.
- Includes optional Codex UI metadata; no scripts, API keys or external service dependencies are bundled.
- Installation guidance follows the official documentation linked below. Cross-product runtime testing has not been completed; identical behavior across models is not guaranteed.
- Installation does not grant historical memory, file access, background scheduling or authority to deploy, transact or send messages.

### Attribution and reuse

References, sharing and adaptation are welcome. Suggested attribution:

> EDGAR WANG. *Fupan — Evidence-based Retrospective*. Based on Lenovo's management philosophy; personally organized and adapted into an AI skill by the author. https://github.com/wanghbc/fupan-skill

The author's original instructions and accompanying documentation are released under the [MIT License](LICENSE). Retain the required copyright and permission notice when redistributing covered material. This license does not grant rights to Lenovo's trademarks or third-party material. When describing the intellectual background, distinguish Lenovo's management philosophy from the author's skill adaptation.

## 中文

### 来源与作者

**本项目基于联想的管理思想，由作者EDGAR WANG（[@wanghbc](https://github.com/wanghbc)）本人梳理并转化为 AI skill。欢迎引用、分享和改编。**

本项目是作者的独立整理，不是联想官方发布或背书的产品。上述说明用于交代作者的思想来源，不主张“复盘”这一通用方法由联想独家首创。技能中的具体指令为作者的整理表达，不作为联想内部手册的原文引用。

### 这个 skill 做什么

适用于项目、经营活动、个人行动和任务执行后的复盘。既分析失败，也检查成功中哪些来自可复制的方法，哪些依赖环境或偶然因素。

| 步骤 | 核心问题 | 主要产出 |
|---|---|---|
| 1. 回顾目标 | 原来要达到什么目标？ | 原始目标、验收标准、期限、资源和约束 |
| 2. 核对结果 | 实际达成了什么？ | 截至明确时点的可核验结果、成本和完成状态 |
| 3. 分析偏差与根因 | 为什么超出或未达目标？ | 有证据的因果分析、替代解释与不确定性 |
| 4. 制定改进计划 | 接下来如何改善？ | 具体措施、责任人、期限、验收标准和复查条件 |

核心要求：不事后改写目标，不把活动数量当成成果，不把推测当成根因，不以“加强管理”等口号代替行动，措施完成后还要检查效果。

### 安装与调用

安装单元为 **`skills/fupan/` 文件夹**，保持文件夹名称为 `fupan`。

- **本地 Codex**：如有 `$skill-installer`，可直接说“请使用 $skill-installer 安装 GitHub 仓库 wanghbc/fupan-skill 中的 skills/fupan”。也可复制到用户目录的 `~/.agents/skills/fupan/` 或项目的 `.agents/skills/fupan/`，随后用 `$fupan` 调用。
- **本地 Claude Code**：复制到 `~/.claude/skills/fupan/` 或项目的 `.claude/skills/fupan/`，随后用 `/fupan` 调用。
- **其他 AI 工具**：支持 Agent Skills 的，按其官方方式安装；不支持的，可以将 `SKILL.md` 作为本次任务指令提供。读取一次不等于永久安装。

`~` 表示用户主目录，Windows 用户应使用自己的用户文件夹。已有同名 skill 时，先对比或备份。安装后未显示，可重启会话并核对所用版本的技能目录。托管的 ChatGPT/Work 环境可能需要插件等专用分发方式。

调用示例：

```text
请使用复盘 skill，按原始目标、实际结果、正负偏差及根因、改进计划
四步复盘这个项目。优先使用已提供的计划、执行记录和上次改进清单，
标明事实与推断，为每项措施提出可核验的验收标准。
```

虚构示例：两周试点原定完成 10 次客户访谈、获得 3 个付费试用；实际完成 8 次访谈、1 个付费试用，另有 2 位客户表达兴趣但尚未付款。提供原计划、访谈记录和收款记录后进行复盘，不能把意向算作付费，也不能在缺乏证据时认定根因。

### 兼容性与边界

- 采用 Agent Skills 的基本结构，正文英文在前、中文在后；输出使用用户指定的语言。
- 附带 Codex 界面配置，不包含执行脚本、密钥或外部服务依赖。
- 安装说明依据下列官方文档整理；本版本尚未完成跨产品运行验证，不宣称所有模型效果相同。
- 安装不会自动带来历史记忆、文件访问权限、后台定时运行或对外执行授权。复盘仍需要可靠的事实材料。

### 引用与许可

欢迎引用，推荐署名方式：

> EDGAR WANG：《Fupan — Evidence-based Retrospective（复盘）》。基于联想的管理思想，由作者本人梳理成 AI skill。https://github.com/wanghbc/fupan-skill

作者原创的技能指令和配套文档采用 [MIT License](LICENSE)，转载或分发相关内容时须保留许可证要求的版权及许可声明。许可证不授予联想商标或第三方材料的权利。介绍思想来源时，请区分联想的管理思想与作者对 skill 的整理贡献。

## Technical references / 技术参考

- [Agent Skills specification](https://agentskills.io/specification)
- [OpenAI: Build skills](https://learn.chatgpt.com/docs/build-skills)
- [Claude Code: Extend Claude with skills](https://code.claude.com/docs/en/skills)

Version / 版本: **0.1.0** · 2026-10-04
