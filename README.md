# Mindset

> Single source of truth for your personal developer mindset, AI agent configurations, and skills across all AI providers.

---

## ⚡ Unified Architecture

Maintain only **`agents/`** and **`skills/`** in your central vault. The CLI script syncs them into the native, default locations of each AI assistant:

```
~/mindset/
├── bin/
│   └── mindset              # Executive CLI tool
├── agents/                  # Universal agent definitions (.md)
│   ├── agent-1.md           # Code Reviewer & Security Auditor
│   ├── agent-2.md           # Test Engineer & QA Specialist
│   └── agent-3.md           # Architecture & Documentation Specialist
├── skills/                  # Universal skills runbooks
│   ├── code-review/
│   │   └── SKILL.md
│   └── git-workflow/
│       └── SKILL.md
└── README.md
```

---

## 🌐 Provider Destination Paths

When synced to any project workspace, Mindset links your agents & skills into each provider's native directory structure:

| Provider | Agents Location | Skills Location | Git Ignore Scope |
| :--- | :--- | :--- | :--- |
| **Cursor** | `.cursor/agents/` & `.cursor/rules/` | `.cursor/skills/` | `.cursor/` |
| **Claude** | `.claude/agents/` | `.claude/skills/` | `.claude/` |
| **Codex** | `.codex/agents/` | `.codex/skills/` | `.codex/` |
| **Grok** | `.grok/agents/` | `.grok/skills/` | `.grok/` |
| **Gemini / Antigravity** | `.agents/agents/` | `.agents/skills/` | `.agents/` |

---

## 🚀 Setup & Installation

Run once to register shell integrations for **Zsh** and **Fish**:

```bash
~/mindset/bin/mindset install
```

Then reload your shell:
```bash
source ~/.zshrc                     # for Zsh
source ~/.config/fish/config.fish   # for Fish
```

---

## 💻 Commands

Navigate to any project repository:

```bash
# Sync ALL providers by default:
mindset

# Or explicitly:
mindset sync

# Sync a specific provider only:
mindset cursor
mindset claude
mindset codex
mindset grok
mindset gemini

# Check sync status across all providers:
mindset status

# List all available agents and skills in your vault:
mindset list

# Unsync ALL providers by default:
mindset unsync

# Unsync a specific provider only:
mindset unsync cursor

# Remove shell aliases:
mindset uninstall
```

---

## 🛡️ Git Protection
`mindset` automatically and silently registers symlinks in `.git/info/exclude`. Your personal developer mindset is fully active, but **never committed or visible in `git status`**.
