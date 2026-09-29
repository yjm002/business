# GPT Business 官网

这是一个使用 Astro 构建的单页静态网站，适合快速部署到 Vercel。页面中的业务介绍、服务内容和联系方式目前是占位提示；上线前请替换为准确且确认可以公开的信息。

## 本地开发

要求 Node.js `22.12.0` 或更高版本。

```bash
npm install
npm run dev
```

终端会显示本地预览地址，通常是 <http://localhost:4321>。

## 构建与预览

```bash
npm run build
npm run preview
```

Astro 会把静态网站生成到 `dist/`。

## 部署到 Vercel

1. 将 Astro 项目文件提交并推送到 GitHub 仓库 `yjm002/business` 的 `main` 分支。
2. 在 Vercel 选择 **Add New → Project**，导入该仓库。
3. Vercel 应自动识别 Astro。确认构建命令为 `npm run build`，输出目录为 `dist`，然后部署。
4. 先用 Vercel 提供的预览地址检查页面。

## 绑定 GoDaddy 域名

1. 在 Vercel 项目打开 **Settings → Domains**，添加 `gptbusiness.com`；需要使用 `www.gptbusiness.com` 时，也一并添加。
2. 按 Vercel 页面为你的项目显示的要求，在 GoDaddy 的 DNS 管理中添加或更新对应记录。记录类型和值以 Vercel 当前显示为准，不要照抄其他教程里的固定 IP。
3. 修改 DNS 前检查现有记录；不要随意删除 MX、TXT 等可能用于邮箱或域名验证的记录，只处理 Vercel 明确要求的冲突项。
4. 等待 Vercel 验证域名和 HTTPS 证书，再测试根域名与 `www` 域名。
