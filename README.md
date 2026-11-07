# 纸上涟漪 · Paper Ripples

把图片转成保留原色的字母画面，让文字像水面一样产生涟漪与摇晃。

这是完整的静态网站。HTML、CSS、JavaScript 都在 index.html 内，没有外部依赖、后端、数据库、API Key 或登录系统。

## 离线使用

下载并解压文件夹，用 Chrome、Edge、Safari 或 Firefox 打开 index.html。无需联网，无需安装依赖，也不需要启动本地服务器。

“离线使用”指保存这份 HTML 后在本机打开；在线网址未配置离线缓存，断网时不能保证直接访问网址。

## 功能

- 本地选择或拖拽图片，随时更换、清空。
- 每个字母采样原图对应区域的 RGB 颜色。
- 点按、长按、拖动产生可叠加的水波纹，不旋转。
- 波纹大小、频率、字母大小、摇晃幅度分别可调。
- 水中摇晃开关、自动演示、全屏、导出 PNG。
- 图片只在浏览器内处理，不会发送到服务器；刷新后需重新选择图片。

支持浏览器能解码的常见图片格式，如 JPG、PNG、WebP；单张最大 40 MB。无法读取的格式请先转换成 JPG 或 PNG。动图转换为静态文字画面。

## 部署到 GitHub Pages

### 准备

- 一个 GitHub 账号。
- 一个仓库，建议命名为 paper-ripples。
- 本文件夹里的 index.html、.nojekyll、README.md、.gitignore。

若使用 GitHub Free，可以选择公开仓库。请知道公开仓库的源码可被其他人查看；你在网页里选择的本地图片不会随源码上传。

### 网页上传方式

1. 在 GitHub 创建仓库 paper-ripples，或使用已有的专用仓库。
2. 打开仓库的 Code 页面，选择 Add file → Upload files。
3. 上传本文件夹中的文件，不要上传整个 ZIP，也不要在仓库里多套一层 paper-ripples-github 文件夹。index.html 必须直接位于仓库根目录。
4. 提交文件到 main 分支。
5. 打开 Settings → Pages。
6. 在 Build and deployment 中，把 Source 设为 Deploy from a branch。
7. Branch 选择 main，文件夹选择 / (root)，然后 Save。
8. 等待部署完成，使用 Pages 页面显示的网站地址访问。

普通项目仓库的网址形式为 https://你的用户名.github.io/paper-ripples/ 。这只是格式示例，最终以 GitHub 显示的地址为准。

.nojekyll 是空文件，用于告诉 GitHub 直接发布静态文件。macOS 可能默认隐藏它，可以按 Command + Shift + . 显示隐藏文件。该项目的 index.html 自身不依赖 Jekyll，即使网页上传时漏掉此空文件，入口页面仍可使用。

### 后续更新

修改 index.html 后重新上传并提交到 main，GitHub Pages 会重新发布。离线版本也只需替换 index.html。

## 常见问题

- 404：检查 index.html 文件名全为小写，且位于 main 分支根目录；Pages 发布目录应为 / (root)。
- 打开的是源码：访问 Pages 显示的 github.io 网站地址，而不是 github.com 仓库文件页面。
- 页面仍是旧版本：确认最新部署已完成，再刷新或强制刷新。
- 没有图片：初始空白是正常的，选择一张本地图片即可开始。
- 图片变浅：字母之间有留白，整体覆盖率低于原图；字母本身仍保留采样颜色。

## 文件说明

- index.html：完整网页，既是 GitHub Pages 入口，也是离线版。
- .nojekyll：静态发布标记。
- .gitignore：避免提交常见系统临时文件和本地配置。
- README.md：项目说明及部署步骤。

没有附加开源许可证；如果以后决定以 MIT 等许可证开放源码，可再自行添加 LICENSE。

## 官方部署说明

- [配置 GitHub Pages 发布来源](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
- [创建 GitHub Pages 网站](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)
