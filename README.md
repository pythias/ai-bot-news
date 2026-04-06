# AI 行业日报/周报存档 (AI News Archive)

本项目基于 **Jekyll** 构建，使用 **GitHub Pages** 零成本托管和自动发布。

## 项目亮点

-   **Jekyll 模板引擎**：内容与模板分离，维护简单
-   **GitHub Pages 原生支持**：push 即发布，无需手动构建
-   **交互式幻灯片设计**：PPT 风格的单页滚动/翻页布局
-   **响应式适配**：支持移动端触摸滑动、PC 键盘导航
-   **Chart.js 可嵌入**：支持数据可视化图表

## 目录结构

```
_reports/           ← 每日/周报 Markdown 文件（仅需编辑这里）
_layouts/           ← HTML 布局模板（固定不动）
_config.yml         ← Jekyll 配置
Gemfile             ← Ruby 依赖
```

## 每日工作流程

1. 在 `_reports/daily/` 创建 `YYYY-MM-DD-标题.md` 文件
2. 填写 Front Matter 和内容
3. `git add` → `git commit` → `git push`
4. GitHub Pages 自动构建发布

详细规范请阅读 [.agent/workflows/generate_report.md](.agent/workflows/generate_report.md)

## 本地调试

```bash
# 安装依赖
bundle install

# 启动本地服务器
bundle exec jekyll serve

# 访问 http://localhost:4000
```

## 技术栈

- Jekyll 4.x
- GitHub Pages
- HTML/CSS/JS（原生）
- Chart.js（可选，用于数据可视化）

---

*记录 AI 的进化，观察未来的缩影。*
