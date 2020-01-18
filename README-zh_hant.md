其他语言：[简体中文](./README-zh_hans.md)，[英文](./README.md)

# Matters 服務器 API

Matters 使用 GraphQL 作為 API 接口，詳情見[Matters API 介紹](https://matters.news/@robertu/%E7%A4%BE%E5%8D%80%E9%96%8B%E6%94%BE%E4%B8%80%E5%B0%8F%E6%AD%A5-matters-api-zdpuAyovU8xL9sYsV5rQfe35XhmN6okTVbnogCFH2J8cqAXCs)。開發者可以[在此](https://server-test.matters.news/playground)查閱 schema、進行調試。

# 點對點客戶端

[Hypha publication](https://github.com/hypha-publication)項目提供與 Matters 服務器兼容的點對點客戶端。目前[瀏覽器插件](https://github.com/hypha-publication/hypha-extension)與[桌面版本](https://github.com/hypha-publication/hypha-desktop)均在開發之中，尚未投入使用。

# 社區項目

- [MatREQ](https://matters.news/@jugu/%E9%9D%9E%E5%AE%98%E6%96%B9-matters%E8%A8%B1%E9%A1%98%E6%B1%A0-zdpuAxEfdxG6MdBHnE7rEvCeAG6TPay6i8ychgiq2EoRRMv2s): 向 Matters 用戶[請求特定主題的文章](https://mat.52tw.cc/)。
- [matters 消音器](https://matters.news/@deserve/%E4%BD%BF%E7%94%A8%E8%BF%99%E4%B8%AA%E6%B5%8F%E8%A7%88%E5%99%A8%E6%89%A9%E5%B1%95%E4%B8%80%E9%94%AE%E5%BC%80%E5%90%AFmatters%E7%9A%84%E5%85%A8%E7%AB%99%E5%B1%8F%E8%94%BD-%E6%8B%89%E9%BB%91-%E9%9D%99%E9%9F%B3%E5%8A%9F%E8%83%BD-zdpuAwGnxxMnyvaBJwCszuRrHjqprMohMPkXXWfYYKwEzvkrX): 瀏覽器插件，用於屏蔽特定用戶，支持共享黑名單。有[Chrome](https://chrome.google.com/webstore/detail/matters-%E6%B6%88%E9%9F%B3%E5%99%A8/hpbebebpjajeiadiakgckpahmhkbkpoa) 與 [Firefox](https://addons.mozilla.org/zh-CN/firefox/addon/matters-%E6%B6%88%E9%9F%B3%E5%99%A8/) 兩個版本，[代碼開源](https://github.com/contributionls/matters-muter)。
- [matters2ipfs](https://matters.news/@deserve/matters%E6%96%87%E7%AB%A0%E7%8E%B0%E5%9C%A8%E5%8F%AF%E4%BB%A5%E4%B8%80%E9%94%AE%E5%9C%A8%E7%BA%BF%E8%BD%AC%E4%B8%BA%E5%A2%99%E5%86%85%E9%93%BE%E6%8E%A5%E4%BA%86-zdpuB1bvMnsAr4APk12FmdRxcqMaEsRo46vKE7p6Arvsg4YiF): 將 Matters 文章轉為 ipfs 鏈接，可以在墻內打開，[代碼開源](https://github.com/contributionls/matters2ipfs).
- [matters 個人網站](https://matters.news/@vibertthio/%E7%9C%9F%E6%AD%A3%E5%8E%BB%E4%B8%AD%E5%BF%83%E5%AA%92%E9%AB%94%E7%9A%84%E7%AC%AC%E4%B8%80%E6%AD%A5-%E5%81%9A%E4%B8%80%E5%80%8B-matters-%E7%9A%84%E7%AC%AC%E4%B8%89%E6%96%B9%E7%B6%B2%E7%AB%99-zdpuArgJXADPgWJ8TfvRWWStTvkYC1vqCTV6fHayisbrABkBp): 通過 matters.news 備份的個人網站，[代碼開源](https://github.com/vibertthio/matters-third-party)。

# Matters 開源項目

- [Matters 編輯器](https://github.com/thematters/matters-editor): matters.news 所見即所得編輯器，基於[Quill](https://github.com/quilljs/quill)。
- [slugify](https://github.com/thematters/slugify): 支持 CJK charset 的 slugify。
- [apollo-upload-client](https://github.com/thematters/apollo-upload-client): Fork 自 [apollo-upload-client](https://github.com/jaydenseric/apollo-upload-client)，支持 persistence query。
