Other language: [简体中文](./README-zh_hans.md)，[繁體中文](./README-zh_hant.md)

# Matters server API

Matters uses GraphQL for the API layer. Queries and mutations can be tested [here](https://server-test.matters.news/playground), and a short introduction can be found [here](https://matters.news/@robertu/%E7%A4%BE%E5%8D%80%E9%96%8B%E6%94%BE%E4%B8%80%E5%B0%8F%E6%AD%A5-matters-api-zdpuAyovU8xL9sYsV5rQfe35XhmN6okTVbnogCFH2J8cqAXCs).

# Peer 2 peer clients

[Hypha publication project](https://github.com/hypha-publication) develops peer 2 peer clients that are
interoperable with Matters sever. Both [browser extension](https://github.com/hypha-publication/hypha-extension) and [desktop client](https://github.com/hypha-publication/hypha-desktop) are heavily under development and not ready for testing yet.

# Community projects

- [MatREQ](https://matters.news/@jugu/%E9%9D%9E%E5%AE%98%E6%96%B9-matters%E8%A8%B1%E9%A1%98%E6%B1%A0-zdpuAxEfdxG6MdBHnE7rEvCeAG6TPay6i8ychgiq2EoRRMv2s): [Request articles](https://mat.52tw.cc/) on certain topic.
- [matters-muter](https://matters.news/@deserve/%E4%BD%BF%E7%94%A8%E8%BF%99%E4%B8%AA%E6%B5%8F%E8%A7%88%E5%99%A8%E6%89%A9%E5%B1%95%E4%B8%80%E9%94%AE%E5%BC%80%E5%90%AFmatters%E7%9A%84%E5%85%A8%E7%AB%99%E5%B1%8F%E8%94%BD-%E6%8B%89%E9%BB%91-%E9%9D%99%E9%9F%B3%E5%8A%9F%E8%83%BD-zdpuAwGnxxMnyvaBJwCszuRrHjqprMohMPkXXWfYYKwEzvkrX): Browser extension to mute articles and comments of given users, support shared blacklist. For [Chrome](https://chrome.google.com/webstore/detail/matters-%E6%B6%88%E9%9F%B3%E5%99%A8/hpbebebpjajeiadiakgckpahmhkbkpoa) and [Firefox](https://addons.mozilla.org/zh-CN/firefox/addon/matters-%E6%B6%88%E9%9F%B3%E5%99%A8/), [open sourced](https://github.com/contributionls/matters-muter).
- [matters2ipfs](https://matters.news/@deserve/matters%E6%96%87%E7%AB%A0%E7%8E%B0%E5%9C%A8%E5%8F%AF%E4%BB%A5%E4%B8%80%E9%94%AE%E5%9C%A8%E7%BA%BF%E8%BD%AC%E4%B8%BA%E5%A2%99%E5%86%85%E9%93%BE%E6%8E%A5%E4%BA%86-zdpuB1bvMnsAr4APk12FmdRxcqMaEsRo46vKE7p6Arvsg4YiF): convert matters article to ipfs public gateway that can be accessed within GFW, [open sourced](https://github.com/contributionls/matters2ipfs).
- [matters personal website](https://matters.news/@vibertthio/%E7%9C%9F%E6%AD%A3%E5%8E%BB%E4%B8%AD%E5%BF%83%E5%AA%92%E9%AB%94%E7%9A%84%E7%AC%AC%E4%B8%80%E6%AD%A5-%E5%81%9A%E4%B8%80%E5%80%8B-matters-%E7%9A%84%E7%AC%AC%E4%B8%89%E6%96%B9%E7%B6%B2%E7%AB%99-zdpuArgJXADPgWJ8TfvRWWStTvkYC1vqCTV6fHayisbrABkBp): personal website mirrored from matters.news, [open sourced](https://github.com/vibertthio/matters-third-party).

# Matters open source

- [Matters editor](https://github.com/thematters/matters-editor): WYSWYG editor used by matters.news, based on [Quill](https://github.com/quilljs/quill).
- [slugify](https://github.com/thematters/slugify): Good old slugify with CJK charset support.
- [apollo-upload-client](https://github.com/thematters/apollo-upload-client): Fork of [apollo-upload-client](https://github.com/jaydenseric/apollo-upload-client) with persistence query support.
