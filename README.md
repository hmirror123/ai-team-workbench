# AI Team Workbench · AI 团队工作台

在自己的电脑或服务器运行一个网页工作台。总管、研究员、工程师、审核员各有持续会话和角色记忆，按项目公开交接。任务保留工具结果、交付文件、审核结论和报错。

[下载完整源码 ai-team-workbench-source.zip](./ai-team-workbench-source.zip?raw=1)

源码包包含网页、Node.js 服务、DeepSeek Harness 协作插件、依赖锁文件、安装脚本、测试和示例。解压后的 `ai-team-workbench/README.md` 提供完整说明。项目是单用户工作台，使用固定版本的 DeepSeek Harness `0.2.2-rc.4`。

## 运行

需要 Linux、Node.js 24.9 或更新版本、npm、GNU coreutils 和 unzip。下载源码包后运行：

```bash
unzip ai-team-workbench-source.zip
cd ai-team-workbench
npm ci --ignore-scripts
npm run setup
npm start
```

首次配置请在终端设置网页口令并输入自己的 DeepSeek API Key，然后打开 `http://127.0.0.1:3358`。使用远程服务器时，可按源码包 README 建立 SSH 转发。需要常驻运行时，可以按 README 安装 systemd 用户服务。

## 验证

安装依赖后可执行 `npm test`、`npm run test:native` 和 `npm run test:ui`。测试使用本地模拟模型，不产生真实 API 调用。`examples/review-sample.csv` 提供一份合成表，适合体验独立复核、修订和正式审核。

源码包 SHA-256：`bd784bc28d820dadae3a42dd653e9abdbefe3d05c2b6c587d07c4a86074f89d7`。

工作台源码使用 MIT 许可证。DeepSeek Harness 作为依赖单独安装，适用其自身许可证。
