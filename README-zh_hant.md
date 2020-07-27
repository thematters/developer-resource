[简体中文](./README-zh_hans.md)，[英文](./README.md)

# 歡迎

本倉庫是關於產品、開发與社群規則的文檔和討論的主入口。這里也包含不屬於其他倉庫的issue，例如需要前後端耦合的新功能提案。

一些本倉庫內的有用資源：

* [API簡介](#服務器-API)
* [各倉庫簡介](#代碼倉庫)
* [架構示意圖](#架構)
* [數據庫文檔](./doc)與[關系圖](./doc/db/diagrams/summary/relationships.real.compact.svg)
* [社區約章](./CODE_OF_CONDUCT.md)
* [協作流程wiki](https://github.com/thematters/developer-resource/wiki)

# 服務器 API

Matters 使用 GraphQL 作為 API 接口，詳情見[簡介文章](https://matters.news/@robertu/%E7%A4%BE%E5%8D%80%E9%96%8B%E6%94%BE%E4%B8%80%E5%B0%8F%E6%AD%A5-matters-api-zdpuAyovU8xL9sYsV5rQfe35XhmN6okTVbnogCFH2J8cqAXCs)。開發者可以在 [Apollo Playground](https://server-test.matters.news/playground) 中查閱文檔、進行調試。

# 架構

![Architecture diagram, rendered from [drawio file](./doc/architecture-diagram.drawio)](./doc/architecture-diagram.png "Architecture diagram showing simplified data flow.")

克隆當前倉庫後，打開 `doc/db/index.html` 文件可查看 [SchemaSpy](http://schemaspy.org/) 數據庫文檔。

# 代碼倉庫
以下為 Matters Lab 代碼倉庫結構與分工。

## 後端
- [server](https://github.com/thematters/matters-server): Matters 服務器主倉庫。使用 Typescript，基於 [Apollo Server](https://github.com/apollographql/apollo-server)建構 GraphQL API。
- [query cache](https://github.com/thematters/apollo-response-cache): 用於緩存控制與清理的 GraphQL directives 及 Apollo Server 插件。
- [image processing](https://github.com/thematters/serverless-file-post-processing): AWS lambda 函數，用於圖片壓縮與轉碼。
- [queue dashboard](https://github.com/thematters/matters-queue-dashboard): 對接 [Bee Queue](https://github.com/bee-queue/bee-queue) 與 [Bull](https://github.com/optimalbits/bull) 的圖形介面，用於查看 Matters 服務器中的隊列任務。

## 前端
- [web](https://github.com/thematters/matters-web): Matters 網頁客戶端主倉庫。使用 Typescript，基於 [React](https://reactjs.org/)，[Nextjs](https://nextjs.org/) 與 [Apollo Client](https://github.com/apollographql/apollo-client)。
- [editor](https://github.com/thematters/matters-editor): matters.news 所見即所得編輯器，基於 [Quilljs](https://github.com/quilljs/quill)。
- [upload client](https://github.com/thematters/apollo-upload-client): GraphQL文件上傳組件。Fork 自 [apollo-upload-client](https://github.com/jaydenseric/apollo-upload-client)，支持 persistence query。

## 通用
- [slugify](https://github.com/thematters/slugify): 支持 CJK charset 的 [slugify](https://github.com/simov/slugify)。
- [docker](https://github.com/thematters/matters-docker): Matters Lab 使用的 docker 鏡像。
- [slack notification](https://github.com/thematters/matters-slacknoti): slack 通知服務 AWS lambda 函數，用於開發操作流程中的通知。

# 點對點客戶端

Matters 在持續探索更好的點對點信息分發的機制和協議。以下是一些相關客戶端。
* [Hypha Publication](https://github.com/hypha-publication): 實驗性項目，對接 Matters 服務器的點對點客戶端。
  * [Hypha Desktop](https://github.com/hypha-publication/hypha-desktop): 桌面版客戶端，基於[Election.js](https://www.electronjs.org/) 與 [IPFS](https://ipfs.io/)
 。可以直接下載作爲IPFS瀏覽器使用。
  * [Hypha Extension](https://github.com/hypha-publication/hypha-extension): 瀏覽器插件客戶端，基於 [js-ipfs](https://github.com/ipfs/js-ipfs) 與 [orbit-db](https://github.com/orbitdb/orbit-db)。可用於加密的點對點通信等功能。目前尚未完工。
* [Beaker Browser](https://github.com/beakerbrowser/beaker):    一個較爲成熟的點對點瀏覽器，支持 [`://dat` 協議](https://dat.foundation/)。目前有關於將 Matters 通過[unwalled.garden 協議](https://github.com/beakerbrowser/unwalled.garden)  與 [Hyperdrive](https://github.com/hypercore-protocol/hyperdrive) 適配到Beaker Browser的[討論](https://github.com/beakerbrowser/unwalled.garden/issues/51)與實驗。


# 社區項目

- [MatREQ](https://matters.news/@jugu/%E9%9D%9E%E5%AE%98%E6%96%B9-matters%E8%A8%B1%E9%A1%98%E6%B1%A0-zdpuAxEfdxG6MdBHnE7rEvCeAG6TPay6i8ychgiq2EoRRMv2s): 向 Matters 用戶[請求特定主題的文章](https://mat.52tw.cc/)。
- [matters 消音器](https://matters.news/@deserve/%E4%BD%BF%E7%94%A8%E8%BF%99%E4%B8%AA%E6%B5%8F%E8%A7%88%E5%99%A8%E6%89%A9%E5%B1%95%E4%B8%80%E9%94%AE%E5%BC%80%E5%90%AFmatters%E7%9A%84%E5%85%A8%E7%AB%99%E5%B1%8F%E8%94%BD-%E6%8B%89%E9%BB%91-%E9%9D%99%E9%9F%B3%E5%8A%9F%E8%83%BD-zdpuAwGnxxMnyvaBJwCszuRrHjqprMohMPkXXWfYYKwEzvkrX): 瀏覽器插件，用於屏蔽特定用戶，支持共享黑名單。有[Chrome](https://chrome.google.com/webstore/detail/matters-%E6%B6%88%E9%9F%B3%E5%99%A8/hpbebebpjajeiadiakgckpahmhkbkpoa) 與 [Firefox](https://addons.mozilla.org/zh-CN/firefox/addon/matters-%E6%B6%88%E9%9F%B3%E5%99%A8/) 兩個版本，[代碼開源](https://github.com/contributionls/matters-muter)。
- [matters2ipfs](https://matters.news/@deserve/matters%E6%96%87%E7%AB%A0%E7%8E%B0%E5%9C%A8%E5%8F%AF%E4%BB%A5%E4%B8%80%E9%94%AE%E5%9C%A8%E7%BA%BF%E8%BD%AC%E4%B8%BA%E5%A2%99%E5%86%85%E9%93%BE%E6%8E%A5%E4%BA%86-zdpuB1bvMnsAr4APk12FmdRxcqMaEsRo46vKE7p6Arvsg4YiF): 將 Matters 文章轉為 ipfs 鏈接，可以在墻內打開，[代碼開源](https://github.com/contributionls/matters2ipfs).
- [matters 個人網站](https://matters.news/@vibertthio/%E7%9C%9F%E6%AD%A3%E5%8E%BB%E4%B8%AD%E5%BF%83%E5%AA%92%E9%AB%94%E7%9A%84%E7%AC%AC%E4%B8%80%E6%AD%A5-%E5%81%9A%E4%B8%80%E5%80%8B-matters-%E7%9A%84%E7%AC%AC%E4%B8%89%E6%96%B9%E7%B6%B2%E7%AB%99-zdpuArgJXADPgWJ8TfvRWWStTvkYC1vqCTV6fHayisbrABkBp): 通過 matters.news 備份的個人網站，[代碼開源](https://github.com/vibertthio/matters-third-party)。
