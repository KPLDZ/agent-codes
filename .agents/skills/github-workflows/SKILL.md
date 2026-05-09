# GitHub Actions 工作流最佳实践

## 功能

提供 GitHub Actions 工作流的最佳实践、常见模板和用例，帮助快速搭建 CI/CD 流程。

## 来源

- **来源**：自创
- **类型**：通用技能
- **状态**：✅ 已验证

## 快速使用

### 基础工作流模板

```yaml
name: Basic CI

on:
  push:
    branches: [main, develop]
  pull_request:
    branches: [main]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Run tests
        run: |
          echo "Running tests..."
          # 在这里添加你的测试命令
```

### 保存位置

1. 在项目根目录创建：`.github/workflows/` 目录
2. 创建 `.github/workflows/ci.yml` 文件
3. 复制上述内容并根据项目调整
4. 提交到仓库，工作流会自动触发

## 参数说明

| 参数 | 说明 | 示例 |
|------|------|------|
| `on` | 触发条件 | `push`, `pull_request`, `schedule` |
| `runs-on` | 运行环境 | `ubuntu-latest`, `windows-latest`, `macos-latest` |
| `steps` | 执行步骤 | 顺序执行的任务 |
| `uses` | 使用的 Action | `actions/checkout@v3` |
| `run` | 执行命令 | bash 命令 |

## 常见用例

### 1. 自动化测试
```yaml
name: Test
on: [push, pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - run: npm test
```

### 2. 自动发布版本
```yaml
name: Release
on:
  push:
    tags:
      - v*
jobs:
  release:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Create Release
        uses: actions/create-release@v1
```

### 3. 代码质量检查
```yaml
name: Lint
on: [push, pull_request]
jobs:
  lint:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Run linter
        run: npm run lint
```

## 更新日志

- v1.0 (2026-05-09): 初始创建，包含基础模板和常见用例

---

## 推荐阅读

- [GitHub Actions 官方文档](https://docs.github.com/en/actions)
- [Awesome GitHub Actions](https://github.com/sdras/awesome-actions)
