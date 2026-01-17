---
name: workflow-template
description: Automatically generates a complete workflow skills system for new projects. Use when setting up a new project, initializing skills, or creating a standardized development workflow. Analyzes project structure and automatically creates 6 core skills customized for the project.
---

# Workflow Template - Auto Generator

This skill automatically generates a complete workflow skills system for your project. It analyzes your project structure, technology stack, and patterns, then creates 6 customized skills that match your project's needs.

## What This Skill Does

When you use `/workflow-template` in a new project, this skill will:

1. **Analyze your project structure**
   - Read `package.json` to identify technology stack
   - Examine project files to understand patterns
   - Identify key frameworks and tools

2. **Automatically generate 6 core skills**
   - `project-coordinator` - Project coordinator and workflow orchestrator
   - `feature-design` - Requirements analysis and feature design
   - `project-standards` - Coding standards and development patterns
   - `testing` - Testing patterns and best practices
   - `code-review` - Code review and quality assurance
   - `debugging` - Debugging and troubleshooting

3. **Customize skills for your project**
   - Adapt to your technology stack (React, Vue, etc.)
   - Include project-specific patterns and conventions
   - Reference your actual project structure

## Usage

Simply use the command in your project:

```
/workflow-template
```

Or be more specific:

```
/workflow-template 为这个项目生成完整的工作流程 skills
```

## Automatic Generation Process

When invoked, this skill will:

### Step 1: Project Analysis

1. Read `package.json` to identify:
   - Framework (React, Vue, Angular, etc.)
   - UI Library (Ant Design, Element Plus, Material-UI, etc.)
   - State Management (Redux, Vuex, Zustand, etc.)
   - Testing Framework (Vitest, Jest, etc.)
   - Build Tool (Vite, Webpack, etc.)
   - Styling (Tailwind CSS, Less, Sass, etc.)

2. Examine project structure:
   - Check `src/` directory structure
   - Identify component patterns
   - Find utility files and patterns
   - Look for existing test files

3. Identify project-specific patterns:
   - Component organization
   - File naming conventions
   - Import patterns
   - State management patterns

### Step 2: Generate Skills

For each of the 6 skills, automatically:

1. **Create the skill directory**: `.cursor/skills/skill-name/`
2. **Generate SKILL.md** with:
   - Project-specific technology stack
   - Actual project patterns and conventions
   - References to real project files
   - Customized examples from your project

