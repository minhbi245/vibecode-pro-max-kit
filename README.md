<p align="center">
  <h1 align="center">vibecode-pro-max-kit</h1>
  <p align="center">
    <strong>The complete agent development harness for Claude Code + Codex</strong>
  </p>
  <p align="center">
    Not just configs — a complete development methodology with phase-locked safety, skill discovery, and subagent orchestration.
  </p>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-1.0.0-blue" alt="Version">
  <img src="https://img.shields.io/badge/license-MIT-green" alt="License">
  <img src="https://img.shields.io/badge/agents-12-orange" alt="Agents">
  <img src="https://img.shields.io/badge/skills-32-purple" alt="Skills">
  <img src="https://img.shields.io/badge/hooks-7-red" alt="Hooks">
  <img src="https://img.shields.io/badge/platforms-Claude_Code_%7C_Codex-black" alt="Platforms">
</p>

---

**12 agents** | **32 skills** | **7 hooks** | **6 dev protocols** | **17 seed templates**

---

## How It Works

```
Your Request
  │
  ▼
┌──────────────────────────────────────┐
│  Step 0: Skill Discovery             │
│  Match keywords → surface skills     │
└──────────────┬───────────────────────┘
               ▼
┌──────────────────────────────────────┐
│  Intent Detection                    │
│  feature / bug / question / UI       │
└──────────────┬───────────────────────┘
               ▼
┌──────────────────────────────────────┐
│  Route to Specialist Agent           │
│  research → innovate → plan → exec   │
└──────────────────────────────────────┘
```

Every request is routed through RIPER-5: a strict phase-locked workflow that prevents premature implementation and ensures quality through enforced mode boundaries.

---

## Quickstart

### 1. Install the harness

```bash
# Clone the kit into a temp directory
git clone --depth 1 https://github.com/withkynam/vibecode-pro-max-kit.git /tmp/vc-kit

# In your project, invoke vc-setup (or copy manually)
# The vc-setup skill scaffolds everything into your repo
```

### 2. Generate your project context

Open Claude Code or Codex in your project and say:

```
Run the generate-context skill
```

This creates `process/context/all-context.md` — the root knowledge file that all agents reference.

### 3. Start building

```
Add a user authentication system
```

The orchestrator detects intent, discovers relevant skills (`ck-security`, `web-testing`), and routes through RESEARCH -> INNOVATE -> PLAN -> EXECUTE automatically.

---

## What's Included

### Core Agents (6)

| Agent | Purpose | Phase |
|---|---|---|
| `research-agent` | Read-only information gathering | RESEARCH |
| `innovate-agent` | Brainstorm approaches, no decisions | INNOVATE |
| `plan-agent` | Write detailed specifications | PLAN |
| `execute-agent` | Implement per approved plan | EXECUTE |
| `fast-mode-agent` | Compressed R->I->P->E with safety pause | FAST |
| `update-process-agent` | Capture learnings, archive plans | UPDATE |

### Specialist Agents (6)

| Agent | Purpose | When to Use |
|---|---|---|
| `tester` | Diff-aware test verification | After implementation steps |
| `debugger` | Root cause analysis | Bug investigation |
| `code-reviewer` | Production-readiness review | Pre-PR quality gate |
| `code-simplifier` | Clarity refactor, no behavior change | After code-reviewer passes |
| `ui-ux-designer` | Design-aware frontend implementation | UI/UX tasks |
| `git-manager` | Clean conventional commits | Git operations |

### Skills by Category

**Contract Skills** — define workflow artifacts:

| Skill | Purpose |
|---|---|
| `generate-plan` | Create SIMPLE or COMPLEX implementation plans |
| `generate-context` | Generate/update repository context |
| `audit-context` | Audit context routing and discoverability |
| `audit-plans` | Audit active-plan inventory and staleness |
| `audit-vc` | Audit harness health and agent parity |

**Analysis Skills** — deep investigation:

| Skill | Purpose |
|---|---|
| `ck-debug` | Root cause analysis helper |
| `ck-scenario` | Edge case generation across 12 dimensions |
| `ck-security` | STRIDE + OWASP security audit |
| `ck-predict` | 5-persona pre-implementation debate |
| `ck-autoresearch` | Autonomous metric optimization loop |
| `scout` | Fast parallel codebase scouting |

**Creation Skills** — build and design:

