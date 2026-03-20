# AI 行业日报/周报存档 (AI News Archive)

本项目是一个基于 HTML/CSS 的静态报告系统，旨在自动化生成并展示 AI 行业的每日新闻速递与每周深度综述。项目设计风格简约、专业，适合作为个人技术动态展示或团队内部共享。

## 🌟 项目亮点 (Highlights)

-   **交互式幻灯片设计**：报告采用 PPT 风格的单页滚动/翻页布局，沉浸式阅读体验。
-   **数据驱动**：集成 `Chart.js` 动态渲染行业数据，直观展示融资现状、裁员趋势、市场规模等关键指标。
-   **响应式适配**：支持移动端触摸滑动、PC 键盘导航，随时随地查看报告。
-   **零成本部署**：纯静态页面，完美支持 GitHub Pages。

## 🤖 AI Agent 生成指南 (Automation)

为了确保报告的结构与索引同步更新，本项目定义了标准的 AI Agent 工作流：

1.  **路径规范**：日报存放于 `daily_reports/YYYY-MM/`，周报存放于 `weekly_reports/YYYY-MM/`。
2.  **首页更新**：生成新报告后，**必须**同步更新根目录下的 `index.html`，且新报告置于列表最上方（保持时间倒序）。
3.  **标准流程**：推荐 AI Agent 阅读 [.agent/workflows/generate_report.md](.agent/workflows/generate_report.md) 以获取详细的操作指引。

---

*“记录 AI 的进化，观察未来的缩影。”*
