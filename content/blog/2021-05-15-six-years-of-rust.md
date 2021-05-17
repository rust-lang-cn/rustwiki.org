+++
title = "Rust 发布六周年"
description = "今天是 Rust 发布的 6 周年，随着 2015 年发布 1.0 版本以来，已经走过 6 年，Rust 变得越来越强大，也越来越好用，已经很多生产环境使用了 Rust 编程语言。Rust 连续多年成为最受欢迎的编程语言，而且得到了 Google、微软、Facebook 等大型公司和项目的支持。未来 Rust 将会做得更好，Rust 值得每个人尝试和使用。"
date = 2021-05-15T14:36:26-04:00
template = "blog/page.html"
slug = "six-years-of-rust"

[taxonomies]
categories = ["Rust 发布周年"]
tags = ["Rust"]

[extra]
author = "Rust 小组"
translator = "Aaran Xu"
translate_tool = '自豪地采用 <a href="https://translate.google.cn">Google 翻译</a>'
english_title = "The Plan for the Rust 2021 Edition"
english_url = "https://blog.rust-lang.org/2021/05/15/six-years-of-rust.html"
release = true
+++

今天是 [Rust] 自 2015 年诞生 1.0 以来的周年的第六个周年生日。此后，尤其是在过去的一年中，发生了很大的变化，Rust 也是如此。到 2020 年，还没有基金会，没有 const 泛型，许多组织仍在怀疑 Rust 是否已准备好投入生产。

在新冠疫情大流行中，除各种错误修正版本外，数百名 Rust 的全球分布式团队成员和志愿者运送了超过 9 种稳定的 Rust 新发行版。今天，“生产中的 Rust” 已经不是一个问题，而是一个声明。新成立的 Rust 基金会有几位成员，他们非常重视在生产中使用 Rust 的价值，以帮助继续支持其开放开发生态系统并为之做出贡献。

我们今天想回顾一下过去一年中的一些重大改进，社区如何在生产中使用 Rust，最后展望了目前正在进行的一些改进工作，这些改进和改进了Rust在小型和小型企业中的使用。明年的大型项目。让我们开始吧！

[rust]: https://www.rust-lang.org

## 最近增加

在过去的一年中，Rust 语言取得了巨大的进步，获得了许多生活质量的功能，尽管它们从根本上没有改变语言，但它们使在更多地方使用和维护 Rust 变得更加容易。

- 随着 Rust 1.52.0 的升级和 LLVM 12 的升级，最终解决方案中出现的一些不完善的情况（例如处理无限循环）部分已得到解决。这是 Rust 团队和 LLVM 项目之间长期的合作，并且是 Rust 改进的一个很好的例子，也使广泛的编程语言生态系统受益。

- 为了支持更广泛的生态系统，引入了对 64 位 ARM Linux 的 Tier 1 支持以及对 ARM macOS 和 ARM Windows 的 Tier 2 支持，这使 Rust 有了更多的选择来轻松地跨新的和不同的体系结构构建项目。

- 完善主题最明显的例外是 Rust 编译时功能的重大改进。用于原始类型的 const 泛型的稳定，用于`const fn` 的控制流的添加，以及允许在更多地方使用过程宏，已允许创建功能强大的新型 API 和 crate。

rustc 并不是唯一具有重大改进的工具。

- Cargo 最近才稳定了其新的功能解析器，这使得在不同目标之间使用依赖项变得更加容易。

- rustdoc 稳定了其“文档内链接”功能，使您可以轻松，自动地交叉引用文档中 的Rust 类型和功能。

- 现在，带有 Cargo 的 Clippy 使用单独的构建缓存，该缓存提供了更加一致的行为。

## 生产环境中的 Rust

每年，Rust 在社区和行业中的增长和采用都令人难以置信，过去的一年也不例外。2020年，Rust 再次被评为 StackOverflow 上[最受欢迎的编程语言][stackoverflow]。感谢社区中的每个人的支持，并帮助 Rust 成为今天的样子。

