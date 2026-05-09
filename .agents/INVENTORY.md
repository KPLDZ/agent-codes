# .agents/INVENTORY.md - 技能库清单

## 📦 技能库概览

| 技能名称 | 功能 | 来源 | 状态 | 更新日期 |
|---------|------|------|------|----------|
| `github-workflows` | GitHub Actions 工作流最佳实践 | 自创 | ✅ 已验证 | 2026-05-09 |

---

## 🔍 详细清单

### 1. github-workflows
- **位置**：`.agents/skills/github-workflows/`
- **功能**：提供 GitHub Actions 工作流的最佳实践、模板和常见用例
- **来源**：自创
- **状态**：✅ 已验证
- **查看**：[SKILL.md](.agencies/skills/github-workflows/SKILL.md)

---

## 📊 统计信息

- **总技能数**：1
- **已验证**：1
- **测试中**：0
- **待实现**：0

---

## ➕ 新增技能流程

每当新增技能时：
1. 在 `.agents/skills/` 下创建技能目录
2. 编写 `SKILL.md` 文档
3. 添加脚本/模板（如需要）
4. 更新本清单（名称、功能、来源、日期）
5. 提交并更新记录

---

## 🔗 相关文件

- **工作规则**：[../AGENTS.md](../../AGENTS.md)
- **长期记忆**：[../MEMORY.md](../../MEMORY.md)
- **技能模板**：见下方

---

## 📝 技能模板

新建技能时参考以下结构：

```
.agents/skills/<skill-name>/
├── SKILL.md              # 必须：功能说明、快速使用、参数说明
├── README.md             # 可选：详细文档
├── script.sh / index.js  # 可选：可执行脚本
├── template/             # 可选：配置或代码模板
└── config.json           # 可选：默认配置
```

### SKILL.md 必填内容

```markdown
# 技能名称

## 功能
一句话说明

## 来源
- 源：GitHub owner/repo 或 Skills.sh 或 自创
- 状态：✅ 已验证 / ⚠️ 测试中

## 快速使用
[可复制的示例代码]

## 参数说明
（如有脚本参数）

## 更新日志
- v1.0 (YYYY-MM-DD): 初始安装
```

---

最后更新：2026-05-09
