# Master Routing Protocol

**Purpose:** Map every developer request to the correct skill file. Read this file first on every prompt.

---

## Routing Table

| If the user asks for... | Route to skill | File |
|---|---|---|
| Debugging, fixing a bug, diagnosing a crash/error/regression | `diagnose` | `skills/diagnose/SKILL.md` |
| Building a quick prototype, mocking a UI, sanity-checking logic | `prototype` | `skills/prototype/SKILL.md` |
| Architecture review, refactoring, decoupling, consolidation | `improve-codebase-architecture` | `skills/improve-codebase-architecture/SKILL.md` |
| Building a new website from scratch | `website-generator-operator` | `skills/website-generator-operator.md` |
| Designing or auditing a website — UI/UX, color, typography, layout, animation, 3D, conversion, or modern trends | `website-mastery` | `skills/website-mastery/SKILL.md` |
| Managing/maintaining The Antigle (Not Gaming Playz) | `manage-not-gaming-playz` | `skills/manage-not-gaming-playz.md` |
| Writing a new skill file | `write-a-skill` | `skills/write-a-skill/SKILL.md` |
| Test-driven development, red-green-refactor | `tdd` | `skills/tdd/SKILL.md` |
| Converting plan to GitHub issues, slicing work | `to-issues` | `skills/to-issues/SKILL.md` |
| Writing a PRD from conversation context | `to-prd` | `skills/to-prd/SKILL.md` |
| Triaging issues, managing issue workflow | `triage` | `skills/triage/SKILL.md` |
| Stress-testing a plan/design (grill session) | `grill-me` | `skills/grill-me/SKILL.md` |
| Grill session using domain docs | `grill-with-docs` | `skills/grill-with-docs/SKILL.md` |
| Handing off to another agent, writing handoff doc | `handoff` | `skills/handoff/SKILL.md` |
| Understanding high-level codebase context | `zoom-out` | `skills/zoom-out/SKILL.md` |
| Ultra-brief responses, token-saving mode | `caveman` | `skills/caveman/SKILL.md` |
| Setting up agent skills for a repo | `setup-matt-pocock-skills` | `skills/setup-matt-pocock-skills/SKILL.md` |
| General chat, simple questions, casual conversation | *(no skill)* | Respond directly |
| Code review, simple feature request, config changes | *(no skill)* | Respond directly |
| Editing code with exact SEARCH/REPLACE, no-placeholder commits | `advanced-unified-editor` | `skills/advanced-unified-editor.md` |
| Planning then executing multi-step code changes | `planner-executor-orchestrator` | `skills/planner-executor-orchestrator.md` |
| QA verification, error root-cause analysis, linting | `adversarial-verifier` | `skills/adversarial-verifier.md` |
| Token-efficient file parsing, CLI-first context access | `context-optimizer` | `skills/context-optimizer.md` |

---

## Project Operations & Management

**Rule:** Every new website/project built automatically generates a corresponding `[project_name]_operations.md` skill file that acts as its operations manual.

| Trigger | Action |
|---|---|
| New website/project created | Auto-generate `[project_name]_operations.md` skill |
| User asks to update/maintain a project | Route to that project's `_operations.md` skill file |
| User asks "how do I update X" | Read the project's ops manual, answer from it |

---

## Upgraded Agentic Workflows

The following skills form the advanced execution layer. They work together in sequence for any non-trivial request:

| Workflow | Skill Chain | Description |
|---|---|---|
| Simple edit (known code, small change) | `context-optimizer` → `advanced-unified-editor` | Read only what's needed, then SEARCH/REPLACE |
| Multi-step feature / refactor | `context-optimizer` → `planner-executor-orchestrator` → `advanced-unified-editor` → `adversarial-verifier` | Explore → Plan → Execute → Verify |
| Bug fix | `context-optimizer` → `planner-executor-orchestrator` → `advanced-unified-editor` → `adversarial-verifier` | Find root cause → Plan fix → Apply → Verify |
| New project from scratch | `website-mastery` → `website-generator-operator` → `context-optimizer` → `planner-executor-orchestrator` → `adversarial-verifier` | Research design → Scaffold → Plan detail → Build → Test |
| Premium website design/redesign | `website-mastery` → `context-optimizer` → `planner-executor-orchestrator` → `advanced-unified-editor` → `adversarial-verifier` | Design → Explore → Plan → Execute → Verify |

**Critical Directive — No Guessing, No Laziness:**
- You MUST consult `direction.md` BEFORE every action. This is not optional.
- You MUST NEVER guess file contents. Always read the actual file first.
- You MUST NEVER output placeholder code, `// ... rest remains same`, or `// include original method body`. Every code block must be complete and functional.
- You MUST run verification (lint, test, or manual check) after every code change.
- If you are uncertain about the existing state of any file, use grep or read before acting.

---

## Prime Directive Execution Rule

On every prompt:

1. **Read this file** (`direction.md`) to identify the matching skill
2. If a skill is matched — **read that skill's files** before responding
3. Execute the prompt strictly following the skill's guidelines
4. If no skill matches — respond directly without loading any skill

---

## Fallback Behavior

- Ambiguous request → ask one clarifying question, then route
- Multi-skill request → sequence skills in dependency order
- Unknown topic → respond with general capabilities
