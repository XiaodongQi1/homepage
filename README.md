# Xiaodong Qi Academic Homepage — GitHub Pages 静态版

基于当前 Sites 线上第 19 版导出（2026-10-16）。保留个人简介、研究方向、工作经历、教育经历、19 篇论文及作者、Awards、照片、三所学校 logo 和 11 个 PDF 链接。4 份本地论文 PDF 已随包附带，其余 7 个外部 PDF 链接保持原样。

目标仓库：`XiaodongQi1/xiaodongqi-homepage.github.io`。正式网址：`https://xiaodongqi1.github.io/xiaodongqi-homepage.github.io/`。

这是可以直接发布的 HTML/CSS 网站，无需 Node.js、npm、构建命令、服务器端程序或 GitHub Actions。

## 上传到 GitHub Pages

1. 解压压缩包。
2. 创建 GitHub **公开仓库**。个人主页建议命名为 `你的用户名.github.io`；普通项目仓库名称也可以，本版本支持仓库子路径。
3. 将解压后的**所有文件和目录**上传到仓库 `main` 分支的根目录，`index.html` 必须直接位于根目录。不要上传 ZIP 文件本身，也不要把整站再套进一层文件夹。
4. 确认 `.nojekyll` 也已上传。它是一个空文件，macOS Finder 默认隐藏点开头文件，可以用 `Command + Shift + .` 显示；也可在 GitHub 用 Add file → Create new file 新建 `.nojekyll`。
5. 在仓库 **Settings → Pages → Build and deployment** 中选择：
   - Source：**Deploy from a branch**
   - Branch：**main**
   - Folder：**/(root)**
6. 点击 Save，等待 Pages 完成部署，在 Pages 设置页点击 Visit site。

个人主页地址为 `https://你的用户名.github.io/`；普通项目仓库地址为 `https://你的用户名.github.io/仓库名/`。

GitHub 官方说明：
- [创建 Pages 网站](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)
- [设置发布分支](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

## 文件说明与日后修改

| 文件或目录 | 用途 |
| --- | --- |
| `index.html` | 全部主页文字、论文作者、PDF 链接、教育经历与奖项；可直接在 GitHub 网页编辑 |
| `styles.css` | 原站配色、布局、字体大小与响应式样式，可直接修改 |
| `base.css` | 原站编译后的基础样式，通常无需修改 |
| `portrait.jpg` | 个人照片 |
| `logos/` | NTU、华东师范大学、南京师范大学 logo |
| `papers/` | 4 份本地论文 PDF，文件名保持不变 |
| `favicon.svg` | 网站图标 |
| `og.png` | 原站分享图片，可在确定新域名后配置到分享元数据中 |
| `publications/`、`research/`、`experience/`、`activities/` | 兼容原站已有路径，跳转到相应主页分区 |
| `.nojekyll` | 指示 GitHub Pages 直接发布静态文件 |

所有本地图片、样式与 PDF 使用相对路径。更换仓库名称或使用仓库子路径时，无需批量修改链接。外部论文链接、Google Scholar、LinkedIn 和导师主页地址与原站一致。

新增论文时，在 `index.html` 中找到 `id="publications"`，复制一条 `<li>` 论文记录并修改内容；如需附带 PDF，将文件放入 `papers/` 并填写类似 `href="./papers/filename.pdf"` 的链接。

在 GitHub 提交修改后，Pages 会重新发布。当前 Sites 网站与这个静态副本独立，修改一处不会自动同步另一处。

## 本地预览

可以直接双击 `index.html` 查看，也可以在当前目录运行：

```bash
python3 -m http.server 8000
```

再打开 `http://localhost:8000/`。

## 分享信息

页面已经保留标题、简介、关键词等基础信息，`canonical`、`og:url`、`og:image` 和 `twitter:image` 已配置为 `https://xiaodongqi1.github.io/xiaodongqi-homepage.github.io/` 下的地址。将来改用其他域名时，同步修改这些元数据即可。

## 版本与核查范围

- 来源版本：Sites v19；源码提交 `4f5376ebc944ecec354ade54147e8283a112796f`。
- 本地 PDF 与原项目文件逐字节一致。
- 主页无需 JavaScript 即可显示全部内容，且不依赖原 Sites 域名加载样式、图片或本地 PDF。
- 不包含原项目的托管配置、开发依赖、Git 历史或认证信息。
