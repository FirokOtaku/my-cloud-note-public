# **Nvm 配置 Node 开发环境**

# 1. 下载安装

下载地址：[https://github.com/coreybutler/nvm-windows/releases](https://github.com/coreybutler/nvm-windows/releases)

![nvm](https://cdn.jsdelivr.net/gh/tomsunyx/my-cloud-img@main/cloud-note/nvm.png)

点击 nvm-setup.zip 安装包, 解压之后直接安装, 安装成功后会自动添加系统环境变量, 查看 nvm 版本号`nvm -v`

# 2. 配置 settings.txt

在安装好的 nvm 的目录下找到`settings.text`文件, 添加下面两行代码设置淘宝镜像

```
nvm node_mirror https://npm.taobao.org/mirrors/node/
```

# 3. 管理 nodejs

## 3.1 查看本地安装的所有版本

### 查看已安装 Node

```
nvm list
```

### 显示所有可下载的 Node

```
nvm list available
```

## 3.2 安装指定版本 Node

```
nvm install 16.13.0
```

## 3.4 使用指定版本 Node

```
nvm use 16.13.0
```

## 3.5 删除指定版本 Node

```
nvm uninstall 16.13.0
```

## 3.6 nvm 命令行提示

```bash
# 显示node是运行在32位还是63位
nvm arch

# 显示nvm版本号
nvm version

# 安装该版本号的nodejs
nvm install 版本号

# 卸载该版本的nodejs
nvm uninstall 版本号

# 使用该版本的nodejs
nvm use 版本号

# 查看已安装的nodejs版本
nvm list

# 显示可下载的nodejs版本号
nvm list available

# 开启nodejs版本管理
nvm on

# 关闭nodejs版本管理
nvm off

# 设置下载代理,不添加url, 显示当前代理, 将url设置为none时则移除代理
nvm proxy [url]

# 设置node镜像, 默认url是https://nodejs.org/dist/, 设置url后可在安装nvm的目录下settings.txt文件查看, 也可操作
nvm node_mirror [url]

# 设置npm镜像, 默认url是https://github.com/npm/cli/archive,设置url后可在nvm目录下settings.txt文件查看, 也可操作
nvm npm_mirror [url]

# 设置存储不同版本的nodejs目录, 如未设置, 默认使用当前目录
nvm root [path]
```

# 4. 改变 Node 的下载依赖包路径

安装完 nodejs 后, 也同时安装了 npm, npm 是 nodejs 中下载依赖包的命令, 管理 nodejs 中的依赖包, 下载依赖包时默认下载的路径是 `C:\Users\Administrator\AppData\Roaming\npm\node_modules`, 可以通过 `npm root -g` 查看

## 4.1 创建文件夹

```
node_global
```

```
node_cache
```

## 4.2 改变下载包位置

```
npm config set prefix "D:\Dev\nvm\node_global"
```

```
npm config set cache "D:\Dev\nvm\node_cache"
```

# 5. 配置 Node 环境变量

## 5.1 配置系统变量: NODE_GLOBAL

```
NODE_GLOBAL
```

```
D:\Dev\nvm\node_global
```

## 5.2 配置系统变量: path

```
%NODE_GLOBAL%
```

# 6. 安装 nrm

```
npm install -g nrm
```

# 7. 安装 pnpm

## 7.1 安装

```
npm install -g pnpm
```

## 7.2 配置仓库目录

```
pnpm config set store-dir "D:\Dev\nvm\pnpm_store"
```

# 8. 安装 rimraf

## 8.1 安装

```
npm install rimraf -g
```

## 8.2 使用

```
rimraf node_modules
```
