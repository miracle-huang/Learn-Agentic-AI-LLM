# 🧭 Agentic AI&LLM：Kaggle

> **Agent 优先的转职路线（v2.4）** — 主线：AI Agent Engineer → LLM Engineer。投入 20h/周，总计约 44–52 周；用时为相对周期，不锚定日期。第 3 个月（P1 结束）起即可开始投简历。算力：无本地 GPU，P0–P3 基本只花 API token，P4 才需租卡。目标市场：中国 + 日本；技术写作英文主稿 + 中/日文版。
>
> [网页版（同一份内容，可对照）](https://claude.ai/artifact/7E12f1Jo4g6fpZw6Yyxvm2)

<!-- notion-toc:start -->

- [市场读数（2026-09）](#市场读数2026-09)
  - [中国 · 五条赛道](#中国--五条赛道)
  - [日本 · 硬性要求与行情](#日本--硬性要求与行情)
- [阶段与求职节点](#阶段与求职节点)
- [教材与视频总览：英文为主，中文版随附](#教材与视频总览英文为主中文版随附)
  - [书](#书)
  - [视频与课程](#视频与课程)
- [P0 · Agent 地基：把 LLM 调用写成工程（4–5 周）](#p0--agent-地基把-llm-调用写成工程45-周)
  - [掌握的知识 / 技能](#掌握的知识--技能)
  - [可实践的 Kaggle 项目](#可实践的-kaggle-项目)
  - [教材](#教材)
  - [阶段产出](#阶段产出)
- [P1 · 能交付的 Agent：编排、安全、可观测（8–10 周）](#p1--能交付的-agent编排安全可观测810-周)
  - [掌握的知识 / 技能](#掌握的知识--技能-1)
  - [可实践的 Kaggle 项目](#可实践的-kaggle-项目-1)
  - [教材](#教材-1)
  - [阶段产出](#阶段产出-1)
- [P2 · RAG 与记忆：agent 的知识侧（8–10 周）](#p2--rag-与记忆agent-的知识侧810-周)
  - [掌握的知识 / 技能](#掌握的知识--技能-2)
  - [可实践的 Kaggle 项目](#可实践的-kaggle-项目-2)
  - [教材](#教材-2)
  - [阶段产出](#阶段产出-2)
- [P3 · 评测与 LLMOps：把「能跑」变成「能证明」（6–8 周）](#p3--评测与-llmops把能跑变成能证明68-周)
  - [掌握的知识 / 技能](#掌握的知识--技能-3)
  - [可实践的 Kaggle 项目](#可实践的-kaggle-项目-3)
  - [教材](#教材-3)
  - [阶段产出](#阶段产出-3)
- [P4 · LLM 工程：微调、量化与推理优化（10–12 周）](#p4--llm-工程微调量化与推理优化1012-周)
  - [掌握的知识 / 技能](#掌握的知识--技能-4)
  - [可实践的 Kaggle 项目](#可实践的-kaggle-项目-4)
  - [教材](#教材-4)
  - [阶段产出](#阶段产出-4)
- [P5 · 综合、冲牌与作品集收口（6–8 周）](#p5--综合冲牌与作品集收口68-周)
  - [掌握的知识 / 技能](#掌握的知识--技能-5)
  - [可实践的 Kaggle 项目](#可实践的-kaggle-项目-5)
  - [教材](#教材-5)
  - [阶段产出](#阶段产出-5)
- [操作手册](#操作手册)
- [这条路线会在哪里断](#这条路线会在哪里断)

<!-- notion-toc:end -->

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

| 阶段 | 主题 | 用时 | 求职节点 |
| --- | --- | --- | --- |
| P0 | Agent 地基 | 4–5 周 | 纯技术积累，**不作为节点** |
| P1 | 能交付的 Agent | 8–10 周 | → Agent / LLM 应用开发工程师 |
| P2 | RAG 与记忆 | 8–10 周 | → RAG 工程师 · 社内 QA 系统开发 |
| P3 | 评测与 LLMOps | 6–8 周 | → LLMOps / AI 品質保証 |
| P4 | 微调与推理 | 10–12 周 | → LLM Engineer（正式转入） |
| P5 | 综合与冲牌 | 6–8 周 | → 高级岗 / 奖牌与作品集收口 |

用时是相对周期，不锚定具体日期，按 20h/周 估算。**P1 结束就开始投**——不要等全部做完。每个节点的「简历能写什么 / 面试能聊什么」写在对应阶段的粉色框里。后续阶段既是能力升级，也是面试时把同一个项目讲得更深的弹药。

# 教材与视频总览：英文为主，中文版随附

## 书

| 资料 | 作者 / 出版 | 中文资料 | 用在 |
| --- | --- | --- | --- |
| AI Agents: The Definitive Guide | Nicole Koenigstein，O'Reilly 2026-09 | 暂无 | P0–P1 动手主线 |
| Agentic Design Patterns | Antonio Gulli，Springer 2025（免费全文） | 社区译本（非官方） | P0–P1 模式速查 |
| Building Applications with AI Agents | Michael Albada，O'Reilly | 暂无 | P1 多 agent |
| AI Engineering | Chip Huyen，O'Reilly 2025 | 《AI工程：大模型应用开发实战》人邮 2026-02 | P2–P4 共用主参考 |
| Hands-On RAG for Production | Mendelevitch、Bao，O'Reilly 2026-05 | 暂无 | P2 RAG 主线 |
| Building Data-Driven Applications with LlamaIndex | Andrei Gheorghiu，Packt 2024 | 《LlamaIndex大模型RAG开发实践》清华 2025-07 | P2 照着敲 |
| Evals for AI Engineers | Shankar、Husain，O'Reilly 2026-10 | 暂无（先看免费 FAQ / 邮件课） | P3 评测专书 |
| Hands-On Large Language Models | Alammar、Grootendorst，O'Reilly 2024 | 《图解大模型》人邮 2025-05 | P4 主线 |
| LLM Engineer's Handbook | Iusztin、Labonne，Packt 2024 | 《大语言模型工程师手册》人邮 2025-05 | P4 工程 |
| Build a Reasoning Model (From Scratch) | Sebastian Raschka，Manning | 暂无 | P4 推理模型 |

## 视频与课程

| 资料 | 出处 | 中文资料 | 用在 |
| --- | --- | --- | --- |
| 吴恩达《Agentic AI》 | [DeepLearning.AI](http://DeepLearning.AI) 2025-10 | B 站中英双语 | P0 主课 |
| Deep Dive into LLMs like ChatGPT | Karpathy，YouTube 2025-02 | B 站中英精校 | P0 原理 |
| 生成式人工智慧導論 | 李宏毅，台大 2025 秋 / 2026 春 | 中文原生 | P0、P4 |
| Hugging Face AI Agents Course | Hugging Face，免费 | — | P0–P2 |
| Agentic AI MOOC（CS294-196） | UC Berkeley，2025 秋 | 英文原版 | P1 主课 |
| Retrieval Augmented Generation | [DeepLearning.AI](http://DeepLearning.AI)，Coursera | 英文原版 | P2 主课 |
| AI Evals（FAQ + 邮件课 + Maven） | Hamel Husain、Shreya Shankar | 英文原版 | P3 |
| CS336 Language Modeling from Scratch | Stanford，2026 春 | B 站中英字幕 | P4 主课 |

**选书原则**：每个阶段只有一本「照着敲」的主线书，其余是参考。英文资料优先，因为 agent 方向的一手内容几乎都先以英文出现，中文书普遍滞后一到两年、代码框架已过时。中文原创书（张奇、郑天民、尹浩、杨威理）保留为**概念参考与理论补充**，不再作为动手教材；已有中文译本的英文书（AI Engineering、Hands-On LLMs、LLM Engineer's Handbook、LlamaIndex）可以直接读中文版。

---

# P0 · Agent 地基：把 LLM 调用写成工程（4–5 周）

**这个阶段是什么**：唯一一个不作为求职节点的阶段。你已经会调多个 LLM、会设计 prompt，但那是研究脚本；这里把它改造成有类型、有重试、有成本账、能被别人调用的工程代码。四周内不追求复杂架构，只追求「一个带三个真实工具的 agent，能跑、能测、能部署」。

能力配比：`Agent 70%` · `LLM 20%` · `工程 10%`

## 掌握的知识 / 技能

- function calling / tool schema 设计与参数校验
- 结构化输出（JSON Schema、Pydantic、解析失败兜底）
- 多模型客户端抽象
- SSE 流式、超时、重试与指数退避、幂等
- **token 计费与响应缓存**
- Python 工程化（uv、pytest、类型标注、FastAPI、Docker、Git/PR）
- Kaggle 断网内核与运行上限

## 可实践的 Kaggle 项目

- [5-Day AI Agents Intensive（Google × Kaggle）](https://www.kaggle.com/competitions/5-day-ai-agents-intensive-vibecoding-course-with-google) — **怎么用：**这是本阶段的主干。2026 年 6 月那期有 35 万人注册，课程覆盖 agent 的设计、安全到云端部署全生命周期。往期材料（视频 + 白皮书 + Notebook）全部公开，按天自学，每天的 Notebook 自己重写一遍而不是跑一遍。若期间开了新一期，立刻报名——它自带一个能提交的 capstone 和一个 Discord 社区。
    - 入口：[5-Day AI Agents: Intensive Vibe Coding Course With Google](https://www.kaggle.com/learn-guide/5-day-agents-vibecoding)
- [AI Agents Intensive Capstone](https://www.kaggle.com/competitions/vibecoding-agents-capstone-project)（[更早一期](https://www.kaggle.com/competitions/agents-intensive-capstone-project)）— **怎么用：**6000+ 份提交。本阶段**只读不做**：挑 10 份优胜作品，逐份记录「它解决什么问题、用了几个工具、怎么处理失败、README 怎么写」。这份笔记就是你 P1 选题的素材库。
- [The Gemma 4 Good Hackathon](https://www.kaggle.com/competitions/gemma-4-good-hackathon)（已结束 2026-05-18）— **怎么用：**\$200K 奖池，Google DeepMind 合办，主题是用 Gemma 4 的多模态与**原生 function calling** 解决健康/教育/气候的真实问题。读优胜作品，重点看「开源模型怎么做工具调用」——这决定了你以后能不能不依赖闭源 API 交付。
- **Kaggle 平台热身** — **怎么用：**只做一件事——在 Kaggle Notebook 的**断网内核**里把你的 agent 代码跑通一次。不用参加任何表格类比赛。断网环境是后面 P2/P4 几场比赛的硬约束，越早适应越好。

## 教材

- **\~\~中文书**：《~~\[~~AI Agent开发实战：从基础原理到企业级应用~~\](~~[~~https://weread.qq.com/web/reader/41232030813abb05bg019c0c)\</span\>~~](https://weread.qq.com/web/reader/41232030813abb05bg019c0c)\</span\>)》郑天民，机械工业出版社 2025-09（智能系统与技术丛书，ISBN 9787111788737），第 1–2 章：Agent 核心概念、开发模式、用 LLM 与 Swarm 框架搭第一个 agent\~\~
    - [x] 第1章 AI Agent开发模式
    - [x] 第2章 LLM和Agent
- **动手主线**：《AI Agents: The Definitive Guide — Design, Deployment, and Evaluation for Production》Nicole Koenigstein，O'Reilly（ISBN 9798341666931）。**本阶段真正照着敲的那本**：从设计到部署到评估，跟着配套 GitHub 代码走一遍。英文，但框架是当前在用的。O'Reilly 2026-09 第一版，全书 12 章、无附录。**P0 先读第 1–2 章，其余随 P1 展开。**中文：暂无中文版。
    - [对应GitHub代码](https://github.com/Nicolepcx/ai-agents-the-definitive-guide)
    - [x] 第 1 章 From LLMs to Agents: The Foundational Blueprint（从 LLM 到 Agent：用有限与分层状态机打控制流的地基）
    - [ ] 第 2 章 Architectures and Patterns: Planning, Reactivity, and Multi-Agent Systems（架构与模式：结构化推理、反思、human-in-the-loop、分层与群体）
    - [ ] 第 3 章 Advanced Planning, Reasoning, and Scalable Execution in Agents（进阶规划与推理：奖励、相对/绝对评估、强化学习、测试时计算、搜索与自适应 MCTS）
    - [ ] 第 4 章 Models Behind the Agents: Capabilities and Optimization（agent 背后的模型：decoder-only / encoder-only / MoE / 推理模型，开源与闭源、adapter、量化）
    - [ ] 第 5 章 From Prototypes to Production: Contracts, Tools, and Reliable Execution（结构化契约、输出校验、工具集成、MCP 与 server 发现、deep agents）
    - [ ] 第 6 章 Secure Execution and Tool Governance（沙箱、运行时隔离、云端代码环境、程序化工具调用的护栏）
    - [ ] 第 7 章 Deploying Agents in Real Products（MVP 到生产：监控、容错与降级、推理后端、冷启动、缓存）
    - [ ] 第 8 章 Foundational Evaluation and Operational Observation of Agentic Systems（上线前压测与上线后观测）
    - [ ] 第 9 章 Customized and Advanced Evaluation of Agentic Systems（自定义基准、生产 trace、跨视觉输入的长周期推理评测）
    - [ ] 第 10 章 Agent Memory: How Persistence Turns Agents into Evolving Systems（短期/长期/情景/语义/程序记忆、记忆卫生、多 agent 记忆设计）
    - [ ] 第 11 章 From Compute to Cost: Designing Efficient Agentic Systems（模型显存、FlashAttention、推理经济学、agentic 状态迁移的复用）
    - [ ] 第 12 章 Threat Modeling for AI Agents（威胁建模、分层防御、红队、贯穿生命周期的系统级防护）
- **模式速查**：[Agentic Design Patterns](https://www.amazon.com/Agentic-Design-Patterns-Hands-Intelligent/dp/3032014018) — Antonio Gulli（Google），Springer 2025，作者公开了免费全文。21 种 agent 设计模式逐一配代码（提示链、路由、反思、工具使用、规划、多智能体、记忆、护栏、评估等）。不用通读，当作**设计取舍时翻的速查手册**。中文：无官方中文版；社区全文译本 [Jimmy Song 在线版](https://jimmysong.io/zh/book/agentic-design-patterns/) / [GitHub 中文版](https://github.com/ginobefun/agentic-design-patterns-cn)。
- **视频主课**：[吴恩达《Agentic AI》](https://www.deeplearning.ai/courses/agentic-ai) — [DeepLearning.AI](http://DeepLearning.AI) 2025-10。围绕反思、工具使用、规划、多智能体四大设计模式，并把**评估与错误分析**当成主线来讲——这正是招聘方最看重、也是你 P3 的护城河。不依赖特定框架，用原生 Python 写，所以不会随框架过时。中文：[B 站中英双语字幕搬运](https://www.bilibili.com/video/BV1LK47z4EHU/)。
- **视频原理**：[Karpathy · Deep Dive into LLMs like ChatGPT](https://x.com/karpathy/status/1887211193099825254) — 2025-02，3.5 小时。从预训练、后训练到 RL 与幻觉的完整心智模型，面向工程师而不是研究者。看完再调 agent，你会知道模型「为什么这样犯错」。中文：[B 站中英精校完整版](https://www.bilibili.com/video/BV1kPNpeTEQ5/)。
- **中文视频**：台大李宏毅《[生成式人工智慧導論](https://speech.ee.ntu.edu.tw/~hylee/GenAI-ML/2025-fall.php)》2025 秋，官方课程页。只看 LLM 原理与 Agent 相关讲次，不要全刷
    - [ ] 【必看】2025 秋 第 1 讲：一堂课搞懂生成式人工智能的原理 — [YouTube](https://youtu.be/TigfpYPJk1s)
    - [ ] 【必看】2025 秋 第 2 讲：上下文工程（Context Engineering）— AI Agent 背后的关键技术 — [YouTube](https://youtu.be/lVdajtNpaGI)
    - [ ] 【必看】补充：一堂课搞懂 AI Agent 的原理（AI 如何透过经验调整行为、使用工具和做计划）— [YouTube](https://youtu.be/M2Yg1kwPpts)
    - [ ] 【必看】2026 春：解剖小龙虾 — 以 OpenClaw 为例介绍 AI Agent 的运作原理 — [YouTube](https://youtu.be/2rcJdFuNbZQ)
    - [ ] 【可选】大型语言模型是如何进行「深度思考」（Reasoning）的？— [YouTube](https://youtu.be/bJFtcwLSNxI)
    - [ ] 【可选】2026 春：Context Engineering 基本概念解说（与第 2 讲二选一）— [YouTube](https://youtu.be/urwDLyNa9FU)
- **课程**：[Hugging Face AI Agents Course](https://huggingface.co/learn/agents-course) Unit 0–1（免费）：Agent 概念与工具调用。中文：无，英文原版。
    - [ ] Unit 0 **Welcome to the 🤗 AI Agents Course**
    - [ ] Unit 1 **Introduction to Agents**
- **白皮书**：[Agent Tools & Interoperability with MCP](https://www.kaggle.com/whitepaper-agent-tools-and-interoperability-with-mcp)
    - [x] 中文翻译：

## 阶段产出

- [ ] `agent-kit` 仓库：多模型客户端 + 工具注册表 + 结构化输出校验 + 重试 + token 计费与缓存，pytest 覆盖，Docker 可跑
- [ ] 一个最小可用 agent：3 个真实工具（如网页检索、文件读写、计算），FastAPI 暴露接口
- [ ] 《工具 schema 设计规范》一页文档（英文），含 5 个反例
- [ ] Capstone 优胜作品拆解笔记（10 份），作为 P1 选题库
- [ ] 算力与成本账本的第一页

> 这个阶段**不要**去打表格/时序类比赛，也不要用你的生理信号经验刷排名——它和 Agent / LLM 岗位的招聘口径接不上，是这一版路线刻意砍掉的部分。你的研究经历会在 P3 以「评测方法论」的形式重新接回来，那才是它真正值钱的地方。

---

# P1 · 能交付的 Agent：编排、安全、可观测（8–10 周）

**这个阶段是什么**：从「能跑的 demo」到「敢交付的 agent」。差别全在三件事上——出错怎么恢复、被恶意输入怎么办、坏了怎么定位。这一阶段做完，你就具备了中国「Agent 工程」赛道和日本「AI Agent 開発」岗位的入门交付能力。

能力配比：`Agent 80%` · `LLM 15%` · `工程 5%`

## 掌握的知识 / 技能

- **LangGraph**：有向图编排、状态机、检查点与断点续跑、human-in-the-loop 审批节点（日本企业尤其看重这个）
- **smolagents**（代码型 agent）与 **LlamaIndex** agents 的适用边界；什么时候单 agent 就够、什么时候才需要多 agent
- **MCP**：写自己的 MCP server、把已有服务包成工具、客户端接入
- 编排模式取舍：ReAct / plan-and-execute / 固定工作流，以及「能用确定性流程就别用 agent」的判断
- **安全与护栏**：prompt 注入与间接注入、工具权限最小化、沙箱代码执行、输出校验、多步攻击链
- 失败恢复：超时、部分失败、补偿事务、降级路径
- **可观测性**：trace / span、成本归因、失败模式聚类（LangSmith / OpenTelemetry / 自建）

## 可实践的 Kaggle 项目

- [AI Agent Security - Multi-Step Tool Attacks](https://www.kaggle.com/competitions/ai-agent-security-multi-step-tool-attacks) （2026 年中开赛·状态见页面）— **本阶段的核心，整条路线里最有面试价值的一场。**Kaggle 与 OpenAI、Google、IEEE 合办的 Simulations 赛：在一个确定性离线基准里，构造攻击算法去找出工具调用 agent 的**可复现多步失败**。**怎么用：**① 先跑公开 baseline notebook，理解基准怎么判定「失败」；② 自己实现攻击算法并提交，拿到榜上分数；③ **最关键的一步——反向用**：把你找到的失败模式整理成一个回归测试集，套到你 P1 自己那个 agent 上，逐条修掉。这样你同时拥有「会攻」和「会防」两份证据，面试里几乎没人能跟上这个话题。若比赛已结束，公开 notebook 和讨论区仍在，照样按上面三步做。
- [BenchFlow - Agent Skill Lift](https://www.kaggle.com/competitions/skill-lift) （状态见页面）— **怎么用：**基于 SkillsBench / Bench-Mix，评估 agent「skill」的有效性、能力与安全性（[SkillsBench](https://www.skillsbench.ai/) 有 87 个任务、8 个专业领域，公开排行榜与 GitHub 数据）。本阶段从**被评测方**的角度用它：给你的 agent 写 skill、看它在别人设计的任务上掉在哪里。P3 会再回来一次，那时换成**评测设计方**的角度。
- [AI Agents Intensive Capstone 标准](https://www.kaggle.com/competitions/vibecoding-agents-capstone-project) （已结束·照标准做）— **怎么用：**这就是你的**旗舰项目 1**。按 capstone 的提交标准（可运行、有 writeup、有演示）做一个**选题足够窄、工具足够真**的 agent。选题原则：宁做「把 arXiv 上某一细分领域的新论文按你的研究口径筛选并生成周报」这种窄题，也不做「通用科研助手」。窄题才能把成功率做到能报数字。
- [Kaggle Community Hackathons](https://www.kaggle.com/competitions?new=true&type=hackathon) （长期开放）— **怎么用：**2026 年 3 月上线的能力，任何人都能免费用 Kaggle 的基建办比赛（数据托管、Notebook、writeup 提交、作品展廊、多赛道评审，奖池上限 \$1 万）。本阶段先作为**参赛者**刷 2–3 场小型 agent 黑客松——周期短、有 deadline、有 writeup 产出，是最适合边学边攒作品的形态。留意 Kaggle 竞赛页有没有新的 agent 主题 hackathon。

## 教材

- **英文书**：[Building Applications with AI Agents](https://www.oreilly.com/library/view/building-applications-with/9781098176495/) — Michael Albada，O'Reilly，副标题 *Designing and Implementing Multiagent Systems*，[配套 GitHub](https://github.com/michaelalbada/BuildingApplicationsWithAIAgents)。专讲多 agent 系统的设计与实现。和 Definitive Guide 互补：那本讲单个 agent 做扎实，这本讲多个 agent 怎么拆分与配合。中文：暂无中文版。
- **视频主课**：[UC Berkeley · Agentic AI MOOC](https://agenticai-learning.org/f25)（CS294-196，2025 秋）— 伯克利 RDI 的旗舰 MOOC 系列（累计 4 万+ 学习者），多位一线研究者轮讲，免费；适合在动手之余补齐 agent 领域的全景与前沿。中文：未找到完整中文字幕版，英文原版 + YouTube 自动字幕。
- **中文书（概念参考，不照做）**：下面三本把 ReAct / Plan-and-Execute / 多智能体（AutoGen、MetaGPT、CrewAI、LangGraph）和 MCP 五大要素讲得最全，**用来快速建立中文的概念地图**；但书里的代码框架已经更新换代，逐例重复实现意义不大，实现一律以官方文档和上面那本英文书为准。
    - 《AI Agent开发实战》郑天民（2025-09）第 3–8 章：ReAct Agent、Plan-and-Execute Agent、接 RAG 的知识型 agent、多模态 agent（LangChain + LlamaIndex），以及**企业级工程化**与多智能体（AutoGen、LangGraph）。只看概念与取舍，代码不照敲。
    - 《AI Agent应用开发：构建多智能体协同系统》尹浩，清华大学出版社 2025-11 — 第 6 章**规划能力**（CoT、Self-Ask、Self-Reflexion、Function Calling、ReAct、Plan-and-Execute、Self-Discover 逐个实现）、第 7 章**多智能体**（AutoGen、MetaGPT、CrewAI、LangGraph 对比）。中文里对编排模式讲得最全的一本。
    - 《MCP开发从入门到实战》杨威理，人民邮电出版社 2025-06 — MCP 架构与五大要素（resources / prompts / tools / sampling / roots）、SDK、自己写 server、MCP Inspector 调试。（另有《MCP极简开发》王双等，人邮 2025-06，偏应用场景，可选。）
- **课程**：[HF Agents Course](https://huggingface.co/learn/agents-course) Unit 2（三个框架各一遍）与 **Unit 4 期末项目（必做，带自动评测和排行榜，是你第一个客观分数）**
- **视频**：[DeepLearning.AI](http://DeepLearning.AI) [AI Agents in LangGraph](https://www.deeplearning.ai/courses/ai-agents-in-langgraph)、[Building Code Agents with smolagents](https://www.deeplearning.ai/courses/building-code-agents-with-hugging-face-smolagents)
- **文档**：LangGraph、smolagents、MCP 的官方文档是这一阶段的唯一 API 依据。**概念看书，API 看官方文档**——框架版本变得比任何书都快，这也是中文书只当概念参考的原因。

## 阶段产出

- [ ] **旗舰项目 1**：上线可访问的窄域 agent —— LangGraph 编排 + MCP 工具 + 护栏 + trace + Docker 部署
- [ ] **agent 回归测试集**：来自 AI Agent Security 的失败模式，逐条对应一个测试用例与修复说明
- [ ] HF Agents Course Unit 4 的自动评测分数（一个客观数字）
- [ ] 自建 MCP server 一个（把你的某项研究工具包成标准接口）
- [ ] 英文技术文章《What broke in my agent, and how I found it》
- [ ] 2–3 场 Community Hackathon 的 writeup

> **求职节点 1：可以开始投了**
>
> **简历能写**：「独立设计并交付带工具调用的 agent 服务，含权限边界与沙箱执行、失败恢复与降级路径、trace 级可观测性；基于公开对抗基准建立 N 条回归测试，修复 M 类多步失败。」用数字说话：工具数、任务成功率、p95 延迟、每任务成本。
>
> **面试能聊**：① 为什么这里用固定工作流而不是让模型自己规划；② 你的工具 schema 怎么防止模型误用；③ 间接 prompt 注入你怎么防的；④ 一次线上失败你是怎么从 trace 定位到根因的。这四个问题是 Agent 岗的高频题，你有实物可以打开给面试官看。
>
> **对口岗位**：中国「Agent 工程 / LLM 应用开发」；日本「AI エージェント開発 / LLM アプリケーションエンジニア」。

---

# P2 · RAG 与记忆：agent 的知识侧（8–10 周）

**这个阶段是什么**：补上 agent 的另一半——知识。这也是两地**岗位数量最大**的方向：中国的「RAG & 记忆」赛道，日本几乎每家公司都在做的「社内 QA / 社内文書検索」。日本招聘明确点名 LangChain / LlamaIndex + 向量库，指的主要就是这块活。做法上要按 **Agentic RAG** 来做（检索是 agent 的一个工具，而不是一条固定流水线），这样 P1 的成果直接复用。

能力配比：`Agent 45%` · `LLM 45%` · `工程 10%`

## 掌握的知识 / 技能

- **文档解析**：PDF / 表格 / 扫描件 / Office，版面还原与表格抽取（企业场景里这一步的工作量常被低估）
- chunk 策略：固定窗口 vs 语义切分 vs 版面感知；父子块与上下文扩展
- embedding 选型与多语言（中/日/英混合语料的坑）
- 向量库工程：Chroma / Milvus / pgvector / Pinecone 的取舍，索引参数、增量更新、删除与重建
- **混合检索**：BM25 + dense 融合、RRF；**rerank**（cross-encoder）带来的收益与延迟代价
- 查询改写、多跳检索、HyDE；何时该让 agent 决定「再检一次」
- **引用与溯源**：answer 到 chunk 到原文页码的可追溯链路
- **权限过滤**：多租户、行级权限、检索阶段就过滤而不是事后过滤
- 记忆：会话记忆、长期记忆、记忆写入与遗忘策略
- **质量量化**：grounding 率、引用准确率、幻觉率、检索召回/命中率的定义与测量

## 可实践的 Kaggle 项目

- [Kaggle - LLM Science Exam](https://www.kaggle.com/competitions/kaggle-llm-science-exam) （已归档）— **本阶段主攻，最好的受限 RAG 训练场。**断网环境下答科学难题，顶层解法的胜负手是**自建维基检索库 + 重排**，而不是更大的模型——这正是企业 RAG 的真实处境（数据在内网、算力有限）。**怎么用：**先自己闭卷做 8–10 天建索引与检索，用 Late Submission 拿私榜分，再读前 10 名方案，把差距分成「没想到 / 想到没做 / 做错了」三类，只补做最关键的 2–3 条。
- [AgentEval Part I: Grounded RAG Benchmark](https://www.kaggle.com/competitions/agent-eval-part-i-grounded-rag-benchmark) （状态见页面）— **怎么用：**这场比赛的评估目标直接就是 **grounding、引用准确率、幻觉控制**——和企业 RAG 的验收标准完全重合。把它当成你旗舰项目 2 的「外部验收标准」：先在这里学会怎么量化这三件事，再把同一套指标搬到自己的系统上报数。
- [Eedi - Mining Misconceptions in Mathematics](https://www.kaggle.com/competitions/eedi-mining-misconceptions-in-mathematics) （已归档）— **怎么用：**把学生的错误选项匹配到对应数学误解——本质是**召回 + 重排**的检索赛，顶层方案用 LLM 生成难负例来训练检索器。专门用来补「检索器怎么训」这一块，这是 RAG 从「能用」到「好用」的分水岭。
- [LLM Agentic Legal Information Retrieval](https://www.kaggle.com/competitions/llm-agentic-legal-information-retrieval) （社区赛·不发牌）— **怎么用：**agentic 检索在法律领域的应用。虽是社区赛、不计奖牌，但**题材对口**——日本的社内規程検索、契約書 QA 就是同一类任务（长文档、严格溯源、错了有后果）。做完可以直接改写成一段面向日本企业的项目描述。
- [The Learning Agency Lab - PII Data Detection](https://www.kaggle.com/competitions/pii-detection-removal-from-educational-data) （已归档）— **怎么用：**企业 RAG 躲不开的合规环节——从文档里检测并移除个人信息。token 级分类、极度类别不平衡，顶层方案的关键是**用 LLM 合成训练数据**。做一个轻量版（2 周）接进你的 RAG 入库流程，作为「脱敏中间件」。隐私 + 合规在中日两地都是加分项。

## 教材

- **主参考书**：**AI Engineering: Building Applications with Foundation Models** — Chip Huyen，O'Reilly 2025。近两年口碑最好的一本 AI 工程书，**P2–P4 三个阶段共用**。本阶段读第 6 章 RAG and Agents；第 3–4 章（评测）留给 P3，第 7–9 章（微调、数据、推理优化）留给 P4。中文：《AI工程：大模型应用开发实战》宝玉 译，人民邮电出版社 2026-02（ISBN 9787115686398，[豆瓣 8.7](https://book.douban.com/subject/38236657/)）。中文版口碑同样很好，可以直接读中文。
- **RAG 专书**：[Hands-On RAG for Production](https://www.oreilly.com/library/view/hands-on-rag-for/9798341621701/) — Ofer Mendelevitch、Forrest Sheng Bao，O'Reilly 2026-05。企业级 RAG 从解析、嵌入、向量库到混合检索、幻觉缓解、评测，再到 agentic RAG、多模态 RAG、知识图谱与治理。**本阶段 RAG 部分的主线**，和你的旗舰项目 2 几乎一一对应。中文：暂无中文版。
- **照着敲**：**Building Data-Driven Applications with LlamaIndex** — Andrei Gheorghiu，Packt 2024。文档与节点、各类索引、检索与后处理、响应合成、agent 与部署，**日本求人票点名的就是 LlamaIndex**。中文：《LlamaIndex大模型RAG开发实践》杨森等 译，清华大学出版社 2025-07（ISBN 9787302697084）。
- **视频主课**：[DeepLearning.AI · Retrieval Augmented Generation](https://www.deeplearning.ai/courses/retrieval-augmented-generation)（Coursera）— Coursera 上的完整课程（不是 1 小时短课），从检索、向量库讲到评测与生产化。中文：未找到可靠中文字幕版，英文原版。
- **课程**：[HF Agents Course](https://huggingface.co/learn/agents-course) Unit 3：Agentic RAG——正好是本阶段要的「检索作为工具」的范式。
- **文档**：LlamaIndex 官方文档的 indexing / retrieval / evaluation 三章要通读。日本求人里点名它，不是随便点的。
- **中文原创**：尹浩《AI Agent应用开发》第 5 章记忆模块（MemGPT / Mem0 / BoT），可选，用来补中文的记忆概念。

## 阶段产出

- [ ] **旗舰项目 2**：企业级 RAG 系统 —— 多格式文档解析 + 混合检索 + rerank + 引用溯源 + 行级权限 + 增量更新
- [ ] **质量报告**：grounding 率、引用准确率、幻觉率、检索召回，含消融表（加 rerank 前后、加查询改写前后）
- [ ] 入库脱敏中间件（PII 检测）
- [ ] 一份中/日/英三语的 demo 数据集与演示脚本（面试时能当场跑）
- [ ] 英文技术文章：《Grounding and citation accuracy: how I measured my RAG》+ 日文版

> **求职节点 2：岗位池最大的那一格**
>
> **简历能写**：「从零构建企业知识库问答系统：支持 PDF/表格/扫描件解析，BM25 + 向量混合检索加 cross-encoder 重排，answer→chunk→原文页码全链路溯源，行级权限在检索阶段过滤；grounding 率 X%、引用准确率 Y%、幻觉率 Z%。」
>
> **面试能聊**：① 为什么加了 rerank 延迟涨了还值得；② 扫描件和表格你怎么处理的；③ 权限为什么必须在检索阶段过滤；④ 你怎么证明它没在胡说——这一条最能区分候选人。
>
> **对口岗位**：中国「RAG & 记忆 / 知识库工程」；日本「RAG システム開発 / 社内 QA ボット構築」。日本市场把「能做出最小 RAG demo」当作转职的起跑线，你到这里已经远超那条线。

---

# P3 · 评测与 LLMOps：把「能跑」变成「能证明」（6–8 周）

**这个阶段是什么**：你的护城河，也是你研究背景变现的地方。日本招聘方明确写出「能设计评测框架、把运维做扎实的人被优先录用」；中国的岗位口径也从 demo 转向「可评测、能降本、能维护」。而你做的正是「不用真标签、从 LLM 行为本身估计任务可推断性」——这套方法论换个包装就是 agent/LLM 系统的难度分层与风险预估。这个阶段短，但性价比最高。

能力配比：`Agent 40%` · `LLM 40%` · `工程 20%`

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

- [Kaggle AI Benchmarks / Community Benchmarks](https://www.kaggle.com/benchmarks) — **整条路线性价比最高的一项，务必做**。2026-01 上线，用 [kaggle-benchmarks SDK](https://github.com/Kaggle/kaggle-benchmarks) 写任务、组基准、跑出主流模型公开排行榜，支持多模态、代码执行、工具调用与多轮对话，官方提供免费模型额度。**怎么用：**把你研究里「从 LLM 行为估计任务可推断性」那套方法做成一个**公开基准**——比如「给定一批任务，在不看真标签的情况下预测哪些任务当前模型做不好」。这是一份别人很难复制的作品，同时让论文和工程能力互相背书。发布后它有 URL、有排行榜、有引用，简历上是硬通货。
- [BenchFlow - Agent Skill Lift](https://www.kaggle.com/competitions/skill-lift) — 第二次回访，这次站在**评测设计方**：为什么把 skill、harness、model 分三层？为什么用 resolution rate 而不是准确率？为什么要跑 3 次 trial？把这些设计决策抄进你自己的评测框架。（参考：v1.1 排行榜 25 个 model-harness 组合 × 87 任务，最高 resolution rate 67.3%——顺手记住这个量级，面试时能说出「业界现状」。）
- [AgentEval Part I](https://www.kaggle.com/competitions/agent-eval-part-i-grounded-rag-benchmark) — P2 用它学指标，P3 用它学**基准设计**：它怎么把「幻觉」这种模糊概念变成可自动判定的分数？这个转化能力就是评测工程的核心技能。
- [AI Agent Security - Multi-Step Tool Attacks](https://www.kaggle.com/competitions/ai-agent-security-multi-step-tool-attacks) — 回访，当**安全评测基准**读：它怎么保证「确定性离线」从而让分数可复现？把这一条做进你自己的 CI——每次提交自动跑一遍攻击集。安全回归测试是目前几乎没有候选人能拿出来的东西。
- 对照读 [Konwinski Prize](https://www.kaggle.com/competitions/konwinski-prize) 的赛制设计（\$1M 奖给能关掉 90% 新 GitHub issue 的 AI；断网、限时、按测试通过计分），不必参赛。

## 教材

- **主参考书**：**AI Engineering**（Chip Huyen）第 3–4 章 — 评测方法论与评估 AI 系统，把「怎么量化一个开放式输出」讲得最清楚的两章。中文：《AI工程：大模型应用开发实战》宝玉 译，人民邮电出版社 2026-02。
- **评测专书**：[Evals for AI Engineers](https://www.oreilly.com/library/view/evals-for-ai/9798341660717/) — Shreya Shankar、Hamel Husain，O'Reilly，2026-10 出版。两位作者的 [AI Evals 课程](https://maven.com/parlance-labs/evals)是目前最受欢迎的评测课。书出之前先用他们的免费资料：[AI Evals FAQ](https://hamel.dev/blog/posts/evals-faq/) 与[免费邮件课程](https://ai.hamel.dev/eval-course)——错误分析、LLM-as-judge 校准、从 trace 里找失败模式，全是本阶段要的东西。中文：暂无中文版。
- **论文**：[SkillsBench 论文](https://www.skillsbench.ai/skillsbench.pdf)（87 任务 / 8 领域 / 三层拆解：skill、harness、model）。当作「一份评测基准该怎么设计」的范本精读——这是你写自己基准的模板。
- **工具**：[kaggle-benchmarks SDK](https://github.com/Kaggle/kaggle-benchmarks) 文档 + Benchmarks Cookbook。本阶段的主要动手工具。
- **中文原创**：张奇、郑锐《大规模语言模型（第2版）：从理论到实践》（电子工业 2025-05）的模型评估部分；尹浩《AI Agent应用开发》第 2 章的 OpenCompass 实操。作为中文理论补充。

## 阶段产出

- [ ] **一个发布在 Kaggle Benchmarks 上的公开基准**（与研究主题连通，有 URL 与排行榜）
- [ ] `agent-eval` 框架仓库：任务集、judge 与校准、轨迹评估、方差报告、一条命令出报告
- [ ] 把 P1/P2 两个旗舰项目接入 CI：改动即回归 + 安全攻击集，分数回归即阻止合并
- [ ] 成本与延迟仪表盘：按功能拆分的 token 成本、p50/p95 延迟
- [ ] 英文长文《Designing an evaluation harness for a production agent》+ 日文版
- [ ] 把研究方法论改写成一篇工程向文章

> **求职节点 3：最稀缺的那格**
>
> **简历能写**：「为生产级 agent/RAG 系统建立评测与回归体系：N 个分层任务的评测集、校准过的 LLM-as-judge（与人工标注一致率 X%）、轨迹级成功率与成本分布，接入 CI 实现改动即回归；另在 Kaggle Benchmarks 发布公开基准一项。」
>
> **面试能聊**：① LLM-as-judge 的偏差你怎么发现和校准的；② 为什么只看最终答案不够，轨迹要怎么评；③ 你的评测集怎么防止过拟合；④ 一次「分数涨了但线上变差」的经历。这一格的候选人极少，问到这里你基本是房间里最懂的人。
>
> **对口岗位**：中国「LLM 应用开发（含评测）/ AI 质量」；日本「LLMOps / AI 品質保証 / 評価設計」。这是日本市场明确说的差异化点。

---

# P4 · LLM 工程：微调、量化与推理优化（10–12 周）

**这个阶段是什么**：正式跨到 LLM Engineer。从「用模型」到「改模型，并让它更便宜更快」。这一段唯一需要真金白银租卡，所以放在后面——前三个阶段你已经能就业了，这里是加薪与拓宽的阶段。核心是两条能力线：微调（能造出一个自己的模型）与推理优化（能把它跑得起）。

能力配比：`LLM 75%` · `Agent 15%` · `工程 10%`

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
- [LMSYS - Chatbot Arena Human Preference Predictions](https://www.kaggle.com/competitions/lmsys-chatbot-arena) — **主攻，3–4 周**。公开比赛里 LLM 工程能力最集中的一场：7B/9B 微调、长对话截断、量化推理、在断网内核的时间预算里跑完全量测试集。顶层方案全部公开。**怎么用：**闭卷做两周 → Late Submission 拿私榜分 → 读前 10 名 → 只补做最关键的 2–3 条改动并验证分数变化。这场做完你就有资格说自己「会微调并部署 LLM」。
- [WSDM Cup - Multilingual Chatbot Arena](https://www.kaggle.com/competitions/wsdm-cup-multilingual-chatbot-arena) — 1–2 周，对你特别对口。同样的偏好预测但**跨语言**。你面向中日两地市场，中/日/英三语能力本身就是差异化卖点，而多语言 tokenizer 与语言不均衡是真实工程问题。做完直接写进简历。
- [AI Mathematical Olympiad - Progress Prize 3](https://www.kaggle.com/competitions/ai-mathematical-olympiad-progress-prize-3)（2026-04 已结束；[PP2](https://www.kaggle.com/competitions/ai-mathematical-olympiad-progress-prize-2)）— 2–3 周，当作推理预算的极限训练。规则要求开源模型、断网、CPU ≤9h / GPU ≤5h。**怎么用：**不追分数，只回答一个工程问题——「给定固定算力，采样多少条、什么时候早退、验证器怎么用，才能最大化正确率」。这套思路直接迁移到线上服务的超时预算分配。前两届解法同样公开；留意下一届开赛公告。
- [LLM - Detect AI Generated Text](https://www.kaggle.com/competitions/llm-detect-ai-generated-text) — 可选，1–2 周。真正的课题是**训练/测试分布严重不一致**，公榜私榜大幅洗牌。用来练「分布偏移下怎么判断该不该相信自己的验证分数」——这和线上模型退化是同一个问题。

## 教材

- **主线书**：**Hands-On Large Language Models** — Jay Alammar、Maarten Grootendorst，O'Reilly 2024。300 幅全彩图解讲透 tokenization、embedding、Transformer，后半直接是**训练 embedding 模型、微调生成模型**的实战。只要 Python 基础。中文：《图解大模型：生成式AI原理与实战》李博杰 译，人民邮电出版社 2025-05（ISBN 9787115670830，[豆瓣](https://book.douban.com/subject/37339504/)），中文版还增补了 DeepSeek-R1 原理一节。
- **工程书**：**LLM Engineer's Handbook** — Paul Iusztin、Maxime Labonne，Packt 2024。一个端到端项目贯穿全书：数据管道、SFT 与偏好对齐、RAG 推理管道、部署与 LLMOps。**和你的旗舰项目 3 最像的一本**。中文：《大语言模型工程师手册：从概念到生产实践》孟凡杰、方佳瑞 译，人民邮电出版社 2025-05（ISBN 9787115667373，[豆瓣](https://book.douban.com/subject/37357674/)）。
- **推理模型**：[Build a Reasoning Model (From Scratch)](https://www.manning.com/books/build-a-reasoning-model-from-scratch) — Sebastian Raschka，Manning。从 CoT、采样与自一致性，到 RLVR、GRPO 与蒸馏，一步步把普通 LLM 训成推理模型。直接对应 AIMO 那场的「推理预算」问题。中文：暂无中文版（同作者前作《从零构建大模型》已有中文版，可作前置）。
- **主参考书**：**AI Engineering**（Chip Huyen）第 7 章微调、第 8 章数据工程、第 9 章推理优化——讲「什么时候该微调、怎么让它便宜」的取舍，正好补上面几本偏动手的空缺。中文：《AI工程：大模型应用开发实战》宝玉 译，人民邮电出版社 2026-02。
- **视频主课**：[Stanford CS336 · Language Modeling from Scratch](https://www.youtube.com/playlist?list=PLoROMvodv4rMqXOcazWaTUHhq-yembLCV)（2026 春）— 从 tokenizer、架构、GPU 与并行、scaling 到对齐，全部自己手写。目前公认最硬的 LLM 工程课，作业量大，挑 tokenizer / 架构 / 推理优化相关的讲次看即可。中文：[B 站 2026 版中英字幕（完结）](https://www.bilibili.com/video/BV1xDMG6KETb/)。
- **视频**：Karpathy「Let's build GPT」与 Zero to Hero 系列（代码即讲解）；李宏毅《生成式人工智慧導論》的训练与后训练讲次（中文原生）。
- **中文原创**：张奇、郑锐《大规模语言模型（第2版）》（电子工业 2025-05）的微调、对齐与推理加速部分，作为中文理论补充。
- **文档**：vLLM 官方文档的 performance 与 scheduling 两章；HF PEFT / TRL 文档

## 阶段产出

- [ ] **旗舰项目 3**：自己微调的模型 + vLLM 服务化（Docker），带**延迟 / 吞吐 / 成本对照表**（fp16 vs 4bit、批大小扫描、TTFT/TPOT）
- [ ] 蒸馏前后对比：把 P1 或 P2 里某个高频子任务从大模型换成自己的小模型，报出成本下降与质量变化
- [ ] 多语言（中/日/英）偏好模型一个，含各语言分项指标
- [ ] 《固定算力下的推理预算分配》技术笔记
- [ ] 算力账本：这一阶段一共租了多少小时卡、花了多少钱、换来了什么
- [ ] 英文长文《Fine-tuning and serving a 9B model on a rented GPU budget》+ 日文版

> **求职节点 4：正式以 LLM Engineer 应聘**
>
> **简历能写**：「QLoRA 微调 9B 级模型并以 vLLM 上线，4bit 量化后 p95 延迟降低 X%、单请求成本降低 Y%；将高频子任务从闭源 API 蒸馏为自有小模型，成本下降 Z% 且质量持平；多语言（中/日/英）偏好模型，各语言分项指标齐全。」
>
> **面试能聊**：① LoRA 的秩和目标模块你怎么定的；② 4bit 量化掉了多少分、值不值；③ vLLM 的吞吐瓶颈在哪、你怎么测出来的；④ 什么情况下你会选 RAG 而不是微调——这是日本面试的高频题，答案要能用成本和数据量说话。
>
> **对口岗位**：中国「LLM 应用开发 + AI Infra 边缘」；日本「LLM エンジニア（ファインチューニング・推論最適化）」。

---

# P5 · 综合、冲牌与作品集收口（6–8 周）

**这个阶段是什么**：把前四个节点合成一个系统（agent 编排 + RAG 知识 + 自有模型 + 评测闭环），同时在正式比赛里换一个客观名次。到这里你的简历已经不缺项目，缺的是「一个能讲 40 分钟的完整系统」和「一个外部背书的排名」。

能力配比：`Agent 40%` · `LLM 40%` · `工程 20%`

## 掌握的知识 / 技能

- 系统集成：把四个组件接成一条链路，端到端 SLA 与失败边界
- Kaggle 组队：在 Discussion 找思路互补的队友、Team Merge 截止规则、代码约定
- 终盘策略：public LB 与 private LB 的偏差、两枚 final submission 的对冲
- Solution writeup 的标准结构：问题 → 验证设计 → 关键 idea → 消融 → 没 work 的尝试
- 简历口径：用指标和决策讲项目；中/日/英三版的语气差异（日文要结论前置、敬体统一）
- 面试准备：系统设计题、成本估算题、作品深挖

## 可实践的 Kaggle 项目

- **一场进行中的 Featured / Research 比赛（组队）** — 从 [Featured 列表](https://www.kaggle.com/competitions?hostSegmentIdFilter=1)选 LLM / NLP / agent 方向、剩余 6 周以上、队数 800–3000 的一场，2–3 人组队，目标铜牌起。**注意：**只有 Featured / Research 发奖牌，Getting Started 和 Playground 不发。铜牌线在 1000+ 队时是前 10%。组队本身也是面试信号——证明你能和人协作交付。
- [ARC Prize — ARC-AGI-3](https://www.kaggle.com/competitions/arc-prize-2026-arc-agi-3)（交互式、面向 agent；静态版 [ARC-AGI-2](https://www.kaggle.com/competitions/arc-prize-2026-arc-agi-2)）— 要求全部方案开源、断网、不能调用外部 API。2026 届赛期到 11 月初，会在你 P1 前后结束，**本轮不作为夺牌目标**；花两小时读懂赛制与顶层思路，把真正参赛放到下一届（届时正好落在 P4/P5）。
- [自己办一场 Community Hackathon](https://www.kaggle.com/competitions?new=true&type=hackathon) — 反向操作：定题、出数据、设评审标准、写 writeup 模板。**主办一场比赛在简历上的分量往往超过参加三场**——它证明你能定义问题和评价标准，这正是 P3 那套能力的最高表现形式。
- [Konwinski Prize](https://www.kaggle.com/competitions/konwinski-prize) — 若还有余力，当毕业考：真实代码库上的 agent 修 bug，断网限时按测试通过计分。用你 P1–P4 的全套家当（编排 + 检索 + 自有小模型 + 评测）去打，就是一个完整的系统能力证明。

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
>
> **简历能写**：「端到端 LLM 系统：agent 编排与工具安全、可溯源 RAG 知识层、自有微调模型服务、评测与安全回归 CI；Kaggle 奖牌 / 公开基准一项 / 主办 agent 评测黑客松一场。」
>
> **面试能聊**：整个系统的取舍链条——哪里用确定性流程、哪里让模型决定、哪里用 RAG、哪里用微调、成本分别多少。能把这条链讲清楚，你面的就不是入门岗了。

---

# 操作手册

<details>

<summary>算力：哪些阶段花钱，哪些不花</summary>

P0–P3 基本不用租卡。这四个阶段的成本主要是 **API token**，不是 GPU。Kaggle Notebook 的免费额度（GPU 约 30h/周、单 session 12h、20GB 磁盘）足够跑 P2 的检索实验与 P3 的评测。从第一天就做 token 计费和响应缓存——一次跑飞的 agent 循环能烧掉一周预算，这是 agent 开发最常见的破财方式。

P4 需要租卡，但可控：先用 0.5B–1.5B 小模型 + 几百条样本把训练脚本完全跑通（这一步在 Kaggle 免费额度里做），确认无误后再租卡跑全量。国内按量计费平台（AutoDL、恒源云、智星云一类）的 4090 时价最低，A100/H100 按需；海外 RunPod、[Vast.ai](http://Vast.ai) 同理。每次租卡前写下「这次要回答什么问题」，跑完记进账本。[国内外 GPU 云价格对比（2026-08）](https://aieii.com/posts/2026-08-20-gpu-cloud-price-comparison-2026/)可作为选平台参考，具体价格以平台当日为准。

把「在免费额度内完成 P0–P3」本身写进简历是有效的——它正是「能降本」这条招聘要求的证据。

</details>

<details>

<summary>归档比赛怎么用才学到东西：彩排法</summary>

这一版路线里大量比赛已归档。它们是最好的教材，因为**有标准答案**；但直接读解法等于抄。流程固定五步：

① 不看任何 Discussion，自己做 8–10 天（P4 的大赛可放宽到两周）。

② 用 Late Submission 提交，拿到私榜分数（多数已结束比赛开放此功能，少数不开放）。

③ 对照当年的奖牌线，确认自己落在什么位置。

④ 读前 10 名方案，把差距分成三类：我没想到的 idea / 想到但没做的 / 我做错的。

⑤ 只挑 2–3 条最关键的补做，验证分数变化。

第 ④ 步的清单本身就是面试素材——「我做这场比赛时漏掉了 X，后来理解了为什么 X 重要」，比「我拿了第几名」更能说明你在学习。解法检索可用 [Kaggle Solutions 索引](https://kaggle.farid.one/)。

</details>

<details>

<summary>每周 20 小时怎么分</summary>

**11h 主线项目** —— 当前阶段的旗舰项目或主攻比赛，集中在两个大块时间里。碎片时间做不了系统设计。

**4h 学习** —— 教材 + 读解法。硬规则：每读完一份解法或一章书，写下一句「我因此能做什么了」。

**2h 工程回收** —— 把这周的一次性脚本收进 `agent-kit` / `agent-eval`。不做这一步，到 P4 你还在重写客户端。

**2h 写作** —— 英文主稿。写作是唯一有复利的动作：它既是面试材料，也是被动曝光。

**1h 复盘** —— 更新进度、看一眼 Kaggle 进行中列表、决定是否要插入一场新比赛。

</details>

<details>

<summary>怎么挑一场进行中的比赛（这一版的筛选口径变了）</summary>

因为主线是 Agent / LLM，筛选标准不再是「哪场好拿牌」，而是**「打完能不能写进这条主线」**。六条：

① 题材是 agent / 工具调用 / 检索 / LLM 微调之一吗？不是就跳过，哪怕容易拿牌。

② 发不发牌（只有 Featured / Research 发）。

③ 剩余时间 ≥6 周。

④ 队数 800–3000 最划算。

⑤ 算力可行：断网内核跑得完吗、需要几张卡。

⑥ 产出能不能接进你现有的三个旗舰项目。

常用入口：[进行中全部](https://www.kaggle.com/competitions?listOption=active) · [Featured](https://www.kaggle.com/competitions?hostSegmentIdFilter=1) · [NLP 标签](https://www.kaggle.com/competitions?tagIds=13204-NLP) · [AI Benchmarks](https://www.kaggle.com/benchmarks) · [全部比赛与黑客松](https://www.kaggle.com/competitions)

</details>

<details>

<summary>中日两地的简历与面试口径差异</summary>

**中国**：直接给指标和赛道关键词。招聘方按赛道筛人（Agent 工程 / RAG & 记忆 / LLM 应用开发），所以简历的项目标题就用赛道语言写，别写「智能助手」这种模糊的名字。面试重技术深度和「你怎么知道它是对的」。

**日本**：更看重「能不能稳定运维」和「能不能和业务沟通」。同一个项目在日文简历里要多写两件事——**運用体制**（监控、回归、事故处理）和**業務課題**（解决了谁的什么问题）。技术栈里务必显式写出 LangChain / LlamaIndex / 向量库 / Docker / 云平台，因为求人票就是按这些关键词筛的。

**英文**是主稿（GitHub、Kaggle writeup、技术文章），中日文版各改写一次。日文版不要逐句翻译：结论前置、敬体统一、把「我做了什么」改写成「这带来了什么」。

</details>

<details>

<summary>三个角色到底差在哪（面试自我定位用）</summary>

**AI Agent Engineer** —— 被考「你的 agent 什么时候会坏，你怎么发现的」。核心资产：工具契约设计、编排取舍、安全护栏、轨迹评测。**你的主身份。**

**LLM Engineer** —— 被考「同样的效果你能做到多便宜多快」。核心资产：微调、量化与服务化、推理优化、成本账。**P4 之后的第二身份。**

**AI Engineer（泛）** —— 被考「你怎么知道这个提升是真的」。核心资产：数据、验证、评估。**P3 让你在这一格也站得住。**

三者的公共底座是同一件事：**可测量**。你研究里那套「不用真标签、从模型行为本身估计可推断性」的思路，恰好是三条线都缺的能力——每份材料里讲一次，每次面试提一次。

</details>

---

# 这条路线会在哪里断

> **Agent 类比赛本来就少，且多为 Hackathon / Simulations 形态。** 这意味着「用 Kaggle 排名证明 agent 能力」这条路本身较窄。应对方式已经写进路线：主要产出物是**旗舰项目 + 公开基准 + writeup**，Kaggle 在这里的角色是提供真实基准与对照解法（尤其 AI Agent Security、Skill Lift、AgentEval 三场），奖牌集中放在 P5 去拿。不要因为找不到 agent 比赛就退回去打表格赛。
> **框架版本变化快于书籍。** LangChain / LangGraph / LlamaIndex 的 API 每几个月就动一次，中文书和 B 站课程一定会滞后。规则：**概念看书，API 看官方文档**。书里的项目照做但用当前版本重写，这本身就是一次有价值的练习。
> **时间被研究挤掉。** 真冲突时的取舍顺序：论文 \> 当前阶段主线项目 \> 写作 \> 读书。研究与路线能合并的点在 **P3**（评测框架 + Kaggle Benchmarks）——尽量让一份工作算两次。
> **demo 病。** Agent 方向最容易做出十个漂亮 demo、零个能上线的东西，而两地招聘方都明确说不看 demo 看交付证据。硬规则：**一个阶段只许有一个旗舰项目**，宁可窄，也要有成功率、延迟、成本三个数字。

---

> 页内比赛链接在编写时已逐条确认可达；**开放状态、截止日与奖牌线以 Kaggle 页面为准**。已知时点：ARC Prize 2026 赛期 2026-03-25 → 11-02；Gemma 4 Good Hackathon 最终提交 2026-05-18（已结束）；AIMO Progress Prize 3 于 2026-04 结束；AI Agent Security - Multi-Step Tool Attacks 于 2026 年中开赛。市场数据引自 2026 年 9 月的公开招聘分析，仅作方向参考。
>
> v2.4（Agent 优先）。本次调整：全部教材与视频改为英文优先、中文版随附——新增 *AI Engineering*（P2–P4 共用）、*Agentic Design Patterns*、*Building Applications with AI Agents*、*Hands-On RAG for Production*、*Evals for AI Engineers*、*LLM Engineer's Handbook*、*Build a Reasoning Model*；视频新增吴恩达《Agentic AI》、Karpathy、Berkeley Agentic AI MOOC、[DeepLearning.AI](http://DeepLearning.AI) RAG、Stanford CS336；中文原创书降为概念参考。每个阶段结束时回来改一次——尤其「可实践的 Kaggle 项目」一栏，它会过期。
