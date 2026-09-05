# 贡献流程 / Contribution Guidelines

> 本文件是 OverSeaDep 组织的默认贡献指南。当某个仓库没有自己的 `CONTRIBUTING.md` 时，以本文件为准。
> This is OverSeaDep's default contribution guide. It applies to repositories that do not ship their own `CONTRIBUTING.md`.

简体中文 | English

## 权限模型 / Access Model

- 组织内上游仓库默认基础权限为 `Read`；`Write` / `Maintain` / `Admin` 仅授予仓库所有者或明确授权者。
- 大多数私有上游仓库不开放直接推送，普通贡献者通过 **私有 Fork + Draft Pull Request** 参与。
- 所有进入 `main` 的改动由所有者审阅后合并。
- 若某仓库允许成员直接推送分支，仍建议走 Pull Request 以便留痕。

- Upstream repositories in the organization default to `Read` base permission; `Write` / `Maintain` / `Admin` is granted only to the repository owner or explicitly authorized members.
- Most private upstreams do not allow direct pushes. Contributors work through a **private Fork and a Draft Pull Request**.
- Every change reaching `main` is reviewed and merged by the owner.
- Even where members may push branches directly, a Pull Request is preferred so the change is recorded.

## 贡献者流程 / Contributor Workflow

1. 将目标仓库 Fork 到个人账号（Fork 保持私有、连接到上游 Fork Network）。
2. 在 Fork 中创建短期分支，命名示例：
   - `feat/<short-description>` — 新功能 / new feature；
   - `fix/<issue-or-short-description>` — 修复 / fix；
   - `case/<operator>/<case-id>`、`eval/<reviewer>/<case-id>/<round>` — 案例或评审类仓库 / case & review repositories；
   - `data/<dataset-or-region>` — 数据与研究类仓库 / data & research repositories。
3. 完成第一个有意义的提交后，**立即**打开 Draft Pull Request 指向上游 `main`，让工作过程对所有者可见。
4. 需要所有者协助修改时，可在 PR 中开启 *Allow edits from maintainers*（涉及 Actions 或 Secrets 的分支请先阅读 GitHub 的安全提示）。
5. 只提交本次任务范围内的改动；原始证据、历史记录只追加、不重写。
6. 保持 Fork 与上游 `main` 同步，在 Fork 中解决冲突并推送到同一 PR 分支。
7. 运行仓库要求的测试/校验（如 `pytest`、`pnpm test:all`），把结果写进 PR 描述。

1. Fork the target repository to your personal account (the Fork stays private and connected to the upstream Fork Network).
2. Create a short-lived branch in your Fork, e.g.:
   - `feat/<short-description>` — new feature;
   - `fix/<issue-or-short-description>` — fix;
   - `case/<operator>/<case-id>`, `eval/<reviewer>/<case-id>/<round>` — case & review repositories;
   - `data/<dataset-or-region>` — data & research repositories.
3. Open a **Draft Pull Request** against upstream `main` immediately after the first meaningful commit, so the work stays visible to the owner.
4. Enable *Allow edits from maintainers* when you want the owner to help revise the PR branch (read GitHub's security note first for branches that change Actions workflows or use secrets).
5. Include only in-scope changes. Raw evidence and history are append-only — never rewrite them.
6. Keep your Fork synchronized with upstream `main`, resolve conflicts in the Fork, and push the resolution to the same PR branch.
7. Run the repository's tests/checks (e.g. `pytest`, `pnpm test:all`) and record the result in the PR description.

## 所有者审阅流程 / Owner Review Workflow

1. 审阅 Draft PR 的提交历史、变更范围与证据来源。
2. 逐行评论或要求修改；开启 maintainer edits 时可直接修正 PR 分支。
3. 确认 PR 基于当前 `main`、不含无关改动。
4. 检查是否有凭据、会话数据或禁止提交的内容。
5. 运行自动化测试与对应的专项校验。
6. 数据/研究类改动核对「已确认 / 需核实 / 低置信度」标注与来源链接。
7. 所有者批准后合并，随后删除 PR 分支。

1. Review the Draft PR's full commit history, diff scope, and evidence provenance.
2. Comment on specific lines or request changes; commit corrections directly to the PR branch when maintainer edits are enabled.
3. Confirm the PR is based on current `main` and contains no unrelated changes.
4. Scan for credentials, session data, and prohibited secrets.
5. Run automated tests and case-specific validation.
6. For data/research changes, verify the confirmed / needs-verification / low-confidence tags and their source links.
7. Merge into `main` only after owner approval; delete the PR branch afterward.

## 硬性边界 / Required Boundaries

- **不提交任何敏感信息**：密码、令牌、Cookie、私钥、浏览器配置、会话存储、客户个人信息。Never commit passwords, tokens, cookies, private keys, browser profiles, session storage, or customer personal information.
- **证据纪律**：预期、假设、计划不能写成历史事实；单一案例不能自动升级为全局规则。Expectations, hypotheses, and plans must never be presented as facts; a single case does not automatically become a global rule.
- **AI 生成内容**：AI 辅助产出需保留操作留痕与评审记录；不得未经核验直接提交模型输出。AI-assisted output keeps an operation trace and review record; never commit model output without verification.
- **来源可追溯**：可发布的数字必须关联来源与核验日期，无法核验的营销描述或无来源数字不进入研究数据。Publishable numbers must link to sources and a verification date; unverifiable marketing claims and sourceless figures do not enter research data.
- **安全漏洞**：不要在 Issue/PR 中公开描述可利用的安全漏洞，按 `SECURITY.md` 的渠道报告。Do not describe exploitable vulnerabilities in Issues/PRs — report them through the channels in `SECURITY.md`.
