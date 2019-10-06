# Nvm 常用命令

```bash
# all node's versions
nvm ls

# Install a specific version number
nvm install v0.10.32

# Use the latest available 0.10.x release
nvm use 0.10

# Run app.js using node v0.10.32
nvm run 0.10.32 app.js

# Run `node app.js` with the PATH pointing to node v0.10.32
nvm exec 0.10.32 node app.js

# Set default node version on a shell
nvm alias default 0.10.32

# Undo effects of `nvm` on current shell
nvm deactivate

# Uninstall a version
nvm uninstall stable
```


