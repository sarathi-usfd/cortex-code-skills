# cortex-code-guide

**Author:** karthick
**Skill Mode:** Live
**Category:** Reference / Documentation

---

## Overview

Complete reference guide for Cortex Code CLI features. Covers slash commands, keyboard shortcuts, configuration settings, skills system, MCP servers, hooks, agents, Snowflake-native tools, and session management.

---

## When to Use

- You want to know what slash commands are available (`/help`, `/commit`, etc.)
- You want to configure Cortex Code settings or hooks
- You need to understand how sessions, forking, or rewinding work
- You want to set up MCP servers for external tool integrations
- You want to understand how the skills system works
- You need keyboard shortcut references

---

## How to Use

Invoke for any question about Cortex Code itself:

```
/cortex-code-guide
```

**Or ask directly:**
> "What slash commands are available?"
> "How do I set up a hook to run before every commit?"
> "How do I connect an MCP server?"
> "What does the `#table` syntax do?"

### Reference Sections

| File | Topic |
|------|-------|
| `COMMANDS.md` | All slash commands and their usage |
| `SHORTCUTS.md` | Keyboard shortcuts reference |
| `CONFIGURATION.md` | Settings, config file locations, options |
| `SKILLS.md` | How skills work, how to install/invoke |
| `MCP.md` | MCP server integration setup |
| `HOOKS.md` | Hook system for automation |
| `AGENTS.md` | Agent and background task system |
| `SNOWFLAKE.md` | Snowflake-native tools (`#table`, `#schema`) |
| `SESSIONS.md` | Session resume, fork, and rewind |

---

## Testing

- This is a documentation/reference skill — no code execution required
- Verify by reading the specific `.md` reference file for the feature in question
- Test slash commands live in the Cortex Code terminal

---

## Related Skills

- `skill_development` — Learn how to create new skills
- `update-config` (built-in) — Configure Claude Code/Cortex Code settings
