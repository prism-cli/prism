<div align="center">

# Prism

**Refract your universal developer agents and skills across all AI assistants.**

A lightweight template and CLI system to maintain your personal AI personas, rules, and runbooks in one central vault — seamlessly linked into any repository for **Cursor**, **Claude Code**, **Codex**, **Grok**, and **Gemini / Antigravity**.

[Quick Start](#quick-start) • [How It Works](#how-it-works) • [Commands](#commands) • [Fork & Customize](#fork--customize)

</div>

> [!NOTE]
> This repository is a starter template. Fork it to your own GitHub account, tailor your agents and skills, and keep your personal AI development environment version-controlled across machines.

```
Applying prism to ~/Sites/project

  gemini ................................... active (3 agents, 2 skills)
  claude ................................... active (3 agents, 2 skills)
  codex .................................... active (3 agents, 2 skills)
  grok ..................................... active (3 agents, 2 skills)
  cursor ................................... active (3 agents, 2 skills)
```

## Quick Start

### 1. Fork & Clone
Fork this repository to your GitHub, then clone it to your local environment:
```bash
git clone https://github.com/<your-username>/prism.git ~/prism
cd ~/prism
```

### 2. Install Shell Integration
Register the `prism` command globally (supports Zsh and Fish):
```bash
./bin/prism install
source ~/.zshrc   # or source ~/.config/fish/config.fish
```

### 3. Activate in Any Project
Open any Git repository on your machine and run:
```bash
prism
```
All universal agents and skills are linked into the project's native provider paths, automatically excluded from Git, and ready to use.

## How It Works

Maintain only your universal Markdown definitions in `~/prism`. The CLI maps them into each tool's native discovery structure:

```
~/prism/
├── bin/prism                # Single zero-dependency executive script
├── agents/                  # Universal personas (.md)
│   ├── agent-1.md           # e.g., Code Reviewer & Security Auditor
│   ├── agent-2.md           # e.g., Test Engineer & QA Specialist
│   └── agent-3.md           # e.g., Architecture Specialist
└── skills/                  # Universal runbooks
    ├── code-review/SKILL.md
    └── git-workflow/SKILL.md
```

### Native Provider Mappings

| Provider | Shortcut | Agents & Rules | Skills | Git Exclude |
| :--- | :---: | :--- | :--- | :--- |
| **Cursor** | `cr` | `.cursor/agents/` & `.cursor/rules/` | `.cursor/skills/` | `.cursor/` |
| **Claude** | `c` | `.claude/agents/` | `.claude/skills/` | `.claude/` |
| **Codex** | `cx` | `.codex/agents/` | `.codex/skills/` | `.codex/` |
| **Grok** | `gk` | `.grok/agents/` | `.grok/skills/` | `.grok/` |
| **Gemini** | `g` | `.agents/agents/` | `.agents/skills/` | `.agents/` |

## Commands

| Command | Shortcut | Description |
| :--- | :---: | :--- |
| `prism` | `prism a` | Apply all providers to the current project |
| `prism <provider>` | `prism cr`, `prism c`, etc. | Apply only a specific provider (`cr`, `c`, `cx`, `gk`, `g`) |
| `prism status` | `prism st` | View active/inactive status across providers |
| `prism list` | `prism ls` | List all available agents and skills in vault |
| `prism clean` | `prism rm` | Safely remove all prism symlinks from project |
| `prism clean <provider>` | `prism rm c` | Clean links for a specific provider only |
| `prism install` | `prism i` | Register shell aliases (`~/.zshrc`, Fish config) |
| `prism uninstall` | `prism ui` | Remove shell aliases |

## Fork & Customize

Make Prism your own:

1. **Add Custom Personas**: Drop new markdown files into `agents/` defining system prompts, constraints, and instructions.
2. **Add Custom Skills**: Create folders under `skills/<name>/SKILL.md` for task-specific playbooks (e.g. database migrations, release checklists).
3. **Commit & Push**: Push changes to your own fork to keep your multi-machine developer setup in sync.

> [!TIP]
> Prism automatically and silently appends active symlinks to `.git/info/exclude`. Your developer configuration is always live in your editor, but **never appears in `git status`, commits, or PR diffs**.

