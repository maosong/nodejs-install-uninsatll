# Nvm Windows 版安装

这里介绍 Windows 版 nvm、node、npm 和 git 命令行的安装。

> 仅在 Windows 10 下测试通过。

## 安装 Git 命令行

这里我们使用 [git-for-windows](https://git-for-windows.github.io) ，下载 **Git-{VERSION}-64-bit.exe** 安装文件，按照默认提示安装。

安装完毕后在命令行提示符测试：

```bash
git --version
```

> Git 图形界面这里推荐 [SourceTree](https://www.sourcetreeapp.com) 。

## 安装 nvm

nvm 官方推荐的 Windows 版本 [nvm-windows](https://github.com/coreybutler/nvm-windows)，安装之前建议先卸载全局 nodejs 环境。

安装完毕后在命令行提示符测试：

```bash
nvm version
```

## 安装 node

打开命令行提示符，执行命令：

```bash
nvm install latest
nvm list # 查看安装的版本
nvm use {VERSION} # 激活安装的版本
node -v
```

> 编写本文档时 nvm-windows 版本是1.1.1，还不支持 node 镜像站点设置，安装速度会很慢！

## 安装 npm

nvm 会自动安装最新版 npm，所以可以直接使用

```bash
npm -v
```

通过以下命令使用 npm 淘宝镜像

```bash
npm config set registry https://registry.npm.taobao.org
```

