# Skills 体系总结

## 概述

本工作流程模板包含 6 个核心 skills，覆盖完整的开发生命周期，从需求分析到问题排查。

## 核心 Skills 详细说明

### 1. project-coordinator (项目总指挥)

**职责**: 项目协调和工作流程编排

**使用场景**:
- 开始新任务时，确定应该使用哪个 skill
- 协调多个 skills 的使用
- 理解项目工作流程
- 需要指导使用哪个技能时

**核心功能**:
- 任务路由：根据任务类型路由到合适的 skill
- 工作流程协调：确保 skills 按正确顺序使用
- 技能选择指导：帮助选择最合适的 skill

**参考文档**: `.cursor/skills/project-coordinator/`

---

### 2. feature-design (功能设计)

**职责**: 需求分析和功能设计

**使用场景**:
- 分析新需求
- 设计新功能
- 头脑风暴解决方案
- 规划实现方案
- 将复杂功能拆解为任务

**核心功能**:
- 需求分析：理解业务需求，识别关键点
- 功能拆解：将复杂功能分解为可实现的模块
- 技术设计：设计技术方案和架构
- 头脑风暴：探索多种解决方案
- 设计决策记录：记录重要设计决策

**参考文档**: `.cursor/skills/feature-design/`

---

### 3. project-standards (编码规范)

**职责**: 编码标准和开发模式

**使用场景**:
- 编写 React 组件
- 组织代码结构
- 管理项目工作流程
- 实现业务逻辑
- 遵循项目规范

**核心功能**:
- 编码标准：代码风格、命名规范、文件组织
- 组件模式：React 组件开发模式
- 文件组织：目录结构、模块划分
- 开发模式：状态管理、数据流、工具使用
- 业务逻辑：ProcessHandler 使用、API 调用

**参考文档**: `.cursor/skills/project-standards/`

---

### 4. testing (测试指南)

**职责**: 测试模式和最佳实践

**使用场景**:
- 编写测试用例
- 测试 React 组件
- 测试 API 端点
- 测试 ProcessHandler 工具
- 设置测试环境

**核心功能**:
- Vitest 设置：测试框架配置
- 组件测试：React 组件测试模式
- API 测试：接口测试方法
- ProcessHandler 测试：工具类测试
- 测试覆盖率：确保代码质量

**参考文档**: `.cursor/skills/testing/`

---

### 5. code-review (代码审查)

**职责**: 代码审查和质量保证

**使用场景**:
- 审查 Pull Request
- 检查代码质量
- 确保代码符合项目规范
- 审查代码安全性
- 审查代码可维护性

**核心功能**:
- 代码质量检查：代码风格、最佳实践
- 安全性审查：安全漏洞、风险识别
- 性能审查：性能问题、优化建议
- 项目规范检查：符合项目编码标准
- ProcessHandler 审查：工具类使用规范

**参考文档**: `.cursor/skills/code-review/`

---

### 6. debugging (问题排查)

**职责**: 调试和问题排查

**使用场景**:
- 调查 Bug
- 定位性能问题
- 调试 React 组件
- 调试网络请求
- 调试状态管理
- 调试 ProcessHandler 逻辑

**核心功能**:
- React 组件调试：组件渲染问题、状态问题
- 网络请求调试：API 调用问题、数据流问题
- 状态管理调试：Redux/Rematch 状态问题
- ProcessHandler 调试：工具类逻辑错误
- 性能问题定位：性能瓶颈分析

**参考文档**: `.cursor/skills/debugging/`

---

## Skills 使用流程

### 典型开发流程

```
1. project-coordinator
   └─> 确定任务类型，路由到合适的 skill

2. feature-design
   └─> 分析需求，设计功能方案

3. project-standards
   └─> 实现功能，遵循编码规范

4. testing
   └─> 编写测试，验证功能

5. code-review
   └─> 审查代码，确保质量

6. debugging (如需要)
   └─> 排查问题，修复 Bug
```

### 任务类型与 Skill 映射

| 任务类型 | 主要 Skill | 辅助 Skills |
|---------|-----------|------------|
| 新功能开发 | feature-design → project-standards | testing, code-review |
| Bug 修复 | debugging → project-standards | testing, code-review |
| 代码审查 | code-review | project-standards |
| 性能优化 | debugging → project-standards | testing |
| 需求分析 | feature-design | project-coordinator |
| 测试编写 | testing | project-standards |

---

## Skills 依赖关系

```
project-coordinator (总指挥)
    │
    ├─> feature-design (需求设计)
    │       └─> project-standards (实现)
    │               ├─> testing (测试)
    │               └─> code-review (审查)
    │                       └─> debugging (如需要)
    │
    └─> debugging (问题排查)
            └─> project-standards (修复)
                    └─> testing (验证)
```

---

## 最佳实践

### 1. 始终从 project-coordinator 开始
- 不确定使用哪个 skill 时，先使用 project-coordinator
- 它会帮你路由到正确的 skill

### 2. 按流程顺序使用
- 新功能：feature-design → project-standards → testing → code-review
- Bug 修复：debugging → project-standards → testing → code-review

### 3. 充分利用参考资料
- 每个 skill 都有详细的 references 目录
- 遇到具体问题时，查看对应的参考文档

### 4. 持续迭代改进
- 在使用过程中发现问题，更新对应的 skill
- 同步改进到全局模板，记录在 CHANGELOG.md

---

## 扩展建议

### 可选补充 Skills

1. **performance** (性能优化)
   - 代码优化技巧
   - 构建优化
   - 运行时优化
   - 性能监控

2. **deployment** (部署流程)
   - CI/CD 流程说明
   - 部署检查清单
   - 回滚策略
   - 环境配置

3. **git-workflow** (Git 工作流)
   - 分支管理
   - 提交规范
   - PR 流程
   - 代码合并策略

**注意**: git-workflow 可以使用全局目录下的 skill，不需要在每个项目创建。
