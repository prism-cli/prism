# Mindset

> Single source of truth for your personal developer mindset, AI agent configurations, and standards across all AI providers.

---

## 🎨 Laravel-Style Terminal UI

Mindset features a high-contrast, polished Laravel Artisan-style CLI with badges, dynamic dot-leaders, agent tree visualization, and millisecond execution timers.

```terminal
   SYNC   Syncing antigravity to project
  target  /Users/dasun/projects/my-app

  antigravity (.agents/agents) .................................. SYNCED
  stealth-mode ............................................ GIT EXCLUDED

   AGENTS   Active subagents available in workspace
    ├── agent-1.md ....... Autonomous code quality reviewer and secur...
    ├── agent-2.md ....... QA Automation specialist that authors comp...
    └── agent-3.md ....... Systems architect and technical writer who...

   DONE   Mindset synced successfully in 84ms
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

Run once to register shell integrations for **Zsh**, **Bash**, and **Fish**:

```bash
~/mindset/bin/mindset install
```

Then reload your shell:
```bash
source ~/.zshrc                     # for Zsh
source ~/.config/fish/config.fish   # for Fish
```

---

## 💻 Usage

Navigate to any project repository and run:

```bash
# Sync Antigravity agents (default)
mindset sync antigravity
# or simply:
mindset antigravity

# Sync other providers
mindset sync cursor
mindset sync claude

# Check sync status across all providers
mindset status

# List all available mindset agents in your vault
mindset list

# Unsync from the current project
mindset unsync antigravity
```

---

## 🛡️ Stealth Mode (Untracked by Git)
`mindset` automatically registers symlinks in `.git/info/exclude`. Your personal developer mindset is fully active, but **never committed or visible in `git status`**.
