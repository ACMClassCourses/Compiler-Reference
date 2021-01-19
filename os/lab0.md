# Lab 0: 开始写Lab之前的一些准备工作

**本部分占比xx%。**

## 环境安装
我们的操作系统目标运行平台为riscv，日常的模拟使用qemu进行模拟。这个作业需要如下的软件：`QEMU 5.0+, GDB 8.3, GCC, and Binutils`。

助教建议使用给出的docker镜像进行编译。（正式编译环境为docker的环境，默认运行的方式也为docker，参考./scripts/build.sh），以下给出的步骤为想要在本地安装工具链并且自主编译而提供。

### 在macOS上安装
第一步：确保你已经有了开发者工具，如果没有执行如下语句安装:

```
$ xcode-select --install
```

第二步：安装Homebrew包管理工具。

```
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

第三步：安装RISC-V编译工具链

```
$ brew tap riscv/riscv
$ brew install riscv-tools
```

在这一步你可能需要手动将编译工具链的位置加入到环境变量中，一般情况为`PATH=$PATH:/usr/local/opt/riscv-gnu-toolchain/bin`，具体路径请根据实际情况更改。安装这一过程可能会耗费较多时间并且可能需要反复执行。

第四步：安装qemu

```
$ brew install qemu
```

第五步：检查版本

```bash
$ riscv64-unknown-elf-gcc --version
riscv64-unknown-elf-gcc (GCC) 10.2.0
Copyright (C) 2020 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

$ qemu-system-riscv64 --version
QEMU emulator version 5.0.0
Copyright (c) 2003-2020 Fabrice Bellard and the QEMU Project developers
```