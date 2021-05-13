[简体中文](./README-zh_hans.md), [繁體中文](./README-zh_hant.md)

# Welcome

This repo is the main portal for documentations and discussions on product, development and community roles. General issues that do not fit in specific repos should also submitted here, for example new feature proposals that require client and server coupling. You can also join us on community maintained [Discord](https://discord.gg/hTe8h7b39U).

Some useful resources in this repo:

* [Introduction to API](#server-api)
* [Introduction to all reposories](#reposories)
* [Architecture diagram](#architecture)
* [Database documentation](./doc) and [relationship diagram](./doc/db/diagrams/summary/relationships.real.compact.svg)
* [Code of conduct](./CODE_OF_CONDUCT.md)
* [Wiki on collabration process](https://github.com/thematters/developer-resource/wiki)


# Server API

Matters uses GraphQL for the API layer. Read the API documention and test queries and mutations in [Apollo playground](https://server-test.matters.news/playground). A short introduction can be found [here](https://matters.news/@robertu/%E7%A4%BE%E5%8D%80%E9%96%8B%E6%94%BE%E4%B8%80%E5%B0%8F%E6%AD%A5-matters-api-zdpuAyovU8xL9sYsV5rQfe35XhmN6okTVbnogCFH2J8cqAXCs).

# Architecture

![Architecture diagram, rendered from [drawio file](./doc/architecture-diagram.drawio)](./doc/architecture-diagram.png "Architecture diagram showing simplified data flow.")

After cloning this repo, you can view the [SchemaSpy](http://schemaspy.org/) generated database documentation by opening `doc/db/index.html`.

# Reposories

The following are major reposories used by matters.news.

## Backend
- [server](https://github.com/thematters/matters-server): Main repo for Matters server. Written in Typescript, using [Apollo Server](https://github.com/apollographql/apollo-server) for GraphQL API.
- [query cache](https://github.com/thematters/apollo-response-cache): Cache related GraphQL directives and Apollo Server plugins. Used to control and invalidate cache in Matters server.
- [image processing](https://github.com/thematters/serverless-file-post-processing): AWS lambda function. Used to resize and transcode images in Matters server.
- [queue dashboard](https://github.com/thematters/matters-queue-dashboard): GUI for for [Bee Queue](https://github.com/bee-queue/bee-queue) and [Bull](https://github.com/optimalbits/bull). Used to view queue jobs in Matters server.

## Frontend
- [web](https://github.com/thematters/matters-web): Main repo for Matters web client. Written in Typescript, built with [React](https://reactjs.org/), [Nextjs](https://nextjs.org/) and [Apollo Client](https://github.com/apollographql/apollo-client).
- [editor](https://github.com/thematters/matters-editor): Opinionated WYSWYG editor used at matters.news, built with [Quilljs](https://github.com/quilljs/quill).
- [upload client](https://github.com/thematters/apollo-upload-client): File upload for GraphQL. Fork of [apollo-upload-client](https://github.com/jaydenseric/apollo-upload-client) with persistence query support.

## Shared
- [slugify](https://github.com/thematters/slugify): Good old slugify with CJK charset support.
- [docker](https://github.com/thematters/matters-docker): Docker images used by Matters Lab.
- [slack notification](https://github.com/thematters/matters-slacknoti): AWS lambda function for sending notifications to slack for DevOps purpose.

# Peer 2 peer clients

Matters is actively finding better ways to deliver content in p2p protocols. Below are some related clients.
* [Hypha publication project](https://github.com/hypha-publication): experimental projects for peer 2 peer clients to be
interoperable with Matters sever. 
  * [Hypha Desktop](https://github.com/hypha-publication/hypha-desktop): Desktop client based on [Election.js](https://www.electronjs.org/) and [IPFS](https://ipfs.io/). Can be downloaded directly and used as a IPFS browser.
  * [Hypha extension](https://github.com/hypha-publication/hypha-extension): Browser extension client based on [js-ipfs](https://github.com/ipfs/js-ipfs) and [orbit-db](https://github.com/orbitdb/orbit-db). Can be used for private p2p messaging etc. Heavily under development.
* [Beaker Browser](https://github.com/beakerbrowser/beaker): A stable p2p browser supporting [`://dat` protocol](https://dat.foundation/). There are some [discussions](https://github.com/beakerbrowser/unwalled.garden/issues/51) and experiments about adapting Matters to Beaker Browser via [unwalled.garden](https://github.com/beakerbrowser/unwalled.garden) protocol and [Hyperdrive](https://github.com/hypercore-protocol/hyperdrive).

# Community projects

- [MatREQ](https://matters.news/@jugu/%E9%9D%9E%E5%AE%98%E6%96%B9-matters%E8%A8%B1%E9%A1%98%E6%B1%A0-zdpuAxEfdxG6MdBHnE7rEvCeAG6TPay6i8ychgiq2EoRRMv2s): [Request articles](https://mat.52tw.cc/) on certain topic.
- [matters-muter](https://matters.news/@deserve/%E4%BD%BF%E7%94%A8%E8%BF%99%E4%B8%AA%E6%B5%8F%E8%A7%88%E5%99%A8%E6%89%A9%E5%B1%95%E4%B8%80%E9%94%AE%E5%BC%80%E5%90%AFmatters%E7%9A%84%E5%85%A8%E7%AB%99%E5%B1%8F%E8%94%BD-%E6%8B%89%E9%BB%91-%E9%9D%99%E9%9F%B3%E5%8A%9F%E8%83%BD-zdpuAwGnxxMnyvaBJwCszuRrHjqprMohMPkXXWfYYKwEzvkrX): Browser extension to mute articles and comments of given users, support shared blacklist. For [Chrome](https://chrome.google.com/webstore/detail/matters-%E6%B6%88%E9%9F%B3%E5%99%A8/hpbebebpjajeiadiakgckpahmhkbkpoa) and [Firefox](https://addons.mozilla.org/zh-CN/firefox/addon/matters-%E6%B6%88%E9%9F%B3%E5%99%A8/), [open sourced](https://github.com/contributionls/matters-muter).
- [matters2ipfs](https://matters.news/@deserve/matters%E6%96%87%E7%AB%A0%E7%8E%B0%E5%9C%A8%E5%8F%AF%E4%BB%A5%E4%B8%80%E9%94%AE%E5%9C%A8%E7%BA%BF%E8%BD%AC%E4%B8%BA%E5%A2%99%E5%86%85%E9%93%BE%E6%8E%A5%E4%BA%86-zdpuB1bvMnsAr4APk12FmdRxcqMaEsRo46vKE7p6Arvsg4YiF): convert matters article to ipfs public gateway that can be accessed within GFW, [open sourced](https://github.com/contributionls/matters2ipfs).
- [matters personal website](https://matters.news/@vibertthio/%E7%9C%9F%E6%AD%A3%E5%8E%BB%E4%B8%AD%E5%BF%83%E5%AA%92%E9%AB%94%E7%9A%84%E7%AC%AC%E4%B8%80%E6%AD%A5-%E5%81%9A%E4%B8%80%E5%80%8B-matters-%E7%9A%84%E7%AC%AC%E4%B8%89%E6%96%B9%E7%B6%B2%E7%AB%99-zdpuArgJXADPgWJ8TfvRWWStTvkYC1vqCTV6fHayisbrABkBp): personal website mirrored from matters.news, [open sourced](https://github.com/vibertthio/matters-third-party).

# Hall of Fame

We would like to thank everyone on the following list for making our products more secure. You can add yourself by making a pull request.

* [huli](https://zeroday.hitcon.org/user/aszx87410)
  * CORS misconfiguration
* catding ([GitHub](https://github.com/catdingding), [Matters](https://matters.news/@catding))
  * Missing size or domain check during uploading assets to IPFS
