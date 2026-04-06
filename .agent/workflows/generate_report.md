---
description: 使用 Jekyll + GitHub Pages 自动生成 AI 报告
---

# AI 报告生成工作流 (Jekyll + GitHub Pages)

本项目使用 **Jekyll 静态网站生成器** + **GitHub Pages** 托管，实现零维护成本的内容发布。

## 目录结构

```
ai-bot-news/
├── _layouts/           # HTML 布局模板（固定不动）
│   ├── default.html    # 基础布局（含 CSS/JS/响应式）
│   └── news.html      # 新闻幻灯片布局
├── _reports/
│   ├── daily/          # 日报 Markdown 文件
│   └── weekly/         # 周报 Markdown 文件
├── _config.yml         # Jekyll 配置
├── Gemfile             # Ruby 依赖
└── index.html          # 自动生成的索引页
```

## 每日工作流程

### 1. 搜索与总结

搜索最近一天的 AI 行业重要动态，包括：
- 技术突破、产品发布
- 行业巨头动向
- 融资并购
- 重要研究论文

### 2. 创建日报文件

在 `_reports/daily/` 目录下创建 Markdown 文件：

**文件名格式**：`YYYY-MM-DD-简短标题.md`

**文件模板**：

```markdown
---
layout: news
title: AI新闻日报 - YYYY年MM月DD日
date: YYYY年MM月DD日
mainTitle: 今日核心新闻标题
subtitle: 副标题要点
slides:
  - category: 分类
    title: 新闻标题
    highlights:
      - 要点1
      - 要点2
      - 要点3
    source: 来源

  - category: 分类2
    title: 新闻标题2
    highlights:
      - 要点1
      - 要点2
    source: 来源2
---
```

### 3. 提交更新

```bash
git add _reports/daily/YYYY-MM-DD-*.md
git commit -m "feat: add AI news report for YYYY-MM-DD"
git push
```

### 4. 自动发布

GitHub Pages 自动检测到 push 事件，Jekyll 构建并发布到 `https://yourname.github.io/ai-bot-news/`

## Front Matter 字段说明

| 字段 | 必填 | 说明 |
|------|------|------|
| `layout` | ✅ | 必须为 `news` |
| `title` | ✅ | 页面标题（用于浏览器标签） |
| `date` | ✅ | 显示日期，格式：`YYYY年MM月DD日` |
| `mainTitle` | ✅ | 封面大标题 |
| `subtitle` | ✅ | 封面副标题 |
| `slides` | ✅ | 幻灯片数组 |
| `slides[].category` | ✅ | 分类标签（如：战略转型、伦理争议） |
| `slides[].title` | ✅ | 新闻标题 |
| `slides[].highlights` | ✅ | 要点数组（3-5条为宜） |
| `slides[].source` | ❌ | 新闻来源 |

## 分类推荐

- 战略转型
- 伦理争议
- 市场格局
- 产品升级
- 行业趋势
- 技术演进
- 应用场景
- 产业落地
- 融资动态

## 注意事项

1. **日期必须准确**：使用执行任务时的真实日期
2. **文件名使用英文**：便于 GitHub Pages 正确处理 URL
3. **highlights 数量**：建议 3-5 条，不要过少或过多
4. **内容为中文**：本项目面向中文读者
5. **push 后等待**：GitHub Pages 构建通常需要 1-2 分钟

## 本地预览

```bash
bundle install
bundle exec jekyll serve
# 访问 http://localhost:4000
```
