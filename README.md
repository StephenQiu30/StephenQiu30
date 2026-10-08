# Hi, I'm Stephen Qiu 👋

📍 **Shanghai, China** · 🤖 **AI Application Engineer** · 🛠️ **Full-stack Developer**

I'm **Stephen Qiu ([@StephenQiu30](https://github.com/StephenQiu30))**. I build **Retrieval-Augmented Generation (RAG)** systems, **large language model (LLM) applications** and self-hosted software. My work spans Java backends, retrieval pipelines, Python workers and the web, desktop and mobile interfaces around them.

我在上海做 AI 应用与全栈开发，主要使用 Java、Go、Python 和 TypeScript。这里记录了我围绕算法教学、视频与剧本分析、公开资讯阅读，以及日常创作和穿搭做的开源项目。

对我来说，接上模型只是开始。我更关心回答引用了什么、任务失败后怎么继续、数据保存在哪里，以及用户能不能方便地核对和带走结果。这些问题贯穿了下面的检索、工作流和自托管项目。

## Focus · 工程关注

- **Retrieval that can be inspected · 能检查的检索** — 从文档解析、分片和索引，到向量与关键词混合召回、融合排序和流式问答；让知识库和召回结果有可检查的入口。
- **AI results with sources · 有依据的 AI 结果** — 把分析与原始文本、视频帧和时间位置联系起来，方便阅读、复核和导出。
- **The software around the model · 模型之外的软件** — API、后台任务、数据存储、多端交互和部署文档，都是我持续投入的部分。

## Currently building · 近期在做

### 🎬 [Framefetch · 帧取](https://github.com/StephenQiu30/framefetch-server)

**A self-hosted workspace for video, screenplay and AI analysis.**

把有权使用的视频和剧本文档放进同一个工作站：导入素材、查看后台任务、阅读分析，再把报告导出为 Markdown / DOCX。适合研究成片、对照剧本，或搭建自己的素材分析工具链。

- 视频分析关联抽样帧与源时间，文本分析关联原文单元与引用，方便回到素材核对结论。
- Web、Electron 和 Flutter 客户端连接同一服务；素材、任务与报告集中管理，导出复用已保存的结果。

`Python / FastAPI` · `Next.js / React` · `Temporal` · `RabbitMQ` · `PostgreSQL` · `MinIO`

