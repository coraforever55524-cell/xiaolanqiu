# 小篮球训练台 · 手机部署包

把这一整个文件夹传到任意免费的静态网站托管上，手机浏览器打开链接后点“添加到主屏幕”，就会像 App 一样全屏使用，并支持离线。

## 上传到 GitHub Pages（免费）

1. 注册 https://github.com （免费），登录后点右上角 + → New repository。
2. 仓库名填 `xiaolanqiu`，选 **Public**，点 Create repository。
3. 在新仓库页面点 **uploading an existing file**，把这个文件夹里的全部内容拖进去（index.html、manifest.webmanifest、sw.js、icons 文件夹、README.md），点 Commit changes。
4. 进仓库 **Settings → Pages**：Source 选 `Deploy from a branch`，Branch 选 `main`、目录选 `/ (root)`，点 Save。
5. 等 1–2 分钟，页面顶部会显示网址：`https://你的用户名.github.io/xiaolanqiu/`。
6. 手机浏览器打开这个网址 → 菜单里选“添加到主屏幕”。桌面上会出现小篮球图标，点开即用。

> GitHub Pages 在国内偶尔访问慢。打不开就换 Cloudflare Pages：登录 https://dash.cloudflare.com → Workers & Pages → Create → Pages → Upload assets，把文件夹拖进去，同样是免费。

## 注意

- 数据存在手机浏览器本地。添加到主屏幕后，请一直用同一个入口打开，别换浏览器、别清理浏览数据，否则记录会丢。
- 重要教案用应用里的“打印”存成 PDF 备份。
- 首次打开需要联网，之后可离线使用（Service Worker 已缓存全部文件）。
- 更新版本：改完 index.html 后，把 sw.js 里的 `xlq-v1` 改成 `xlq-v2` 再上传，手机下次打开就会拿到新版本。
