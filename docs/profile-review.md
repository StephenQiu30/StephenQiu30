# GitHub 主页研究与资料建议

核对日期：2026-10-08（Asia/Shanghai）。按用户指定的 followers 从高到低排序，阅读前十个账号的主页、Bio、置顶展示与可用的个人 README。本轮采用纯 Markdown，移除前两版 SVG，不再使用 beautify-github-readme 的视觉工作流。

## 榜单与一手来源

以 GitHub Search API `search/users?q=type:user+followers:>10000&sort=followers&order=desc&per_page=10` 返回的顺序为准；与 [ghrank 全球榜](https://ghrank.com/) 的前十名交叉核对。排序依据为 followers，不是贡献数、项目 Stars 或 README 设计评分。下面 follower 数来自本次 GitHub API 查询快照，后续会变化。

| 次序 | 账号 | Followers | 实际主页写法 |
| --- | --- | ---: | --- |
| 1 | [torvalds](https://github.com/torvalds) | 326,657 | 未展示个人 README；依靠置顶仓库和原生活动。 |
| 2 | [karpathy](https://github.com/karpathy) | 224,898 | 个人 README 只有一句话表达兴趣；置顶项目承担展示。 |
| 3 | [claude](https://github.com/claude) | 187,526 | 没有公开仓库或个人 README，主要提供外部链接。 |
| 4 | [gustavoguanabara](https://github.com/gustavoguanabara) | 116,514 | Bio 直接说明教师身份与受众，配合课程链接和仓库。 |
| 5 | [yyx990803](https://github.com/yyx990803) | 111,669 | Bio 写具体作品与作者身份，并附一句个人兴趣；无个人 README。 |
| 6 | [gaearon](https://github.com/gaearon) | 93,887 | 极简个人资料、个人网站与置顶项目；无个人 README。 |
| 7 | [ruanyf](https://github.com/ruanyf) | 87,847 | 简短资料与置顶教程、周刊；无个人 README。 |
| 8 | [peng-zhihui](https://github.com/peng-zhihui) | 87,479 | 短 Bio、状态与作品仓库；无个人 README。 |
| 9 | [sindresorhus](https://github.com/sindresorhus) | 84,584 | 复古 GIF 与个人兴趣，正文只给近期 App、博客等少量入口。 |
| 10 | [bradtraversy](https://github.com/bradtraversy) | 76,632 | Bio 写全栈开发与讲师身份、课程链接；无个人 README。 |

前十个账号中，八个没有展示个人 README，Karpathy 的 README 只有一句话。Sindre 是明显不同的例子：复古 GIF 风格，但内容依然很短。不能由榜单推导某种样式会增加关注者；这次借鉴的是清晰身份、具体作品和直接链接的阅读方式，不据此追求最短正文。

补充阅读了 [Peter Steinberger](https://github.com/steipete)，不计入前十名。他用一句身份介绍、项目入口和较长的分类目录展示很多作品；与本账号更相关的是用分类目录和明确入口组织多个项目，而非照搬其数量、经历或品牌。用户指出上一版过度精简后，本轮恢复项目层次与技术说明。

## 本次 README

- 恢复旧版的身份行、分组项目、技术栈与联系区，继续使用纯 Markdown，不恢复 SVG、徽章或卡片模板。
- 开头建立 Stephen Qiu、GitHub 账号、AI Application Engineer、Full-stack Developer 与 Shanghai 的关系，补充中文背景及对来源、任务、数据和结果交付的关注。
- 用“能检查的检索”“有依据的 AI 结果”“模型之外的软件”解释工程方向，每项都可关联到实际项目。
- 近期项目、检索与开发工具、其他开发中项目分组展示；六个项目各自说明用途、实现特点和相关仓库入口，重点项目增加技术选型。
- RAG、LLM、RRF 首次出现时使用英文全称，不添加关键词堆砌或重复身份的 FAQ。
- 展示名统一为“English · 中文”，保留仓库地址；客户端入口和章节也采用英文在前的顺序。
- 帧取保留公开预览入口；知微见澜、浮光、于是描述当前边界，不将规划、mock 或局部实现写成已经完成的产品能力。

## 项目展示名称

| 展示名称 | 依据 |
| --- | --- |
| Framefetch · 帧取 | 当前 Server README 与客户端仓库的产品名称。 |
| Ripplesight · 知微见澜 | 当前默认分支品牌组件 `frontend/src/components/brand/brand-lockup.tsx:63` 和登录品牌页 `frontend/src/app/login/components/login-brand-story.tsx:25`；这次已通过 GitHub API 核对，不只读取根 README。 |
| Algorithm · 算法课堂 | 英文沿用 Algorithm；中文为主页的描述性展示名，对应排序算法可视化课堂与 RAG 教学，不改仓库品牌或标识。 |
| Code Ark · 代码方舟 | 当前仓库 README 的正式名称。 |
| Lanverse · 浮光 | 英文沿用已有仓库名 Lanverse，中文采用当前产品名浮光；删除先前的拼音展示名。 |
| Then · 于是 | 沿用当前 Then / 于是项目名称。 |

Ripplesight 品牌名称依据：[品牌组件](https://github.com/StephenQiu30/Ripplesight/blob/main/frontend/src/components/brand/brand-lockup.tsx#L63)、[登录页](https://github.com/StephenQiu30/Ripplesight/blob/main/frontend/src/app/login/components/login-brand-story.tsx#L25)。

## SEO / GEO 内容处理

补充身份、真实工程方向、术语全称、中英文名称及直接的仓库链接，使读者和检索系统能更准确地理解作者、项目与能力之间的关系。以上属于内容清晰度和基础搜索可发现性优化，不代表已测得排名或 AI 引用增长。

参考 [Google 的 AI 搜索优化指南](https://developers.google.com/search/docs/fundamentals/ai-optimization-guide) 与 [AI features and your website](https://developers.google.com/search/docs/appearance/ai-features)：重视有依据、对读者有用的文字与链接；没有固定的“AI 专用写法”或保证收录的方法。本仓库没有独立站点的搜索流量数据，效果需要发布后观察。

## 可直接使用的资料字段

| 字段 | 建议值 |
| --- | --- |
| Name | Stephen Qiu |
| Bio | AI Application Engineer & Full-stack Developer \| RAG, LLM applications, hybrid search & self-hosted tools \| Shanghai |
| Location | Shanghai, China |
| Profile repository description | Stephen Qiu — AI Application Engineer & Full-stack Developer. RAG, LLM applications and self-hosted tools. |

Bio 为 116 个字符。Website 目前为空，没有发现应添加的独立个人网站，保留为空。邮箱沿用公开 README 的 `Popcornqhd@gmail.com`。

## 置顶与仓库描述

已有六个置顶仓库，建议排列为 `framefetch-server` → `Ripplesight` → `algorithm-cloud` → `code-ark` → `lanverse` → `then-server`。

下面两个仓库的元信息与本次读取的默认分支 README 不一致，可采用以下文案：

| 仓库 | 建议描述 |
| --- | --- |
| lanverse | Lanverse · 浮光：项目、画布、镜头与故事板创作工作台。当前页面使用 mock 数据，真实业务接入进行中。 |
| then-server | Then · 于是：衣橱与穿搭规划的 Go 服务端及产品文档。SwiftUI 客户端开发中，云接入与生成链路尚未完成。 |

## 项目内容依据

本次项目描述沿用此前对各仓库默认分支 README 的核对：

- [Framefetch · 帧取](https://github.com/StephenQiu30/framefetch-server/blob/main/README.md)：自托管视频与剧本工作台；另有 Electron、Flutter 仓库。没有承诺全部平台下载或客户端安装已经验收。
- [Ripplesight · 知微见澜](https://github.com/StephenQiu30/Ripplesight/blob/main/README.md)：个人非商业公开资讯阅读与关键词监控，不承诺全平台覆盖。
- [Algorithm · 算法课堂](https://github.com/StephenQiu30/algorithm-cloud/blob/main/README.md)：排序算法教学 RAG、向量检索、BM25 与 RRF。
- [Code Ark · 代码方舟](https://github.com/StephenQiu30/code-ark/blob/main/README.md)：本地开发 Compose 配置，不使用容易过期的数量。
- [Lanverse · 浮光](https://github.com/StephenQiu30/lanverse/blob/main/README.md)：当前前端使用 mock 数据，真实业务尚在接入。
- [Then · 于是](https://github.com/StephenQiu30/then-server/blob/main/README.md)：衣橱与穿搭方向，App 云接入与生成链路未完成。

## 验证与范围

本地 GitHub 风格预览检查浅色、深色及窄屏阅读。链接继续使用已核对的公开仓库地址，检查 README 不含图像引用与旧项目链接；`git diff --check` 通过。此处验证的是主页内容，不代表项目业务验收。

本轮修改 README、这份资料建议，删除本轮先前创建的两个 SVG。起始提交为 `0c70e210df218c17ac0e3143a08ff2d46ef19b9c`。修改范围仅限本仓库的 README 与这份资料建议；其他项目、`.idea`、GitHub Bio 和置顶设置不在本次变更范围。提交与推送目标为 `origin/main`。研究快照及预览位于仓库之外，避免把参考账号的 README 带进个人资料仓库。
