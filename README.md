# Prism

> Refract your personal developer agents and skills across all AI providers.

---

## Clean Terminal UI

```terminal
Applying prism to ~/Sites/jacasa-cp

  gemini ................................... active (3 agents, 2 skills)
  claude ................................... active (3 agents, 2 skills)
  codex .................................... active (3 agents, 2 skills)
  grok ..................................... active (3 agents, 2 skills)
  cursor ................................... active (3 agents, 2 skills)
```

---

## Directory Structure

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

## Provider Destination Paths

| Provider | Shortcut | Agents Location | Skills Location | Git Ignore Scope |
| :--- | :--- | :--- | :--- | :--- |
| **Cursor** | `cr` | `.cursor/agents/` & `.cursor/rules/` | `.cursor/skills/` | `.cursor/` |
| **Claude** | `c` | `.claude/agents/` | `.claude/skills/` | `.claude/` |
| **Codex** | `cx` | `.codex/agents/` | `.codex/skills/` | `.codex/` |
| **Grok** | `gk` | `.grok/agents/` | `.grok/skills/` | `.grok/` |
| **Gemini** | `g` | `.agents/agents/` | `.agents/skills/` | `.agents/` |

---

## Installation

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

## Commands

Navigate to any project repository:

```bash
# Apply ALL providers by default:
prism

# Apply a specific provider only:
prism cursor        # (shortcut: prism cr)
prism claude        # (shortcut: prism c)
prism codex         # (shortcut: prism cx)
prism grok          # (shortcut: prism gk)
prism gemini        # (shortcut: prism g)

# Check status across all providers:
prism status        # (shortcut: prism st)

# List all available agents and skills in your vault:
prism list          # (shortcut: prism ls)

# Clean ALL providers from the project:
prism clean         # (shortcut: prism rm)

# Clean a specific provider only:
prism clean cursor  # (shortcut: prism clean cr)

# Remove shell aliases:
prism uninstall     # (shortcut: prism ui)
```

---

## Git Protection
`prism` automatically and silently registers symlinks in `.git/info/exclude`. Your personal developer mindset is fully active, but **never committed or visible in `git status`**.

