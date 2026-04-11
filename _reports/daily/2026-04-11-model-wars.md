---
layout: news
title: AI新闻日报 - 2026年4月11日
date: 2026-04-11
mainTitle: OpenAI o3满血版发布 · 微软Copilot全面集成GPT-5 · 中国大模型降价潮持续
subtitle: OpenAI反击 | 降价潮 | 开源模型爆发 | 英伟达新GPU细节泄露
slides:
  - category: 模型发布
    title: OpenAI发布o3满血版：推理能力超越Claude 4，定价下调40%反击竞争
    highlights:
      - OpenAI于4月11日正式发布o3满血版本（o3-Full），在ARC-AGI和GPQA Diamond基准上分别达到87.5%和91.2%，大幅超越Claude 4和Gemini 3.5 Ultra
      - o3-Full引入"自适应推理"架构，可根据问题难度动态分配计算资源，简单问题响应速度提升3倍；支持200万token上下文并原生集成浏览器和代码执行环境
      - OpenAI同步宣布API定价下调40%，o3-Full输入$15/百万token、输出$60/百万token，直接回应Anthropic和Google的定价竞争
    source: OpenAI Blog | TechCrunch | The Verge

  - category: 模型发布
    title: 微软Copilot全面集成GPT-5：Windows 12预览版内置AI操作系统层
    highlights:
      - 微软于4月11日发布Windows 12首个预览版，GPT-5通过Copilot+ PC架构深度集成至系统层，实现真正的AI原生操作系统体验
      - Windows 12 Copilot支持"跨应用AI流"：用户可用自然语言指挥AI在Word、Excel、PowerPoint、Outlook之间协同工作，任务完成率较前代提升70%
      - 微软同时推出Azure AI Foundry企业版，提供GPT-5定制微调服务，支持企业基于自有数据训练私有AI模型，数据不出企业边界
    source: Microsoft Blog | ZDNet | Ars Technica

  - category: 价格战
    title: 字节跳动豆包大模型降价90%：中国AI大模型价格战进入最终阶段
    highlights:
      - 字节跳动于4月11日宣布豆包Pro 32B模型API价格降至$0.0003/千token，降幅达90%，直接拉平GPT-4o-mini价格，同时性能超越GPT-4
      - 阿里云通义千问、百度文心一言、腾讯混元同步跟进降价，1B参数以下小模型免费开放，中国AI大模型价格战正式进入"零毛利"阶段
      - 分析指出，中国大模型厂商本轮降价旨在快速抢占开发者生态，为未来AI应用爆发储备用户基础，但商业化压力将倒逼差异化竞争
    source: 36kr | 机器之心 | 量子位

  - category: 开源动态
    title: Meta发布LLaMA 4：开源模型首次在推理能力上追平闭源前沿模型
    highlights:
      - Meta于4月11日发布LLaMA 4系列，包括LLaMA 4-405B和LLaMA 4-70B两个版本，其中405B参数版本在MMLU上达到92.1%，首次接近Claude 4和GPT-5水平
      - LLaMA 4采用分组查询注意力（GQA）和稀疏MoE架构，在保持开源属性的同时大幅优化推理效率，推理速度较LLaMA 3提升2.5倍
      - Meta同步开源LLaMA 4训练数据集和微调工具链，承诺永久开源并禁止将LLaMA品牌用于闭源商业产品，生态策略进一步与OpenAI对抗
    source: Meta AI Blog | VentureBeat | TechCrunch

  - category: 硬件动态
    title: 英伟达GB300芯片规格泄露：HBM4内存+第五代NVLink，AI训练性能提升3倍
    highlights:
      - 知情人士于4月11日披露英伟达GB300（Blackwell Ultra）详细规格：采用HBM4内存、192GB GPU显存、第五代NVLink互连，FP8训练性能为H100的3倍
      - GB300预计2026年Q3量产，已获OpenAI、Google DeepMind和Microsoft Azure首批订单，总量超过50万片；单片定价预计为$35,000-$45,000
      - AMD Instinct MI400X同步曝光，采用HBM4和Chiplet设计，定位与GB300正面竞争；两大GPU厂商的AI算力军备竞赛持续升级
    source: Wccftech | AnandTech | Tom's Hardware
---
