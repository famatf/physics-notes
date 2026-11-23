# LYC's notes

这是一个用 Jekyll 编译的个人笔记站。笔记的 Markdown 源文件集中在 `_notes/`，首页按日期倒序自动列出所有笔记。

## 本地编译

安装 Ruby 3.4 和 Bundler。Windows 可以使用 RubyInstaller with Devkit。在仓库目录执行：

```sh
bundle install
bundle exec jekyll build
```

生成的网站在 `_site/`，可直接打开 `_site/index.html`。运行 `bundle exec jekyll serve` 后，也可在浏览器访问 `http://localhost:4000/` 预览修改。

## 编辑和添加笔记

直接编辑 `_notes/` 中的 Markdown 文件。添加笔记时，在该目录新建文件，例如 `example.md`：

```markdown
---
title: 新笔记
date: 2026-11-23
---

在这里写正文。
```

文件名决定编译后的地址，例如 `example.md` 生成 `example.html`。行内公式用 `$...$`，独立公式用 `$$...$$`。图片、KaTeX 脚本和字体均随仓库提供。首页模板为 `index.html`，About 页为 `about.md`。
