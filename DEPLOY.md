# 上线部署说明（Cloudflare Pages，免费）

本文件夹是一个**纯静态网站**，零依赖，整站约 1.4MB。两种上线方式任选其一。

## 方式一：控制台拖拽（最省事，不用命令行）
1. 打开 https://dash.cloudflare.com/ 并登录（没有账号用邮箱注册一个，免费）。
2. 左侧菜单 → **Workers 和 Pages** → **创建** → 选择 **Pages** → **上传资产（直接上传文件夹）**。
3. 把本文件夹（`resume-site`）整个拖进去，项目名随便起（如 `liangbeirui`）。
4. 构建命令、**构建输出目录都留空**（我们是纯静态，不需要构建）。
5. 部署完成后会得到一个 `xxx.pages.dev` 的网址，直接发给别人即可，电脑关机也能访问。

## 方式二：命令行（Wrangler）
在本文件夹所在目录执行（需要 Node.js）：
```bash
npx wrangler login      # 浏览器里点一下授权（只需一次）
npx wrangler pages deploy "E:/软件/workbuddy缓存/2026-10-21-03-32-44/resume-site"
```
部署完终端会打印公开网址。

## 改完内容后重新上线
- 方式一：回到 Pages 项目 → **上传资产** → 重新拖一次本文件夹覆盖即可。
- 方式二：再跑一次上面的 `wrangler pages deploy` 命令。

## 说明
- 免费额度足够：Pages 带宽免费、请求免费；视频/图片都在这 1.4MB 里，不会额外花钱。
- 自定义域名（如 `resume.你的域名.com`）可选：在 Pages 项目里绑域名即可，免费。
- 视频区现在用的是占位 B 站链接（`BV1xx411c7XD`），换成你自己的视频链接即可。
- Hero 里的邮箱目前是占位的 `Berry@foxmail.com`，请替换成真实邮箱/电话。
