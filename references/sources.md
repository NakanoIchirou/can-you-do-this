# 来源核验与集成边界

核验日期：2026-10-15。四份 GitHub 原文件和仓库根许可证均已实际下载并阅读。它们是本 Skill 的方法参考，没有安装或调用其原始工作流。当前会话技能目录及检查的用户技能目录未发现四个同名入口；这不排除其他未知目录有副本。

|Skill|固定版本原文件|许可证|借鉴点与原版调用障碍|
|---|---|---|---|
|create-existing-solutions|[tomzx/agents](https://github.com/tomzx/agents/blob/698f806de04d92574121473898aba72223789efb/skills/create-existing-solutions/SKILL.md)|根 MIT|先调查再决定采用/扩展/自研。原版依赖 SDLC 约定和模板，并要求后续审查 Agent；本项目不接入该流水线。|
|build-buy-partner|[event4u-app/agent-config](https://github.com/event4u-app/agent-config/blob/a139cd6bf273499c65695b38ac0843939a17e508/src/skills/build-buy-partner/SKILL.md)|根 MIT|计入集成、维护和机会成本。原版包含自定义 frontmatter、上下文体系和 adr-create 依赖；不直接复制为 Codex 入口。|
|ai-stage-gate|[ML-SystemDesign/MLSystemDesign](https://github.com/ML-SystemDesign/MLSystemDesign/blob/8dd0d88852fe7445e9d2627c59124f0f161040c1/skills/ai-stage-gate/SKILL.md)|根 MIT|下一阶段投资必须有证据，关键未知不能平均掉。原版依赖多份 references；本包未下载完整依赖，不声称可原样运行。|
|premortem|[matteotitta/genesys-skills](https://github.com/matteotitta/genesys-skills/blob/2f397d346ff6719aacfd64e9ad4b2c6e6c0214df/skills/meta/orchestration/premortem/SKILL.md)|根 MIT|预先说清失败方式和缓解。原版依赖 Claude hook/约定及 premium references，且 frontmatter 存在可疑层级；未经移植验证不能称可调用。|

同名 Skill 存在多个仓库。以上是本轮明确选定的实现，不宣称它们就是历史对话中作者原本指的版本。event4u 仓库另含其他组件许可证，本次参考的是上述路径及根 MIT，不推广为全仓所有文件都是 MIT。

本包采用自包含中文流程，不分发原始 Skill 正文。保留 [THIRD-PARTY-NOTICES.txt](../THIRD-PARTY-NOTICES.txt) 中四份根许可证文本。将来需要原版集成时，应下载固定版本完整相关目录、检查相对资源和执行依赖、验证格式，并在隔离的小任务上测试；MIT 不等于自动兼容。

## 本轮一次 find-skills 发现

已读取本地 find-skills 说明、查看 skills.sh 目录；当前命令路径未找到 npx，因此使用网站搜索替代 CLI，没有安装依赖。一次查询：`site:skills.sh requirements discovery feasibility systems engineering`。

候选 [github/awesome-copilot 的 prd](https://www.skills.sh/github/awesome-copilot/prd)：目录当时显示约 23.8K 安装、40.0K 仓库星标（第三方统计，非质量保证）。已打开 [GitHub 原文件](https://raw.githubusercontent.com/github/awesome-copilot/main/skills/prd/SKILL.md)，确认其软件需求和澄清流程相关。未核验该候选完整许可证/依赖，因此不安装、不复制、不宣称可直接集成。它不能完整替代本 Skill 的跨领域质询与资源判断。

## 产品方案证据

- [DaVinci Resolve 官方产品页](https://www.blackmagicdesign.com/products/davinciresolve)：提供免费版，Studio 页面标价 US$295；这是页面价格快照，不含地区税费核验。可用于剪辑和后期，不自动提供合格的角色动画。未安装或实测。
- [FFmpeg 官方说明](https://ffmpeg.org/about.html)及[许可证](https://ffmpeg.org/legal.html)：可处理编码、滤镜、封装与播放；主要 LGPL 2.1+，启用部分组件会转为 GPL。适合已有资产处理，不能据此承诺动作设计。未在本轮制作视频。
- [Google 官方资料工具说明](https://support.google.com/gemininotebook/answer/16164461)：本次页面标题为 Gemini Notebook，原 NotebookLM 帮助入口有跳转；支持来源导入、带引用问答和学习材料。用户账号地区、额度、价格、具体导出能力未核验，不以文档可访问推断账号可用。
- [Quarto Books](https://quarto.org/docs/books/)：文档展示可编辑书籍工程及 PDF 输出。[Quarto COPYRIGHT](https://raw.githubusercontent.com/quarto-dev/quarto-cli/main/COPYRIGHT)为许可证核对入口；发行包含第三方组件，实际集成需核对所用版本。能解决出版结构，不解决教材内容正确性。未安装或渲染。
- [OpenAI 官方 Skill 文档](https://learn.chatgpt.com/docs/build-skills)：SKILL.md 必需 name、description；项目可放 `.agents/skills`。本地文件存在不证明已经完成账号同步或聊天界面自动发现。

两次 Blender 官方页面读取失败，未拿失败页面支持能力推荐。全部产品只做选型证据，不作为本次实际制作成功的证明。