3. **Generate README.md** (Chinese introduction)
4. **Create references/** directory with:
   - Project-specific documentation
   - Real examples from your codebase
   - Customized patterns

### Step 3: Customization

Each skill is customized based on:

- **Technology Stack**: React vs Vue, Ant Design vs Element Plus, etc.
- **Project Structure**: Actual file organization patterns
- **Existing Code**: References to real components and utilities
- **Conventions**: Naming conventions, import patterns, etc.

## Generated Skills Details

### 1. project-coordinator

**Location**: `.cursor/skills/project-coordinator/`

**Customization**:
- Routes tasks to other 5 skills
- References actual project structure
- Includes project-specific workflow

### 2. feature-design

**Location**: `.cursor/skills/feature-design/`

**Customization**:
- Component design patterns from your project
- Integration with your actual utilities (e.g., ProcessHandler)
- Project-specific design examples

### 3. project-standards

**Location**: `.cursor/skills/project-standards/`

**Customization**:
- Your actual technology stack (from package.json)
- Real file organization patterns
- Component patterns from your codebase
- Business logic patterns (e.g., ProcessHandler usage)

### 4. testing

**Location**: `.cursor/skills/testing/`

**Customization**:
- Your testing framework (Vitest, Jest, etc.)
- Component testing patterns for your UI library
- API testing patterns
- Project-specific utility testing

### 5. code-review

**Location**: `.cursor/skills/code-review/`

**Customization**:
- Project-specific coding standards
- Technology stack review checklist
- Project patterns review guidelines

### 6. debugging

**Location**: `.cursor/skills/debugging/`

**Customization**:
- Framework-specific debugging (React, Vue, etc.)
- State management debugging (Redux, Vuex, etc.)
- Project-specific utility debugging

## Implementation Instructions

**CRITICAL**: When a user invokes `/workflow-template`, you MUST automatically generate all 6 skills. Do NOT just provide instructions - actually create them.

### Step 1: Analyze Project (REQUIRED)

Before generating, you MUST:

1. **Read package.json** to extract:
   - Framework: React/Vue/Angular version
   - UI Library: Ant Design/Element Plus/Material-UI version
   - State Management: Redux/Rematch/Vuex/Zustand
   - Testing: Vitest/Jest version
   - Build Tool: Vite/Webpack version
   - Styling: Tailwind CSS/Less/Sass
   - Other key dependencies

2. **Examine project structure**:
   - List `src/` directory structure
   - Identify component organization patterns
   - Find utility files (e.g., processHandler.ts, tools.ts)
   - Check existing test files
   - Identify file naming conventions

3. **Extract project patterns**:
   - Component patterns from actual files
   - Import patterns
   - State management usage
   - API calling patterns

### Step 2: Generate All 6 Skills (AUTOMATIC)

You MUST automatically generate all 6 skills in this order. For EACH skill:

1. **Create the directory**: `.cursor/skills/skill-name/`
2. **Generate SKILL.md** with:
   - Project-specific technology stack (from package.json)
   - Actual project patterns (from codebase analysis)
   - Real file references (from project structure)
   - Customized examples (from actual code)

3. **Generate README.md** (Chinese introduction)
4. **Create references/** directory with project-specific docs

**Generation Order**:
```
1. project-coordinator (first - coordinates others)
2. project-standards (foundation - others reference this)
3. feature-design
4. testing
5. code-review
6. debugging
```

### Step 3: Customization Requirements

For EACH skill, you MUST customize:

- **Technology Stack**: Use actual versions from package.json
- **Project Structure**: Reference real directory structure
- **Component Patterns**: Use patterns from actual components
- **Utilities**: Reference real utility files (e.g., ProcessHandler)
- **Examples**: Use or adapt examples from actual codebase

### Step 4: Execution

When user says `/workflow-template` or `/workflow-template 为这个项目生成完整的工作流程 skills`:

1. ✅ Read package.json (REQUIRED)
2. ✅ Analyze project structure (REQUIRED)
3. ✅ Generate project-coordinator skill (AUTOMATIC)
4. ✅ Generate project-standards skill (AUTOMATIC)
5. ✅ Generate feature-design skill (AUTOMATIC)
6. ✅ Generate testing skill (AUTOMATIC)
7. ✅ Generate code-review skill (AUTOMATIC)
8. ✅ Generate debugging skill (AUTOMATIC)
9. ✅ Verify all skills created
10. ✅ Report completion

**DO NOT**:
- ❌ Just provide instructions
- ❌ Ask user to manually create skills
- ❌ Skip any of the 6 skills
- ❌ Use generic templates without customization

## Example Generation Process

When generating, follow this process for EACH skill:

### Template for Each Skill Generation

For each skill, you should:

1. **Read the template** from `~/.cursor/skills/workflow-template/references/skills-summary.md`
2. **Customize based on project analysis**:
   - Replace generic technology stack with actual versions
   - Replace example patterns with real project patterns
   - Reference actual project files
   - Adapt examples from real codebase

3. **Use skill-creator with project context**:
   ```
   /skill-creator [skill description]。项目技术栈：[实际技术栈]，项目结构：[实际结构]，组件模式：[实际模式]
   ```

### Example: Project Standards Generation

**Before generation, analyze**:
- Read package.json → React 18.2.0, TypeScript 5.1.6, Vite 7.1.3, Ant Design 5.27.1, etc.
- Examine src/ structure → pages/, components/, util/, etc.
- Read actual component → EngineeringManagement/index.tsx pattern
- Check utilities → processHandler.ts, tools.ts patterns

**Then generate with**:
```
/skill-creator 创建编码规范 skill，用于编码标准和开发模式。
技术栈：React 18.2.0 + TypeScript 5.1.6 + Vite 7.1.3 + Ant Design 5.27.1 + Redux 4.2.1 + Rematch 2.2.0 + Tailwind CSS 4.1.12。
项目文件组织：pages/PageName/index.tsx + index.type.ts + index.less，components/ComponentName/index.tsx。
组件模式：参考 src/pages/Project/EngineeringManagement/index.tsx 的模式。
工具类：参考 src/util/processHandler.ts 和 src/util/tools.ts。
```

**Key Point**: Always include actual project information, not placeholders.

## Key Points

1. **Automatic**: No manual configuration needed
2. **Customized**: Skills match your actual project
3. **Complete**: All 6 skills generated in one go
4. **Project-specific**: References your real code and patterns

## After Generation

Once all skills are generated:

1. Verify all 6 skills exist in `.cursor/skills/`
2. Test each skill with a simple query
3. Customize further if needed (skills are editable)

## References

- **Template Location**: `~/.cursor/skills/workflow-template/`
- **Skills Summary**: See [references/skills-summary.md](references/skills-summary.md)
- **Quick Start Guide**: See [references/quick-start.md](references/quick-start.md)
- **Workflow Diagram**: See [references/workflow-diagram.md](references/workflow-diagram.md)
- **Changelog**: See [CHANGELOG.md](CHANGELOG.md)
