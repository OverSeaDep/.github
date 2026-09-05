# 安全策略 / Security Policy

简体中文 | English

OverSeaDep 的仓库存放跨境业务运营、市场研究、客户数据与内部工具相关内容，安全边界同时包含「软件安全」与「信息保密」两个层面。

OverSeaDep repositories hold cross-border business operations, market research, customer data, and internal tooling. Our security boundary covers both *software security* and *information confidentiality*.

## 报告漏洞 / Reporting a Vulnerability

- **公开仓库**：优先使用 GitHub 的 Private vulnerability reporting（仓库 → Settings → Security）。如仓库未开启该功能，请通过 GitHub 私信直接联系仓库所有者，**不要**在公开 Issue/PR 中描述可利用漏洞。
- **私有仓库**：直接私信联系仓库所有者或组织管理员；信息按需授权，不向无关人员转发。
- 报告时请说明：受影响仓库与文件、漏洞类型、复现步骤、影响范围。感谢信/致谢默认匿名，除非报告者明确希望具名。

- **Public repositories**: prefer GitHub's Private vulnerability reporting (Repository → Settings → Security). If it is disabled, contact the repository owner privately via GitHub — **never** describe an exploitable vulnerability in a public Issue/PR.
- **Private repositories**: contact the repository owner or an organization admin privately; access is granted on a need-to-know basis.
- When reporting, include: affected repository and file, vulnerability type, reproduction steps, and impact. Acknowledgments are anonymous by default unless the reporter asks to be named.

## 禁止入库的敏感内容 / Prohibited Secrets

下列内容**不得**进入任何 OverSeaDep 仓库（含提交历史、Issue、附件）：

- 密码、访问令牌、API Key、私钥；
- Cookie、浏览器配置/Profile、会话存储与认证头；
- 客户个人信息、学生/联系人隐私数据；
- 未公开的完整案例证据、可识别个人的内部记录。

The following must **never** enter any OverSeaDep repository (including commit history, Issues, and attachments):

- passwords, access tokens, API keys, private keys;
- cookies, browser profiles, session storage, authentication headers;
- customer personal information and private records of identifiable individuals;
- unpublished full case evidence or internal records that identify individuals.

## 发现敏感内容后的处理 / If a Secret Is Discovered

1. 立即停止传播并收回相关产物的访问；
2. 轮换/吊销该凭据；
3. 从当前文件与 Git 历史中清除（历史清理按仓库发布流程单独审批执行）；
4. 记录事件（不复制敏感值本身）；
5. 推送前核验替换后的历史，确认无残留。

1. Stop publication and revoke access to the affected artifact immediately;
2. rotate or revoke the credential;
3. remove it from current files and Git history (history rewriting is executed separately under the repository's release process);
4. record the incident without reproducing the secret;
5. verify the replacement history before pushing.

## 数据与证据保密 / Data & Evidence Confidentiality

- 客户数据、市场研究与未公开证据仅对授权成员可见，按需授予、不再需要时移除。
- 移除 GitHub 访问权限不能删除成员本地已有克隆；组织成员管理须谨慎。
- 公开发布研究内容前，先完成脱敏与事实核验；本仓库不约束各仓库各自发布的 CC BY 等许可条款。

- Customer data, market research, and unpublished evidence are visible only to authorized members — granted on a need-to-know basis and revoked when no longer needed.
- Removing GitHub access does not erase local clones a member already made; membership must be managed carefully.
- Before publishing research publicly, sanitize and verify the facts first; individual repositories keep their own licensing terms (e.g. CC BY) outside this policy.
