# Nvm 安装

## 卸载全局 node

安装 Nvm 之前建议删除已安装的 Node.js 和全局 Node.js 模块：

```sh
npm ls -g --depth=0 # 查看已经安装在全局的模块，以便删除这些全局模块后再按照不同的 node 版本重新进行全局安装
sudo rm -rf /usr/local/lib/node_modules # 删除全局 node_modules 目录
sudo rm /usr/local/bin/node # 删除 node
cd  /usr/local/bin && ls -l | grep "../lib/node_modules/" | awk '{print $9}'| xargs rm # 删除全局 node 模块注册的软链
```

## 安装 Nvm

官网推荐的两种安装方式：

```bash
version=0.33.6
curl -o- "https://raw.githubusercontent.com/creationix/nvm/v${version}/install.sh" | bash
```

安装器会在~/.bashrc文件中自动增加以下代码：

```bash
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh" # This loads nvm
```
我们在`NVM_DIR`上方加入nvm的淘宝镜像，提高node下载速度。⚠️注意，不是npm镜像！

```bash
export NVM_NODEJS_ORG_MIRROR=https://npm.taobao.org/mirrors/node; # nvm的淘宝镜像
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh" # This loads nvm
```

现在`重新打开终端`执行以下命令验证安装：

```bash
command -v nvm
```

## 安装 Node.js

```bash
nvm install stable # 安装最新稳定版
nvm current # 查看当前node版本
node -v
```
## 安装 npm

node内置了npm，所以可以直接使用

```bash
npm -v
```

通过以下命令使用npm淘宝镜像

```bash
npm config set registry https://registry.npm.taobao.org
```

