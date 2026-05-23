# 打卡草稿 (Check-in Draft) - 2026-05-23

## 今日学习内容

### WCB Event: Open Agentic Economy
参加了 Open Agentic Economy 分享会，主题：From ERC-8004 / ERC-8183 to Builder Path。学习了 Agentic Economy 中连接 Agent、支付、身份、验证的标准和 Builder 路径。

### Handbook: Agent Wallet（智能体钱包）
精读了 AI × Web3 Bridge 第四章，完整内容：

**核心思想**：Agent Wallet 不是给 AI 一个私钥，而是让用户把一小部分、可撤销、可审计的权限交给 Agent。

**9 个知识节点**：
1. AA Wallet — 账户表达规则，而非私钥控制
2. Smart Account — 合约钱包承载权限边界
3. Safe — 多签分散执行权
4. Session Key — 临时有限权限，限制时间/额度/目标/方法
5. Policy — 系统可检查的执行规则（每日额度、白名单、滑点）
6. Guard — 确定性拦截层，在交易发出前拒绝越界动作
7. Simulation — 签名前预演结果，让用户看懂影响
8. Revocation — 权限必须可随时撤销，系统自动收紧
9. Human Check — 分层确认：低风险自动、中风险模拟后确认、高风险明确展示

## 四层架构完整关系

```
Chain-aware Context → Tool Use → Workflow → Wallet
   输入层             能力层        流程层     权限层
```

四层缺一不可，构成 Agent 从"解释链上信息"到"安全参与链上执行"的完整链路。

## 关键收获

1. Agent Wallet 的核心矛盾是执行能力 vs 安全边界，解决方案是"有限授权、自动执行、随时撤销、可追踪"
2. 产品标准：用户能不能清楚地知道 Agent 拿了什么权限、做过什么、还能做什么、怎么关掉
3. 分工原则：Agent 生成候选 → Guard 拒绝越界 → Simulation 预演 → Human 确认关键决策

## 下一步

- 阅读 Machine Payment（机器支付）
- 补看 Open Agentic Economy 回放
- 设计"Agent 受限支付钱包"最小实践
