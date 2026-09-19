# Prism

> Refract your personal developer agents and skills across all AI providers.

---

## ⚡ Clean Terminal UI

```terminal
⚡ Syncing prism to ~/Sites/jacasa-cp

  gemini ................................... synced (3 agents, 2 skills)
  claude ................................... synced (3 agents, 2 skills)
  codex .................................... synced (3 agents, 2 skills)
  grok ..................................... synced (3 agents, 2 skills)
  cursor ................................... synced (3 agents, 2 skills)
```

---

## 📦 Directory Structure

Maintain only **`agents/`** and **`skills/`** in your central vault. Prism automatically links them into each AI assistant's native directories:

```
~/prism/
├── bin/
│   └── prism                # Executive CLI tool
├── agents/                  # Universal subagent definitions (.md)
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

| Provider | Agents Location | Skills Location | Git Ignore Scope |
| :--- | :--- | :--- | :--- |
| **Cursor** | `.cursor/agents/` & `.cursor/rules/` | `.cursor/skills/` | `.cursor/` |
| **Claude** | `.claude/agents/` | `.claude/skills/` | `.claude/` |
| **Codex** | `.codex/agents/` | `.codex/skills/` | `.codex/` |
| **Grok** | `.grok/agents/` | `.grok/skills/` | `.grok/` |
| **Gemini / Antigravity** | `.agents/agents/` | `.agents/skills/` | `.agents/` |

---

## 🚀 Installation

Run once to register shell integrations for **Zsh** and **Fish**:

```bash
~/prism/bin/prism install
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
prism

# Sync a specific provider only:
prism cursor
prism claude
prism codex
prism grok
prism gemini

# Check sync status across all providers:
prism status

# List all available agents and skills in your vault:
prism list

# Unsync ALL providers by default:
prism unsync

# Unsync a specific provider only:
prism unsync cursor

# Remove shell aliases:
prism uninstall
```

---

## 🛡️ Git Protection
`prism` automatically and silently registers symlinks in `.git/info/exclude`. Your personal developer mindset is fully active, but **never committed or visible in `git status`**.
