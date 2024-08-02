# Linux下超轻量级Rust开发环境搭建 
### tages:
    - Rust
    - Rust开发环境搭建 
    - 安装Rust
    - 官网推荐安装

  
## 一、安装Rust   
Rust语言在国内逐步开始流行，但开发环境的不成熟依然困扰不少小伙伴。
结合我个人的使用体验，推荐一种超轻量级的开发环境：Rust + Helix Editor。运行环境需求很低，可以直接在Linux终端里进行代码开发。对于工程不是太过庞大的Rust项目，是一种不错的选择。
Linux环境下，先从Rust安装开始，流水帐。
我们选择从中国科学技术大学的镜像网站下载环境：   
```
$> export RUSTUP_DIST_SERVER=https://mirrors.ustc.edu.cn/rust-static $> export RUSTUP_UPDATE_ROOT=https://mirrors.ustc.edu.cn/rust-static/rustup

```
创建上面两个环境变量，让rustup的安装脚本从镜像站点下载开发环境：   
```
$> curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

```
如果需要代理才能访问互联网，可以这样：   
```
$> curl --proxy "socks5://ip:port" --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

按提示，运行一下：source "$HOME/.cargo/env"。

使用rustup命令再安装两个组件：

    $> rustup component add rust-src
    $> rustup component add rust-analyze

```
## 官网推荐安装   
使用 Rustup（推荐）   
您似乎正在运行 Windows。要使用 Rust，请下载安装器，然后运行该程序并遵循屏幕上的指示。当看到相应提示时，您可能需要安装[ Microsoft C++ 生成工具](https://visualstudio.microsoft.com/zh-hans/visual-cpp-build-tools/)。如果您不在 Windows 上，参看 “[其他安装方式](https://forge.rust-lang.org/infra/other-installation-methods.html)”。
[下载 rustup-init.exe（32位）](https://static.rust-lang.org/rustup/dist/i686-pc-windows-msvc/rustup-init.exe)
[下载 rustup-init.exe（64位）](https://static.rust-lang.org/rustup/dist/x86_64-pc-windows-msvc/rustup-init.exe)
Windows 的 Linux 子系统（WSL）   
如果您是 Windows 的 Linux 子系统（WSL）用户，要安装 Rust，请在终端中运行以下命令，然后遵循屏幕上的指示。   
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

```
### Rust 安装须知   
### 入门   
如果您希望通过一份详细的步骤指南来开始学习 Rust ，请阅读马上开始页面。   
### 用 rustup 管理工具链   
```
 Rust 由工具 rustup 安装和管理。Rust 有着以 6 星期为周期的 快速版本迭代机制，支持 大量平台，因而不同时期存在大量不同的 Rust 构建版本。 rustup 用于管理不同平台下的 Rust 构建版本并使其互相兼容， 支持安装由 Beta 和 Nightly 频道发布的版本，并支持其他用于交叉编译的编译版本。

如果您曾经安装过 rustup，可以执行 rustup update 来升级 Rust。

更多信息请查阅 rustup 文档。 

```
### 配置 PATH 环境变量   
```
 在 Rust 开发环境中，所有工具都安装在 ~/.cargo/bin 目录中，您可以在这里找到包括 rustc、cargo 和 rustup 在内的 Rust 工具链。

Rust 开发者通常会将该目录加入 PATH环境变量中。在安装过程中，rustup 会尝试配置 PATH。 由于不同平台、命令行 Shell 之间存在差异，rustup 中也可能存在 Bug，因此在终端重启或用户重新登录之前，rustup 对 PATH 的修改可能不会生效，甚至完全无效。

如果安装后在终端尝试执行 rustc --version 失败，那么，以上内容就是最可能的原因。 

```
### 卸载 Rust   
```
在任何时候如果您想卸载 Rust，您可以运行 rustup self uninstall。但我们会想念您的！ 

```