[Server & Web · 服务端与网页](https://github.com/StephenQiu30/framefetch-server) · [Desktop · 桌面端](https://github.com/StephenQiu30/framefetch-electron) · [Mobile · 移动端](https://github.com/StephenQiu30/framefetch-app) · [Releases · 公开预览](https://github.com/StephenQiu30/framefetch-server/releases)

### 🌊 [Ripplesight · 知微见澜](https://github.com/StephenQiu30/Ripplesight)

**Public information reading and keyword monitoring, with traceable sources.**

围绕一个关键词，把公开资讯、来源材料、讨论和事件进展联系起来。它面向个人非商业使用，帮助阅读者从零散信息中了解发生了什么，并回到原始出处继续判断。

- 阅读有出处、经过去重的资讯与事件；配置关键词和来源，查看采集到的帖子、评论和任务状态。
- 继续推进来源接入、监控工作台和阅读体验；各来源、分析与告警的可用范围以仓库中的当前进度为准。

`Python / FastAPI` · `Next.js / TypeScript` · `PostgreSQL` · `Redis` · `Kafka`

[Repository · 项目仓库](https://github.com/StephenQiu30/Ripplesight) · [Workspace · 产品与工程文档](https://github.com/StephenQiu30/Ripplesight/tree/main/workspace/content)

## RAG & developer tools · 检索与开发工具

### 📚 [Algorithm · 算法课堂](https://github.com/StephenQiu30/algorithm-cloud)

**Sorting-algorithm education with Spring AI and Elasticsearch hybrid search.**

一个把算法可视化课堂与 RAG 问答结合起来的项目。如果你想看 Java / Spring AI 如何组织文档入库、混合检索和流式回答，可以从这里开始。

- 解析 Markdown、PDF、Word 教学材料，进行分片与索引；并行执行向量检索和 BM25，再用 **Reciprocal Rank Fusion (RRF)** 融合结果。
- 提供知识库、文档与召回分析入口，通过 SSE 输出问答；前端配合排序过程、代码和复杂度讲解。
- 后端采用 Spring Cloud Alibaba，包含网关、认证、搜索、文件、通知与异步任务等服务模块。

`Java` · `Spring Boot / Spring Cloud Alibaba` · `Spring AI` · `Elasticsearch` · `RabbitMQ`

[Backend · 微服务与 RAG](https://github.com/StephenQiu30/algorithm-cloud) · [Classroom · 可视化课堂](https://github.com/StephenQiu30/algorithm-next) · [Admin · 管理后台](https://github.com/StephenQiu30/algorithm-admin)

### 🐳 [Code Ark · 代码方舟](https://github.com/StephenQiu30/code-ark)

**Docker Compose configurations for everyday backend development.**

把搭建中间件的时间，留给写代码。按需选择数据库、缓存、消息队列、搜索、对象存储或监控服务，用于本地开发、接口联调和集成测试。

- 服务按目录组织，提供各自的 Compose 配置、启动条件、端口和数据位置说明。
- 覆盖 PostgreSQL、MySQL、Redis、Kafka、RabbitMQ、Temporal、Elasticsearch、MinIO、Prometheus / Grafana 等常用组件，也包含 RSSHub 与 SearXNG。

`Docker Compose` · `Local development` · `Middleware` · `Observability`

[Service catalog · 服务目录与使用说明](https://github.com/StephenQiu30/code-ark#服务目录)

## More in progress · 其他进行中的项目

### 🎭 [Lanverse · 浮光](https://github.com/StephenQiu30/lanverse)

**A creative workspace organized around projects, canvases, shots and storyboards.**

围绕项目、画布、镜头、故事板、设定与素材组织创作。当前在把新的页面设计、数据结构和接口需求对齐；前端使用 mock 数据，真实业务接入进行中。

### 👗 [Then · 于是](https://github.com/StephenQiu30/then-server)

**Wardrobe organization and outfit planning, with a Go backend and SwiftUI client.**

从数字衣橱、穿搭计划到实际穿着与私人日记，探索怎样把每天的选衣和记录放在一起。Go 服务端已包含相应的数据与 API；SwiftUI 客户端的云接入、生成与主动同步仍在开发。

[Backend · Go 服务端](https://github.com/StephenQiu30/then-server) · [iOS · SwiftUI 客户端](https://github.com/StephenQiu30/then-app)

## Tech I use · 常用技术

- **Backend · 后端** — Java / Spring Boot / Spring Cloud Alibaba / Spring AI · Go · Python / FastAPI
- **Web & clients · 网页与客户端** — TypeScript / React / Next.js · Flutter · SwiftUI · Electron
- **Data & search · 数据与检索** — PostgreSQL · MySQL · Redis · Elasticsearch · Vector search / BM25 / RRF
- **Workflows & infrastructure · 工作流与基础设施** — Temporal · RabbitMQ · Kafka · MinIO · Docker Compose

## Let's connect · 联系我

Happy to discuss **RAG, hybrid search, AI application development, Java backends and self-hosted software**. Questions, issues and pull requests are welcome.

欢迎交流检索效果、后台任务、多端体验和自托管实践。遇到具体问题，可以在对应仓库留下复现步骤或样例；产品想法和文档改进也欢迎一起讨论。

📧 [Popcornqhd@gmail.com](mailto:Popcornqhd@gmail.com) · [All repositories · 所有项目](https://github.com/StephenQiu30?tab=repositories)
