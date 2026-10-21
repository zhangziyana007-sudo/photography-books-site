# 摄影书籍资源库

725 本摄影书的网盘资源导航页：从基础入门、器材、用光、构图，到人像、风光、后期、教材、摄影史，共 19 个分类、约 18.9 GB。全部书籍为作者本人百度网盘分享，链接已内嵌提取码，点开即是转存 / 下载页。

在线演示：<https://zhangziyana007-sudo.github.io/photography-books-site/>

## 页面能力

- 单文件静态页（`index.html`，内嵌全部书目数据），无需构建、无后端、无第三方脚本
- 书名 / 关键词搜索（`/` 快速定位）、按分类顺序（推荐学习路径）/ 书目数 / 体积排序、分类标签横滑筛选
- 每本书配百度网盘自己渲染的真实预览封面（719 张，缺预览的少数条目用渐变占位）
- 多册书合并为一个单元并标注「全 N 册」
- 移动端适配：两列大封面网格、搜索框 16px 防自动缩放、分类条横向滚动、悬停效果仅在桌面生效

## 目录结构

```
index.html      页面本体，书目数据以 JSON 内嵌
covers/         719 张封面，按书目序号命名（0001.jpg … 0725.jpg）
.nojekyll       关闭 Jekyll 处理，作为纯静态资源直接发布
```

## 本地预览

```bash
python -m http.server 4173 --bind 127.0.0.1
```

打开 <http://127.0.0.1:4173/> 即可。

## 部署到 GitHub Pages

仓库已开启 Pages（Settings → Pages，来源为 `main` 分支根目录）。手动重开：

```bash
gh api -X POST repos/OWNER/REPO/pages --input - <<'JSON'
{"build_type":"full","source":{"branch":"main","path":"/"}}
JSON
```

推送更新后 Pages 会在 1 分钟内重新发布，访问地址为 `https://<user>.github.io/<repo>/`。

## 说明

- 链接指向作者自有网盘目录，若某条提示失效，说明该分享已被百度和谐，可开 Issue 求补档。
- 页面只是导航，不存放书籍文件本身；如涉及版权方异议，请开 Issue 联系，会对应移除条目。
