# 追光

Hugo + [Fuji](https://github.com/dsrkafuu/hugo-theme-fuji/) 主题的光学技术博客。

项目配置使用 Hugo 官方当前推荐的 `hugo.toml` 文件名。

## 本地预览

```powershell
.\.tools\hugo\hugo.exe server -D
```

如果你已经在系统中安装了 Hugo，也可以直接运行：

```powershell
hugo server -D
```

## 构建

```powershell
.\.tools\hugo\hugo.exe --minify
```

生成结果会输出到 `public/`。

## 发布到 GitHub Pages

推荐使用 GitHub Actions 发布，流程和 Hugo 官方文档一致：

1. 在 GitHub 创建仓库。如果想得到 `https://用户名.github.io/` 这种地址，仓库名必须是 `用户名.github.io`。
2. 把本项目推送到该仓库的 `main` 分支。
3. 进入 GitHub 仓库的 `Settings` -> `Pages`。
4. 在 `Build and deployment` 里把 `Source` 选为 `GitHub Actions`。
5. 打开 `Actions` 标签页，等待 `Build and deploy` 工作流变绿。
6. 访问 `https://用户名.github.io/post/monochromatic_light/`。

本项目已经包含 `.github/workflows/hugo.yaml`，push 后会自动构建并部署 `public/`。
