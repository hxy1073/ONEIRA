# ONEIRA 梦境空间

ONEIRA 将梦境文字或语音整理为意象与场景信息，生成画面，并在浏览器中查看、漫游和解读三维梦境。

## 下载完整项目

完整源码、18 个梦的数据库以及图片、PLY、GLB 等资源放在本仓库的 Release 附件中。请下载 `ONEIRA-github-safe-2026-11-14.zip` 并完整解压。仓库公开后，任何人都能下载其中的梦境内容与资源。

## Windows 启动

需要 Node.js 22 或更高版本。在解压目录运行：

```powershell
cd oneira-server
npm ci --omit=dev
npm run web
```

然后打开 `http://127.0.0.1:8787/`。不配置外部服务也能查看包内已有梦境和三维场景。生成新内容需要自行配置 AI 服务和 WorldGen。

## 配置与安全

分享包没有真实 `.env`、`.worldgen.token`、API 密钥、服务器密码或固定的展厅服务器地址。复制 `oneira-server/.env.example` 为 `.env`，填入自己的密钥；如使用自己部署的 WorldGen，设置 `WORLDGEN_BASE_URL` 并在 `oneira-server/.worldgen.token` 写入自己的令牌。这两个本地文件不要提交到 GitHub。

完整的模块说明、数据位置、局域网配置和开发命令请见 ZIP 内的 `README.md`。