随着 Rust 基础的形成，Rust 处于建立可持续的开源生态系统的更好位置，使每个人都可以构建可靠而高效的软件。许多使用 Rust 的公司已经组建了专门致力于维护和改进 Rust 项目的团队，包括 [AWS](https://aws.amazon.com/blogs/opensource/how-our-aws-rust-team-will-contribute-to-rusts-future-successes/)，[Facebook](https://engineering.fb.com/2021/04/29/developer-tools/rust/) 和 Microsoft。

而且，不仅仅是 Rust 变得越来越大。越来越多的公司在他们的项目中采用了 Rust，并提供了官方支持的 Rust API。

- 微软和亚马逊最近都宣布并发布了新的正式支持的 Rust 库，用于与 [Windows] 和 [AWS] 进行交互。对这些大量 API 的官方第一方支持有助于使 Rust 人们在决定使用什么项目时成为他们的首选。
- cURL项目发布了新版本，这些新版本提供了加入支持，从而支持使用Rust库来处理 [HTTP/s] 和 [TLS] 通信。这是 ISRG，Hyper＆Rustls 团队和 cURL 项目之间的一次大型社区间合作，我们要感谢每个人在为大规模且广泛使用的项目提供新的内存安全后端方面所做的辛勤工作作为cURL！
- Tokio（用Rust编写的异步运行时）发布了 [1.0版本][tokio-1.0]，并宣布了三年的稳定性保证，为每个人提供了一个坚实而稳定的基础，可以在不影响速度的情况下编写可靠的网络应用程序。

[stackoverflow]: https://stackoverflow.blog/2020/06/05/why-the-developers-who-use-rust-love-it-so-much/
[tokio-1.0]: https://tokio.rs/blog/2020-12-tokio-1-0
[http/s]: https://daniel.haxx.se/blog/2020/10/09/rust-in-curl-with-hyper/
[tls]: https://daniel.haxx.se/blog/2021/02/09/curl-supports-rustls/
[rust foundation]: https://foundation.rust-lang.org/posts/2021-02-08-hello-world/
[windows]:https://github.com/microsoft/windows-rs
[aws]: https://github.com/awslabs/aws-sdk-rust

## 未来的工作

当然，所有这一切只是开始，我们看到越来越多的计划将 Rust 引入了令人兴奋的新内容。

- 临界区和 Ferrous 系统已经开始使用 [Ferrocene]。这是一个使 Rust 成为适用于整个行业安全和关键任务系统的可行编程语言的项目。
- Embark Studios 发布了的初始原型 [`rust-gpu`]，这是一个新的编译器后端，该后端允许使用 Rust 为 GPU 编写图形着色器。
- Linux 项目目前正在考虑一项提议，[将Rust作为第二种语言添加到内核中][linux-rust]，以使编写更安全的驱动程序和内核空间代码成为可能。
- Google 宣布，[它现在支持在Rust中构建 Android 系统的底层组件][android-rust]，并且已经开始着手用 Rust 重写其蓝牙堆栈！

目前，Rust 团队正在计划和协调 2021 年版的 Rust。就像去年一样，这些变化的许多主题都围绕着生活质量的提高。您可以查看我们最近有关 [“Rust 2021 版计划”][edition-plan] 的帖子，以了解团队正在计划进行哪些更改。

以上只是冰山一角；在 Rust 中，还有更多的工作要做，令人兴奋的新开放项目每天都在启动。我们迫不及待地想看到你们明年的发展！

您是否对过去一年的变化或项目感到兴奋？您是否要开始使用 Rust？您想为 2021 版做出贡献吗？马上过来，自我介绍，并在我们的 [Discourse][Discourse] 论坛和 [Zulip][Zulip] 聊天中加入讨论！欢迎大家，我们致力于为所有人提供友好，安全和热情的环境，无论性别，性取向，残疾，种族，宗教或类似个人特征如何。

[ferrocene]: https://ferrous-systems.com/ferrocene
[`rust-gpu`]: https://github.com/EmbarkStudios/rust-gpu
[linux-rust]: https://lore.kernel.org/lkml/CANiq72khBa2GcB6-PHM3A44Y90d6vzYAS=BVpk3nT4B6u+NVDw@mail.gmail.com/T/#mb5e524dae9d5a5815c6e68eb36b9bde4e87c861d
[edition-plan]: https://rustwiki.org/blog/edition-2021/
[discourse]: https://users.rust-lang.org/
[zulip]: https://rust-lang.zulipchat.com/
[android-rust]: https://security.googleblog.com/2021/04/rust-in-android-platform.html
