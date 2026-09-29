# GPT Business 网站

这是一个无需构建工具的静态网站起始页。业务介绍、服务内容和联系方式目前都是占位内容；对外发布前请先替换成准确且确认可以公开的信息。本页面不代表与任何 AI 公司或产品存在合作或隶属关系。

## 本地预览

在此目录运行：

```bash
python -m http.server 8000
```

然后访问 <http://localhost:8000>。

## 部署到 Vercel

1. 将 `index.html`、`styles.css` 和本 README 上传并推送到 GitHub 仓库 `yjm002/business` 的根目录。
2. 登录 Vercel，选择 **Add New → Project**，导入该 GitHub 仓库。
3. 这是纯静态网站，无需框架或构建命令；若 Vercel 要求选择框架，选 **Other**，输出目录使用项目根目录或界面默认值。
4. 部署成功后，先打开 Vercel 提供的预览地址检查页面。

## 绑定 GoDaddy 域名

1. 在 Vercel 项目打开 **Settings → Domains**，添加 `gptbusiness.com`；如果也要启用 `www.gptbusiness.com`，一并添加。
2. 按 Vercel 对你的项目显示的要求，在 GoDaddy 的域名 DNS 管理中添加或更新对应记录。记录类型和值以 Vercel 当前页面为准，不要使用其他教程里的固定 IP。
3. 修改 DNS 前先检查现有记录。不要随意删除 MX、TXT 等可能用于邮箱或域名验证的记录；只处理 Vercel 明确要求的冲突项。
4. 等待 Vercel 验证域名和 HTTPS 证书，再分别测试根域名和 `www` 域名。

DNS 可能需要一段时间传播。Vercel 仪表板会显示验证状态和该域名当前需要的记录。
