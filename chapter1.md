# Night+ Tech Review - Mar. 23th

Night+ 的前身是夜点娱乐这个基于微信公众号的微信APP产品，经过一段时间的摸索和探究，线上线下的业务推动，产品逐渐有了一定的用户基础，随着团队的丰满，新的想法不断的被提出来，随之而来的就是大量的开发需求和迭代任务，这对技术团队来说，从开发理念到技术架构本身都是一个不小的挑战。而之前的技术基本上是由一个PHP的外包团队主导开发和维护，技术人员本身的能力不错，但毕竟整个项目都是基于一个从POC（Proof of concept）阶段就开始迭代的项目上反复开发，垒砌，补丁，总有一种摇摇欲坠的感觉。再加上外包团队与核心团队一个在帝都一个在魔都，这样远程的协作，对需求的解构和项目的沟通都是很大的挑战。

从去年10月份起，我们就发现老的架构虽然基本功能迭代效率尚可，但是一旦产品有新的开发或者重大调整，就变得举步维艰。 所以我们考虑，是时候按照快速迭代，灵活稳定，服务可拓展，资源有弹性的基本思路来重新设计我们的技术架构和团队了。将原来非常“庞大”而繁杂的产品线整理出来，同时引入一些比较流行而利于高效迭代的技术架构来替代老的框架，而保证老的功能继续运行，新的功能得以拓展，全部加起来是如此痛苦的一件事情，但是又势在必行。于是，艰难的技术选型和实践就开始了。

微服务是我们首先选定的整体技术架构，考虑到产品马上会进入一个快速拓展的阶段，诸多功能模块概念已经初见雏形，但不论是代码拓展能力和开发资源拓展能力都非常有限，于是我们非常小心的决定将各个功能模块按照职能 和 



同时预计到O2O产品用户角色相对比较复杂（实际到目前为止，已经有大小角色超过 8 种），



从组织架构来说，我们认为服务商模式有它的好处，比如说组织架构灵活，对于比较新的技术需求，服务商模式可以规避掉很多不必要的短期招聘，培训压力，也不需要因为手里有限的技术团队能力而在产品上委曲求全。但是

