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

| Provider | Shortcut | Agents Location | Skills Location | Git Ignore Scope |
| :--- | :--- | :--- | :--- | :--- |
| **Cursor** | `cr` | `.cursor/agents/` & `.cursor/rules/` | `.cursor/skills/` | `.cursor/` |
| **Claude** | `c` | `.claude/agents/` | `.claude/skills/` | `.claude/` |
| **Codex** | `cx` | `.codex/agents/` | `.codex/skills/` | `.codex/` |
| **Grok** | `gk` | `.grok/agents/` | `.grok/skills/` | `.grok/` |
| **Gemini** | `g` | `.agents/agents/` | `.agents/skills/` | `.agents/` |

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

## ⌨️ Fast Shortcuts Reference

| Full Command | Shortcut | Description |
| :--- | :--- | :--- |
| `prism` or `prism sync` | `prism s` | Sync all providers |
| `prism status` | `prism st` | Check sync status |
| `prism list` | `prism ls` (or `prism l`) | List vault agents & skills |
| `prism unsync` | `prism u` (or `prism rm`) | Unsync all providers |
| `prism cursor` | `prism cr` | Sync only Cursor |
| `prism claude` | `prism c` | Sync only Claude |
| `prism codex` | `prism cx` | Sync only Codex |
| `prism grok` | `prism gk` | Sync only Grok |
| `prism gemini` | `prism g` | Sync only Gemini |
| `prism unsync claude` | `prism u c` | Unsync only Claude |

---

## 🛡️ Git Protection
`prism` automatically and silently registers symlinks in `.git/info/exclude`. Your personal developer mindset is fully active, but **never committed or visible in `git status`**.
