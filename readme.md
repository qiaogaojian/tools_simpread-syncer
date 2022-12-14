# 简悦 · 同步助手 · 命令行 · 伪

模拟「简悦 · 同步助手」的功能，需要高级账户。

## Features

- 自动同步
- 增强导出
  - [x] Markdown
  - [x] HTML
  - [ ] PDF
  - [x] epub
  - [x] 邮件
  - [x] Kindle
- 稍后读加载本地文件

稍后读设置里请不要勾选「使用简悦 · 同步助手内置的解析器」，此功能无法实现。

## Usage

```sh
./simpread-sync -c <configPath>
```

config.json 默认配置如下：

```json
{
    "port": 7026,
    "syncPath": "",
    "outputPath": "",
    "smtpHost": "",
    "smtpPort": 465,
    "smtpUsername": "",
    "smtpPassword": "",
    "mailTitle": "[简悦] - {{title}}",
    "receiverMail": "",
    "kindleMail": ""
}
```

`syncPath` 必须填写，否则无法自动同步。

`outputPath` 如果不填写，默认为 `syncPath` 下的 output 文件夹。

## 自动启动

#### Windows

Windows 上可以计划任务，可参考[此文章](https://docs.syncthing.net/users/autostart.html#windows)。

推荐使用[git_syncer](https://github.com/qiaogaojian/tools_git-syncer)

#### [](https://github.com/j1g5awi/simpread-sync#docker)Docker

参见[使用 Docker 部署简悦同步助手 · 命令行](https://github.com/Kenshin/simpread/discussions/4312)