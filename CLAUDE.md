# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Purpose

This is the **Tag1 Consulting Claude Code Plugin Marketplace** — a registry that tells Claude Code where to find plugins published by Tag1. It contains no plugin code itself; each plugin lives in its own repository.

## Structure

- `.claude-plugin/marketplace.json` — The marketplace manifest. Conforms to `https://anthropic.com/claude-code/marketplace.schema.json`. Each entry in the `plugins` array points to an external git repository containing the actual plugin.
- `README.md` — Public-facing docs listing available plugins and install instructions.

## Adding a New Plugin

1. Add an entry to the `plugins` array in `.claude-plugin/marketplace.json` with: `name`, `version`, `source` (git URL), `description`, `author`, `category`, and `homepage`.
2. Add a row to the "Available Plugins" table in `README.md`.
3. Both files must stay in sync — same plugin name, same description intent, same homepage URL.

## Current Plugins

| Plugin | Source Repo |
|--------|-------------|
| `comprehensive-review` | `tag1consulting/claude-comprehensive-review` |

## Install Command (for reference)

```
/plugins install <plugin-name>@tag1consulting
```
