# Prism

Sync your personal AI agents and skills across all coding tools from one central vault.

```
~/prism (your vault)
  ├── agents/      ──►  .cursor/   .claude/   .codex/   .grok/   .agents/
  └── skills/      ──►  (auto-symlinked & hidden from git status)
```

> [!NOTE]
> This repository is a starter template. Fork it to build and version-control your own AI developer environment across machines.

## Why Prism?

Every AI coding tool looks in a different folder:
- Cursor looks in `.cursor/`
- Claude looks in `.claude/`
- Codex looks in `.codex/`
- Grok looks in `.grok/`
- Gemini / Antigravity looks in `.agents/`

Instead of copying and pasting instructions across every project and tool, keep your personas and runbooks once in `~/prism`. Running `prism` links them into whichever tool you use—instantly and without polluting Git.

## Quick Start

```bash
# 1. Clone your fork
git clone https://github.com/<your-username>/prism.git ~/prism

# 2. Install CLI to ~/.local/bin
~/prism/bin/prism install

# 3. In any project, run:
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

## How It Works

1. **One Vault (`~/prism`)**: Edit your agents (`agents/*.md`) and skills (`skills/*/SKILL.md`) in one place. Starter examples are included.
2. **Native Mapping**: `prism` creates symlinks in your project matching each AI assistant's expected structure.
3. **Zero Git Noise**: Symlinks are automatically registered in `.git/info/exclude`. Your team never sees your personal setup in PRs or `git status`.

## Commands

| Command | Shortcut | Description |
| :--- | :---: | :--- |
| `prism` | `prism a` | Link all AI assistants into current project |
| `prism <provider>` | `prism cr`, `prism c`, etc. | Link a single assistant (`cr`, `c`, `cx`, `gk`, `g`) |
| `prism status` | `prism st` | View active assistants in current project |
| `prism list` | `prism ls` | List all available agents and skills in your vault |
| `prism clean` | `prism rm` | Unlink all assistants from project |
| `prism clean <provider>` | `prism rm c` | Unlink a specific assistant |
| `prism install` / `uninstall` | `i` / `ui` | Setup or remove CLI from `~/.local/bin` |

## Contributing

Pull requests are welcome to add new providers or improve starter templates.

