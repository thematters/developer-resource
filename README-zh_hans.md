其他语言：[繁体中文](./README-zh_hant.md)，[英文](./README.md)

# Matters 服务器 API

Matters 使用 GraphQL 作为 API 接口，详情见[Matters API 介绍](https://matters.news/@robertu/%E7%A4%BE%E5%8D%80%E9%96%8B%E6%94%BE%E4%B8%80%E5%B0%8F%E6%AD%A5-matters-api-zdpuAyovU8xL9sYsV5rQfe35XhmN6okTVbnogCFH2J8cqAXCs)。开发者可以[在此](https://server-test.matters.news/playground)查阅 schema、进行调试。

# 点对点客户端

[Hypha publication](https://github.com/hypha-publication)项目提供与 Matters 服务器兼容的点对点客户端。目前[浏览器插件](https://github.com/hypha-publication/hypha-extension)与[桌面版本](https://github.com/hypha-publication/hypha-desktop)均在开发之中，尚未投入使用。

# 社区项目

- [MatREQ](https://matters.news/@jugu/%E9%9D%9E%E5%AE%98%E6%96%B9-matters%E8%A8%B1%E9%A1%98%E6%B1%A0-zdpuAxEfdxG6MdBHnE7rEvCeAG6TPay6i8ychgiq2EoRRMv2s): 向 Matters 用户[请求特定主题的文章](https://mat.52tw.cc/)。
- [matters 消音器](https://matters.news/@deserve/%E4%BD%BF%E7%94%A8%E8%BF%99%E4%B8%AA%E6%B5%8F%E8%A7%88%E5%99%A8%E6%89%A9%E5%B1%95%E4%B8%80%E9%94%AE%E5%BC%80%E5%90%AFmatters%E7%9A%84%E5%85%A8%E7%AB%99%E5%B1%8F%E8%94%BD-%E6%8B%89%E9%BB%91-%E9%9D%99%E9%9F%B3%E5%8A%9F%E8%83%BD-zdpuAwGnxxMnyvaBJwCszuRrHjqprMohMPkXXWfYYKwEzvkrX): 浏览器插件，用于屏蔽特定用户，支持共享黑名单。有[Chrome](https://chrome.google.com/webstore/detail/matters-%E6%B6%88%E9%9F%B3%E5%99%A8/hpbebebpjajeiadiakgckpahmhkbkpoa) 与 [Firefox](https://addons.mozilla.org/zh-CN/firefox/addon/matters-%E6%B6%88%E9%9F%B3%E5%99%A8/) 两个版本，[代码开源](https://github.com/contributionls/matters-muter)。
- [matters2ipfs](https://matters.news/@deserve/matters%E6%96%87%E7%AB%A0%E7%8E%B0%E5%9C%A8%E5%8F%AF%E4%BB%A5%E4%B8%80%E9%94%AE%E5%9C%A8%E7%BA%BF%E8%BD%AC%E4%B8%BA%E5%A2%99%E5%86%85%E9%93%BE%E6%8E%A5%E4%BA%86-zdpuB1bvMnsAr4APk12FmdRxcqMaEsRo46vKE7p6Arvsg4YiF): 将 Matters 文章转为 ipfs 链接，可以在墙内打开，[代码开源](https://github.com/contributionls/matters2ipfs).
- [matters 个人网站](https://matters.news/@vibertthio/%E7%9C%9F%E6%AD%A3%E5%8E%BB%E4%B8%AD%E5%BF%83%E5%AA%92%E9%AB%94%E7%9A%84%E7%AC%AC%E4%B8%80%E6%AD%A5-%E5%81%9A%E4%B8%80%E5%80%8B-matters-%E7%9A%84%E7%AC%AC%E4%B8%89%E6%96%B9%E7%B6%B2%E7%AB%99-zdpuArgJXADPgWJ8TfvRWWStTvkYC1vqCTV6fHayisbrABkBp): 通过 matters.news 备份的个人网站，[代码开源](https://github.com/vibertthio/matters-third-party)。

# Matters 开源项目

- [Matters 编辑器](https://github.com/thematters/matters-editor): matters.news 所见即所得编辑器，基于[Quill](https://github.com/quilljs/quill)。
- [slugify](https://github.com/thematters/slugify): 支持 CJK charset 的 slugify。
- [apollo-upload-client](https://github.com/thematters/apollo-upload-client): Fork 自 [apollo-upload-client](https://github.com/jaydenseric/apollo-upload-client)，支持 persistence query。
