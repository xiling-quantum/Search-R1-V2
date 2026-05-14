# Search-R1 学习过程总记录

目标：围绕 Search-R1 建立可展示、可复盘、可面试的 Agentic RAG 后训练项目经验，服务于大厂大模型岗位求职。

## 记录方式

- 每天结束后更新一篇 daily 日志。
- 总记录只保留阶段目标、每日索引和关键结论。
- 日志优先记录事实：读了什么、跑了什么、理解了什么、还有什么问题。

## 阶段目标

### 阶段 1：跑通与定位

时间：Day 1-7

目标：
- 理解 Search-R1 为什么不是普通 RAG。
- 定位核心源码：Agent loop、检索服务、reward、训练配置。
- 明确后续二改方向：Hybrid Retriever、Reward v2、Trajectory Logger、消融实验。

交付物：
- 项目源码地图。
- GitHub issue 观察记录。
- Search-R1 与大模型 JD 能力映射。

## 每日记录

- [2026-05-14](daily/2026-05-14.md)：clone 项目、配置 fork remote、完成 GitHub issue 初步调研。

## 当前关键判断

- Search-R1 的核心不是固定流程的普通 RAG，而是让模型在推理过程中学习何时搜索、搜索什么、何时回答。
- 第一阶段不要急着改 CUDA/vLLM/faiss 兼容问题，优先读懂 Agent loop 和 `/retrieve` 服务。
- 最适合作为求职项目二改的方向，是可解释、可评估、可消融的检索与 reward 改造。
