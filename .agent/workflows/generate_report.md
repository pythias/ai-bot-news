---
description: 自动化生成 AI 报告并更新首页索引
---

# AI 报告生成与首页更新工作流

当需要生成新的日报（Daily）或周报（Weekly）时，请 AI Agent 严格遵循以下标准程序：

## 1. 准备工作 (Preparation)
-   **获取当前日期**：确定当前年份 (YYYY)、月份 (MM) 和日期 (DD)。
-   **确定文件路径**：
    -   日报：`daily_reports/YYYY-MM/ai_news_YYYY-MM-DD.html`
    -   周报：`weekly_reports/YYYY-MM/ai_weekly_YYYY-MM-DD.html`
-   **创建目录**：如果对应的 `YYYY-MM` 文件夹不存在，请先行创建。

## 2. 内容生成 (Generation)
-   **读取模板**：从 `templates/ai_news_template.html` 读取基础结构。
-   **填充内容**：
    -   更新标题、日期、核心数据概览、主要动态及 Chart.js 图表数据。
    -   确保所有视觉风格（配色、字体）与现有报告保持一致。
-   **写入文件**：将生成的 HTML 内容写入第 1步确定的文件路径，并使用 `UTF-8` 编码。

## 3. 首页索引更新 (Index Update)
-   **定位 Section**：打开根目录下的 `index.html`。
-   **插入新卡片**：
    -   在对应的 `<h2 class="section-title">`（每周综述 或 每日速递）下方的 `<div class="grid">` **首位**（即最上方）插入新的 HTML 卡片。
    -   **卡片模板**：
        ```html
        <a href="[路径]" class="card">
            <div>
                <div class="card-type">[Daily News | Weekly Report]</div>
                <div class="card-title">[报告标题]</div>
                <div class="card-date">[YYYY年MM月DD日]</div>
            </div>
            <div class="card-footer">查看详情</div>
        </a>
        ```
-   **保持整洁**：检查 `index.html` 的结构是否依然完整，确保没有破坏 HTML 标签嵌套。

## 4. 提交清理 (Finalize)
-   **Git 操作**：执行 `git add .`。
-   **Commit 信息**：使用规范的提交信息，例如 `feat: add ai_news_YYYY-MM-DD and update index`。

---

> [!IMPORTANT]
> **始终保持时间倒序**：最新的报告必须出现在 `index.html` 列表的最上方，以便用户第一时间看到。
