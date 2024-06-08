# Kotori 一键安装包

<div align="center">
  <img src="https://pic.imgdb.cn/item/666313795e6d1bfa056104cd.jpg" alt="b_73db5f2400041414479b949766b08712.jpg" width="210">

## 看完后还不会安装 Kotori 的话，小鸟小姐就要哭了 www

</div>

## 使用方法

### 下载本仓库

- 方法 1：使用 git 克隆

```bash
git clone https://github.com/kotorijs/kotori-app.git
```

- 方法 2：直接下载压缩包并解压

[下载地址](https://github.com/kotorijs/kotori-app/archive/refs/heads/master.zip)

### 安装依赖

1.安装 Node.js

- 下载地址：[https://nodejs.org/zh-cn/](https://nodejs.org/zh-cn/)

  2.安装项目依赖

支持 `npm`、`yarn` 主流包管理器安装，`pnpm` 安装后可能存在启动问题，`cnpm`、`deno`、`bun` 未经测试，但理论仍可以进行安装并运行。先进入仓库根目录，输入以下任一命令安装：

```bash
npm i
```

强制更新所有包：

```bash
npm update -f
```

### 配置 `kotori.toml`

> 关于 kotori.toml 的详细介绍请参考 [配置详解](https://kotori.js.org/basic/config.html)

### 正式启动

仓库根目录下已提供两个启动文件：

- Windows 平台下使用 `start.bat`
- Linux/Mac 平台下使用 `start.sh`

启动完成后，在控制台内输入 `/status` 查看，输入 `/help` 查看帮助内容

### 进入 Webui

启动 Kotori 后，会在控制台看到以下类似信息：

```log
[server]: server start at http://127.0.0.1:720
```

此处的 `http://127.0.0.1:720` 即为 Kotori 网页控制台，第一次启动会提示设置用户名与密码，之后便可通过浏览器访问网页控制台进行登录。

### 安装适配器与插件

- 适配器：用于对接各个聊天平台，比如说你要用 qq 即安装 qq 适配器即可

- 插件：扩展机器人的各种功能

- 模块中心：[https://kotori.js.org/modules/](https://kotori.js.org/modules/)

此处收录了大部分的 Kotori 模块，选择自己喜欢的模块打开详情页查看说明，复制包名使用你的包管理器进行安装。以下指令会为你安装一些重要的基础插件：

### 更新 Kotori 与模块

一般地，在需要更新时使用以下命令即可进行更新：

```bash
npm update -f
```

此外，当变动较大时可重新重复上述安装步骤。

## 参考

- [kotorijs/kotori](https://github.com/kotorijs/kotori)
- [kotorijs/webui](https://github.com/kotorijs/webui)
- [Kotori Docs](https://kotori.js.org/)
