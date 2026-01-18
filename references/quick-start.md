# 快速开始指南

## 在新项目中使用工作流程模板

本指南将帮助你在新项目中快速建立完整的工作流程体系。

---

## 前置条件

1. **Cursor IDE** 已安装并配置
2. **项目已初始化**（React/TypeScript 项目）
3. **全局 skill-creator** 可用（`~/.cursor/skills-cursor/create-skill/`）

---

## 步骤 1: 了解模板结构

工作流程模板包含 6 个核心 skills：

1. **project-best-coordinator** - 项目总指挥
2. **feature-design** - 功能设计
3. **project-standards** - 编码规范
4. **testing** - 测试指南
5. **code-review** - 代码审查
6. **debugging** - 问题排查

详细说明请参考 [skills-summary.md](skills-summary.md)

---

## 步骤 2: 创建 Skills（按顺序）

在项目根目录下，使用 `/skill-creator` 命令创建每个 skill：

### 2.1 创建项目总指挥

```bash
/skill-creator 创建项目总指挥 skill，用于协调所有 skills 的使用
```

**参考**: `~/.cursor/skills/workflow-best-practices/` 中的 project-best-coordinator 说明

**创建位置**: `.cursor/skills/project-best-coordinator/`

---

### 2.2 创建功能设计

```bash
/skill-creator 创建功能设计 skill，用于需求分析和功能设计
```

**参考**: `~/.cursor/skills/workflow-best-practices/` 中的 feature-design 说明

**创建位置**: `.cursor/skills/feature-design/`

---

### 2.3 创建编码规范

```bash
/skill-creator 创建编码规范 skill，用于编码标准和开发模式
```

**参考**: `~/.cursor/skills/workflow-best-practices/` 中的 project-standards 说明

**创建位置**: `.cursor/skills/project-standards/`

---

### 2.4 创建测试指南

```bash
/skill-creator 创建测试指南 skill，用于测试模式和最佳实践
```

**参考**: `~/.cursor/skills/workflow-best-practices/` 中的 testing 说明

**创建位置**: `.cursor/skills/testing/`

---

### 2.5 创建代码审查

```bash
/skill-creator 创建代码审查 skill，用于代码审查和质量保证
```

**参考**: `~/.cursor/skills/workflow-best-practices/` 中的 code-review 说明

**创建位置**: `.cursor/skills/code-review/`

---

### 2.6 创建问题排查

```bash
/skill-creator 创建问题排查 skill，用于调试和问题排查
```

**参考**: `~/.cursor/skills/workflow-best-practices/` 中的 debugging 说明

**创建位置**: `.cursor/skills/debugging/`

---

## 步骤 3: 自定义 Skills（可选）

根据项目特点，自定义每个 skill 的内容：

1. **查看全局模板**: `~/.cursor/skills/workflow-best-practices/references/`
2. **调整项目特定内容**:
   - 更新编码规范（技术栈、框架版本）
   - 添加项目特定的测试模式
   - 补充项目特定的审查清单
3. **添加项目特定参考资料**:
   - 在 `references/` 目录下添加项目文档
   - 记录项目特定的模式和最佳实践

---

## 步骤 4: 验证设置

### 4.1 测试 Skills 可用性

在 Cursor 中测试每个 skill：

```
/project-best-coordinator 我应该使用哪个 skill 来设计新功能？
/feature-design 分析这个需求：[描述需求]
/project-standards 如何在这个项目中组织组件代码？
/testing 如何为这个组件编写测试？
/code-review 审查这段代码：[代码片段]
/debugging 这个错误是什么原因：[错误信息]
```

### 4.2 检查文件结构

确保项目目录结构如下：

```
项目根目录/
├── .cursor/
│   └── skills/
│       ├── project-best-coordinator/
│       ├── feature-design/
│       ├── project-standards/
│       ├── testing/
│       ├── code-review/
│       └── debugging/
└── ...
```

---

## 步骤 5: 开始使用

### 5.1 典型工作流程

**新功能开发**:
```
1. /project-best-coordinator → 确定使用 feature-design
2. /feature-design → 分析需求，设计方案
3. /project-standards → 实现功能
4. /testing → 编写测试
5. /code-review → 审查代码
```

**Bug 修复**:
```
1. /debugging → 定位问题
2. /project-standards → 修复代码
3. /testing → 验证修复
4. /code-review → 审查修复
```

### 5.2 使用技巧

1. **从 project-best-coordinator 开始**: 不确定时，先问总指挥
2. **查看参考资料**: 每个 skill 都有详细的 references
3. **记录设计决策**: 使用 feature-design 记录重要决策
4. **持续改进**: 在使用过程中优化 skills

---

## 常见问题

### Q: 可以跳过某些 skill 吗？

A: 可以，但建议至少创建：
- project-best-coordinator（总指挥）
- project-standards（编码规范）
- code-review（代码审查）

其他 skills 可以根据项目需要选择。

### Q: 如何更新 skills？

A: 
1. 在项目中使用过程中发现问题
2. 更新项目中的 skill 文件
3. 如果改进通用，同步到全局模板
4. 记录在 CHANGELOG.md

### Q: 可以添加自定义 skills 吗？

A: 当然可以！使用 `/skill-creator` 创建项目特定的 skills。

### Q: Git 工作流 skill 在哪里？

A: 使用全局目录下的 git-workflow skill：
`~/.cursor/skills/git-workflow/`

不需要在每个项目创建。

---

## 下一步

1. ✅ 完成所有 skills 的创建
2. ✅ 自定义项目特定内容
3. ✅ 验证 skills 可用性
4. 📖 阅读 [skills-summary.md](skills-summary.md) 了解详细说明
5. 📖 查看 [workflow-diagram.md](workflow-diagram.md) 了解工作流程
6. 🚀 开始使用工作流程！

---

## 获取帮助

- **模板文档**: `~/.cursor/skills/workflow-best-practices/README.md`
- **Skills 总结**: `~/.cursor/skills/workflow-best-practices/references/skills-summary.md`
- **工作流程图**: `~/.cursor/skills/workflow-best-practices/references/workflow-diagram.md`
- **版本记录**: `~/.cursor/skills/workflow-best-practices/CHANGELOG.md`