| Skill | Purpose |
|---|---|
| `frontend-design` | Polished UI from designs/screenshots |
| `tech-graph` | Publish-grade SVG/PNG diagrams |
| `web-testing` | Playwright/Vitest/k6 test automation |
| `docs` | Project documentation management |

**Utility Skills** — workflow helpers:

| Skill | Purpose |
|---|---|
| `sequential-thinking` | Step-by-step structured reasoning |
| `problem-solving` | Cognitive unblocking techniques |
| `context-engineering` | Token/context optimization |
| `preview` | Visual diagrams, slides, file viewer |
| `repomix` | Repository packing for audits |
| `xia` | Repo comparison and adaptation |
| `watzup` | Worktree and active-plan summary |
| `docs-seeker` | Library docs via context7 |
| `chrome-devtools` | Puppeteer browser automation |
| `agent-browser` | AI browser automation CLI |
| `mcp-management` | MCP server tools |
| `team` | Multi-agent parallel collaboration |

**Harness Management Skills**:

| Skill | Purpose |
|---|---|
| `vc-setup` | Scaffold harness into new project |
| `vc-update` | Pull latest harness from remote |
| `vc-publish` | Push improvements to remote kit repo |
| `add-worktree` | Create Git worktrees |
| `merge-worktree` | Merge Git worktrees |

### Hooks (7)

| Hook | Purpose |
|---|---|
| `session-init` | Initialize session context and statusline |
| `session-state` | Track session state across messages |
| `subagent-init` | Configure subagent context injection |
| `descriptive-name` | Generate descriptive session names |
| `scout-block` | Prevent unscoped file searches |
| `privacy-block` | Block sensitive data exposure |
| `post-edit-simplify-reminder` | Suggest simplification after edits |

### Development Protocols (6)

| Protocol | Purpose |
|---|---|
| `orchestration` | Delegation rules, status codes, context isolation |
| `implementation-standards` | Coding conventions and quality gates |
| `plan-lifecycle` | Plan creation, review, archival workflow |
| `phase-programs` | Multi-phase large program management |
| `context-maintenance` | Context group lifecycle and discovery |
| `all-development-protocols` | Root entrypoint and routing |

### Seed Templates (17)

Ready-to-use templates for bootstrapping your `process/` directory:

- Context router template (`all-context.md.seed`)
- Context group template (`_all-group-template.md.seed`)
- Test routing template (`all-tests.md.seed`)
- Planning routing template (`all-planning.md.seed`)
- Feature folder template with guides for each subdirectory
- General plans directory structure with guides
- Example PRDs (simple and complex)

---

## RIPER-5 Phases

| Phase | Command | What Happens |
|---|---|---|
| **RESEARCH** | `ENTER RESEARCH MODE` | Read-only investigation. No file modifications. |
| **INNOVATE** | `ENTER INNOVATE MODE` | Discuss approaches. No decisions made. |
| **PLAN** | `ENTER PLAN MODE` | Write detailed spec. No implementation. |
| **EXECUTE** | `ENTER EXECUTE MODE` | Implement exactly per approved plan. |
| **UPDATE** | `ENTER UPDATE PROCESS MODE` | Capture learnings, archive plan. |
| **FAST** | `ENTER FAST MODE` | All phases compressed with safety pause before EXECUTE. |

Phase transitions are strict: you cannot skip from RESEARCH to EXECUTE. The orchestrator enforces this automatically.

---

## Session Examples

### New Feature

```
You: Add a webhook notification system

Orchestrator: [MODE: ORCHESTRATOR] Detected feature request.
  Relevant skills: web-testing, ck-scenario, ck-security
  Routing to research-agent...

research-agent: [MODE: RESEARCH] Found existing notification patterns...
  Ready for INNOVATE.

You: go

innovate-agent: [MODE: INNOVATE] Three approaches considered...
  Recommended: event-driven with queue. Ready for PLAN.

You: go

plan-agent: [MODE: PLAN] Created webhook-notifications_PLAN_27-05-26.md
  Please review and say "ENTER EXECUTE MODE" to proceed.

You: ENTER EXECUTE MODE

execute-agent: [MODE: EXECUTE] Implementing per approved plan...
  ✓ 8/8 checklist items complete. All tests passing.
```

### Quick Bug Fix

