# 来源获取与完整性门禁

## 1. 锁定论文与版本

从用户提供的 DOI、PMID、题名、链接或文件提取身份，交叉核验：

- 完整题名、作者、期刊/平台、年份；
- DOI、PMID、PMCID、arXiv/bioRxiv/medRxiv 等标识；
- 期刊版、accepted manuscript 和预印本之间的版本链；
- 当前版本、勘误、撤稿、Expression of Concern 或重大更新。

精读时以用户指定版本为准；未指定时优先已同行评审的最新正式版本，同时记录预印本与正式版差异线索。

## 2. 正文检索顺序

只使用合法公开或用户授权提供的来源。按可用性检查：

1. 用户上传的 PDF/附件。
2. 出版社官方开放全文或直接 PDF。
3. PubMed Central、Europe PMC 或论文官方预印本。
4. 机构知识库、作者接受稿或合法公共存档。
5. Crossref/PubMed LinkOut/开放获取发现服务提供的官方入口，再回到实际来源核验。

搜索时同时尝试 DOI、精确题名和第一作者组合。不得使用盗版站点、绕过付费墙，或把摘要页、图形摘要、网页片段当成正文。

“可用正文”必须包含研究的完整方法/结果叙述和主图图注。公开 HTML 可以满足正文门禁，但仍应继续寻找直接 PDF；若最终没有 PDF，报告末尾只能给全文 HTML 入口并明确“未发现直接 PDF 下载”。

## 3. 正文不可得时的唯一允许输出

响应开头直接写：

`缺少来源：目前未找到该论文可合法公开访问的完整正文。`

随后只提供：

- 已确认的论文身份和版本；
- 已检查的官方/公共来源及结果；
- 当前能获得的内容（例如仅摘要），明确其不足；
- 清晰请求：请上传主文 PDF；若有 Supplementary/Extended/Source Data，也请一并上传。

此时停止。不得先给摘要式“精读”、逐图猜测或结论扩写。用户上传正文后，从材料清单步骤继续。

## 4. 材料清单

正文门禁通过后，逐项记录状态和来源：

- 主文 PDF 或完整 HTML；
- 主图高分辨率文件与完整图注；
- Supplementary Information/Methods/Notes；
- 每个 Supplementary Figure、Table、Dataset、Video 或其他附件；
- Extended Data 与 Source Data；
- 数据可用性声明中的 accession 和仓库；
- Code availability 声明、官方 GitHub/GitLab、Zenodo release 或软件包；
- 关键协议、模型权重、环境文件或在线浏览器。

状态统一标为：`已获得并审阅`、`存在但无法获得`、`论文未提供/未声明`、`链接失效`、`与论文身份不符`。

如果论文明确引用了无法获得的补充材料，立即告诉用户缺少的具体文件。它可能影响图或结论解释时，暂停并请求上传；只有用户明确接受非完整报告后才能继续。论文未发布代码不是来源门禁失败，但必须作为可重复性结果报告。

## 5. 查找补充材料、代码和数据

- 检查出版社页面的 Supplementary、Extended Data、Source Data、Peer Review File 和附件区域，不只看主 PDF。
- 检索正文中的 `Data availability`、`Code availability`、`GitHub`、`GitLab`、`Zenodo`、`OSF`、accession 和 URL。
- 代码仓库需核对题名、作者/实验室、论文 DOI、release/tag 或 README 引用，避免审错同名项目。
- 数据仓库需验证 accession 是否存在、公开、版本匹配，并区分原始数据、处理后数据和示例数据。
- 记录下载/访问时间；动态仓库记录审阅的 commit、tag 或 release（可获得时）。

不要默认执行第三方代码。先静态审阅；执行不受信代码、大规模下载、GPU 任务或产生费用前，遵守当前环境授权并说明风险与资源需求。
