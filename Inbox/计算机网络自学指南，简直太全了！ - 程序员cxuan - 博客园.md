---
page-title: "计算机网络自学指南，简直太全了！ - 程序员cxuan - 博客园"
url: https://www.cnblogs.com/cxuanBlog/p/14414681.html
date: "2024-08-20 09:38:19"
---
今天偶然发现了**计算机网络如何自学**的问题，于是决定`怒答一波`。

关于计算机网络如何学习，我就拿自己亲身实践的来举例吧，因为我也自学学起的。

我觉得最重要的就是**看书(博客) + 实践**。

首先是看书。

## 书籍推荐

书也分为不同的层次，最基础的入门书籍有

### 网络是怎样连接的

这是我推荐给你的第一本书。  
![](https://img2020.cnblogs.com/blog/1515111/202102/1515111-20210219094610897-477583842.png)

这本书是日本人写的，它和《程序是怎样运行的》、《计算机是怎样跑起来的》统称为`图解入门`系列，最大的特点就是**风趣幽默，简单易懂**。这本书通过多图来解释浏览器中从输入网址开始，一路追踪了到显示出网页内容为止的整个过程，以图配文，讲解了网络的全貌，并重点介绍了实际的网络设备和软件是如何工作的。

本书图文并茂，通俗易懂，非常适合计算机、网络爱好者及相关从业人员阅读。

所以如果大家是新手的话，强烈推荐一下这本书。

日本人就爱图解，同样图解系列的入门书籍还有《图解 HTTP》、《图解 TCP/IP》。

### 图解 HTTP

这是我推荐给你的第二本书。

![](https://img2020.cnblogs.com/blog/1515111/202102/1515111-20210219094623884-573888377.png)

《图解 HTTP》是 HTTP 协议的入门书籍，当然 HTTP 也是属于计算机网络的范畴，这本书适合于**想要对 HTTP 有基本认知的程序员，同样也适合查漏补缺**。

这类书看起来就毫无难度了，不得不说图解系列是给小白的圣经，它能增强你的自信，让你觉得计算机其实`没那么难`，这是非常重要的。初学者，最怕的就是劝退了。

### 图解 TCP/IP

这是我推荐给你的第三本书

![](https://img2020.cnblogs.com/blog/1515111/202102/1515111-20210219094638246-47343288.png)

上面的图解 HTTP 是针对 HTTP 协议的，那么《图解 TCP/IP》就是针对 TCP/IP 协议簇中的协议了，这本书我已经看了 80% 了，还是比较系统的一本书，**基本上涵盖了 TCP/IP 协议簇中的所有协议知识了，这本书看完了完全就可以直接深入理解 TCP/IP 协议簇了**。

对于新手来说，最重要的一点就是帮助你理解，怎么简单怎么来，这样才能快速入门，对于快餐式的社会来说，快速理解当然是当仁不让的首选了。

如果上面这几本书你都搞定了的话，那你就可以读一下 《计算机网络：自顶向下方法》这本书了，这本书可以作为基础书籍也可以作为进阶书籍，这里我归为了进阶书籍，因为里面有一些章节不是那么好理解，比如介绍网络层的时候，会分为数据平面和控制平面，介绍 TCP 和 UDP 的时候，也会聊到一些原理性问题。

### 计算机网络：自顶向下方法

这是我推荐给你的第四本书

![](https://img2020.cnblogs.com/blog/1515111/202102/1515111-20210219094648890-2136264629.png)

这本书是一本计算机网络的`圣经`书籍，圣经就在于人人都应该读一下这本书，原著非常经典，翻译也很不错，我自己也马上就看完了，这本书会从顶层也就是网络层逐步下探到物理层，一层一层的带你入门，解释各层之间的协议，主要特征是什么，一个数据包的发送历程。这本书并不局限于某个具体的协议，而是从宏观的角度来看待计算机网络到底是什么，里面有一些专业名词，理解并掌握后会对深入学习计算机网络非常有用。

### 计算机网络：谢希仁版

这是我推荐给你的第五本书籍

![](https://img2020.cnblogs.com/blog/1515111/202102/1515111-20210219094701693-1787347325.png)

这本书是很多大学的教材，也是一本非常好的`进阶`书籍，这本书相对于自顶向下方法更多是对于通信网络的阐述。

这本书的特点是**突出基本原理和基本概念的阐述**，同时力图反映计算机网络的一些最新发展。本书可供电气信息类和计算机类专业的大学本科生和研究生使用，对从事计算机网络工作的工程技术人员也有参考价值

现在我们接着聊，如果上面这两本书随便一本看完了，那么恭喜你已经是一个`老手`了，你的网络基础能打败 90% 以上的人了，如果你还不满足的话，那你就需要继续深入，继续深入也是我推荐给你的提高书籍。

### HTTP 权威指南

这是我推荐给你的第六本书

![](https://img2020.cnblogs.com/blog/1515111/202102/1515111-20210219094711751-1596959403.png)

HTTP 权威指南是深入 HTTP 非常值得一看的书，这本书写的非常全了。

此书第一部分是 HTTP 的概述，如果你没有时间，通读第一部分就能让你应付普通的日常开发工作。

第二部分主要讲现实世界中 HTTP 的架构，也可以看作 HTTP 的全景图，包括 Web Server/Cache/Proxy/Gateway，是全书中精华的部分。

第三部分主要是 HTTP 安全，其中 Basic 和 Digest 概略看下即可，现实世界中用的应该不多。看 HTTPS 最好有一些计算机安全基础，这样会顺畅很多。

第四部分主要是关于 HTTP Message Body 的部分，包括 Content Negotiation，MIME Type，chunked encoding等，概略看下即可。

第五部分的内容，Web Hosting 可以认真看下，了解下 Virtual Host(话说我上学的时候一直搞不懂 Virtual Host，一个 IP 怎么能同时 Host 两个不同域名的 Web 页面呢)。

剩下三章已经过时，基本可以忽略。 最后的附录，可以用作边用边学的字典，如果你自己来写 Web Server，那么这一部分是极有价值的参考。

总而言之，无论你是前端还是后端，只要是 Web 相关的，那么此书就是必读的。

### TCP/IP 详解

这是我推荐给你的第七本书

这是一本被翻译耽误的经典书，两个硬核作者 Kevin R. Fall 和 W. Richard Stevens 被南开大学的某计算机系的译者给毁了。我第一开始读这本书以为是自己智商不够，原来是翻译`瞎TM翻`啊。语句不通且不说，您好歹走点心，改点措辞也行啊，纯碎是生搬硬套谷歌翻译啊，哎。

![](https://img2020.cnblogs.com/blog/1515111/202102/1515111-20210219094723993-396010590.png)

来看看豆瓣读者们对这本书的评价吧，比我有力量多了。

![](https://img2020.cnblogs.com/blog/1515111/202102/1515111-20210219094750050-1148675236.png)

这个回答给我看乐了，嗯，把这本书当作一本 Google 词典确实是一种不错的选择。

不过这本书确实是一本非常好的书，这本书的关注点在于 TCP/IP 协议栈上，可以说把 TCP/IP 讲透讲细了，比如讲 TCP 就会分别从连接管理、TCP 超时重传、TCP 拥塞控制、TCP 保活机制来讲起，不管你是从事哪个技术栈的研究，不管你是程序员还是网络工程师，这本书都是你值得一读的一本，不过要读最好还是读英文版。

TCP/IP 详解有三本，第二本是

![](https://img2020.cnblogs.com/blog/1515111/202102/1515111-20210219094756083-983513213.png)

这本黑皮书主要是介绍如何实现 TCP/IP 协议的，这本书很难入门。书中给出了约 500 个图例，15000 行实际操作的 C 代码，采用举例教学的方法帮助你掌握 TCP/IP 实现。

本书不仅说明了插口 API 和协议族的关系以及主机实现与路由器实现的差别。还介绍了 4.4BSD-Lite 版的新的特点。本书适用于希望理解 TCP/IP 协议如何实现的人，包括编写网络应用程序的程序员以及利用 TCP/IP 维护计算机网络的系统管理员。

第三卷是 tcp 事务协议、http、nntp 和 unix 域协议

![](https://img2020.cnblogs.com/blog/1515111/202102/1515111-20210219094804052-750846267.png)

这本书看的人就更少了。

第 3 卷详细介绍了当今 TCP/IP 程序员和网络管理员必须非常熟悉的四个基本主题： TCP 的扩展、Hyper 文本传输协议、网络新闻传输协议和 UNIX 域协议。与前两卷一样，本书介绍了 4.4BSD-Lite 网络代码中的示例和实现细节。

嗯。。。有一些沉重了，其实这些深入协议底层的书籍我们 99% 的人都接触不到，但是为了回答的完整性，我就都列出来了，这样的好处是让你能系统了解。

上面都是一些理论书籍，下面是稍微偏实战一些的书籍了。

计算机网络实战最有效的当然就属于抓包了，有很多抓包工具比如 **wireshark、sniffer、httpwatch、iptool、fiddle** 等，但是我用的和使用频率最高的应该就是 `wireshark` 了，关于 wireshark 还有几本实战方面的书你需要知道

### wireshark 数据包分析实战

这是我推荐给你的第八本书

![](https://img2020.cnblogs.com/blog/1515111/202102/1515111-20210219094811710-1565511991.png)

初学者必备，介绍了 wireshark 安装，嗅探网络流量，wireshark 的基本使用，用 wireshark 分析了一圈常用的TCP，UDP 协议，也简要分析了 HTTP 等应用层协议，概要介绍了一些 TCP 重传的机制，最后是无线分析。

整个书定位应该是入门级别的，基本上每章都是简要介绍，并没有特别深入大张阔斧地进行描述。文章行文思路清晰，译者的翻译水平也不错。**总的来说，是初步认识和了解 wireshark 的好书**。

### wireshark 网络分析就是这么简单

这是我推荐给你的第九本书

![](https://img2020.cnblogs.com/blog/1515111/202102/1515111-20210219094824819-1470162799.png)

读的时候你会忍不住笑的，区别于《Wireshark数据包分析实战》，本书就像一本侦探小说集，以幽默风趣的语言风格，借助wireshark以理性的思考来不断探险，根据蛛丝马迹来`侦破案情`。总结，读完数据包分析实战来读这本。

### Wireshark网络分析实战

这是我推荐给你的第十本书

![](https://img2020.cnblogs.com/blog/1515111/202102/1515111-20210219094832343-668124944.png)

其内容涵盖了 Wireshark 的基础知识，抓包过滤器的用法，显示过滤器的用法，基本/高级信息统计工具的用法，Expert Info 工具的用法，Wiresahrk 在 Ethernet、LAN 及无线 LAN 中的用法，ARP 和 IP 故障分析，TCP/UDP故障分析，HTTP 和 DNS 故障分析，企业网应用程序行为分析，SIP 多媒体和 IP电话，排除由低带宽或高延迟所引发的故障，认识网络安全等知识。

书籍推荐大概就是上面那些，除了书之外，还有一些视频、博客、官网网站可以学习

## 视频推荐

很烦微信公众平台怎么不支持外链呢，这个体验就很差啊。

今天在 b 站看视频的时候，看到了一句话**众所周知，b 站是用来搞学习的**，对于我们学习编程的童鞋来说，b 站有着非常多的学习资源，但是有一些质量并不是很好，看了之后不容易理解，这也是写这一篇文章的原因，为大家分

享一些质量超高的`计算机基础`的学习视频，往下看就完了。

### \*\*1. \*\*[计算机网络微课堂（有字幕无背景音乐版）（陆续更新中......）\_哔哩哔哩 (゜-゜)つロ 干杯~-bilibili](https://link.zhihu.com/?target=https%3A//www.bilibili.com/video/BV1c4411d7jb%3Fp%3D1)

学习计算机网络，我首先推荐的 UP 主`湖科大教书匠`，他讲的计算机网络十分通俗易懂，重点的地方讲的十分细致，并且还有一些实验，更好的是有考研 408 的难题的讲解，也是非常适合考研党，除了课程内容外还有很多习题讲解视频，特别赞的一点是每天动态里都会更新一道考研题，播放量也非常的多。

![](https://img2020.cnblogs.com/blog/1515111/202102/1515111-20210219094842061-891454751.png)

### **2.** [2019 王道考研 计算机网络\_哔哩哔哩 (゜-゜)つロ 干杯~-bilibili](https://link.zhihu.com/?target=https%3A//www.bilibili.com/video/BV19E411D78Q%3Fp%3D1)

既然说到了考研，那我就不得不提一下`王道考研`了，恭喜你发现了宝藏。王道考研的计算机网络视频，播放量非常多，而且老师是一位小姐姐，声音十分动听，声音这么好听的老师给你讲课，妈妈再也不用担心我的学习了呢，总之，这个视频的质量也非常高，弹幕全是对小姐姐的高度评价。（王道考研其他的视频也不错哦，暗示一下：操作系统，数据结构等等）

![](https://img2020.cnblogs.com/blog/1515111/202102/1515111-20210219094910837-1169053660.png)

### **3.** [韩立刚计算机网络 谢希仁 第7版 2020年12月\_哔哩哔哩 (゜-゜)つロ 干杯~-bilibili](https://link.zhihu.com/?target=https%3A//www.bilibili.com/video/BV1gV411h7r7%3Fp%3D1)

`韩立刚老师`所讲的计算机网络视频，内容比较多，但是讲解的通俗易懂，并且老师讲课的经验也十分的丰富。配套的教材是谢希仁老师的计算机网络教材，韩老师的最近的一个视频视频比较新，播放量还比较少，但是他讲的是真的不错，相比于王道考研所讲的计算机网络，韩老师更加细致一些。

![](https://img2020.cnblogs.com/blog/1515111/202102/1515111-20210219094920266-548949891.png)

### **4.** [计算机网络（谢希仁第七版）-方老师\_哔哩哔哩 (゜-゜)つロ 干杯~-bilibili](https://link.zhihu.com/?target=https%3A//www.bilibili.com/video/BV1yE411G7Ma%3Fp%3D1)

在计算机网络方面，我还想推荐的一位老师就是`方老师`，也是一位小姐姐老师。她的视频配套的教材也是谢老师的网络教材，在线看的小伙伴也超多，弹幕都是对方老师的评价。

![](https://img2020.cnblogs.com/blog/1515111/202102/1515111-20210219094928295-1106711736.png)

## 博客推荐

推荐几个不错的学习博客。

互联网协议入门-阮一峰：[http://www.ruanyifeng.com/blog/2012/05/internet\_protocol\_suite\_part\_i....](https://link.zhihu.com/?target=http%3A//www.ruanyifeng.com/blog/2012/05/internet_protocol_suite_part_i.html)

网络协议-兰亭风雨：[http://blog.csdn.net/ns\_code/article/category/1805481](https://link.zhihu.com/?target=http%3A//blog.csdn.net/ns_code/article/category/1805481)

HTTP协议：[http://www.cnblogs.com/TankXiao/category/415412.html](https://link.zhihu.com/?target=http%3A//www.cnblogs.com/TankXiao/category/415412.html)

Unix 网络编程：[http://blog.csdn.net/chenhanzhun/article/category/2767131/2](https://link.zhihu.com/?target=http%3A//blog.csdn.net/chenhanzhun/article/category/2767131/2)

TCP/IP详解：[http://blog.csdn.net/chenhanzhun/article/category/2734921/1](https://link.zhihu.com/?target=http%3A//blog.csdn.net/chenhanzhun/article/category/2734921/1)

计算机网络面试题：[http://blog.csdn.net/shadowkiss/article/details/6552144](https://link.zhihu.com/?target=http%3A//blog.csdn.net/shadowkiss/article/details/6552144)

国外优秀计算机网络站点：[http://www.tcpipguide.com/free/t\_TCPSlidingWindowAcknowledgmentSystemForDataTranspo-6.htm](https://link.zhihu.com/?target=http%3A//www.tcpipguide.com/free/t_TCPSlidingWindowAcknowledgmentSystemForDataTranspo-6.htm)

当然最硬核的就是 RFC 文档了 [RFC Index](https://link.zhihu.com/?target=https%3A//tools.ietf.org/rfc/index)

学习 HTTP ，必须要看一下 MDN 官网 [HTTP | MDN](https://link.zhihu.com/?target=https%3A//developer.mozilla.org/zh-CN/docs/Web/HTTP)

学习计算机网络，Cloudflare 你必须要去看 [https://www.cloudflare.com/zh-cn/learning/](https://link.zhihu.com/?target=https%3A//www.cloudflare.com/zh-cn/learning/)

GeeksforGeeks 学习计算机网络也非常不错 [Basics of Computer Networking - GeeksforGeeks](https://link.zhihu.com/?target=https%3A//www.geeksforgeeks.org/basics-computer-networking/)

Tutorialspoint 系统学习计算机，不仅仅局限于计算机网络 [Computer - Networking](https://link.zhihu.com/?target=https%3A//www.tutorialspoint.com/computer_fundamentals/computer_networking.htm)

国外优秀的学习网站不能少了 javapoint [Types of Computer Network - javatpoint](https://link.zhihu.com/?target=https%3A//www.javatpoint.com/types-of-computer-network)

> 以上这些网站都是我精心汇总的一些内容。

我自己也输出了一些关于计算机网络非常硬核的连载教程

作为配套，我写了一些关于计算机网络的文章，你也可以作为参考

计算机网络第一篇，聊一聊网络基础 ：[计算机网络基础知识总结](https://mp.weixin.qq.com/s?__biz=MzI0ODk2NDIyMQ==&mid=2247486242&idx=1&sn=fac49b0b79515a5ed6afd4b341aff87b&chksm=e999fe30deee772637e1c52fb9001c60e60a772e7adba6701329c81974e76c57bb7b2e570225&scene=21#wechat_redirect)

计算机网络第二篇，聊一聊 TCP/IP 基础：[TCP/IP 基础知识总结](https://mp.weixin.qq.com/s?__biz=MzI0ODk2NDIyMQ==&mid=2247486408&idx=1&sn=c332ae7ae448f3eb98865003ecade589&chksm=e999fedadeee77cc6281d1b170bd906b58220d6cd83054bc741821f4167f1f18ceee9ba0e449&scene=21#wechat_redirect)

计算机网络第三篇，这些应用层协议你也应该知道：[拿下计网协议后，我就是公园里最靓的仔](https://mp.weixin.qq.com/s?__biz=MzI0ODk2NDIyMQ==&mid=2247486507&idx=1&sn=622cc363b34bce54f4953076faa1cad6&chksm=e999f939deee702f2444df83ad9805de8c70fb88b89d299fdf0a82b3463e253f32372963c039&scene=21#wechat_redirect)

计算机网络第四篇，这篇文章写的时间很长了，图文精美，非常值得花时间阅读：[40 张图带你搞懂 TCP 和 UDP](https://mp.weixin.qq.com/s?__biz=MzI0ODk2NDIyMQ==&mid=2247487108&idx=1&sn=7b47f421bb1dee4edb357a10399b7fec&chksm=e999fb96deee7280a17bfff44c27ef11a60e93e48f9da738670a779ecf6accb5a6a4ebd3cbcc&scene=21#wechat_redirect)

计算机网络第五篇，网络层之路由器的基本概念：[路由器你竟然是这样的...](https://mp.weixin.qq.com/s?__biz=MzI0ODk2NDIyMQ==&mid=2247487351&idx=1&sn=9aa613589f85ce4c0c4142274e2a287d&chksm=e999fa65deee73732f97267db0e58d28925f4c57f7850d1e3b4633275385ac844e204fd03f03&scene=21#wechat_redirect)

计算机网络第六篇，了解一下 IP 基础知识的概念：[IP 基础知识总结](https://mp.weixin.qq.com/s?__biz=MzI0ODk2NDIyMQ==&mid=2247487569&idx=1&sn=b3a34ddd6cc99bc205a9bf7629a7753c&chksm=e999e543deee6c5528f275cdcf8da569ded23a79c926dd8310c3d14389f2c01a49519d96d88e&scene=21#wechat_redirect)

计算机网络第七篇，全方位了解一下网络层的知识：[我画了 40 张图就是为了让你搞懂计算机网络层](https://mp.weixin.qq.com/s?__biz=MzI0ODk2NDIyMQ==&mid=2247487683&idx=1&sn=e0949e72e039759545450852d8bc0ada&chksm=e999e5d1deee6cc7ab9e42b50329924fee39c45955516b406046605d27928825a0f628d13e7c&scene=21#wechat_redirect)

计算机网络第八篇，了解一下 ARP 协议是什么：[ARP，这个隐匿在计网背后的男人](https://mp.weixin.qq.com/s?__biz=MzI0ODk2NDIyMQ==&mid=2247487804&idx=1&sn=f001a24a308053b3723dfb12d36045ee&chksm=e999e42edeee6d383fbb411792e22e4028bb8c2441255786f50cf848443af7b1bd5e382078dc&scene=21#wechat_redirect)

计算机网络第九篇，DNS 协议是面试经常会考到的点，这篇带你深入了解一下 DNS 协议：[万字长文爆肝 DNS 协议！](https://mp.weixin.qq.com/s?__biz=MzI0ODk2NDIyMQ==&mid=2247487880&idx=1&sn=fd38ce30ae82fa7d08e5f83fabb9d497&chksm=e999e49adeee6d8c1adacbfe27dc59097e4cb9d39c6a04802b0fe61877653330e75721cbde0b&scene=21#wechat_redirect)

关于 HTTP 协议的相关硬核内容 ，可以作为参考，希望能帮到你

[看完这篇HTTP，跟面试官扯皮就没问题了](https://mp.weixin.qq.com/s?__biz=MzkwMDE1MzkwNQ==&mid=2247496030&idx=1&sn=82f56874f82f372af71e23a8e385f8cd&chksm=c04ae600f73d6f16d707c1d32b00e3f0d47e893c9cf59a2eb60ace418943aeb5c5c679cb27ea&scene=21#wechat_redirect)

[你还在为 HTTP 的这些概念头疼吗](https://mp.weixin.qq.com/s?__biz=MzkwMDE1MzkwNQ==&mid=2247496024&idx=1&sn=4af35bca85abae7e7637e835e833424b&chksm=c04ae606f73d6f104643c9ab85effe7e9471286fc6f76b8d3b9c41f9131458dfce27a4d78726&scene=21#wechat_redirect)

[震惊 | HTTP 在疫情期间把我吓得不敢出门了](https://mp.weixin.qq.com/s?__biz=MzkwMDE1MzkwNQ==&mid=2247496023&idx=1&sn=7281feaf0853d5465d7b082329b7f2d7&chksm=c04ae609f73d6f1f2bac28a3222f83ce24ef199e9869e887aa23f627f194d9d9cb43e1683ddb&scene=21#wechat_redirect)

[看完这篇 HTTPS，和面试官扯皮就没问题了](https://mp.weixin.qq.com/s?__biz=MzkwMDE1MzkwNQ==&mid=2247496004&idx=1&sn=348692f37a45eb3079ec5bba78227318&chksm=c04ae61af73d6f0c1dbc3e91a23fd0039fbd64c8d55182521e41bdbe4fb06e15de9995e0f5d5&scene=21#wechat_redirect)

[面试 HTTP ，99% 的面试官都爱问这些问题](https://mp.weixin.qq.com/s?__biz=MzkwMDE1MzkwNQ==&mid=2247495971&idx=1&sn=3a56fe5eca74b63a970cf345b18879d7&chksm=c04ae67df73d6f6b362e6cca1e4f23dad898cbbd3edb4effaf8c56119df6be1baa70cca55afe&scene=21#wechat_redirect)

[看完这篇 Session、Cookie、Token，和面试官扯皮就没问题了](https://mp.weixin.qq.com/s?__biz=MzkwMDE1MzkwNQ==&mid=2247495989&idx=1&sn=f9ef22964f1fde1e7f9fae2043fbd363&chksm=c04ae66bf73d6f7d43c1841e3a632fd40e4b73e7895aaeae4c487ea8a922555f48e5751adab7&scene=21#wechat_redirect)

这些文章也是在连载中，希望小伙伴能够喜欢，如果有任何关于网络方面的知识，欢迎与我一起探讨，你可以在

[成为最好的 bestJavaer](https://github.com/crisxuan/bestJavaer)

这个github 上联系到我，我的这个 github 也有一些不错的文章，希望能够对你有所帮助。

## 实验

借鉴一些大佬的回答，给你推荐一个斯坦福课程的实验

推荐 Stanford 课程 cs144，配合《计算机网络：自顶向下方法》（Computer Networking: A Top-Down Approach）。具体来说就是跟着 cs144 的课程安排走一遍，\*\*完成课程的 lab \*\*啦。

**另外，添加我的微信 becomecxuan，加入每日一题群，每天一道面试题分享，更多内容请参见我的 Github，成为最好的 bestJavaer，已经收录此篇文章，详情见原文链接**。

**我自己肝了六本 PDF，微信搜索「程序员cxuan」关注公众号后，在后台回复 cxuan ，领取全部 PDF，这些 PDF 如下**

[六本 PDF 链接](https://s3.ax1x.com/2020/11/30/DgOK6f.png)

![](https://img2020.cnblogs.com/blog/1515111/202011/1515111-20201130090550310-1032998206.png)