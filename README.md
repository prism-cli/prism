# Prism

Sync your personal AI developer agents and skills across Cursor, Claude, Codex, Grok, and Gemini from one central vault.

[Create your vault from this template](https://github.com/prism-cli/prism/generate) to version-control your personal AI setup across machines.

## Why Prism?

| Without Prism ❌ | With Prism ✅ |
| :--- | :--- |
| Copy-pasting AI configs across projects | Run `prism` once |
| Updating rules in 20 different repos | Edit once in `~/prism`, updated everywhere |
| Personal AI files leaking into git commits | Silently ignored via `.git/info/exclude` |

## How it Works

1. Keep your custom agents (`agents/*.md`) and skills (`skills/*/SKILL.md`) once in `~/prism`.
2. Running `prism` links them into each tool's native folder (`.cursor/`, `.claude/`, `.agents/`, etc.).
3. Symlinks are automatically added to `.git/info/exclude`—never polluting `git status` or PRs.

## Quick Start

```terminal
$ git clone https://github.com/<your-username>/prism.git ~/prism
$ ~/prism/bin/prism install

$ cd ~/Sites/my-project
$ prism

Applying prism to ~/Sites/my-project

  gemini ................................... active (3 agents, 2 skills)
  claude ................................... active (3 agents, 2 skills)
  codex .................................... active (3 agents, 2 skills)
  grok ..................................... active (3 agents, 2 skills)
  cursor ................................... active (3 agents, 2 skills)
```

## Commands

| Command | Shortcut | Description |
| :--- | :---: | :--- |
| `prism` | `prism a` | Link all tools (stealth mode, ignored by git) |
| `prism --track` | `prism -t` | Link all tools and track in Git to share with team |
| `prism <tool>` | `prism cr`, `prism c`, etc. | Link one tool (`cr`, `c`, `cx`, `gk`, `g`) |
| `prism clean` | `prism rm` | Unlink tools from project |
| `prism status` | `prism st` | Check project status |
| `prism list` | `prism ls` | List agents and skills |
| `prism install` | `prism i` | Symlink CLI to `~/.local/bin` |
| `prism uninstall` | `prism ui` | Remove CLI symlink |

## Requirements

- **macOS** or **Linux** (native bash, zsh, fish)
- **Windows** via **WSL2** or **Git Bash**

## Contributing

PRs are welcome to add tools or improve templates.
