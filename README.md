# Jinhan Gao — academic homepage

Live site: https://gaojinhan.github.io/

Based on [Minimal Light](https://github.com/yaoyao-liu/minimal-light), with a separate Working Papers section. The original theme license is in LICENSE.

## 如何更新

直接在 GitHub 打开文件，点击铅笔图标，修改后点击 **Commit changes**。推送到 main 后，GitHub Actions 会自动构建并发布。无需在本地安装软件。

| 内容 | 文件 |
| --- | --- |
| About Me、Research Interests，以及想新增的正文栏目 | `index.md` |
| 姓名、单位、邮箱、GitHub、LinkedIn | `_config.yml` |
| 已发表论文 | `_data/publications.yml` |
| Working Papers | `_data/working_papers.yml` |
| 照片 | `assets/img/jinhan-gao.jpg` |
| 字体、间距、照片显示裁切 | `assets/css/custom.css` |

`index.md` 开头的三行和末尾两行 `{% include ... %}` 要保留，其余正文可以自己编辑。

使用 `## 标题` 新增栏目、`**文字**` 加粗、`[名称](https://...)` 插入超链接。

没有 News 或 Services 内容时无需添加空栏目。Google Scholar 和 Twitter 不显示。

## CV

上传选定的 PDF 到 `assets/files/jinhan-gao-cv.pdf`，然后在 `_config.yml` 取消 `cv_link` 一行的注释。未指定公开版 CV，因此当前没有显示下载入口。

## Publications / Working Papers

论文数据彼此独立，改简介不会影响论文列表。每篇论文可选字段包括 `doi`、`pdf`、`code`、`page`、`bibtex`、`status`；没有的链接不要填写。已发表论文移入 publications.yml，未发表稿件保留在 working_papers.yml。本站不会自动抓取 Google Scholar。

## Local preview

Use Ruby 3.3 or newer:

```sh
bundle install
bundle exec jekyll serve --host 127.0.0.1 --port 4000
```

Open http://127.0.0.1:4000/ . GitHub Pages uses `.github/workflows/pages.yml`.

## Sources

- MARS: https://cordis.europa.eu/project/id/101091783
- CHARM: https://cordis.europa.eu/project/id/876362
- ZDMP: https://cordis.europa.eu/project/id/825631
- Publication metadata checked against publisher/Crossref records on 2026-11-13.
- Biography and working-paper selection confirmed by Jinhan Gao on 2026-11-13.
