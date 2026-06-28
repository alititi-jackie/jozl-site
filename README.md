# Jozl.com

Jozl.com 是 Jackie 的个人品牌与项目展示站。

## 当前路由

```text
/
/about/
/projects/
/projects/openaa/
/projects/tools/
/projects/go/
/projects/number/
/projects/premium-domains/
/projects/premium-domains/<domain-slug>/
/contact/
```

## 公共模块

- `assets/css/jozl-site.css`：全站移动端优先样式。
- `assets/js/jozl-site.js`：顶部导航、滚动条、底部导航、分享、返回顶部、域名筛选。
- `assets/js/domain-detail.js`：域名详情页公共渲染模块。
- `data/domains.json`：Premium Domains 数据源。

## 维护方式

新增或修改域名时，优先更新 `data/domains.json`。如果要在总页展示，需要同步在 `/projects/premium-domains/index.html` 中加入卡片；如果要有独立详情路由，需要新增对应的 `/projects/premium-domains/<slug>/index.html`。

旧的 `/domain/` 页面已改为跳转到新的 Premium Domains 页面，并在 `robots.txt` 中禁止搜索引擎继续抓取旧目录。
