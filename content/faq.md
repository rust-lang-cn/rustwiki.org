+++
title = "FAQ"
description = "关于 Rust Wiki、Rust 语言、Rust 中文社区和 Rust 教程的相关常见问题。"

[extra]
lead = "关于 Rust Wiki、Rust 语言、Rust 中文社区和 Rust 教程的相关常见问题"
id = "kube-faq"
+++

## Rust Wiki 是什么网站？

Rust Wiki 是非营利性的关于 Rust 教程的中文资源网，由 [Rust 中文翻译项目组][rust-lang-cn]创建。我们深受 Rust 开发团队的影响，Rust 开发团队以前所未有的开放形式开发出 Rust 语言，并给出了全面且规范的开源组织范例。正因于此，我们创立了 Rust Wiki 网，从而更好地将中文资源呈现给大家。我们的所有资源都以开源的形式提供，在 [GitHub][rust-lang-cn] 上均可以找到相关资源，包括[本网站的源码和文章][rustwiki]。

本网站主要采用的是 Rust 相关的工具链完成:

- 网站使用 [Zola][zola] 技术制作，Zola 是一个使用 Rust 语言编写的具有极速生成速度的静态网站生成器;
- 网站的 Logo 来自 [Rust 官方的多媒体资源][rust-logo];
- 网站的主题包含两部分：
  1. 第一部分是主站，采用的是 [kube 主题][kube] 来构建页面；
  2. 第二部分是 Wiki 站，采用的是 [EasyDocs 主题][zola-easydocs-theme] 来构建。

[rust-lang-cn]: https://github.com/rust-lang-cn
[rustwiki]: https://github.com/rust-lang-cn/rustwiki.org
[zola]: https://www.getzola.org
[rust-logo]: https://github.com/rust-lang/rust-artwork
[kube]: https://kube.elemnts.net/
[zola-easydocs-theme]: https://www.getzola.org/themes/zola-easydocs-theme/

## Rust Wiki 的中文资源来源于哪里？

Rust Wiki 的中文教程等相关资源主要来源于两方面：

1. Rust Wiki 自身的组织，即 Rust 中文翻译项目组完成的翻译作品，比如[《通过例子学 Rust》][rbe]和[《Rust 版本指南》][edition-guide]；
2. 源自组织外的 Rust 翻译作品，如[《Rust 程序设计语言》][book]。

我们遵循 “DRY”（Don't Repeat Yourself）原则，以减少不必要的重复劳动。一般来说，组织都会计划翻译 Rust 官方的作品，若是发现已经有别处给出了译作，我们将采用可取的作品，比如第二版的《Rust 程序设计语言》本组织也翻译了前几个章节，后面发现有更完整的翻译成品，所以本组织整合已有的资源而不再重新翻译，我们欢迎所有的 Rust 中文翻译作者加入翻译项目组。

注意：Rust 中文翻译项目组的作品一般采用 MIT 或 Apache 2.0 协议，除非特定教程使用了其他不兼容的许可协议（如 GPL 和 CC BY-SA-4.0 等协议）。另外对于未指定开源协议或是以闭源形式公开的作品，我们项目组均不会采用。

[rbe]: https://rustwiki.org/zh-CN/rust-by-example
[edition-guide]: https://rustwiki.org/zh-CN/edition-guide
[book]: https://rustwiki.org/zh-CN/book

## Rust 中文项目组有什么目标和计划？

我们的总体目标是构建一个完整且完善的 Rust 中文知识库，为此我们会翻译所有必要的 Rust 官方资源以及部分非官方的 Rust 资源，这也是我们的总的计划，但并未给出时间表。为了达成这个目标，我们会一步步翻译相关的作品，目前我们已经翻译了部分重要的作品，未来还需要进一步翻译。

对于具体的翻译作品而言，我们会给出特定的计划和说明，在相关的作品说明页会有说明。

## 如何加入 Rust 中文项目组？

