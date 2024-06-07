# Kotori 手把手安装教程

<video controls src="https://raw.githubusercontent.com/kotorijs/res/master/video/Kotori.mp4?raw=true" >
</video>

- [视频教程](https://raw.githubusercontent.com/kotorijs/res/master/video/Kotori.mp4?raw=true)

## 创建文件夹

名字任意即可，并进入该文件夹。

## 使用包管理工具安装

推荐使用 `npm` 或 `yarn`，请勿使用 `pnpm`，该方法下会有问题。

```sh
npm install kotori-bot
```

## 配置 `kotori.yml`

- Kotori 仓库地址：[https://github.com/kotorijs/kotori](https://github.com/kotorijs/kotori)

找到根目录下的 `kotori.yml` 复制到本地文件夹根目录，注意把 `global.lang` 中的 `en_US`（英文）改成 `zh_CN`（简体中文）。当然也可以直接复制下面的：

```yaml
# yaml-language-server: $schema=https://kotori.js.org/schema/1.3.0.json
global:
  port: 720
  lang: zh_CN
  command-prefix: /
  dirs:
    - ./node_modules/
    - ./node_modules/@kotori-bot/

adapter:
  cmd-test:
    extends: cmd
    master: 2333
    nickname: Kotarou
    age: 18
    sex: male
    self-id: 720

plugin:
  menu:
    content: test menu
```

> 关于 kotori.yml 的详细介绍请参考 [配置详解](https://kotori.js.org/basic/config.html)

## 创建启动文件

在根目录内新建文件 `start.后缀` 文件，对于具体后缀取决于你的操作系统：

- Windows 系统：`.bat`, `.cmd`, `.ps1` 均可
- Linux 系统：`.sh`

写入以下内容：

```sh
cd ./node_modules/kotori-bot
npm start
```

## 安装适配器与插件

- 适配器：用于对接各个聊天平台，比如说你要用 qq 即安装 qq 适配器即可，这里使用 cmd 适配器（命令行适配器）进行演示

- 插件：扩展机器人的各种功能

- 模块中心：[https://kotori.js.org/modules/](https://kotori.js.org/modules/)

此处收录了大部分的 Kotori 模块，选择自己喜欢的模块打开详情页查看说明，复制包名使用你的包管理器进行安装。以下指令会为你安装一些重要的基础插件：

```sh
npm install @kotori-bot/kotori-plugin-access @kotori-bot/kotori-plugin-adapter-sandbox @kotori-bot/kotori-plugin-adapter-cmd @kotori-bot/kotori-plugin-alias @kotori-bot/kotori-plugin-core @kotori-bot/kotori-plugin-helper @kotori-bot/kotori-plugin-status @kotori-bot/kotori-plugin-webui
```

## 设置 Webui

- Webui：即可视化的网页控制台，由 `@kotori-bot/kotori-plugin-webui` 模块提供

通过启动文件启动后，可发现控制台会提供一个链接，通过浏览器打开即可:

```log
[server]: server start at http://127.0.0.1:720
```

Webui 的默认账号为 `kotori`，默认密码为 `123456`。打开 `kotori.yml` 在 `plugin` 中加入以下字段即可更改默认账号密码：

```
webui:
	username: 账户名
	password: 密码（纯数字密码请加引号）
```

## 正式启动

启动完成后，在控制台内输入 `/status` 查看，输入 `/help` 查看帮助内容
