# Lexury · 黄怿（Yi Huang）

个人博客和中英文学术履历。基于 [Fuwari](https://github.com/saicaca/fuwari) 和 Astro。

## 本地预览

使用 Node.js 22 或 24，以及项目声明的 pnpm 9.14.4。

    pnpm install --frozen-lockfile
    pnpm dev

请先构建再预览，以测试站内搜索。

    pnpm build
    pnpm preview

## 编辑内容

- 站名、简介、头像和横幅设置在 `src/config.ts`。
- 头像和横幅暂用模板素材，分别位于 `src/assets/images/demo-avatar.png` 和 `src/assets/images/demo-banner.png`。替换同名文件即可，换文件名时同步修改 `profileConfig.avatar` 或 `siteConfig.banner.src`。
- 中英文简历分别在 `src/content/spec/cv-zh.md` 和 `src/content/spec/cv-en.md`，公开地址为 `/cv/`。
- 博客文章放在 `src/content/posts/`。

## 发布到 GitHub Pages

`main` 保存源码，`gh-pages` 保存构建结果并对外发布。用有仓库写权限的 Git 凭据，从仓库根目录运行以下命令。

    pnpm build
    pnpm dlx gh-pages@6.3.0 --dist dist --branch gh-pages --dotfiles

正式构建使用 https://yihuanglab.top/ 作为站点地址，站点地图、RSS 和规范网址使用同一个域名。临时预览可通过 SITE_URL 覆盖构建地址。

Fuwari 的原始图源说明见[模板的关于页](https://github.com/saicaca/fuwari/blob/6d39b0d/src/content/spec/about.md)。