Rust 中文项目组是一个开放的组织，我们欢迎每一个热爱 Rust 的人加入，并一起朝着组织的目标一步步完善 Rust 的中文知识库。加入组织前，请确保已经注册了 [GitHub][github] 账号并熟悉 Git 工具，因为我们的资料内容均采用 Git 工具和 GitHub 托管平台来进行编写。


[github]: https://github.com


## 我想为 Rust Wiki 提交博客文章或技术分享文章，如何投稿？

Rust Wiki 网站会不定期发表博客文章，我们欢迎所有人为 Rust Wiki 网站投稿。注意我们网站的博客只发表关于 Rust 编程相关的内容，比如 Rust 的技术分享的文章、翻译 Rust 英文技术文章，或是 Rust 的新闻资讯相关的文章等等。若是有这类文章，请随时在在本站仓库中[创建一个新的 PR][pr]，只要文章内容合适、格式符合规范，我们都会快速合并到主分支并更新网站。

[pr]: https://github.com/rust-lang-cn/rustwiki.org/pulls

## 我该如何学习 Rust？

这个问题没有统一的答案，因为每个人的知识结构（数学、英语等）以及编程能力各不相同，不同人的学习方式也不尽相同。总的来说，学习 Rust 分两类：

- 有其他编程语言的基础，比如已经熟悉 C、C++、Python 等，那么最好的学习方式是通过项目驱动型来学习，比如通过《Rust 程序设计语言》中的[“猜数字游戏”][guessing-game]这个章节了解 Rust 的大概全貌，在此基础上不断拓展了解 Rust 的各个知识点。
- 没有编程基础。这种情况下学习 Rust 可能会稍感觉有点难，也有一些人提到 Rust 不太适合作为第一门编程语言来学习，这是因为 Rust 的概念相对比较多，要快速掌握并写出一些有成绩的代码并不太容易，但是确实想将 Rust 作为第一门语言来学习不是不可以。这种情况下就需要按照官方的《Rust 程序设计语言》和《通过例子学 Rust》一步步熟悉各个编程的概念，多看多思考多写代码，不断总结和深入。

以上只是给出一些通用建议，但学习是一种很主观的行为，个人应该选择或尝试出最适合自己的学习方式。

在有一定的基础后，我们还可以通过去一些编程平台（如 LeetCode）使用 Rust 语言来编写相关算法，找一些合适的 Rust 项目（比如一些 crate 项目）的源码来阅读学习。

相关资料：

- [《Rust 程序设计语言》][book]
- [《通过例子学 Rust》][rbe]
- [Rust 小练习][rustlings]
- [crates.io][crates]
- [LeetCode][leetcode]

[guessing-game]: https://rustwiki.org/zh-CN/book/ch02-00-guessing-game-tutorial.html
[rustlings]: https://github.com/rust-lang-cn/rustlings-cn
[crates]: https://crates.io/
[leetcode]: https://leetcode-cn.com/

## 我要学习 Rust，看中文教程还是英文教程？

最重要是看自己的英文水平。若是英语水平足够好，建议直接看英文的文档。若是直接看英文吃力，可以选择看中文的文档，这种在学习 Rust 的过程中逐渐看一些英文文档，慢慢加强自己的英文水平。

但是对于大多数国人来说，看英文的能力都会差于看中文的能力，特别是快速浏览了解内容的能力，这些能力是需要慢慢锻炼提高的。我们创建 Rust Wiki 网并翻译 Rust 资源，也有一部分这样的原因。我们提供越来越完善的中文资料，丰富中文知识的同时，也为我们更多英语不好的人能够通过中文的译文来快速了解 Rust 的概要。

我们也希望更多热爱 Rust 的人加入 Rust 中文翻译项目组，共同打造出更丰富的 Rust 中文知识库。

## 我想翻译 Rust 的文章，该如何进行？

请参阅 [Rust 文档翻译指引][translation-guide]，我们将不断完善整个社区翻译的指南，让更多人更好地翻译出 Rust 的相关的作品。

[translation-guide]: https://rustwiki.org/wiki/translate/rust-translation-guide/