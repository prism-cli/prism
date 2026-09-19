# Prism

Sync your personal AI developer agents and skills across Cursor, Claude, Codex, Grok, and Gemini from one central vault.

Fork this template to version-control your personal setup across machines.

## Quick Start

```bash
# 1. Clone your fork
git clone https://github.com/<your-username>/prism.git ~/prism

# 2. Install CLI (~/.local/bin)
~/prism/bin/prism install

# 3. In any project:
prism
```

```
Applying prism to ~/Sites/my-project

  gemini ................................... active (3 agents, 2 skills)
  claude ................................... active (3 agents, 2 skills)
  codex .................................... active (3 agents, 2 skills)
  grok ..................................... active (3 agents, 2 skills)
  cursor ................................... active (3 agents, 2 skills)
```

## How it Works

1. Keep your custom agents (`agents/*.md`) and skills (`skills/*/SKILL.md`) once in `~/prism`.
2. Running `prism` links them into each tool's native folder (`.cursor/`, `.claude/`, `.agents/`, etc.).
3. Symlinks are automatically added to `.git/info/exclude`—never polluting `git status` or PRs.

## Commands

| Command | Shortcut | Description |
| :--- | :---: | :--- |
| `prism` | `prism a` | Link all tools to project |
| `prism <tool>` | `prism cr`, `prism c`, etc. | Link one tool (`cr`, `c`, `cx`, `gk`, `g`) |
| `prism clean` | `prism rm` | Unlink tools from project |
| `prism status` | `prism st` | Check project status |
| `prism list` | `prism ls` | List agents and skills |
| `prism install` | `prism i` | Symlink CLI to `~/.local/bin` |
| `prism uninstall` | `prism ui` | Remove CLI symlink |

## Contributing

PRs are welcome to add tools or improve templates.
