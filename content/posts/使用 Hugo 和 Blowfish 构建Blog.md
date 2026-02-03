---
title: "使用 Hugo 和 Blowfish 构建Blog"
---

可能每个博客站的第一篇文章都是记录它自己是如何诞生的，本站也不例外。

## Background

本网站在以下环境/版本构筑

* Windows 11 IoT 企业版 LTSC 24H2 26100.7623
* Hugo v0.147.4+extended
* Blowfish v2.97.0
* Git v2.51.1

特别感谢[ChatGPT Plus](https://chatgpt.com/)对于本项目的大力支持，没有他我或许得折腾很久

## 安装过程

### Hugo

```bash
choco install hugo-extended
```

### Blowfish

```bash
hugo new site mywebsite
cd mywebsite

git init
git submodule add -b main https://github.com/nunocoracao/blowfish.git themes/blowfish
```

删除 Hugo 自动生成的 `hugo.toml`，然后把主题里的 `themes/blowfish/config/_default/` 下的` *.toml `复制到你站点的 `config/_default/`

最终目录大概长这样：

```arduino
config/_default/
├─ hugo.toml
├─ languages.en.toml
├─ markup.toml
├─ menus.en.toml
└─ params.toml
```

剩下的是私人化的定制了，可惜我一向很懒，就先默认看着吧。
