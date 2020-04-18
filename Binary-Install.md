# Node.js 二进制安装（推荐）

## 安装
安装包我们从[淘宝镜像](https://npm.taobao.org/mirrors/node)下载，根据主机选择合适的版本（以64位Linux为例）

## Linux

```shell
$ version=12.16.2
$ wget "https://npm.taobao.org/mirrors/node/v${version}/node-v${version}-linux-x64.tar.gz"
$ tar zxf "node-v${version}-linux-x64.tar.gz"
$ sudo mv "node-v${version}-linux-x64" /usr/local/
$ sudo ln -s /usr/local/node-v${version}-linux-x64 /usr/local/node
```

## macOS

```shell
$ version=12.16.2
$ wget "https://npm.taobao.org/mirrors/node/v${version}/node-v${version}-darwin-x64.tar.gz"
$ tar zxf "node-v${version}-darwin-x64.tar.gz"
$ sudo mv "node-v${version}-darwin-x64" /usr/local/
$ sudo ln -s /usr/local/node-v${version}-darwin-x64 /usr/local/node
```

## 配置PATH

### Linux

```shell
$ echo "export PATH=\"$PATH:/usr/local/node/bin\";" | sudo tee /etc/profile.d/node.sh
$ source /etc/profile
```

### macOS

```shell
$ echo "/usr/local/node/bin" | sudo tee /etc/paths.d/node.sh
$ sudo chmod 0444 /etc/paths.d/node.sh
```

重新打开终端（Terminal）

## 配置npm

node内置了npm，可直接使用

```shell
$ npm -v
```

通过以下命令使用npm淘宝镜像

```shell
$ sudo npm config -g set registry https://registry.npm.taobao.org
```

