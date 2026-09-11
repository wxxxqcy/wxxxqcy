# 👋 你好，我是 BOBO

**AI 产品经理 / Agent 产品经理**

有软件工程背景，也有教育行业一线经验。  
我关注的是：**怎么把真实业务问题，做成能落地、能评测、能持续优化的 AI 产品。**

目前主要在实践：

**AI Agent｜工具调用｜智能体评测｜提示词与上下文设计｜AI MVP**

> 我关注的不只是“让 AI 回答得更好”，  
> 更关注“让 Agent 在真实业务里把事情做对，并且能被评测、复盘和持续优化”。

---

## 🚀 重点项目

### 🎓 AI 学管 Agent / EduAgent Eval

从真实辅导老师学管工作流出发，设计并实现 AI 学管 Agent：

**学生数据读取 → 学情判断 → 专项练习 → 家长反馈 → 周报**

在完成可运行 MVP 后，进一步抽象出一套 **教育场景 Agent 端到端评测框架**，用于判断 Agent 是否真的把事情做对，而不是只看最终回答。

目前已实现：

- 有状态教育任务环境
- DeepSeek 工具调用 Agent
- 状态评测 / 流程评测 / 安全评测
- 多次运行稳定性测试
- 完整执行轨迹与实验结果留档
- Bad Case 分析与回归测试

#### 一个真实的 Agent Bad Case

在“要求伪造成绩”的安全场景中：

**Agent v1**
虽然拒绝了虚假成绩，但未经用户确认，擅自保存了“真实成绩版本”  
→ **安全评测失败**

我将问题归类为：

**未经授权的安全替代写入**

随后增加“必须等待用户再次确认”的确认边界规则。

**Agent v2**
→ 同一场景回归测试 **3/3 通过**

这形成了：

**评测 → Bad Case → Failure Mode → Agent 优化 → 回归测试**

👉 [查看项目](https://github.com/wxxxqcy/ai-learning-assistant)

---

### 🧩 AI Product Spec Skill

面向 AI Coding 场景设计的一套 **产品规格生成工作流**。

核心问题是：

当需求上下文缺失时，Coding AI 很容易出现页面遗漏、字段理解错误、权限不一致、异常流程缺失等问题。

因此我把 PRD 分析过程拆成标准化流程：

**产品目标 / 用户角色  
→ 功能与信息架构  
→ 业务流程 / 状态机  
→ 页面 / 字段 / 权限  
→ 异常场景  
→ Given / When / Then 验收标准**

目标是把“模糊需求”转化成 **AI 可以直接执行的产品规格**。

同时对无法确认的信息使用：

**推断 / 建议补充 / 待确认**

避免 AI 把不确定内容直接当成事实。

👉 [查看项目](https://github.com/wxxxqcy/detailed-software-prd-skill)

---

### 💬 AI 文件问答系统

一个从 0 到 1 完成的 AI 应用 MVP。

技术链路：

**Vue3 → FastAPI → SQLite → API → DeepSeek**

实现了：

- 用户注册与登录
- JWT 身份认证
- 普通 / 高级用户分层
- TXT 文件上传
- 用户文件隔离
- 基于附件内容进行 AI 问答
- 用户 → 文件 → 数据库 → API → 模型的完整链路

当前采用轻量级 Context 注入方案，适合 MVP 快速验证。

下一阶段计划升级：

**Chunking → Embedding → 向量检索 → RAG → 答案来源引用**

👉 [查看项目](https://github.com/wxxxqcy/llm-qa-system)

---

## 🧠 我的产品关注点

**AI 产品设计｜Agent Workflow｜工具调用｜Agent Eval｜Prompt / Context Design｜MVP｜PRD｜原型｜Bad Case 分析｜回归测试**

我更关心的问题包括：

- 哪些业务场景真正适合 AI？
- 哪些任务应该交给模型，哪些应该交给工具？
- Agent 怎么知道什么时候该执行、什么时候该停？
- 怎么定义 Agent 的“成功”？
- 怎么通过评测发现 Failure Mode？
- 怎么用 Bad Case 驱动下一版产品迭代？

---

## 🛠 技术理解

**DeepSeek API｜Python｜FastAPI｜Vue3｜SQLite｜SQL｜JWT｜Git**

我的目标不是做纯算法研究，而是具备足够的技术理解，能够：

**定义 AI 产品 → 设计 Agent Workflow → 与研发沟通 → 快速验证方案 → 通过 Eval 持续迭代**

---

## 📫 Contact

- GitHub: [wxxxqcy](https://github.com/wxxxqcy)
- 求职方向：**AI 应用产品经理 / Agent 产品经理**
