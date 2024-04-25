# Rust学习经验

作为经验分享，我不会写太多，一小篇足以

## 前言
Rust作为新时代的语言，其语法特性相对于以前的语言有着较大的差别，而且目前的Rust教程都是非常繁琐且没有梳理出一条很好的路线的，具体表现为既不是阶梯式也不是直接深入讲一个点，前后内容穿插令人无法理解。当然这也与Rust本身语言的特性相关，而并非完全是教程编写者的原因。

学习任何语言的思想都应该是读大量的项目源码，Rust也是如此，不过更应该先掌握Rust语法基础。


以下为Rust学习的部分参考资料：
[官方学习文档](https://doc.rust-lang.org/book/)

[Rust圣经(可以看作官方文档的中文替代版)](https://course.rs)

[THU-Rust学习建议](https://github.com/rcore-os/rCore/wiki/os-tutorial-summer-of-code-2020#step-0-%E8%87%AA%E5%AD%A6rust%E7%BC%96%E7%A8%8B%E5%A4%A7%E7%BA%A67%E5%A4%A9)

[Rustlings](https://github.com/rust-lang/rustlings)

## 我的建议

先通过学习文档练习语法，然后刷Rustlings，学习过程中参考教程代码or别人的代码，通过[crate doc文档](https://docs.rs/)查询相关crate源码

## Rust特色分享

### 所有权与生命周期

众所周知，Rust同C++一样是没有GC的，虽然C++在C++11有过GC提案，但是并未有编译器实现（可以当作没有），在C++23移除。C++可以通过RAII控制资源，那么Rust也有智能指针可以实现RAII，但是本文不讨论这个。本篇的主角是**所有权**。

既然我要聊所有权，那么我为什么要标注生命周期这个东西呢，那当然是因为所有权和生命周期息息相关，C++的内存安全问题基本上都是对于所有权和生命周期的错误使用导致的。

TODO!
PS:慢慢写