# Node.js 二进制安装（推荐）

## 安装
安装包我们从[淘宝镜像](https://npm.taobao.org/mirrors/node)下载，根据主机选择合适的版本（以64位Linux为例）

```bash
$ version=10.16.3
$ wget "https://npm.taobao.org/mirrors/node/v${version}/node-v${version}-linux-x64.tar.gz"
$ tar zxf "node-v${version}-linux-x64.tar.gz"
$ sudo mv "node-v${version}-linux-x64" /usr/local/
$ sudo ln -s "/usr/local/node-v${version}-linux-x64/bin/node" /usr/bin/node
$ sudo ln -s "/usr/local/node-v${version}-linux-x64/bin/npm" /usr/bin/npm
$ sudo ln -s "/usr/local/node-v${version}-linux-x64/bin/npx" /usr/bin/npx
```

## 安装 npm

node内置了npm，所以可以直接使用

```bash
$ npm -v
```

通过以下命令使用npm淘宝镜像

```bash
$ sudo npm config -g set registry https://registry.npm.taobao.org
```




