# 打卡草稿 (Check-in Draft) - 2026-05-22

## 今日学习内容

精读了 AI × Web3 Bridge 前三章：

### 1. Chain-aware Context（链感知上下文）
- 核心：让 AI 在回答前能看见正确的链、地址、合约、交易、事件、余额、授权和数据来源
- 关键原则：模型不能凭语言记忆判断链上事实，必须从工具和索引层读取
- 7 个知识节点：On-chain Data、Contract Docs、ABI/Event、Transaction History、Explorer Context、Indexing Context、Citation
- 每条关键结论必须附带 citation（链上证据：tx hash、block number、contract address、explorer link）

### 2. Web3 Tool Use（Web3 工具调用）
- 核心：将 RPC、合约读写、钱包、区块浏览器、DeFi 封装为 Agent 可调用的工具
- 关键原则：工具必须用确定性边界限制模型，读写分离，权限分层
- 8 个核心工具：RPC、Contract Read、Contract Write、Wallet、Explorer、DeFi、Tool Permission、Tool Log
- 权限分层：查询自动 → 小额 session key → 大额人工确认 → 任意合约禁止

### 3. Agent Workflow（智能体工作流）
- 核心：把用户目标拆成可控步骤（上下文→计划→工具→风险检查→执行→记录）
- 关键原则：高风险 Agent 必须有状态、边界和停止条件
- 7 个知识节点：Task Graph、State Machine、Human-in-the-Loop、Retry/Fallback、Trace、Evaluation Harness、Regression Set

## 关键收获

1. AI × Web3 产品 = 链感知上下文包 + 受限工具集 + 显式工作流 + 可审计日志
2. 三层架构：Context（事实层）→ Tool Use（能力层）→ Workflow（流程层）
3. 安全底线：Citation（引用）、读写分离、Human-in-the-Loop（人在回路）、日志可审计

## 下一步

- 继续阅读 Agent Wallet（智能体钱包）
- 完成 WCB 平台任务
- 开始最小实践：为一笔交易构建上下文包
