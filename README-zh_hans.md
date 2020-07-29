[繁體中文](./README-zh_hant.md)，[英文](./README.md)

# 欢迎

本仓库是关于产品、开发与社群规则的文档和讨论的主入口。这里也包含不属于其他仓库的issue，例如需要前后端耦合的新功能提案。也欢迎在 [Gitter](https://gitter.im/thematters/community) 中加入我们。

一些本仓库内的有用资源：

* [API简介](#服务器-API)
* [各仓库简介](#代码仓库)
* [架构示意图](#架构)
* [数据库文档](./doc)与[关系图](./doc/db/diagrams/summary/relationships.real.compact.svg)
* [社区约章](./CODE_OF_CONDUCT.md)
* [协作流程wiki](https://github.com/thematters/developer-resource/wiki)

# 服务器 API

Matters 使用 GraphQL 作为 API 接口，详情见[简介文章](https://matters.news/@robertu/%E7%A4%BE%E5%8D%80%E9%96%8B%E6%94%BE%E4%B8%80%E5%B0%8F%E6%AD%A5-matters-api-zdpuAyovU8xL9sYsV5rQfe35XhmN6okTVbnogCFH2J8cqAXCs)。开發者可以在 [Apollo Playground](https://server-test.matters.news/playground) 中查阅文档、进行调试。

# 架构

![Architecture diagram, rendered from [drawio file](./doc/architecture-diagram.drawio)](./doc/architecture-diagram.png "Architecture diagram showing simplified data flow.")

克隆当前仓库后，打开 `doc/db/index.html` 文件可查看 [SchemaSpy](http://schemaspy.org/) 数据库文档。

# 代码仓库

以下为 Matters Lab 代码仓库结构与分工。

## 后端
- [server](https://github.com/thematters/matters-server): Matters 服务器主仓库。使用 Typescript，基于 [Apollo Server](https://github.com/apollographql/apollo-server)建构 GraphQL API。
- [query cache](https://github.com/thematters/apollo-response-cache): 用于缓存控制与清理的 GraphQL directives 及 Apollo Server 插件。
- [image processing](https://github.com/thematters/serverless-file-post-processing): AWS lambda 函数，用于图片压缩与转码。
- [queue dashboard](https://github.com/thematters/matters-queue-dashboard): 对接 [Bee Queue](https://github.com/bee-queue/bee-queue) 与 [Bull](https://github.com/optimalbits/bull) 的图形介面，用于查看 Matters 服务器中的队列任务。

## 前端
- [web](https://github.com/thematters/matters-web): Matters 网页客户端主仓库。使用 Typescript，基于 [React](https://reactjs.org/)，[Nextjs](https://nextjs.org/) 与 [Apollo Client](https://github.com/apollographql/apollo-client)。
- [editor](https://github.com/thematters/matters-editor): matters.news 所见即所得编辑器，基于 [Quilljs](https://github.com/quilljs/quill)。
- [upload client](https://github.com/thematters/apollo-upload-client): GraphQL文件上传组件。Fork 自 [apollo-upload-client](https://github.com/jaydenseric/apollo-upload-client)，支持 persistence query。

## 通用
- [slugify](https://github.com/thematters/slugify): 支持 CJK charset 的 [slugify](https://github.com/simov/slugify)。
- [docker](https://github.com/thematters/matters-docker): Matters Lab 使用的 docker 镜像。
- [slack notification](https://github.com/thematters/matters-slacknoti): slack 通知服务 AWS lambda 函数，用于开發操作流程中的通知。

# 点对点客户端

Matters 在持续探索更好的点对点信息分發的机制和协议。以下是一些相关客户端。
* [Hypha Publication](https://github.com/hypha-publication): 实验性项目，对接 Matters 服务器的点对点客户端。
  * [Hypha Desktop](https://github.com/hypha-publication/hypha-desktop): 桌面版客户端，基于[Election.js](https://www.electronjs.org/) 与 [IPFS](https://ipfs.io/)
 。可以直接下载作爲IPFS浏览器使用。
  * [Hypha Extension](https://github.com/hypha-publication/hypha-extension): 浏览器插件客户端，基于 [js-ipfs](https://github.com/ipfs/js-ipfs) 与 [orbit-db](https://github.com/orbitdb/orbit-db)。可用于加密的点对点通信等功能。目前尚未完工。
* [Beaker Browser](https://github.com/beakerbrowser/beaker):    一个较爲成熟的点对点浏览器，支持 [`://dat` 协议](https://dat.foundation/)。目前有关于将 Matters 通过[unwalled.garden 协议](https://github.com/beakerbrowser/unwalled.garden)  与 [Hyperdrive](https://github.com/hypercore-protocol/hyperdrive) 适配到Beaker Browser的[讨论](https://github.com/beakerbrowser/unwalled.garden/issues/51)与实验。


# 社区项目

- [MatREQ](https://matters.news/@jugu/%E9%9D%9E%E5%AE%98%E6%96%B9-matters%E8%A8%B1%E9%A1%98%E6%B1%A0-zdpuAxEfdxG6MdBHnE7rEvCeAG6TPay6i8ychgiq2EoRRMv2s): 向 Matters 用户[请求特定主题的文章](https://mat.52tw.cc/)。
- [matters 消音器](https://matters.news/@deserve/%E4%BD%BF%E7%94%A8%E8%BF%99%E4%B8%AA%E6%B5%8F%E8%A7%88%E5%99%A8%E6%89%A9%E5%B1%95%E4%B8%80%E9%94%AE%E5%BC%80%E5%90%AFmatters%E7%9A%84%E5%85%A8%E7%AB%99%E5%B1%8F%E8%94%BD-%E6%8B%89%E9%BB%91-%E9%9D%99%E9%9F%B3%E5%8A%9F%E8%83%BD-zdpuAwGnxxMnyvaBJwCszuRrHjqprMohMPkXXWfYYKwEzvkrX): 浏览器插件，用于屏蔽特定用户，支持共享黑名单。有[Chrome](https://chrome.google.com/webstore/detail/matters-%E6%B6%88%E9%9F%B3%E5%99%A8/hpbebebpjajeiadiakgckpahmhkbkpoa) 与 [Firefox](https://addons.mozilla.org/zh-CN/firefox/addon/matters-%E6%B6%88%E9%9F%B3%E5%99%A8/) 两个版本，[代码开源](https://github.com/contributionls/matters-muter)。
- [matters2ipfs](https://matters.news/@deserve/matters%E6%96%87%E7%AB%A0%E7%8E%B0%E5%9C%A8%E5%8F%AF%E4%BB%A5%E4%B8%80%E9%94%AE%E5%9C%A8%E7%BA%BF%E8%BD%AC%E4%B8%BA%E5%A2%99%E5%86%85%E9%93%BE%E6%8E%A5%E4%BA%86-zdpuB1bvMnsAr4APk12FmdRxcqMaEsRo46vKE7p6Arvsg4YiF): 将 Matters 文章转为 ipfs 链接，可以在墙内打开，[代码开源](https://github.com/contributionls/matters2ipfs).
- [matters 个人网站](https://matters.news/@vibertthio/%E7%9C%9F%E6%AD%A3%E5%8E%BB%E4%B8%AD%E5%BF%83%E5%AA%92%E9%AB%94%E7%9A%84%E7%AC%AC%E4%B8%80%E6%AD%A5-%E5%81%9A%E4%B8%80%E5%80%8B-matters-%E7%9A%84%E7%AC%AC%E4%B8%89%E6%96%B9%E7%B6%B2%E7%AB%99-zdpuArgJXADPgWJ8TfvRWWStTvkYC1vqCTV6fHayisbrABkBp): 通过 matters.news 备份的个人网站，[代码开源](https://github.com/vibertthio/matters-third-party)。
