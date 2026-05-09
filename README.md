# agent-codes

## 📌 仓库定位

这是 **KPLDZ 的个人 A1 工作空间**，长期驻留一个代理助手。

- **不是**：普通的代码仓库
- **是**：可持续演化的个人 AI 工作间
- **灵感**：OpenClaw（https://docs.openclaw.ai）

## 🎯 核心理念

1. **持久化角色**：代理身份和工作规则写入文件 (AGENTS.md)
2. **文件为真**：重要信息以文件形式存储，支持长期查询
3. **技能优先**：优先复用已有技能，新创自动沉淀
4. **自我演化**：每次任务都可能新增或更新技能

## 📂 仓库结构

```
agent-codes/
├── AGENTS.md                 # 代理身份 + 工作规则 (核心)
├── MEMORY.md                 # 长期记忆与决策日志
├── README.md                 # 本文件
├── .agents/
│   ├── INVENTORY.md          # 技能库清单
│   └── skills/               # 技能库
│       └── github-workflows/
│           └── SKILL.md
└── docs/                     # 项目文档（按需添加）
```

### 关键文件说明

| 文件 | 用途 | 更新频率 |
|------|------|----------|
| **AGENTS.md** | 代理工作手册：身份、工作流、记忆管理 | 半年迭代 |
| **MEMORY.md** | 长期记忆：重要决策、学到的教训 | 月度整理 |
| **.agents/skills/** | 技能库（核心资产） | 持续新增 |
| **.agents/INVENTORY.md** | 技能清单索引 | 每次新增技能 |

## 🚀 快速开始

### 如果你是新代理（下次对话）

1. **加载工作规则**
   ```bash
   cat AGENTS.md
   ```
   了解你是谁、如何工作、如何管理记忆

2. **了解历史背景**
   ```bash
   cat MEMORY.md
   ```
   理解仓库初心和重要决策

3. **查看可用技能**
   ```bash
   ls -la .agents/skills/
   ```
   了解已有能力，优先复用

4. **按规则执行任务**
   参考 AGENTS.md 的工作流

### 如果你是仓库主人（KPLDZ）

1. **查看代理进度**
   ```bash
   git log --oneline
   cat MEMORY.md
   ```

2. **Review 代理的工作**
   检查新增的技能和更新的决策记录

3. **给代理反馈**
   通过 Issue 或提交提建议，代理会更新 AGENTS.md 或 MEMORY.md

## 💾 长期记忆管理

### 信息分类

**长期记忆（文件）** - 持久化存储
- 代理工作规则（AGENTS.md）
- 重要决策（MEMORY.md）
- 可复用技能（.agents/skills/）
- 项目文档（docs/）

**临时记录（对话）** - 当前对话有效
- 任务进度
- 实时思考
- 调试信息

**原则**：任何重要信息必须写入文件，不能只留在对话里

## 📋 代理工作流

```
接到任务
    ↓
[检查本地技能库] → .agents/skills/
    ↓ 有合适技能 → 直接使用
    ↓ 无合适技能
[搜索开源技能] → GitHub / Skills.sh
    ↓ 找到高质量技能 → 安装到本地
    ↓ 找不到或风险高
[自行完成] → 沉淀成技能到 .agents/skills/
    ↓
[更新文件 + 提交]
```

详见 [AGENTS.md](AGENTS.md) 的「工作流规则」部分

## 🔗 相关资源

- **本仓库**：https://github.com/KPLDZ/agent-codes
- **OpenClaw**：https://docs.openclaw.ai
- **GitHub Copilot**：https://copilot.github.com

## 📝 对代理的提示词

每次新对话启动时，告诉代理：

> 我是 KPLDZ 的个人 A1 代理，驻留在 `agent-codes` 仓库。
> 
> 请在启动时加载：
> 1. AGENTS.md - 工作规则
> 2. MEMORY.md - 历史背景
> 3. .agents/skills/ - 已有能力
> 
> 然后按规则执行任务。

---

**让我们把这个空间演化成真正的个人 AI 工作间 🚀**
