# Node.js 二进制卸载

### Linux

```bash
$ version=12.16.2
$ sudo rm -rf "/usr/local/node-v${version}-linux-x64"
$ sudo rm -f "/usr/local/node"
$ sudo rm -f "/etc/profile.d/node.sh"
$ rm -rf ~/.npm
$ rm -f ~/.npmrc
$ rm -f ~/.yarnrc
$ rm -f ~/.vuerc
```

### macOS

```bash
$ version=12.16.2
$ sudo rm -rf "/usr/local/node-v${version}-darwin-x64";
$ sudo rm -f "/usr/local/node"
$ sudo rm -f "/etc/paths.d/node.sh"
$ rm -rf ~/.npm
$ rm -f ~/.npmrc
$ rm -f ~/.yarnrc
$ rm -f ~/.vuerc
```
