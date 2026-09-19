# Prism

Refract your personal developer agents and skills across AI assistants.

> [!NOTE]
> Fork this template to version-control your personal AI setup across machines.

## What is this?

Every AI coding tool expects agent personas and skill runbooks in different hidden folders (`.cursor/`, `.claude/`, `.agents/`, etc.). 

**Prism** is a single central vault (`~/prism`) for all your custom developer instructions. The CLI links them into whichever AI assistants you use in any repository—instantly and without polluting Git.

## How it works

1. **One Vault**: You maintain universal Markdown agents (`agents/*.md`) and skills (`skills/*/SKILL.md`) in `~/prism`.
2. **Native Symlinks**: Running `prism` in any project creates symlinks mapped to each provider's native discovery folder.
3. **Zero Git Noise**: Created paths are automatically registered in `.git/info/exclude`, so your private personas are never tracked or committed.

## Quick Start

```bash
# 1. Clone your fork
git clone https://github.com/<your-username>/prism.git ~/prism

# 2. Install CLI
~/prism/bin/prism install

# 3. Apply to any project
prism
```

```
Applying prism to ~/Sites/project

  gemini ................................... active (3 agents, 2 skills)
  claude ................................... active (3 agents, 2 skills)
  codex .................................... active (3 agents, 2 skills)
  grok ..................................... active (3 agents, 2 skills)
  cursor ................................... active (3 agents, 2 skills)
```

## Providers

Prism symlinks your `~/prism/agents` and `~/prism/skills` into native directories and silently excludes them via `.git/info/exclude`.

| Provider | Shortcut | Target Path |
| :--- | :---: | :--- |
| **Cursor** | `cr` | `.cursor/agents/`, `.cursor/rules/`, `.cursor/skills/` |
| **Claude** | `c` | `.claude/agents/`, `.claude/skills/` |
| **Codex** | `cx` | `.codex/agents/`, `.codex/skills/` |
| **Grok** | `gk` | `.grok/agents/`, `.grok/skills/` |
| **Gemini** | `g` | `.agents/agents/`, `.agents/skills/` |

## Commands

| Command | Shortcut | Description |
| :--- | :---: | :--- |
| `prism` | `prism a` | Apply all providers |
| `prism <provider>` | `prism cr`, `prism c`, etc. | Apply specific provider |
| `prism status` | `prism st` | Check project status |
| `prism list` | `prism ls` | List agents and skills |
| `prism clean` | `prism rm` | Remove links from project |
| `prism clean <provider>` | `prism rm c` | Remove links for specific provider |
| `prism install` / `uninstall` | `i` / `ui` | Setup or remove CLI integration |

## Contributing

Pull requests are welcome to add new providers or improve templates.
