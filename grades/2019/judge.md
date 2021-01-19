# How to judge your code

## Instruction
Step 1: Use the given account to log into the system.

Step 2: Click 'Request Judge' to make a new judge attempt.

## About git repo
Make sure that the following public key is added to the repo that you commit.

## Environment
1. 构筑工具链
    - Java:
    ```
    openjdk 15.0.1 2020-10-20
    OpenJDK Runtime Environment (build 15.0.1+9-18)
    OpenJDK 64-Bit Server VM (build 15.0.1+9-18, mixed mode, sharing)
    ```
    - Clang: 
    ```
    clang version 6.0.0-1ubuntu2 (tags/RELEASE_600/final)
    Target: x86_64-pc-linux-gnu
    Thread model: posix
    InstalledDir: /usr/bin
    ```
    - gcc:
    ```
    gcc (Ubuntu 7.5.0-3ubuntu1~18.04) 7.5.0
    Copyright (C) 2017 Free Software Foundation, Inc.
    This is free software; see the source for copying conditions.  There is NO
    warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
    ```
    - Go:
    ```
    go version go1.14 linux/amd64
    ```
    - Python3:
    ```
    Python 3.6.9
    ```
    - CMake:
    ```
    cmake version 3.10.2

    CMake suite maintained and supported by Kitware (kitware.com/cmake).
    ```
    - Swift:
    ```
    Swift version 5.1.5 (swift-5.1.5-RELEASE)
    Target: x86_64-unknown-linux-gnu
    ```
    - awk:
    ```
    GNU Awk 4.1.4, API: 1.1 (GNU MPFR 4.0.1, GNU MP 6.1.2)
    Copyright (C) 1989, 1991-2016 Free Software Foundation.
    ```
    - sed:
    ```
    sed (GNU sed) 4.4
    Copyright (C) 2017 Free Software Foundation, Inc.
    ```
2. 一些有用的库

| Component | File Name | Path | Language |
|:-----------:|-----------|------|:----------:|
|ANTLR 4.9.1| antlr-4.9.1-complete.jar |`/ulib/java/antlr-4.9.1-complete.jar`|Java|
|ANTLR 4.9| antlr-4.9-complete.jar |`/ulib/java/antlr-4.9-complete.jar`|Java|
|ANTLR 4.8| antlr-4.8-complete.jar |`/ulib/java/antlr-4.8-complete.jar`|Java|
|ANTLR 4.7.2| antlr-4.7.2-complete.jar |`/ulib/java/antlr-4.7.2-complete.jar`|Java|
|ANTLR 4.7.1| antlr-4.7.1-complete.jar |`/ulib/java/antlr-4.7.1-complete.jar`|Java|
|ANTLR 4.7| antlr-4.7-complete.jar |`/ulib/java/antlr-4.7-complete.jar`|Java|
|ANTLR 4.6| antlr-4.6-complete.jar |`/ulib/java/antlr-4.6-complete.jar`|Java|


## FAQ
### Semantic Stage
1. 什么样的标准才算通过了Semantic测试？
    - 在[Compiler List](http://52.82.12.10:20500/compiler/list)页面上你的阶段（Stage）显示为Codegen意味着你通过了Semantic测试。
    - 对于某一个特定的测试，你可以查看详细页（[例子](http://52.82.12.10:20500/judge/detail/1/RxDNTPR8hakoTvfdRd4uZF)），右上角1-Semantic的通过率为100.0%

2. 我Request Judge之后一直显示GitFailed怎么办？
    - 你可以在[Judge Status](http://52.82.12.10:20500/judge/list/0)页面上，找到你的评测记录并且单击前面的序号查看详细信息。
        - 如果**Commit Information**为空，则很大可能是Git的仓库克隆过程出现了问题，请联系@peterzheng98助教。
        - 如果**Build Message**有内容，可以查看构建过程的stderr描述判断问题。

3. 我怎么知道我的某一个具体测试的情况？
    - 你可以在[Judge Status](http://52.82.12.10:20500/judge/list/0)页面上，找到你的评测记录并且单击前面的序号查看详细信息。在子页面上你可以点击某一个具体的测试点找到你的输出等信息。
    - 为了节约土豆的空间，我们限制输出了前 4096 字节，所以请不要把AST这种庞大的东西直接打出来。

4. 我到现在还是不知道怎么开工，怎么办？
    - 建议先阅读Yx的简单代码，[传送门](https://github.com/ZYHowell/Yx)。
    - 如果真的读不懂，抓紧时间私戳助教。

5. DDL之前我铁定写不完了，怎么办？
    - **如果真的有一些特殊情况，请联系@peterzheng98或者@ZYHowell助教，这种情况下会给出个别的调整方案。**
    - 没有特殊情况建议搞快点哈。

6. 我在DDL之后能通过一些点，会怎么处理？
    - 没有特殊情况建议搞快点哈。
    - 如果你通过了95个点或者88个点，那么我们会视作进度为0。因为这两个情况代表了你的编译器直接`return 0`和直接`return 1`的情况。
    - 如果你只有10个点以内没有通过，建议搞快点哈，当天就可以搞完了。
    - 如果你某个点超时了，建议优化你的算法。我们的编译时间有 15 秒。

7. 我就是不想开工，能48小时内完成吗？
    - Finish all. Believe the potential of human beings.
    - **Be careful with your liver.**
    - 身体是革命的本钱，年轻人不要老熬夜，早点开工每天写一点还能轻轻松松的哈。

8. 一些温馨小贴士：
    - bash里面涉及mkdir操作的，建议使用`mkdir -p`操作以防止第二次创建失败造成构建失败，同时在`build.bash`创建的文件**一定一定要插入`gitignore`**。
    - 提交之前请务必检查是否从`stdin`读取程序。
