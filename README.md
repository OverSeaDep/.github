# OverSeaDep / .github

这是 OverSeaDep 组织的 GitHub 默认仓库（organization defaults）。GitHub 会把这里的公共内容作为组织的统一入口，并把缺失的社区健康文件、Issue/PR 模板与可复用工作流应用到本组织「没有自带对应文件」的仓库（公开与私有仓库都适用）。

This is OverSeaDep's organization defaults repository. GitHub uses it as the organization's unified entry point, and applies missing community health files, Issue/PR templates, and reusable workflows to repositories owned by the organization **that do not define their own** (for both public and private repositories).

> 优先级：具体仓库自己的文件 > 本仓库的默认文件。
> Precedence: a repository's own files win over these defaults.

## 内容 / Contents

| 路径 / Path | 用途 / Purpose |
|---|---|
| `profile/README.md` | 组织主页展示的内容 / Org profile shown on the organization's Overview page |
| `CONTRIBUTING.md` | 默认贡献流程（Fork + PR、证据与验收边界）/ Default contribution workflow (Fork + PR, evidence & acceptance boundaries) |
| `SECURITY.md` | 默认安全策略与漏洞报告渠道 / Default security policy and vulnerability reporting |
| `SUPPORT.md` | 默认支持渠道 / Default support channels |
| `CODE_OF_CONDUCT.md` | 默认行为准则 / Default code of conduct |
| `.github/ISSUE_TEMPLATE/` | 默认 Issue 表单模板（Bug、功能建议、数据纠错）/ Default issue forms (bug, feature, data correction) |
| `.github/PULL_REQUEST_TEMPLATE.md` | 默认 Pull Request 模板 / Default pull request template |
| `workflow-templates/` | 新建仓库时可选的 GitHub Actions 起步模板（Node/pnpm、Python/pytest）/ Reusable Actions starters for new repositories (Node/pnpm, Python/pytest) |

## 仓库约定 / Organization Conventions

- **文档语言 / Documentation language**: 简体中文为主，重要仓库提供英文版（`README-en.md`）。本仓库以中英对照组织。Simplified Chinese first, English versions for important repositories (`README-en.md`). This repository is bilingual.
- **权限模型 / Access model**: 上游仓库默认 `Read` 基础权限、所有者维护；贡献通过私有 Fork + Draft Pull Request 进行，由所有者审阅合并。Upstream repositories default to `Read` base permission with owner-only maintenance; contributions go through private Fork + Draft Pull Request, reviewed and merged by the owner.
- **证据与留痕 / Evidence**: 研究数据区分「已确认 / 需核实 / 低置信度」并关联来源；事实与假设分开表述；原始证据只追加、不覆盖。Research data distinguishes confirmed / needs-verification / low-confidence with linked sources; facts and assumptions are separated; raw evidence is append-only.
- **安全红线 / Security**: 任何仓库不得提交密码、令牌、Cookie、浏览器配置、会话数据或客户个人信息。No repository may contain passwords, tokens, cookies, browser profiles, session data, or customer personal information.
- **AI 协作 / AI collaboration**: AI 辅助产出应有操作留痕与评审记录，不得把模型输出当作既定事实提交。AI-assisted output keeps an operation trace and review record; model output is never committed as established fact.

## 如何修改本仓库 / How to Modify This Repository

本仓库同样采用「提交 PR、由所有者合并」的方式。改动默认模板或社区健康文件会影响组织内所有未自备文件的仓库，请在 PR 中说明影响范围。

This repository follows the same "open a PR, owner merges" flow. Changes to default templates or community health files affect every org repository without its own files — describe the blast radius in the PR.

## 参考 / References

- [About your organization's profile (GitHub Docs)](https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/customizing-your-organizations-profile)
- [Creating a default community health file (GitHub Docs)](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)
- [Creating workflow templates for your organization (GitHub Docs)](https://docs.github.com/en/actions/sharing-automations/creating-workflow-templates-for-your-organization)
