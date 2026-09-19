# Mindset

> Single source of truth for your personal developer mindset, AI agent configurations, and standards across all AI providers.

---

## ⚡ Visual CLI Experience

```terminal
⚡ Syncing my mindset to ~/projects/my-app
  ◈ antigravity ──● synced (3 agents)

⚡ My mindset status in ~/projects/my-app
  ◈ antigravity ──● in sync (3 agents)
  ◈ cursor      ──○ not synced
  ◈ claude      ──○ not synced

⚡ Unsyncing my mindset from ~/projects/my-app
  ◈ antigravity ──○ unsynced
```

---

## 📦 Directory Structure

```
~/mindset/
├── bin/
│   └── mindset              # Executive CLI tool
├── antigravity/
│   └── agents/              # Antigravity subagent markdown definitions
│       ├── agent-1.md       # Code Reviewer & Security Auditor
│       ├── agent-2.md       # Test Engineer & QA Specialist
│       └── agent-3.md       # Architecture & Documentation Specialist
├── cursor/
│   └── rules/               # Cursor rules (.cursor/rules/)
└── claude/                  # Claude Code configurations (.claude/)
```

---

## 🚀 Installation

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
# Sync Antigravity agents (default)
mindset sync antigravity
# or simply:
mindset antigravity

# Check sync status across all providers
mindset status

# List all available mindset agents in your vault
mindset list

# Unsync from the current project
mindset unsync antigravity

# Remove shell aliases
mindset uninstall
```

---

## 🛡️ Git Protection
`mindset` automatically and silently registers symlinks in `.git/info/exclude`. Your personal developer mindset is fully active, but **never committed or visible in `git status`**.
