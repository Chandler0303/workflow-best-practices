# Changelog

## Version History

### v1.0.0 (2026-01-17)

#### 初始版本
- ✅ 创建独立全局 skill `~/.cursor/skills/workflow-template/`
- ✅ 包含 6 个核心 skills 的完整工作流程模板
- ✅ 创建 SKILL.md、README.md 和参考资料目录
- ✅ 建立版本记录机制

#### 核心 Skills
1. **project-coordinator** - 项目总指挥，协调所有 skills 的使用
2. **feature-design** - 功能设计，需求分析和功能设计
3. **project-standards** - 编码规范，编码标准和开发模式
4. **testing** - 测试指南，测试模式和最佳实践
5. **code-review** - 代码审查，代码审查和质量保证
6. **debugging** - 问题排查，调试和问题排查

#### 文档结构
- SKILL.md - 核心 skill 文件（AI 使用）
- README.md - 模板概述和结构说明
- CHANGELOG.md - 版本历史记录
- references/ - 详细文档
  - skills-summary.md - Skills 体系总结
  - quick-start.md - 快速开始指南
  - workflow-diagram.md - 工作流程图

#### 迁移历史
- 2026-01-17: 从项目目录 `docs/workflow-template/` 迁移到全局 skill
- 2026-01-17: 从 skill-creator 模板目录迁移到独立全局 skill
- 2026-01-17: 清理多余模板，统一使用全局 skill

---

## 更新指南

### 如何更新模板

1. **在使用过程中发现问题或改进点**
   - 记录在项目中的 skill 文件
   - 测试改进效果

2. **同步改进到全局模板**
   - 更新 `~/.cursor/skills/workflow-template/` 下的对应文件
   - 更新 CHANGELOG.md 记录改进内容

3. **版本号规则**
   - 主版本号：重大结构调整
   - 次版本号：新增 skill 或重要功能
   - 修订版本号：文档更新或小改进

### 未来计划

- [ ] 添加更多项目类型的示例
- [ ] 完善工作流程图
- [ ] 添加最佳实践案例
- [ ] 支持更多技术栈的模板
