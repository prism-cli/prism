# Mindset

> Single source of truth for your personal developer mindset, AI agent configurations, and standards across all AI providers.

## Architecture

```
~/mindset/
├── bin/
│   └── mindset              # CLI management tool
├── antigravity/
│   └── agents/              # Antigravity subagent markdown definitions
│       ├── agent-1.md       # Code Reviewer & Security Auditor
│       ├── agent-2.md       # Test Engineer & QA Specialist
│       └── agent-3.md       # Architecture & Documentation Specialist
├── cursor/
│   └── rules/               # Cursor rules (.cursor/rules/)
└── claude/                  # Claude Code configurations (.claude/)
```

## Setup & Installation

Run once to register shell aliases for **Zsh**, **Bash**, and **Fish**:

```bash
~/mindset/bin/mindset install
```

Then reload your shell (`source ~/.zshrc` or `source ~/.config/fish/config.fish`).

## Usage in Projects

Navigate to any project repository and run:

```bash
# Injects your Antigravity agents (default)
mindset antigravity

# Injects Cursor rules
mindset cursor

# Injects Claude settings
mindset claude

# Check what is currently linked
mindset status

# Cleanly remove links
mindset unlink antigravity
```

## Stealth Mode (Git Ignored)
`mindset` automatically registers symlinks in `.git/info/exclude`, so your personal configuration is **never committed** to the project repository.
