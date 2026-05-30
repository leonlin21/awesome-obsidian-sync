# Obsidian 同步方案怎么选

Obsidian 的笔记都存在本地文件夹里。同步方案选错后，常见问题是冲突文件、附件丢失、移动端不同步、旧版本覆盖新版本。

先看这篇总览：

- [Obsidian 10 种主流同步方案对比](https://21obsidian.com/blog/obsidian-sync-methods-comparison)

## 快速选择

| 使用场景 | 推荐方案 | 完整教程 |
| --- | --- | --- |
| 想省心，能接受订阅 | Obsidian Sync | [官方同步教程](https://21obsidian.com/blog/obsidian-official-sync) |
| 只用 Mac、iPhone、iPad | iCloud | [iCloud 同步教程](https://21obsidian.com/blog/obsidian-icloud-sync) |
| 只在电脑之间同步 | 百度网盘同步空间 | [百度网盘同步教程](https://21obsidian.com/blog/obsidian-baidu-netdisk-sync) |
| 已经在用 OneDrive | Remotely Save + OneDrive | [OneDrive 同步教程](https://21obsidian.com/blog/obsidian-onedrive-sync) |
| 已经在用坚果云 | Nutstore Sync | [坚果云同步教程](https://21obsidian.com/blog/obsidian-nutstore-sync) |
| 想用对象存储 | Remotely Save + 腾讯云 COS | [腾讯云 COS 同步教程](https://21obsidian.com/blog/obsidian-remotely-save-sync) |
| 有 NAS 或 WebDAV | Remotely Save + WebDAV | [飞牛 NAS WebDAV 教程](https://21obsidian.com/blog/obsidian-remotely-save-fn-connect-webdav) |
| 想自建实时同步 | LiveSync + CouchDB | [LiveSync 自建同步教程](https://21obsidian.com/blog/obsidian-livesync-fn-nas-couchdb) |
| 想点对点同步 | Syncthing | [Syncthing 同步教程](https://21obsidian.com/blog/obsidian-syncthing-sync) |
| 想保留完整版本历史 | Git + GitHub | [Obsidian Git 同步教程](https://21obsidian.com/blog/obsidian-git-sync) |

## 同步前先做的事

配置任何同步工具前，先复制一份完整 Vault 备份。

同步工具会把变化传到其他设备。正常修改会同步，错误删除、空文件、冲突文件也可能同步过去。重要笔记不要只依赖同步服务，至少保留一种能恢复旧版本的办法。

## 各方案适合谁

### Obsidian Sync

适合想少折腾的人。官方服务配置最简单，跨 Mac、Windows、iPhone、Android 都比较省心，缺点是需要订阅。

- [Obsidian 官方同步教程](https://21obsidian.com/blog/obsidian-official-sync)

### iCloud

适合 Apple 设备为主的人。Mac、iPhone、iPad 之间上手很快，重点是从 iPhone 端创建正确的 Obsidian iCloud 文件夹。

- [Obsidian iCloud 同步教程](https://21obsidian.com/blog/obsidian-icloud-sync)

### 百度网盘

适合只在电脑之间同步的人。它不适合手机端同步，使用前也要确认账号有可用的同步空间权益。

- [Obsidian 百度网盘同步教程](https://21obsidian.com/blog/obsidian-baidu-netdisk-sync)

### OneDrive

适合已经在用微软云盘的人。通过 Remotely Save 连接 OneDrive，能覆盖 Mac、Windows、iPhone 和 Android。

- [Obsidian OneDrive 同步教程](https://21obsidian.com/blog/obsidian-onedrive-sync)

### 坚果云

适合已经在用坚果云的人。Nutstore Sync 配置比较简单，但免费版流量和请求限制需要注意。

- [Obsidian 坚果云同步教程](https://21obsidian.com/blog/obsidian-nutstore-sync)

### Remotely Save + 对象存储

适合愿意配置云服务的人。腾讯云 COS 这类 S3 兼容存储成本低，但需要自己处理存储桶、密钥和权限。

- [Obsidian Remotely Save 同步教程](https://21obsidian.com/blog/obsidian-remotely-save-sync)

### NAS WebDAV

适合已经有 NAS 的人。WebDAV 可以让数据放在自己的设备或私有服务里，配置难度比普通网盘高一点。

- [Obsidian 飞牛 NAS 同步教程](https://21obsidian.com/blog/obsidian-remotely-save-fn-connect-webdav)

### LiveSync

适合能接受自建服务的人。它可以做到接近实时同步，但要部署 CouchDB，排查成本也更高。

- [Obsidian LiveSync 自建同步教程](https://21obsidian.com/blog/obsidian-livesync-fn-nas-couchdb)

### Syncthing

适合不想依赖云盘的人。它通过设备之间直接同步文件，配置时要注意设备在线状态、文件夹共享和冲突处理。

- [Obsidian Syncthing 同步教程](https://21obsidian.com/blog/obsidian-syncthing-sync)

### Git + GitHub

适合熟悉 Git 的人。它的优势是版本历史清楚，代价是要理解提交、拉取、推送和冲突处理。

- [Obsidian Git 同步教程](https://21obsidian.com/blog/obsidian-git-sync)

## 插件和工具

### Obsidian 插件

- [Remotely Save](https://github.com/remotely-save/remotely-save)：支持 S3、WebDAV、OneDrive、Dropbox、Google Drive、Box、pCloud 等后端的同步插件。
- [Self-hosted LiveSync](https://github.com/vrtmrz/obsidian-livesync)：基于 CouchDB 的 Obsidian 自建同步插件。
- [Obsidian Git](https://github.com/Vinzent03/obsidian-git)：在 Obsidian 里使用 Git，支持提交、拉取、推送。
- [Nutstore Sync](https://github.com/nutstore/obsidian-nutstore-sync)：通过坚果云 WebDAV 同步 Obsidian 的插件。
- [BRAT](https://github.com/TfTHacker/obsidian42-brat)：从 GitHub 仓库安装和更新 Obsidian 插件。

### 同步工具

- [Syncthing](https://github.com/syncthing/syncthing)：开源点对点文件同步工具。
- [Syncthing for macOS](https://github.com/syncthing/syncthing-macos)：Syncthing 官方 macOS 应用包。
- [Syncthing-Fork for Android](https://github.com/researchxxl/syncthing-android)：Android 上的 Syncthing 包装应用。
- [Sushitrain](https://github.com/pixelspark/sushitrain)：iOS 上使用 Syncthing 协议的同步应用。
- [GitSync](https://github.com/ViscousPot/GitSync)：移动端 Git 客户端，可以把本地文件夹和远程 Git 仓库同步。

## 官方文档

- [Obsidian Sync Help](https://help.obsidian.md/sync)
- [Obsidian Community Plugins Registry](https://github.com/obsidianmd/obsidian-releases)
- [Syncthing Documentation](https://docs.syncthing.net/)

## 相关教程

- [Obsidian 全平台插件安装教程](https://21obsidian.com/blog/obsidian-plugin-install-guide)

## 常见风险

- 不要让多个同步工具同时同步同一个 Vault。
- 不要在同步没完成时立刻换设备继续编辑。
- 不要只同步 Markdown 文件，附件、配置和子文件夹也可能被 Obsidian 用到。
- 不要在没有备份的情况下批量删除冲突文件。
- 不要把包含私人笔记、Token、API Key 的仓库公开到 GitHub。

## 反馈

如果某篇教程步骤过期、插件仓库迁移、工具停止维护，或者某个同步方案出现新的限制，可以开 issue 说明。

请不要在 issue 里放私人 Vault 内容、邮箱、Token、服务器地址、带有个人信息的截图或真实笔记正文。

## License

这份目录使用 [CC BY-NC-SA 4.0](LICENSE.md)。

代码片段、命令模板和脚本示例使用 [MIT License](LICENSE-CODE.md)。
