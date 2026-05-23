# CLAUDE.md

## 发布流程（自动 push 到 main）

每期书单完成后，自动执行：
1. 在 `main` 分支上 add / commit / push
2. commit message: `Add Issue {N}: {本期主题}`
3. 不需要再问"要不要 push"——默认 push

GitHub Pages 从 `main` 分支发布，所以最终必须推到 `main`。

## Git 配置

```
user.email = chengchen0802@gmail.com
user.name  = BigCat
```

## 文件约定

- 每期 HTML 文件名格式：`{主题slug}-book{N}.html`，放在仓库根目录
- 每期发布后必须更新 `index.html`（在 `<!-- entries -->` 之前插入新条目）
- 不要手动添加 `comments.js` / `search.js` / `index-button.js`——仓库 GitHub Action 会自动注入
