# 👋 你好，我是龙姝

热衷于将 AI 能力落地为可用的工程产品，从对话系统到多模态推理，从后端架构到前端交互，享受全链路的技术打磨。

---

## 🛠 技术栈

| 类别 | 技术 |
| :--- | :--- |
| **AI 框架** | LangChain / LangGraph, PyTorch, Transformers, Whisper, Pyannote, Kokoro |
| **模型部署** | Qwen3-VL, Qwen (DashScope), 本地推理, CUDA, FFmpeg |
| **后端** | Python, FastAPI, 异步编程, Pydantic, SSE, WebSocket |
| **数据库与存储** | PostgreSQL, Redis, Milvus, ChromaDB, SQLAlchemy |
| **检索与 RAG** | 混合检索, Rerank, GraphRAG, 查询优化, 父文档上下文 |
| **前端** | Vue 3 (Composition API), Vite, JavaScript (ES6+), HTML5/CSS3, Axios, Pinia |
| **工程化** | Docker, LangSmith, Loguru, Git, 生命周期管理, 中间件 |
| **协议与工具** | MCP (FastMCP), RESTful API, JWT, LocalStorage |

---

## 📌 主要项目

### 🧭 RoadMuse — 多 Agent 协作智能旅行系统
基于 LangGraph 的多 Agent 架构，融合 Handoffs + Router + Subagents 三种模式，提供端到端的旅行规划服务。

- **架构设计**：通过 Middleware 动态注入步骤级提示词与工具集，实现业务逻辑与框架解耦；支持状态回退与中断恢复。
- **RAG 引擎**：构建查询优化→混合检索→LLM 重排序→父文档映射的四阶段管道，结合 Redis 缓存加速。
- **MCP 标准化**：基于 FastMCP 搭建自建 MCP Server，客户端统一管理 stdio 与 StreamableHTTP 两种传输方式。
- **记忆持久化**：基于 PostgreSQL 的 Checkpointer + Store，实现长短期记忆双轨存储，每次调用前自动加载用户画像。
- **实时交互**：FastAPI + SSE 实现 Token 流式推送，集成 Loguru 日志与 LangSmith 全链路监控。

### 🧠 MindStream — 本地多模态 AI 推理平台
整合 Qwen3-VL、Whisper、Pyannote、Kokoro 四个异构模型，提供“听、说、看、思、译”一站式私有化部署能力。

- **模型生命周期管理**：通过应用钩子 + 线程安全单例统一预热，定位并解决并行加载时的张量污染问题，采用串行预热根治异常。
- **单模型多场景复用**：以 Qwen3-VL-2B 为核心，通过差异化 system prompt + 消息构造层驱动对话、OCR、翻译、会议纪要四类任务，降低显存压力。
- **流式输出与中断**：后台生成线程 + 队列拼接实现异步流式推送，每个会话注册独立中断信号，支持用户随时停止生成。
- **会议处理管线**：构建“音频→说话人分割→同人段合并/超长段拆分→逐段转写→结构化纪要”全流程；对 Whisper 输出启用温度回退、压缩比和静音阈值三重过滤，并通过 Prompt 约束 + JSON 后处理保证输出稳定性。
- **视觉适配优化**：针对小图与极短长宽比图进行自动放大和白边补齐，控制视觉 token 数量上下界，平衡精度与延迟。

---

## 🎬 更多项目

- **Video Platform（视频点播/直播平台）**：Vue 3 + FastAPI 全栈开发，支持 JWT 鉴权、HLS 流播放、实时评论、智能搜索、收藏及直播间管理。前端 Pinia 状态管理，后端异步 SQLAlchemy + 模块化路由。
- **食光厨房（智能烹饪助手）**：基于 LangGraph 的状态机设计，涵盖需求收集、菜谱推荐、营养分析、周菜单生成，集成 RAG 检索与食材过敏校验，支持多轮对话中断与恢复。

---

## 📈 GitHub 统计

<a href="https://github.com/111Decepticon">
  <img align="center" src="https://github-readme-stats.vercel.app/api?username=111Decepticon&show_icons=true&theme=transparent&hide_title=true" />
</a>
<a href="https://github.com/111Decepticon">
  <img align="center" src="https://github-readme-stats.vercel.app/api/top-langs/?username=111Decepticon&layout=compact&theme=transparent&hide_title=true" />
</a>

---

⚡ 持续探索 AI 应用落地与全栈工程的最佳实践。