# 毛新宇个人主页部署说明

本项目已基于 PRISM 模板改为毛新宇个人主页，支持 GitHub Pages 静态部署。

## 本地预览

```bash
npm install
npm run dev
```

访问：`http://localhost:3000`

## 本地静态构建

```bash
npm run build
python3 -m http.server 4173 -d out
```

## GitHub Pages 部署

推荐仓库名：`PRISM`，GitHub 用户名按当前简历链接使用 `Sweet4tars`。

1. 在 GitHub 创建仓库：`Sweet4tars/PRISM`
2. 将当前 `/home/maoxy/code/private/PRISM` 推送到该仓库的 `main` 分支。
3. 在 GitHub 仓库设置中启用 Pages：`Settings -> Pages -> Source: GitHub Actions`。
4. 推送后 `.github/workflows/deploy.yml` 会自动构建并发布。

上线地址：

```text
https://sweet4tars.github.io/PRISM/
```

如果仓库名不是 `PRISM`，需要同步修改：

- 简历中的主页链接
- `.github/workflows/deploy.yml` 里的 `NEXT_PUBLIC_BASE_PATH=/PRISM`
