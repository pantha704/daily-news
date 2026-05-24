---
layout: default
title: "Horizon Summary: 2026-05-24 (ZH)"
description: "From 20 items, 14 important content pieces were selected"
date: 2026-05-24
lang: zh
---

> From 20 items, 14 important content pieces were selected

---

1. [从第一原理优化深度学习性能](#item-1) ⭐️ 9.0/10
2. [苹果开源 corecrypto 密码库，附形式化验证证明量子安全算法正确性](#item-2) ⭐️ 9.0/10
3. [HTML 定义列表的局限性](#item-3) ⭐️ 8.0/10
4. [80386 微码反汇编：详细见解](#item-4) ⭐️ 8.0/10
5. [微软内部大规模推广 Claude Code，鼓励非技术员工使用 AI 编程](#item-5) ⭐️ 8.0/10
6. [百度 CEO 李彦宏：AI 大模型已接近应用爆发的临界点](#item-6) ⭐️ 8.0/10
7. [中国日均词元调用量两年增超千倍](#item-7) ⭐️ 8.0/10
8. [美国白宫要求在所有政府手机上安装官方应用](#item-8) ⭐️ 8.0/10
9. [找到自己的真正天赋并做自己擅长的事情](#item-9) ⭐️ 7.0/10
10. [腾讯游戏屏蔽词系统疑似存在偏向性，测试违禁词或触发十年封禁](#item-10) ⭐️ 7.0/10
11. [微软对 OpenAI 的投资导致 31 亿美元净利润减少](#item-11) ⭐️ 6.0/10
12. [海盗船开始采用长鑫存储芯片，DDR5 内存价格有望下调](#item-12) ⭐️ 6.0/10
13. [一位作家分享了他们的定制化 WriterDeck 设置，引发了关于专注和实用性的讨论](#item-13) ⭐️ 5.0/10
14. [Android 17 将引入 Noto 3D 表情设计](#item-14) ⭐️ 5.0/10

---

<a id="item-1"></a>
## [从第一原理优化深度学习性能](https://horace.io/brrr_intro.html) ⭐️ 9.0/10

一篇技术文章阐述了如何从第一原理优化深度学习性能，强调了理解硬件和软件的权衡的重要性。 这篇文章重要，因为它提供了一个全面指南，帮助开发者优化深度学习性能，使他们能够对模型和基础设施做出明智的决策。 这篇文章强调了理解硬件和软件的权衡的重要性，并提供了一个分析和优化深度学习性能的框架。

hackernews · tosh · May 23, 11:50 · [社区讨论](https://news.ycombinator.com/item?id=48246889)

**背景**: 深度学习性能优化是机器学习系统的一个关键方面，理解硬件和软件的权衡对于构建高效模型至关重要。硬件加速，如使用 GPU，可以显著提高性能，但需要仔细考虑内存和计算资源。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Hardware_acceleration">Hardware acceleration - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/accelerated-computing">What is Accelerated Computing? | IBM</a></li>
<li><a href="https://www.amd.com/en/resources/articles/what-is-accelerated-computing-and-why-is-it-important.html">Accelerated Computing 101</a></li>

</ul>
</details>

**社区讨论**: 社区讨论强调了深度学习性能优化的复杂性，有些用户注意到没有可移植的建议，并且不同的硬件和软件配置可能会导致不同的结果。

**标签**: `#Deep Learning`, `#Performance Optimization`, `#Machine Learning Systems`, `#Hardware-Accelerated Computing`, `#Technical Deep-Dive`

---

<a id="item-2"></a>
## [苹果开源 corecrypto 密码库，附形式化验证证明量子安全算法正确性](https://security.apple.com/blog/formal-verification-corecrypto/) ⭐️ 9.0/10

苹果发布了 corecrypto 源代码，公开了用于对抗未来量子计算机的 ML-KEM 和 ML-DSA 算法实现，并首次提供了端到端的形式化验证数学证明。 这是重要的，因为它为超过 25 亿台活跃设备提供了安全的基础，并确保了量子安全算法的正确性。 该库包括定制验证工具和 Isabelle 理论库，使独立专家能够评估证明。

telegram · zaihuapd · May 23, 04:49

**背景**: 形式化验证是一种数学方法，用于证明系统的正确性，确保代码和手工优化的 ARM64 汇编与 NIST 标准严格一致。 ML-KEM 和 ML-DSA 是量子安全算法，旨在抵抗经典计算机和量子计算机的攻击。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Formal_verification">Formal verification</a></li>
<li><a href="https://en.wikipedia.org/wiki/ML-KEM">ML-KEM</a></li>

</ul>
</details>

**标签**: `#cryptography`, `#quantum-security`, `#apple`, `#corecrypto`, `#formal-verification`

---

<a id="item-3"></a>
## [HTML 定义列表的局限性](https://benmyers.dev/blog/on-the-dl/) ⭐️ 8.0/10

本·迈尔斯讨论了 HTML 定义列表元素（&lt;dl&gt;）的局限性和滥用，以及其潜在替代方案。 这篇文章强调了理解 HTML 元素局限性的重要性以及需要替代解决方案的必要性。 这篇文章讨论了&lt;dl&gt;的滥用，包括多层包装、分隔符、图标和标题等，并提出了替代解决方案。

hackernews · ravenical · May 23, 13:03 · [社区讨论](https://news.ycombinator.com/item?id=48247325)

**背景**: HTML 定义列表（&lt;dl&gt;）用于表示术语组和描述，但其局限性和滥用已在 web 开发社区中讨论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Semantic_HTML">Semantic HTML</a></li>
<li><a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/dl">HTML description list element - MDN Web Docs</a></li>
<li><a href="https://www.w3.org/TR/html401/struct/lists.html">Lists in HTML documents</a></li>

</ul>
</details>

**社区讨论**: 这篇文章在 web 开发者中引发了讨论，有些人认为&lt;dl&gt;太具约束性，而其他人则认为它仍然是一个有用的元素。

**标签**: `#HTML`, `#Accessibility`, `#Semantic-HTML`, `#Web-Development`

---

<a id="item-4"></a>
## [80386 微码反汇编：详细见解](https://www.reenigne.org/blog/80386-microcode-disassembled/) ⭐️ 8.0/10

通过高分辨率 die 成像、先进图像处理和神经网络分析，80386 微码进行了详细的反汇编。 这项成就为我们提供了 80386 处理器内部工作的独特见解，并表明从处理器 die 中恢复微码是可行的。 反汇编结果显示，80386 微码包含 94,720 个比特，包括一个标记为“未使用”的程序段，没有与其相关的入口点。

hackernews · nand2mario · May 23, 12:11 · [社区讨论](https://news.ycombinator.com/item?id=48247004)

**背景**: 微码是中央处理器（CPU）中的一个低级别编程层，实现处理器指令集架构（ISA）的机器指令。80386 处理器是第一个 32 位处理器，于 1985 年首次发布，是 x86 微架构的重大进步。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Microcode">Microcode</a></li>
<li><a href="https://www.reenigne.org/blog/80386-microcode-disassembled/">80386 microcode disassembled « Reenigne blog</a></li>
<li><a href="https://bestcadpapers.com/art-and-technology/80386-microcode-disassembled/">80386 Microcode Disassembled - Best CAD papers</a></li>

</ul>
</details>

**社区讨论**: 用户正在讨论从处理器 die 中恢复微码的可行性以及这种技术的潜在应用。

**标签**: `#microcode`, `#disassembly`, `#80386`, `#processor`, `#computer architecture`

---

<a id="item-5"></a>
## [微软内部大规模推广 Claude Code，鼓励非技术员工使用 AI 编程](https://t.me/zaihuapd/41535) ⭐️ 8.0/10

微软正在其最重要的工程团队中广泛推广 Anthropic 的 Claude Code，甚至鼓励没有编程经验的员工使用该工具进行原型设计。据消息人士透露，微软 CoreAI 团队和负责 Windows、Microsoft 365、Outlook 等产品的体验与设备部门都被要求安装 Claude Code。 这项举动对 AI 编程和软件工程有着重大影响，可能会改变开发人员与代码的工作方式。它还可能会影响行业中 AI 工具的采用。 Claude Code 是 Anthropic 开发的 Visual Studio Code 扩展，集成 Claude AI 为编程辅助。它需要明确的许可才能修改文件或运行命令。

telegram · zaihuapd · May 23, 06:05

**背景**: Anthropic 的 Claude Code 是一个编程辅助工具，工作在开发人员的现有环境中，并使用他们的工具，而不是在不透明的后端操作。它旨在提供安全可靠的 AI 编程辅助。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_(language_model)">Claude (language model) - Wikipedia</a></li>
<li><a href="https://www.anthropic.com/product/claude-code">Claude Code | Anthropic's agentic coding system</a></li>
<li><a href="https://github.com/features/copilot">GitHub Copilot · Your AI pair programmer</a></li>

</ul>
</details>

**标签**: `#AI`, `#Microsoft`, `#Software Engineering`, `#Anthropic`, `#Claude Code`

---

<a id="item-6"></a>
## [百度 CEO 李彦宏：AI 大模型已接近应用爆发的临界点](https://t.me/zaihuapd/41538) ⭐️ 8.0/10

百度 CEO 李彦宏认为，AI 大模型的发展已接近“临界点”，一个非常有价值的应用即将爆发。 这很重要，因为这表明了 AI 大模型的潜在突破，可能会带来新的应用和创新。 李彦宏提到，百度正在对核心产品进行 AI 重构，目前其搜索引擎已有 65%的结果带有生成式内容。

telegram · zaihuapd · May 23, 08:40

**背景**: AI 大模型已成为技术领域的焦点，Google 的 BERT 和 OpenAI 的 GPT 等模型的参数规模已达到数十亿甚至数十万亿，导致训练数据和计算能力的显著增加。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zh.wikipedia.org/zh-hk/临界点_(数学)">臨界點 (數學) - 維基百科，自由的百科全書</a></li>
<li><a href="https://www.symbolab.com/solver/function-critical-points-calculator">Functions Critical Points Calculator - Free Online Calculator With Steps & Examples</a></li>
<li><a href="https://link.springer.com/article/10.1007/s44267-024-00065-8">An overview of large AI models and their applications</a></li>

</ul>
</details>

**标签**: `#AI`, `#Machine Learning`, `#Deep Learning`, `#Search Engines`, `#Industry Insights`

---

<a id="item-7"></a>
## [中国日均词元调用量两年增超千倍](https://t.me/zaihuapd/41542) ⭐️ 8.0/10

中国日均词元调用量已在两年内增幅超千倍，今年 3 月突破 140 万亿。 这一增长表明，词元经济和数据市场化在中国人工智能产业中的重要性日益增强。 词元经济是基于行为条件反射原理的系统性强化目标行为的系统，具有可计量、可定价、可交易的特征。

telegram · zaihuapd · May 23, 14:36

**背景**: 词元经济是基于行为条件反射原理的系统性强化目标行为的系统，具有可计量、可定价、可交易的特征。数据市场化是指将数据作为新的生产要素纳入市场资源配置，促进数据流动和优化配置。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Token_economy">Token economy</a></li>
<li><a href="https://keendata.com/en/solution/data-marketization.html">Data Factor Market Allocation | Solutions - KeenTech</a></li>

</ul>
</details>

**社区讨论**: No community discussion available.

**标签**: `#AI`, `#China`, `#Token Economy`, `#Data Marketization`, `#Natural Language Processing`

---

<a id="item-8"></a>
## [美国白宫要求在所有政府手机上安装官方应用](https://www.govexec.com/management/2026/05/white-house-ordering-agencies-place-its-new-app-all-employees-government-phones/413738/) ⭐️ 8.0/10

白宫已下令联邦机构在所有雇员的政府手机和平板电脑上强制安装新开发的“白宫”应用程序。该应用旨在提供政策简报、实时新闻和社交媒体动态。 这一举措引发了安全专家的广泛质疑，认为该应用可能存在泄露用户数据或为政府内网留下后门的风险。此外，由于应用内包含具有明显政治倾向的内容，批评者认为强制安装此类应用更像是在向联邦职员推送政治宣传，而非单纯的政务沟通。 该应用将在下周起自动安装在政府手机和平板电脑上，无需员工进行任何操作。应用内包含政策简报、实时新闻和社交媒体动态。

telegram · zaihuapd · May 24, 03:26

**背景**: 白宫开发了该应用，以提供一个集中平台提供政策简报、实时新闻和社交媒体动态。应用内容旨在提供信息和非党派，但批评者认为它具有明显的政治倾向。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.gitcode.com/497abd4a5c5906da4f89185b848dad81.html">Cursor AI 项目中的 Windows... | GitCode博客</a></li>
<li><a href="https://blog.csdn.net/nbspzs/article/details/132814149">winform...</a></li>
<li><a href="https://tug.org/texlive/doc/texlive-zh-cn/texlive-zh-cn.pdf">TEX Live 指南 —2026</a></li>
<li><a href="https://xnewera.pku.edu.cn/docs/2021-07/2ad42e49c8ca42b6848c15fe468b8b00.pdf">xnewera.pku.edu.cn/docs/2021-07/2ad42e49c8ca42b6848c15fe468...</a></li>
<li><a href="http://www.hprc.org.cn/gsyj/whs/xzgwhjs/202507/P020250729563500368635.pdf">TheDevelopmentHistory , CharacteristicsandPromotionStrategies</a></li>
<li><a href="https://ishare.ifeng.com/hotNewsShare404">ishare.ifeng.com/hotNewsShare404</a></li>

</ul>
</details>

**社区讨论**: 社区讨论仍在进行中，有些用户表达了对应用可能对政府安全造成的影响的担忧，另一些用户则批评应用内容具有偏见。

**标签**: `#Government Technology`, `#Security Risks`, `#Policy`, `#Federal Agencies`, `#Mobile Apps`

---

<a id="item-9"></a>
## [找到自己的真正天赋并做自己擅长的事情](https://kk.org/cooltools/book-freak-210-the-art-of-money-getting/) ⭐️ 7.0/10

讨论了找到自己的真正天赋并做自己擅长的事情的重要性，参考了巴纳姆的第一规则和埃德加·迪克斯特拉的建议 这次讨论很重要，因为它强调了找到与自己才能和激情相匹配的职业的重要性 巴纳姆的第一规则是选择自己擅长的工作，然后努力成为最好的，而迪克斯特拉建议只做自己才能做的事情

hackernews · dxs · May 23, 12:48 · [社区讨论](https://news.ycombinator.com/item?id=48247208)

**背景**: 巴纳姆是美国著名的演出家和商人，他编纂了他的赚钱规则，而迪克斯特拉是著名的计算机科学家，他给出了成功职业生涯的建议

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/There's_a_sucker_born_every_minute">There's a sucker born every minute - Wikipedia</a></li>
<li><a href="https://www.gutenberg.org/files/8581/8581-h/8581-h.htm">The Art of Money Getting, by P.T. Barnum - Project Gutenberg</a></li>
<li><a href="https://www.quora.com/Why-was-Edsger-Dijkstra-so-cool">Why was Edsger Dijkstra so cool? - Quora</a></li>

</ul>
</details>

**社区讨论**: 社区讨论强调了找到自己的真正天赋的挑战和追求有意义职业的重要性

**标签**: `#productivity`, `#career development`, `#self-improvement`, `#software engineering`

---

<a id="item-10"></a>
## [腾讯游戏屏蔽词系统疑似存在偏向性，测试违禁词或触发十年封禁](https://cloud.tencent.com/document/product/1124/64683) ⭐️ 7.0/10

腾讯游戏屏蔽词系统被指存在偏向性，并且惩罚过严，引发了社区的关注。玩家反馈称，某些词语，如「捞女」，被列为屏蔽词，而类似的词语，如「捞男」，却不受限制。 这引发了对腾讯游戏屏蔽词系统公平性和准确性的担忧，这可能会影响游戏体验和社区参与度。 该系统使用统一关键词库结合机器学习模型，这可能导致偏向性和过度惩罚。玩家反馈称，仅因为输入相关屏蔽词，可能触发十年封禁，或导致账号永久丧失命名权。

telegram · zaihuapd · May 24, 02:41

**背景**: 腾讯游戏屏蔽词系统用于多个游戏，玩家反馈称其他标题也有类似的问题。该系统使用机器学习模型和统一关键词库，这可能导致偏向性和过度惩罚。

**标签**: `#Tencent`, `#Game Development`, `#Content Moderation`, `#Bias in AI`, `#Community Discussion`

---

<a id="item-11"></a>
## [微软对 OpenAI 的投资导致 31 亿美元净利润减少](https://t.me/zaihuapd/41537) ⭐️ 6.0/10

微软对 OpenAI 的投资导致 OpenAI 单季度巨亏 115 亿美元，导致微软净利润减少 31 亿美元。 这一巨额亏损凸显了人工智能开发的高成本以及投资新兴技术的风险。 这一亏损规模是 OpenAI 今年上半年 43 亿美元营收的近三倍。

telegram · zaihuapd · May 23, 07:40

**背景**: 微软已向 OpenAI 投资 116 亿美元，占其 130 亿美元承诺投资的绝大部分。OpenAI 的亏损主要是由于其高烧钱速度，这是人工智能领域常见的挑战。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zhuanlan.zhihu.com/p/496165358">长期股权投资——权益法（干货总结） - 知乎</a></li>
<li><a href="https://www.toutiao.com/article/7474579167422464546/">采用权益法核算的长期股权投资账务处理流程（附案例详解）</a></li>

</ul>
</details>

**标签**: `#artificial-intelligence`, `#openai`, `#microsoft`, `#finance`, `#tech-industry`

---

<a id="item-12"></a>
## [海盗船开始采用长鑫存储芯片，DDR5 内存价格有望下调](https://thenextweb.com/news/chinese-dram-cxmt-corsair-ddr5-memory-prices) ⭐️ 6.0/10

海盗船已开始在其 DDR5 内存模组中使用长鑫存储的芯片，这可能导致 DDR5 内存价格下降。 这可能导致 DDR5 内存价格下降，从而惠及消费者和整个行业。 长鑫存储的采用是由于全球 DDR5 内存短缺，导致消费市场短缺。

telegram · zaihuapd · May 23, 11:17

**背景**: 长鑫存储是一家专门生产 DRAM 内存的中国半导体集成设备制造商。该公司正在扩大其生产能力以满足 DDR5 内存的日益增长的需求。海盗船采用长鑫存储的芯片是内存市场的一个重要发展，这可能导致 DDR5 内存价格下降。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/CXMT">CXMT</a></li>
<li><a href="https://en.wikipedia.org/wiki/DDR5_SDRAM">DDR 5 SDRAM - Wikipedia</a></li>

</ul>
</details>

**标签**: `#memory`, `#storage`, `#Corsair`, `#CXMT`, `#DDR5`

---

<a id="item-13"></a>
## [一位作家分享了他们的定制化 WriterDeck 设置，引发了关于专注和实用性的讨论](https://veronicaexplains.net/my-first-writerdeck/) ⭐️ 5.0/10

一位作家分享了他们的定制化 WriterDeck 设置，这些设置据说可以帮助他们专注，但社区却提出了关于实用性和潜在缺点的担忧 这场讨论突出了过度工程化和分散注意力的潜在问题，这可能会影响作家的生产力和整体福祉 WriterDeck 设置涉及定制操作系统、文本编辑器和其他软件以创建一个无干扰的写作环境

hackernews · hggh · May 23, 18:45 · [社区讨论](https://news.ycombinator.com/item?id=48250144)

**背景**: WriterDeck 是一项社区驱动的项目，用户将小显示器附加到键盘上以创建定制化的写作设备。设置可以根据个人偏好进行定制，但一些用户质疑其实用性和潜在缺点

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.youtube.com/watch?v=zcHL68JWXqc">Build your own writerDeck with your favorite Mecanical... - YouTube</a></li>
<li><a href="https://chuck.is/writerdeck/">My E-Ink Writerdeck Setup | Chuck Carroll</a></li>
<li><a href="https://www.writerdeck.org/">writerDeck.org | writerDeck</a></li>

</ul>
</details>

**社区讨论**: 社区讨论提出了对设置的实用性、潜在分散注意力和过度工程化的担忧，一些用户建议替代方案

**标签**: `#productivity`, `#writing`, `#customization`, `#personal anecdote`, `#software setup`

---

<a id="item-14"></a>
## [Android 17 将引入 Noto 3D 表情设计](https://www.androidpolice.com/google-has-confirmed-android-17-will-make-emoji-more-boring-and-i-think-its-missing-the-point-of-what-people-like-about-them/) ⭐️ 5.0/10

Android 17 将推出名为“Noto 3D”的全新表情符号，全面取代现有的平面设计。这套新表情旨在为线上交流增添“实体感”，避免情感表达显得过于平淡。 Noto 3D 表情设计的引入可能会改变人们在线表达方式，可能影响我们之间的交流和互动方式。 新设计是由人工手绘的，通过增加反光和颜色渐变来营造立体效果。它将首先在 Pixel 手机上更新，然后扩展到其他设备。

telegram · zaihuapd · May 23, 13:51

**背景**: 表情符号的交流方式在几年前已经发生了变化，早期的“blob”表情符号逐渐被苹果风格的设计取代，以实现跨平台的一致性。Noto 3D 的推出是谷歌努力使数字表达更具实体感的一部分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.croma.com/unboxed/googles-noto-3d-emoji-collection-unveiled">Google Noto 3 D emoji collection unveiled | Croma Unboxed</a></li>
<li><a href="https://www.neowin.net/news/google-introduces-noto-3d-its-new-emoji-set-to-make-digital-expression-feel-more-tangible/">Google introduces Noto 3 D , its new emoji set to make digital... - Neowin</a></li>

</ul>
</details>

**社区讨论**: 一些用户担心新设计的 3D 风格可能会让表情符号的象征意义减弱，并且在小屏幕上不如旧版清晰。

**标签**: `#Android`, `#Emoji`, `#Design`, `#Google`, `#Mobile`

---