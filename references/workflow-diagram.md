# Workflow Diagram

## Complete Development Workflow

```
┌─────────────────────────────────────────────────────────────┐
│                    Project Coordinator                        │
│              (Central Command & Control)                     │
└─────────────────────────────────────────────────────────────┘
                            │
                            │ Routes Tasks
                            │
        ┌───────────────────┼───────────────────┐
        │                   │                   │
        ▼                   ▼                   ▼
┌───────────────┐   ┌───────────────┐   ┌───────────────┐
│ feature-design│   │project-standards│   │   testing     │
│               │   │                │   │               │
│ • Requirements│   │ • Coding       │   │ • Unit Tests  │
│ • Design      │   │ • Patterns     │   │ • Integration │
│ • Brainstorm  │   │ • Organization │   │ • Coverage    │
└───────┬───────┘   └───────┬───────┘   └───────┬───────┘
        │                   │                   │
        └───────────────────┼───────────────────┘
                            │
                            ▼
                    ┌───────────────┐
                    │  code-review  │
                    │               │
                    │ • Quality     │
                    │ • Standards   │
                    │ • Security    │
                    └───────┬───────┘
                            │
                            ▼
                    ┌───────────────┐
                    │   debugging   │
                    │               │
                    │ • Issues      │
                    │ • Performance │
                    │ • Fixes       │
                    └───────────────┘
```

## Task Flow Examples

### New Feature Development

```
User Request
    │
    ▼
feature-design (Requirements & Design)
    │
    ▼
project-standards (Implementation)
    │
    ▼
testing (Verification)
    │
    ▼
code-review (Quality Check)
    │
    ▼
(If Issues) debugging
    │
    ▼
Complete
```

### Bug Fix Workflow

```
Bug Report
    │
    ▼
debugging (Investigation)
    │
    ▼
project-standards (Fix Implementation)
    │
    ▼
testing (Verify Fix)
    │
    ▼
code-review (Quality Check)
    │
    ▼
Complete
```

### Code Review Workflow

```
Code Submission
    │
    ▼
code-review (Review)
    │
    ├─ Pass → Complete
    │
    └─ Issues Found
           │
           ▼
    project-standards (Fix)
           │
           ▼
    testing (Verify)
           │
           ▼
    code-review (Re-review)
           │
           ▼
    Complete
```
