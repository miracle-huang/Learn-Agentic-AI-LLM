# Learn Agentic AI & LLM

> Agent-first learning and career roadmap: **AI Agent Engineer → LLM Engineer**, with Kaggle competitions, production-oriented projects, evaluation, RAG, LLMOps, fine-tuning and inference optimization.
>
> Source: Notion page **职业发展 / Agentic AI&LLM：Kaggle** · v2.1 · last synced 2026-09-21.

> **Agent 优先的转职路线（v2.1）** — 主线：AI Agent Engineer → LLM Engineer。投入 20h/周，总计约 44–52 周；用时为相对周期，不锚定日期。第 3 个月（P1 结束）起即可开始投简历。算力：无本地 GPU，P0–P3 基本只花 API token，P4 才需租卡。目标市场：中国 + 日本；技术写作英文主稿 + 中/日文版。
> [网页版（同一份内容，可对照）](https://claude.ai/artifact/7E12f1Jo4g6fpZw6Yyxvm2)


## Contents

- [市场读数（2026-09）](#市场读数2026-09)
- [阶段与求职节点](#阶段与求职节点)
- [P0 · Agent 地基](#p0--agent-地基把-llm-调用写成工程45-周)
- [P1 · 能交付的 Agent](#p1--能交付的-agent编排安全可观测810-周)
- [P2 · RAG 与记忆](#p2--rag-与记忆agent-的知识侧810-周)
- [P3 · 评测与 LLMOps](#p3--评测与-llmops把能跑变成能证明68-周)
- [P4 · LLM 工程](#p4--llm-工程微调量化与推理优化1012-周)
- [P5 · 综合、冲牌与作品集收口](#p5--综合冲牌与作品集收口68-周)
- [操作手册](#操作手册)
- [这条路线会在哪里断](#这条路线会在哪里断)

---
# 市场读数（2026-09）
## 中国 · 五条赛道
- **LLM 应用开发** — prompt、function calling、结构化输出、缓存与成本
- **Agent 工程** — 工作流设计、工具安全、记忆、失败恢复 ← **主攻**
- **RAG & 记忆** — 文档解析、检索质量、重排、权限、引用 ← **岗位池最大，第二主攻**
- Java AI 工程 — 与背景不符，放弃
- AI Infra — vLLM、TTFT/TPOT、KV Cache、GPU 调度
市场口径已从「API 调用者」转向「全栈 AI 工程师」——能落进业务、稳定运行、可评测、能降本、能维护；面试看交付证据不看 demo。
## 日本 · 硬性要求与行情
- **必须会**：Python、API 集成、**LangChain / LlamaIndex**、向量库（Chroma / Pinecone）、Git、Docker
- **加分**：云平台（AWS / Azure / GCP）、MLOps、**评测设计方法论**
- **工作内容五类**：RAG 构建（社内 QA）、RAG vs 微调选型、LLMOps、模型评估、AI Agent 开发
年收参考：AI エンジニア平均约 626 万円、生成 AI 関連约 743 万円、个别求人 400 万〜1800 万円超；AI 求人検索量为 2023-09 的 3.7 倍。转职周期通行估算：后端工程师约 6 个月（从最小 RAG demo 起），数据科学背景约 3 个月（**评测能力可迁移**），完全未经验 12–18 个月。**明确的差异化点：能设计评测框架、把运维做扎实的人被优先录用。**
> 两地指向同一结论，也是本路线的设计依据：会搭 agent 的人很多，能证明 agent 稳定、可评测、算得清成本的人很少。所以 P3（评测与 LLMOps）是护城河，而 LLM 行为分析的研究背景正好落在这里。


---
# 阶段与求职节点

<table>
<tr>
<td>阶段</td>
<td>主题</td>
<td>用时</td>
<td>求职节点</td>
</tr>
<tr>
<td>P0</td>
<td>Agent 地基</td>
<td>4–5 周</td>
<td>纯技术积累，**不作为节点**</td>
</tr>
<tr>
<td>P1</td>
<td>能交付的 Agent</td>
<td>8–10 周</td>
<td>→ Agent / LLM 应用开发工程师</td>
</tr>
<tr>
<td>P2</td>
<td>RAG 与记忆</td>
<td>8–10 周</td>
<td>→ RAG 工程师 · 社内 QA 系统开发</td>
</tr>
<tr>
<td>P3</td>
<td>评测与 LLMOps</td>
<td>6–8 周</td>
<td>→ LLMOps / AI 品質保証</td>
</tr>
<tr>
<td>P4</td>
<td>微调与推理</td>
<td>10–12 周</td>
<td>→ LLM Engineer（正式转入）</td>
</tr>
<tr>
<td>P5</td>
<td>综合与冲牌</td>
<td>6–8 周</td>
<td>→ 高级岗 / 奖牌与作品集收口</td>
</tr>
</table>

# 中文教材总览（全部 2025–2026 年出版）

<table>
<tr>
<td>书</td>
<td>作者 / 出版</td>
<td>用在</td>
</tr>
<tr>
<td>《AI Agent开发实战：从基础原理到企业级应用》</td>
<td>郑天民，机械工业出版社 2025-09，ISBN 9787111788737</td>
<td>P0（1–2 章）、P1（3–8 章）主线</td>
</tr>
<tr>
<td>《AI Agent应用开发：构建多智能体协同系统》</td>
<td>尹浩，清华大学出版社 2025-11，ISBN 9787302703761，368 页</td>
<td>P1（6–7 章 规划/多智能体）、P2（4–5 章 RAG/记忆）、P3（2 章 评测与 OpenCompass）</td>
</tr>
<tr>
<td>《MCP开发从入门到实战》</td>
<td>杨威理，人民邮电出版社 2025-06，ISBN 9787115674142</td>
<td>P1 的 MCP 部分（另有《MCP极简开发》王双等，人邮 2025-06，偏应用，可选）</td>
</tr>
<tr>
<td>《LlamaIndex大模型RAG开发实践》</td>
<td>Andrei Gheorghiu 著／杨森等译，清华大学出版社 2025-07，ISBN 9787302697084，396 页</td>
<td>P2 主线</td>
</tr>
<tr>
<td>《大规模语言模型（第2版）：从理论到实践》</td>
<td>张奇、郑锐，电子工业出版社 2025-05，ISBN 9787121500572，454 页</td>
<td>P3（模型评估、对齐）、P4（微调/对齐/推理加速）</td>
</tr>
<tr>
<td>《图解大模型：生成式AI原理与实战》</td>
<td>Jay Alammar、Maarten Grootendorst 著／李博杰译，人民邮电出版社 2025-05，ISBN 9787115670830，350 页</td>
<td>P4 主线</td>
</tr>
</table>

---
# P0 · Agent 地基：把 LLM 调用写成工程（4–5 周）
**是什么**：唯一不作为求职节点的阶段。把研究脚本改造成有类型、有重试、有成本账、能被别人调用的工程代码。目标只有一个：一个带三个真实工具的 agent，能跑、能测、能部署。
## 掌握的知识 / 技能
- function calling / tool schema 设计与参数校验
- 结构化输出（JSON Schema、Pydantic、解析失败兜底）
- 多模型客户端抽象
- SSE 流式、超时、重试与指数退避、幂等
- **token 计费与响应缓存**
- Python 工程化（uv、pytest、类型标注、FastAPI、Docker、Git/PR）
- Kaggle 断网内核与运行上限
## 可实践的 Kaggle 项目
- [5-Day AI Agents Intensive（Google × Kaggle）](https://www.kaggle.com/competitions/5-day-ai-agents-intensive-vibecoding-course-with-google) — 本阶段主干。2026-06 那期 35 万人注册，覆盖 agent 设计/安全/云端部署全生命周期。往期材料公开，按天自学，**每天的 Notebook 自己重写一遍而不是跑一遍**；有新一期立刻报名。
- [AI Agents Intensive Capstone](https://www.kaggle.com/competitions/vibecoding-agents-capstone-project)（[更早一期](https://www.kaggle.com/competitions/agents-intensive-capstone-project)）— **只读不做**。挑 10 份优胜作品，记录「解决什么问题 / 几个工具 / 怎么处理失败 / README 怎么写」，作为 P1 选题库。
- [The Gemma 4 Good Hackathon](https://www.kaggle.com/competitions/gemma-4-good-hackathon)（已结束 2026-05-18，$200K）— 读优胜作品，重点看**开源模型怎么做原生 function calling**。
- Kaggle 平台热身 — 只做一件事：把 agent 代码在**断网内核**里跑通一次。不参加任何表格赛。
## 教材
- **中文书**：《[AI Agent开发实战：从基础原理到企业级应用](https://weread.qq.com/web/reader/41232030813abb05bg019c0c)》郑天民，机械工业出版社 2025-09（智能系统与技术丛书，ISBN 9787111788737），第 1–2 章：Agent 核心概念、开发模式、用 LLM 与 Swarm 框架搭第一个 agent
- **视频**：台大李宏毅《生成式人工智能导论》（[B 站 2026 版合集](https://www.bilibili.com/video/BV1bDvHBhEhP/)），只看 LLM 原理与 Agent 单元
- **课程**：[HF AI Agents Course](https://huggingface.co/learn/agents-course) Unit 0–1（免费）
- **白皮书**：[Agent Tools & Interoperability with MCP](https://www.kaggle.com/whitepaper-agent-tools-and-interoperability-with-mcp)
## 阶段产出
- [ ] `agent-kit` 仓库：多模型客户端 + 工具注册表 + 输出校验 + 重试 + 计费缓存，pytest + Docker
- [ ] 带 3 个真实工具的最小 agent（FastAPI）
- [ ] 《工具 schema 设计规范》一页英文文档，含 5 个反例
- [ ] 10 份 capstone 拆解笔记
- [ ] 成本账本第一页
---
# P1 · 能交付的 Agent：编排、安全、可观测（8–10 周）
**是什么**：从「能跑的 demo」到「敢交付的 agent」。差别全在出错怎么恢复、恶意输入怎么办、坏了怎么定位。
## 掌握的知识 / 技能
- **LangGraph**：有向图编排、状态机、检查点与断点续跑、human-in-the-loop 审批（日企尤其看重）
- smolagents（代码型）与 LlamaIndex agents 的边界
- **MCP**：写 server、包装已有服务、客户端接入
- 编排模式取舍：ReAct / plan-and-execute / 固定工作流，以及「能用确定性流程就别用 agent」
- **安全护栏**：prompt 注入与间接注入、工具权限最小化、沙箱执行、输出校验、多步攻击链
- 失败恢复：超时、部分失败、补偿、降级
- **可观测性**：trace/span、成本归因、失败模式聚类
## 可实践的 Kaggle 项目
- [AI Agent Security - Multi-Step Tool Attacks](https://www.kaggle.com/competitions/ai-agent-security-multi-step-tool-attacks) — **核心，整条路线最有面试价值的一场**。Kaggle × OpenAI × Google × IEEE，在确定性离线基准里构造攻击算法找出工具调用 agent 的可复现多步失败。用法：① 跑公开 baseline 理解「失败」如何判定；② 自己实现攻击算法并提交；③ **反向用**——把找到的失败模式整理成回归测试集，套到自己的 agent 上逐条修掉。同时拥有「会攻」和「会防」两份证据。已结束也照这三步做。
- [BenchFlow - Agent Skill Lift](https://www.kaggle.com/competitions/skill-lift) — 基于 [SkillsBench](https://www.skillsbench.ai/)（87 任务 / 8 领域 / 公开排行榜 / GitHub 数据）评估 agent skill 的有效性、能力与安全性。本阶段站在**被评测方**。P3 再回来站评测设计方。
- [AI Agents Intensive Capstone 标准](https://www.kaggle.com/competitions/vibecoding-agents-capstone-project) — 这就是**旗舰项目 1**。按 capstone 提交标准做一个**选题足够窄、工具足够真**的 agent。宁做「按你的研究口径筛 arXiv 新论文并生成周报」，也不做「通用科研助手」。
- [Kaggle Community Hackathons](https://www.kaggle.com/competitions?new=true&type=hackathon) — 2026-03 上线，免费用 Kaggle 基建办赛（奖池上限 $1 万）。本阶段作**参赛者**刷 2–3 场小型 agent 黑客松。
## 教材
- **中文书**：《AI Agent开发实战》郑天民（2025-09）第 3–8 章：ReAct Agent、Plan-and-Execute Agent、接 RAG 的知识型 agent、多模态 agent（LangChain + LlamaIndex），以及**企业级工程化**与多智能体（AutoGen、LangGraph）。**照做，但每个项目都加上护栏、重试、trace 三件事。**
- **中文书**：《AI Agent应用开发：构建多智能体协同系统》尹浩，清华大学出版社 2025-11 — 第 6 章**规划能力**（CoT、Self-Ask、Self-Reflexion、Function Calling、ReAct、Plan-and-Execute、Self-Discover 逐个实现）、第 7 章**多智能体**（AutoGen、MetaGPT、CrewAI、LangGraph 对比）。中文里对编排模式讲得最全的一本。
- **中文书**：《MCP开发从入门到实战》杨威理，人民邮电出版社 2025-06 — MCP 架构与五大要素（resources / prompts / tools / sampling / roots）、SDK、自己写 server、MCP Inspector 调试。（另有《MCP极简开发》王双等，人邮 2025-06，偏应用场景，可选。）
- **课程**：[HF Agents Course](https://huggingface.co/learn/agents-course) Unit 2（三个框架各一遍）与 **Unit 4 期末项目（必做，带自动评测和排行榜，是你第一个客观分数）**
- **视频**：[DeepLearning.AI](http://DeepLearning.AI) [AI Agents in LangGraph](https://www.deeplearning.ai/courses/ai-agents-in-langgraph)、[Building Code Agents with smolagents](https://www.deeplearning.ai/courses/building-code-agents-with-hugging-face-smolagents)
- **概念看书、API 看官方文档**——框架版本变得比书快
## 阶段产出
- [ ] **旗舰项目 1**：上线窄域 agent（LangGraph + MCP 工具 + 护栏 + trace + Docker）
- [ ] **agent 回归测试集**：来自 AI Agent Security 的失败模式，逐条对应测试用例与修复说明
- [ ] HF Agents Course Unit 4 自动评测分数（一个客观数字）
- [ ] 自建 MCP server 一个
- [ ] 英文技术文章《What broke in my agent, and how I found it》
- [ ] 2–3 场 Community Hackathon 的 writeup
> **求职节点 1：可以开始投了**
> **简历能写**：「独立设计并交付带工具调用的 agent 服务，含权限边界与沙箱执行、失败恢复与降级路径、trace 级可观测性；基于公开对抗基准建立 N 条回归测试，修复 M 类多步失败。」用数字说话：工具数、任务成功率、p95 延迟、每任务成本。
> **面试能聊**：① 为什么这里用固定工作流而不是让模型自己规划；② 你的工具 schema 怎么防止模型误用；③ 间接 prompt 注入你怎么防的；④ 一次线上失败你是怎么从 trace 定位到根因的。
> **对口岗位**：中国「Agent 工程 / LLM 应用开发」；日本「AI エージェント開発 / LLM アプリケーションエンジニア」。


---
# P2 · RAG 与记忆：agent 的知识侧（8–10 周）
**是什么**：补上 agent 的另一半。两地**岗位数量最大**的方向（中国「RAG & 记忆」赛道、日本的社内 QA / 社内文書検索）。按 **Agentic RAG** 做（检索是 agent 的一个工具，不是固定流水线），P1 成果直接复用。
## 掌握的知识 / 技能
- **文档解析**：PDF / 表格 / 扫描件 / Office，版面还原与表格抽取
- chunk 策略：固定窗口 vs 语义切分 vs 版面感知；父子块与上下文扩展
- embedding 选型与多语言（中/日/英混合语料的坑）
- 向量库工程：Chroma / Milvus / pgvector / Pinecone，索引参数、增量更新、删除与重建
- **混合检索**：BM25 + dense、RRF；**rerank**（cross-encoder）的收益与延迟代价
- 查询改写、多跳检索、HyDE
- **引用与溯源**：answer → chunk → 原文页码
- **权限过滤**：多租户、行级权限、检索阶段就过滤
- 记忆：会话记忆、长期记忆、写入与遗忘策略
- **质量量化**：grounding 率、引用准确率、幻觉率、检索召回/命中率
## 可实践的 Kaggle 项目
- [Kaggle - LLM Science Exam](https://www.kaggle.com/competitions/kaggle-llm-science-exam) — **主攻，最好的受限 RAG 训练场**。断网答科学难题，胜负手是自建检索库 + 重排而非更大模型，正是企业 RAG 的真实处境。用彩排法（见操作手册）。
- [AgentEval Part I: Grounded RAG Benchmark](https://www.kaggle.com/competitions/agent-eval-part-i-grounded-rag-benchmark) — 评估目标直接是 grounding / 引用准确率 / 幻觉控制，与企业验收标准重合。当作旗舰项目 2 的**外部验收标准**。
- [Eedi - Mining Misconceptions in Mathematics](https://www.kaggle.com/competitions/eedi-mining-misconceptions-in-mathematics) — 召回 + 重排的检索赛，顶层方案用 LLM 生成难负例训练检索器。补「检索器怎么训」这一块。
- [LLM Agentic Legal Information Retrieval](https://www.kaggle.com/competitions/llm-agentic-legal-information-retrieval) — 社区赛不发牌，但**题材对口**日本的社内規程検索 / 契約書 QA（长文档、严格溯源、错了有后果）。
- [The Learning Agency Lab - PII Data Detection](https://www.kaggle.com/competitions/pii-detection-removal-from-educational-data) — 做轻量版（2 周）接进入库流程当脱敏中间件；隐私 + 合规在两地都加分。
## 教材
- **中文书**：《LlamaIndex大模型RAG开发实践》Andrei Gheorghiu 著／杨森等译，清华大学出版社 2025-07（人工智能前沿实践丛书，ISBN 9787302697084，396 页）。11 章走完文档与节点、各类索引、数据接入、检索与后处理、响应合成、agent 与部署。**本阶段主线教材**——日本求人票点名的就是 LlamaIndex。
- **中文书**：《AI Agent应用开发》尹浩（2025-11）第 4 章 **RAG 系统构建**（文档解析、优化策略、LangChain 实现、**RAGas 评测**）与第 5 章 **记忆模块**（记忆类型、手写实现、MemGPT / Mem0 / BoT）。中文里少有把「记忆」单独讲透的一本。
- **课程**：HF Agents Course Unit 3（Agentic RAG）
- **文档**：LlamaIndex 官方 indexing / retrieval / evaluation 三章通读
## 阶段产出
- [ ] **旗舰项目 2**：企业级 RAG（多格式解析 + 混合检索 + rerank + 引用溯源 + 行级权限 + 增量更新）
- [ ] **质量报告**：grounding 率、引用准确率、幻觉率、检索召回，含 rerank 前后与查询改写前后的消融表
- [ ] 入库脱敏中间件（PII 检测）
- [ ] 中/日/英三语 demo 数据集与演示脚本（面试时能当场跑）
- [ ] 英文技术文章《Grounding and citation accuracy: how I measured my RAG》+ 日文版
> **求职节点 2：岗位池最大的那一格**
> **简历能写**：「从零构建企业知识库问答系统：支持 PDF/表格/扫描件解析，BM25 + 向量混合检索加 cross-encoder 重排，answer→chunk→原文页码全链路溯源，行级权限在检索阶段过滤；grounding 率 X%、引用准确率 Y%、幻觉率 Z%。」
> **面试能聊**：① 为什么加了 rerank 延迟涨了还值得；② 扫描件和表格你怎么处理的；③ 权限为什么必须在检索阶段过滤；④ 你怎么证明它没在胡说——这一条最能区分候选人。
> **对口岗位**：中国「RAG & 记忆 / 知识库工程」；日本「RAG システム開発 / 社内 QA ボット構築」。日本市场把「能做出最小 RAG demo」当作转职的起跑线，你到这里已经远超那条线。


---
# P3 · 评测与 LLMOps：把「能跑」变成「能证明」（6–8 周）
**是什么**：护城河，也是研究背景变现的地方。日本招聘明确写「能设计评测框架的人被优先录用」；你做的「不用真标签、从 LLM 行为估计任务可推断性」换个包装就是 agent/LLM 系统的难度分层与风险预估。阶段最短，性价比最高。
## 掌握的知识 / 技能
- **评测集构造**：任务分层、边界样例、对抗样例；标注一致性与样本量估算
- **LLM-as-judge**：位置偏差、长度偏差、自我偏好，以及怎么校准（人工锚点、成对比较、置信区间）
- **轨迹级评估**：不只看最终答案，看工具调用序列对不对；pass@k、任务成功率、步数与成本分布
- 回归测试与 CI：每次改 prompt / 换模型自动跑全量评测，分数掉了阻止合并
- 灰度与 A/B、prompt 与配置的版本管理、可回滚
- **可观测性与成本归因**：trace/span、按用户/功能拆成本、异常告警
- 延迟指标：TTFT / TPOT、p50 与 p95 的区别、超时预算怎么分配
- 数据飞轮：线上失败样例回流成评测集
## 可实践的 Kaggle 项目
- [Kaggle AI Benchmarks / Community Benchmarks](https://www.kaggle.com/benchmarks) — **整条路线性价比最高的一项，务必做**。2026-01 上线，用 [kaggle-benchmarks SDK](https://github.com/Kaggle/kaggle-benchmarks) 写任务、组基准、跑出主流模型公开排行榜，支持多模态、代码执行、工具调用与多轮对话，官方提供免费模型额度。把研究里「从 LLM 行为估计任务可推断性」那套方法做成一个**公开基准**（例：给定一批任务，在不看真标签的情况下预测哪些任务当前模型做不好）。有 URL、有排行榜、别人很难复制。
- [BenchFlow - Agent Skill Lift](https://www.kaggle.com/competitions/skill-lift) — 第二次回访，这次站在**评测设计方**：为什么把 skill、harness、model 分三层？为什么用 resolution rate 而不是准确率？为什么要跑 3 次 trial？（v1.1 排行榜 25 个 model-harness 组合 × 87 任务，最高 resolution rate 67.3%——记住这个量级，面试时能说出业界现状。）
- [AgentEval Part I](https://www.kaggle.com/competitions/agent-eval-part-i-grounded-rag-benchmark) — P2 用它学指标，P3 用它学**基准设计**：它怎么把「幻觉」这种模糊概念变成可自动判定的分数。
- [AI Agent Security - Multi-Step Tool Attacks](https://www.kaggle.com/competitions/ai-agent-security-multi-step-tool-attacks) — 回访，当**安全评测基准**读：它怎么保证「确定性离线」从而让分数可复现？把攻击集做进自己的 CI。
- 对照读 [Konwinski Prize](https://www.kaggle.com/competitions/konwinski-prize) 的赛制设计（$1M 奖给能关掉 90% 新 GitHub issue 的 AI；断网、限时、按测试通过计分），不必参赛。
## 教材
- **中文书**：《大规模语言模型（第2版）：从理论到实践》张奇、郑锐，电子工业出版社 2025-05（[豆瓣](https://book.douban.com/subject/37332616/)，ISBN 9787121500572，454 页）。读**模型评估**与对齐两部分；第四、五篇还覆盖智能体、RAG 与效率优化。中文里体系最完整的 LLM 教材。
- **中文书**：《AI Agent应用开发》尹浩（2025-11）第 2 章的评测部分：国内外模型的评测方法与 **OpenCompass** 工具链。中文侧少见的「怎么跑一套模型评测」的实操材料。
- **论文**：[SkillsBench 论文](https://www.skillsbench.ai/skillsbench.pdf)（87 任务 / 8 领域 / 三层拆解）精读，当作「一份评测基准该怎么设计」的范本。
- **工具**：[kaggle-benchmarks SDK](https://github.com/Kaggle/kaggle-benchmarks) 文档 + Benchmarks Cookbook
## 阶段产出
- [ ] **一个发布在 Kaggle Benchmarks 上的公开基准**（与研究主题连通，有 URL 与排行榜）
- [ ] `agent-eval` 框架仓库：任务集、judge 与校准、轨迹评估、方差报告、一条命令出报告
- [ ] 把 P1/P2 两个旗舰项目接入 CI：改动即回归 + 安全攻击集，分数回归即阻止合并
- [ ] 成本与延迟仪表盘：按功能拆分的 token 成本、p50/p95 延迟
- [ ] 英文长文《Designing an evaluation harness for a production agent》+ 日文版
- [ ] 把研究方法论改写成一篇工程向文章
> **求职节点 3：最稀缺的那格**
> **简历能写**：「为生产级 agent/RAG 系统建立评测与回归体系：N 个分层任务的评测集、校准过的 LLM-as-judge（与人工标注一致率 X%）、轨迹级成功率与成本分布，接入 CI 实现改动即回归；另在 Kaggle Benchmarks 发布公开基准一项。」
> **面试能聊**：① LLM-as-judge 的偏差你怎么发现和校准的；② 为什么只看最终答案不够，轨迹要怎么评；③ 你的评测集怎么防止过拟合；④ 一次「分数涨了但线上变差」的经历。
> **对口岗位**：中国「LLM 应用开发（含评测）/ AI 质量」；日本「LLMOps / AI 品質保証 / 評価設計」。这是日本市场明确说的差异化点。


---
# P4 · LLM 工程：微调、量化与推理优化（10–12 周）
**是什么**：正式跨到 LLM Engineer。从「用模型」到「改模型，并让它更便宜更快」。这一段唯一需要真金白银租卡，所以放在后面——前三个阶段你已经能就业了，这里是加薪与拓宽的阶段。
## 掌握的知识 / 技能
- **参数高效微调**：LoRA / QLoRA 的秩与目标模块选择、序列 packing、FlashAttention、梯度检查点
- **训练数据工程**：指令数据构造、去重、质量过滤、泄漏检查（这一步决定成败，比调参重要）
- SFT → DPO 基础；给解码器模型加分类头做偏好/打分任务
- **量化**：bitsandbytes / AWQ / GPTQ 的精度-延迟-显存三角权衡
- **推理服务**：vLLM 的 continuous batching、PagedAttention、KV cache 行为；并发与批大小扫描；TTFT / TPOT 优化
- 结构化输出的约束解码
- **蒸馏**：大模型标注 → 小模型上线，产业里最常用的降本路径
- 受限推理：断网、限时环境下的预算分配、采样条数与早退策略
- 租卡成本控制：先小模型小样本跑通，再上卡跑全量
## 可实践的 Kaggle 项目
- [LLM Classification Finetuning](https://www.kaggle.com/competitions/llm-classification-finetuning) — 入口，1–2 周。唯一目标是把 QLoRA 微调链路端到端跑通（数据加载、训练、保存 adapter、量化、推理、提交），不追分数。
- [LMSYS - Chatbot Arena Human Preference Predictions](https://www.kaggle.com/competitions/lmsys-chatbot-arena) — **主攻，3–4 周**。公开比赛里 LLM 工程能力最集中的一场：7B/9B 微调、长对话截断、量化推理、在断网内核的时间预算里跑完全量测试集。顶层方案全部公开。做完你就有资格说自己「会微调并部署 LLM」。
- [WSDM Cup - Multilingual Chatbot Arena](https://www.kaggle.com/competitions/wsdm-cup-multilingual-chatbot-arena) — 1–2 周，对你特别对口。同样的偏好预测但**跨语言**，中/日/英三语能力本身就是差异化卖点。
- [AI Mathematical Olympiad - Progress Prize 3](https://www.kaggle.com/competitions/ai-mathematical-olympiad-progress-prize-3)（2026-04 已结束；[PP2](https://www.kaggle.com/competitions/ai-mathematical-olympiad-progress-prize-2)）— 2–3 周，当作推理预算的极限训练。规则要求开源模型、断网、CPU ≤9h / GPU ≤5h。只回答一个工程问题：给定固定算力，采样多少条、什么时候早退、验证器怎么用，才能最大化正确率。
- [LLM - Detect AI Generated Text](https://www.kaggle.com/competitions/llm-detect-ai-generated-text) — 可选，1–2 周。真正的课题是训练/测试分布严重不一致，用来练「分布偏移下怎么判断该不该相信自己的验证分数」。
## 教材
- **中文书**：《图解大模型：生成式AI原理与实战》Jay Alammar、Maarten Grootendorst 著／李博杰译，人民邮电出版社 2025-05（[豆瓣](https://book.douban.com/subject/37339504/)，ISBN 9787115670830，350 页）。300 幅全彩图解讲透 tokenization、embedding、Transformer，后半直接是**训练 embedding 模型、微调生成模型**的实战，还带一节 DeepSeek-R1 原理。**本阶段主线教材**，只要 Python 基础，不要求深度学习背景。
- **中文书**：《大规模语言模型（第2版）》张奇、郑锐（2025-05）—— 有监督微调与强化学习对齐、效率优化与推理加速三部分，作为图解那本的理论补充。
- **视频**：李宏毅《生成式人工智能导论》的微调与对齐单元；Karpathy 的 "Let's build GPT" 系列
- **文档**：vLLM 官方文档的 performance 与 scheduling 两章；HF PEFT / TRL 文档
## 阶段产出
- [ ] **旗舰项目 3**：自己微调的模型 + vLLM 服务化（Docker），带**延迟 / 吞吐 / 成本对照表**（fp16 vs 4bit、批大小扫描、TTFT/TPOT）
- [ ] 蒸馏前后对比：把 P1 或 P2 某个高频子任务换成自己的小模型，报出成本下降与质量变化
- [ ] 多语言（中/日/英）偏好模型一个，含各语言分项指标
- [ ] 《固定算力下的推理预算分配》技术笔记
- [ ] 算力账本：这一阶段租了多少小时卡、花了多少钱、换来了什么
- [ ] 英文长文《Fine-tuning and serving a 9B model on a rented GPU budget》+ 日文版
> **求职节点 4：正式以 LLM Engineer 应聘**
> **简历能写**：「QLoRA 微调 9B 级模型并以 vLLM 上线，4bit 量化后 p95 延迟降低 X%、单请求成本降低 Y%；将高频子任务从闭源 API 蒸馏为自有小模型，成本下降 Z% 且质量持平；多语言（中/日/英）偏好模型，各语言分项指标齐全。」
> **面试能聊**：① LoRA 的秩和目标模块你怎么定的；② 4bit 量化掉了多少分、值不值；③ vLLM 的吞吐瓶颈在哪、你怎么测出来的；④ 什么情况下你会选 RAG 而不是微调——这是日本面试的高频题，答案要能用成本和数据量说话。
> **对口岗位**：中国「LLM 应用开发 + AI Infra 边缘」；日本「LLM エンジニア（ファインチューニング・推論最適化）」。


---
# P5 · 综合、冲牌与作品集收口（6–8 周）
**是什么**：把前四个节点合成一个系统（agent 编排 + RAG 知识 + 自有模型 + 评测闭环），同时在正式比赛里换一个客观名次。到这里简历已经不缺项目，缺的是「一个能讲 40 分钟的完整系统」和「一个外部背书的排名」。
## 掌握的知识 / 技能
- 系统集成：把四个组件接成一条链路，端到端 SLA 与失败边界
- Kaggle 组队：在 Discussion 找思路互补的队友、Team Merge 截止规则、代码约定
- 终盘策略：public LB 与 private LB 的偏差、两枚 final submission 的对冲
- Solution writeup 的标准结构：问题 → 验证设计 → 关键 idea → 消融 → 没 work 的尝试
- 简历口径：用指标和决策讲项目；中/日/英三版的语气差异（日文要结论前置、敬体统一）
- 面试准备：系统设计题、成本估算题、作品深挖
## 可实践的 Kaggle 项目
- **一场进行中的 Featured / Research 比赛（组队）** — 从 [Featured 列表](https://www.kaggle.com/competitions?hostSegmentIdFilter=1)选 LLM / NLP / agent 方向、剩余 6 周以上、队数 800–3000 的一场，2–3 人组队，目标铜牌起。**只有 Featured / Research 发奖牌**，Getting Started 和 Playground 不发；1000+ 队时铜牌线为前 10%。组队本身也是面试信号。
- [ARC Prize — ARC-AGI-3](https://www.kaggle.com/competitions/arc-prize-2026-arc-agi-3)（交互式、面向 agent；静态版 [ARC-AGI-2](https://www.kaggle.com/competitions/arc-prize-2026-arc-agi-2)）— 要求全部方案开源、断网、不能调用外部 API。2026 届赛期到 11 月初，会在你 P1 前后结束，**本轮不作为夺牌目标**；花两小时读懂赛制，参赛放到下一届。
- [自己办一场 Community Hackathon](https://www.kaggle.com/competitions?new=true&type=hackathon) — 反向操作：定题、出数据、设评审标准、写 writeup 模板。**主办一场比赛在简历上的分量往往超过参加三场**——它证明你能定义问题和评价标准。
- [Konwinski Prize](https://www.kaggle.com/competitions/konwinski-prize) — 若还有余力，当毕业考：真实代码库上的 agent 修 bug，用 P1–P4 的全套家当去打。
## 教材
- **资料**：读 10 份以上 Kaggle 金牌 writeup（[Kaggle Solutions 索引](https://kaggle.farid.one/)），学的是**怎么写**，不只是怎么做。
- **日本**：资格证在日本市场是「未经验者的客观证明」，不替代作品集。若时间有余且需要简历过筛，G検定（入门）或 E資格（进阶）可考；但招聘方自己说最重要的是 Python/SQL、数理基础、以及**用业务语言解决问题的能力**。你有论文和作品集，优先级低于把项目讲清楚。
- **中国**：面试题库类资源用来自测盲点，不要用来背答案——你的项目经历比标准答案值钱。
## 阶段产出
- [ ] 一个整合系统：agent 编排 + RAG + 自有微调模型 + 评测闭环，一张架构图讲完
- [ ] Kaggle 奖牌一枚（或一次前 15% 的完整参赛记录 + 公开 writeup）
- [ ] GitHub 主页改造：置顶 3 个旗舰项目 + `agent-kit` + `agent-eval`，README 全英文带架构图与指标表
- [ ] 三语简历各一份（中 / 日 / 英），项目条目统一为「问题 → 做法 → 指标 → 我的贡献」
- [ ] 作品集网页一页：3 旗舰项目 + 1 公开基准 + 8 篇以上技术文章索引
- [ ] 面试问答备忘：每个项目预设 10 个深挖问题及回答要点（中/日/英）
> **求职节点 5：往高级岗谈**
> **简历能写**：「端到端 LLM 系统：agent 编排与工具安全、可溯源 RAG 知识层、自有微调模型服务、评测与安全回归 CI；Kaggle 奖牌 / 公开基准一项 / 主办 agent 评测黑客松一场。」
> **面试能聊**：整个系统的取舍链条——哪里用确定性流程、哪里让模型决定、哪里用 RAG、哪里用微调、成本分别多少。能把这条链讲清楚，你面的就不是入门岗了。


---
# 操作手册
<details>
<summary>算力：哪些阶段花钱，哪些不花</summary>
> P0–P3 基本不用租卡。这四个阶段的成本主要是 **API token**，不是 GPU。Kaggle Notebook 的免费额度（GPU 约 30h/周、单 session 12h、20GB 磁盘）足够跑 P2 的检索实验与 P3 的评测。从第一天就做 token 计费和响应缓存——一次跑飞的 agent 循环能烧掉一周预算，这是 agent 开发最常见的破财方式。
> P4 需要租卡，但可控：先用 0.5B–1.5B 小模型 + 几百条样本把训练脚本完全跑通（这一步在 Kaggle 免费额度里做），确认无误后再租卡跑全量。国内按量计费平台（AutoDL、恒源云、智星云一类）的 4090 时价最低，A100/H100 按需；海外 RunPod、[Vast.ai](http://Vast.ai) 同理。每次租卡前写下「这次要回答什么问题」，跑完记进账本。[国内外 GPU 云价格对比（2026-08）](https://aieii.com/posts/2026-08-20-gpu-cloud-price-comparison-2026/)可作为选平台参考，具体价格以平台当日为准。
> 把「在免费额度内完成 P0–P3」本身写进简历是有效的——它正是「能降本」这条招聘要求的证据。
</details>
<details>
<summary>归档比赛怎么用才学到东西：彩排法</summary>
> 这一版路线里大量比赛已归档。它们是最好的教材，因为**有标准答案**；但直接读解法等于抄。流程固定五步：
> ① 不看任何 Discussion，自己做 8–10 天（P4 的大赛可放宽到两周）。
> ② 用 Late Submission 提交，拿到私榜分数（多数已结束比赛开放此功能，少数不开放）。
> ③ 对照当年的奖牌线，确认自己落在什么位置。
> ④ 读前 10 名方案，把差距分成三类：我没想到的 idea / 想到但没做的 / 我做错的。
> ⑤ 只挑 2–3 条最关键的补做，验证分数变化。
> 第 ④ 步的清单本身就是面试素材——「我做这场比赛时漏掉了 X，后来理解了为什么 X 重要」，比「我拿了第几名」更能说明你在学习。解法检索可用 [Kaggle Solutions 索引](https://kaggle.farid.one/)。
</details>
<details>
<summary>每周 20 小时怎么分</summary>
> **11h 主线项目** —— 当前阶段的旗舰项目或主攻比赛，集中在两个大块时间里。碎片时间做不了系统设计。
> **4h 学习** —— 教材 + 读解法。硬规则：每读完一份解法或一章书，写下一句「我因此能做什么了」。
> **2h 工程回收** —— 把这周的一次性脚本收进 `agent-kit` / `agent-eval`。不做这一步，到 P4 你还在重写客户端。
> **2h 写作** —— 英文主稿。写作是唯一有复利的动作：它既是面试材料，也是被动曝光。
> **1h 复盘** —— 更新进度、看一眼 Kaggle 进行中列表、决定是否要插入一场新比赛。
</details>
<details>
<summary>怎么挑一场进行中的比赛（这一版的筛选口径变了）</summary>
> 因为主线是 Agent / LLM，筛选标准不再是「哪场好拿牌」，而是**「打完能不能写进这条主线」**。六条：
> ① 题材是 agent / 工具调用 / 检索 / LLM 微调之一吗？不是就跳过，哪怕容易拿牌。
> ② 发不发牌（只有 Featured / Research 发）。
> ③ 剩余时间 ≥6 周。
> ④ 队数 800–3000 最划算。
> ⑤ 算力可行：断网内核跑得完吗、需要几张卡。
> ⑥ 产出能不能接进你现有的三个旗舰项目。
> 常用入口：[进行中全部](https://www.kaggle.com/competitions?listOption=active) · [Featured](https://www.kaggle.com/competitions?hostSegmentIdFilter=1) · [NLP 标签](https://www.kaggle.com/competitions?tagIds=13204-NLP) · [AI Benchmarks](https://www.kaggle.com/benchmarks) · [全部比赛与黑客松](https://www.kaggle.com/competitions)
</details>
<details>
<summary>中日两地的简历与面试口径差异</summary>
> **中国**：直接给指标和赛道关键词。招聘方按赛道筛人（Agent 工程 / RAG & 记忆 / LLM 应用开发），所以简历的项目标题就用赛道语言写，别写「智能助手」这种模糊的名字。面试重技术深度和「你怎么知道它是对的」。
> **日本**：更看重「能不能稳定运维」和「能不能和业务沟通」。同一个项目在日文简历里要多写两件事——**運用体制**（监控、回归、事故处理）和**業務課題**（解决了谁的什么问题）。技术栈里务必显式写出 LangChain / LlamaIndex / 向量库 / Docker / 云平台，因为求人票就是按这些关键词筛的。
> **英文**是主稿（GitHub、Kaggle writeup、技术文章），中日文版各改写一次。日文版不要逐句翻译：结论前置、敬体统一、把「我做了什么」改写成「这带来了什么」。
</details>
<details>
<summary>三个角色到底差在哪（面试自我定位用）</summary>
> **AI Agent Engineer** —— 被考「你的 agent 什么时候会坏，你怎么发现的」。核心资产：工具契约设计、编排取舍、安全护栏、轨迹评测。**你的主身份。**
> **LLM Engineer** —— 被考「同样的效果你能做到多便宜多快」。核心资产：微调、量化与服务化、推理优化、成本账。**P4 之后的第二身份。**
> **AI Engineer（泛）** —— 被考「你怎么知道这个提升是真的」。核心资产：数据、验证、评估。**P3 让你在这一格也站得住。**
> 三者的公共底座是同一件事：**可测量**。你研究里那套「不用真标签、从模型行为本身估计可推断性」的思路，恰好是三条线都缺的能力——每份材料里讲一次，每次面试提一次。
</details>
---
# 这条路线会在哪里断
> **Agent 类比赛本来就少，且多为 Hackathon / Simulations 形态。** 这意味着「用 Kaggle 排名证明 agent 能力」这条路本身较窄。应对方式已经写进路线：主要产出物是**旗舰项目 + 公开基准 + writeup**，Kaggle 在这里的角色是提供真实基准与对照解法（尤其 AI Agent Security、Skill Lift、AgentEval 三场），奖牌集中放在 P5 去拿。不要因为找不到 agent 比赛就退回去打表格赛。


> **框架版本变化快于书籍。** LangChain / LangGraph / LlamaIndex 的 API 每几个月就动一次，中文书和 B 站课程一定会滞后。规则：**概念看书，API 看官方文档**。书里的项目照做但用当前版本重写，这本身就是一次有价值的练习。


> **时间被研究挤掉。** 真冲突时的取舍顺序：论文 > 当前阶段主线项目 > 写作 > 读书。研究与路线能合并的点在 **P3**（评测框架 + Kaggle Benchmarks）——尽量让一份工作算两次。


> **demo 病。** Agent 方向最容易做出十个漂亮 demo、零个能上线的东西，而两地招聘方都明确说不看 demo 看交付证据。硬规则：**一个阶段只许有一个旗舰项目**，宁可窄，也要有成功率、延迟、成本三个数字。


---
> 页内比赛链接在编写时已逐条确认可达；**开放状态、截止日与奖牌线以 Kaggle 页面为准**。已知时点：ARC Prize 2026 赛期 2026-03-25 → 11-02；Gemma 4 Good Hackathon 最终提交 2026-05-18（已结束）；AIMO Progress Prize 3 于 2026-04 结束；AI Agent Security - Multi-Step Tool Attacks 于 2026 年中开赛。市场数据引自 2026 年 9 月的公开招聘分析，仅作方向参考。
> v2.1（Agent 优先，中文教材已更新为 2025–2026 年版）。每个阶段结束时回来改一次——尤其「可实践的 Kaggle 项目」一栏，它会过期。