```
You: Fix the broken date formatting in the dashboard

Orchestrator: Trivial fix detected (single file, no schema change).
  Routing directly to execute-agent.

execute-agent: Fixed date format string in dashboard-utils.ts.
  Changed: "YYYY-DD-MM" → "YYYY-MM-DD"
```

### Fast Mode

```
You: ENTER FAST MODE - add dark mode toggle to settings page

fast-mode-agent: [MODE: FAST]
  RESEARCH: Found existing theme system...
  INNOVATE: CSS variables approach selected...
  PLAN: Created dark-mode_PLAN_27-05-26.md

  ⏸ PAUSED — Review plan above. Say "ENTER EXECUTE MODE" to proceed.

You: ENTER EXECUTE MODE

fast-mode-agent: [MODE: EXECUTE] Implementing...
  ✓ Toggle component created
  ✓ CSS variables added
  ✓ LocalStorage persistence
  Done.
```

---

## Updating the Harness

Already using the kit? Pull the latest improvements:

```
Run the vc-update skill
```

**What happens:**

1. Clones the latest kit from remote
2. Compares every managed file against your local copy
3. Shows a dry-run diff summary table
4. **Waits for your confirmation** before applying
5. Updates managed files, syncs skills, refreshes seeds
6. Records the version in `.vc-version`

Your project-specific files (`process/context/`, `process/features/`, `process/general-plans/`) are **never touched** by updates.

---

## For Kit Maintainers

Push harness improvements from your development repo to this kit:

```
Run the vc-publish skill
```

**What happens:**

1. Reads your `.vc-publish-config` for the kit repo checkout path
2. Diffs all managed files and skills
3. Shows what changed
4. Asks for version bump type (patch/minor/major)
5. Copies files, bumps version, commits, tags, pushes
6. Verifies no project-specific content leaked

---

## Multi-Platform Support

| Platform | Support | How |
|---|---|---|
| **Claude Code** | Full | `.claude/agents/*.md` + `.claude/skills/` + `.claude/hooks/` |
| **Codex** | Full | `.codex/agents/*.toml` + `.agents/skills/` symlink + `.codex/hooks/` |
| **Cursor** | Partial | Reads `CLAUDE.md` for conventions; agents/hooks not supported |
| **Windsurf** | Partial | Reads `CLAUDE.md` for conventions; agents/hooks not supported |

The `.agents/skills/` symlink points to `.claude/skills/`, so both Claude Code and Codex discover the same skill tree automatically.

---

## Repository Structure

```
vibecode-pro-max-kit/
├── CLAUDE.md                    # Claude Code instructions (harness-only)
├── AGENTS.md                    # Codex compatibility layer
├── README.md                    # This file
├── vc-manifest.json             # Managed file manifest
├── .gitignore
├── .claude/
│   ├── agents/                  # 12 agent definitions (.md)
│   ├── hooks/                   # 7 hooks + lib/ + scout-block/
│   ├── hooks.json               # Claude hook discovery
│   └── skills/                  # 32 skill directories
├── .codex/
│   ├── agents/                  # 12 agent mirrors (.toml)
│   ├── hooks/                   # Codex hook copies
│   ├── hooks.json               # Codex hook discovery
│   └── config.toml              # Codex project config
├── .agents/
│   └── skills -> ../.claude/skills  # Symlink for Codex discovery
└── process/
    ├── _seeds/                  # Read-only bootstrap templates
    ├── development-protocols/   # 6 managed protocol files
    ├── context/                 # Project-specific knowledge (user-owned)
    │   └── planning/            # Example PRDs
    ├── features/                # Feature-scoped plans (user-owned)
    └── general-plans/           # Cross-cutting plans (user-owned)
        ├── active/
        ├── completed/
        ├── backlog/
        ├── reports/
        └── references/
```

---

## Contributing

1. Fork this repository
2. Create a feature branch
3. Make your changes (follow RIPER-5 — use the harness on itself)
4. Run `audit-vc` to verify harness health
5. Submit a pull request

When adding new skills, place them in `.claude/skills/{skill-name}/SKILL.md` with YAML frontmatter. Update the skill registry table in both `CLAUDE.md` and `AGENTS.md`.

When adding new agents, create both `.claude/agents/{name}.md` and `.codex/agents/{name}.toml`.

---

## License

MIT

---

<p align="center">
  <sub>Built with RIPER-5 methodology. Every feature of this kit was developed using the kit itself.</sub>
</p>
