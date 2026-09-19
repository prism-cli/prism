# Prism

Refract your universal developer agents and skills across Cursor, Claude, Codex, Grok, and Gemini.

> [!NOTE]
> This is a starter template. Fork it to your own GitHub account to maintain and version-control your personal developer setup across machines.

```
Applying prism to ~/Sites/project

  gemini ................................... active (3 agents, 2 skills)
  claude ................................... active (3 agents, 2 skills)
  codex .................................... active (3 agents, 2 skills)
  grok ..................................... active (3 agents, 2 skills)
  cursor ................................... active (3 agents, 2 skills)
```

## Quick Start

```bash
# 1. Clone your fork
git clone https://github.com/<your-username>/prism.git ~/prism

# 2. Install
~/prism/bin/prism install

# 3. Apply to any project
cd ~/Sites/my-project
prism
```

## Structure & Mappings

Define agents and skills once in `~/prism`. Prism links them to native paths:

```
~/prism/
├── bin/prism        # CLI runner
├── agents/*.md      # Universal agent personas
└── skills/*/SKILL.md # Reusable workflows
```

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
| `prism` | `prism a` | Apply all providers to current project |
| `prism <provider>` | `prism cr`, `prism c`, etc. | Apply a single provider |
| `prism status` | `prism st` | View status across providers |
| `prism list` | `prism ls` | List all available agents and skills |
| `prism clean` | `prism rm` | Remove all symlinks from project |
| `prism clean <provider>` | `prism rm c` | Remove links for a single provider |
| `prism install` / `uninstall` | `i` / `ui` | Manage shell aliases |

> [!TIP]
> Prism automatically registers symlinks in `.git/info/exclude`. Your setup is active without polluting `git status` or commit diffs.

## Contributing

Contributions are welcome. Feel free to open issues or PRs to support new providers, improve shell integrations, or refine default agent and skill templates.


