# Draw.io Skill

`drawio-skill` is a Codex skill for creating and editing draw.io diagrams through a configured `drawio` MCP server.

It is designed for:

- flowcharts
- architecture and deployment diagrams
- ML model diagrams such as LSTM, Transformer, and CNN
- Chinese labels and Chinese output
- animated connectors
- `.drawio` and `.svg` export workflows

## What This Skill Does

This skill teaches Codex how to use a draw.io MCP server in a stable workflow:

1. start a draw.io session
2. create diagrams from full XML
3. read the current diagram before editing
4. export editable and shareable outputs

It also includes rules for:

- diagram naming conventions
- Chinese labeling
- architecture-focused layouts
- ML model diagram layouts
- animated connector export behavior

## Requirements

This repository contains the skill only. It does not bundle the MCP server itself.

You need a working `drawio` MCP server in Codex before using this skill.

One common setup is:

```bash
codex mcp add drawio -- npx -y @next-ai-drawio/mcp-server@latest
```

After configuring the server, restart Codex or reload the IDE window if the tools do not appear.

## Install

### Option 1: Clone directly into Codex skills

Clone this repository into your Codex skills directory and keep the folder name as `drawio-skill`.

Typical locations:

- Windows: `%USERPROFILE%\\.codex\\skills\\drawio-skill`
- macOS/Linux: `~/.codex/skills/drawio-skill`

### Option 2: Copy the files manually

Copy these files into a folder named `drawio-skill` inside your Codex skills directory:

- `SKILL.md`
- `agents/openai.yaml`

## Usage

Example prompts:

```text
Use $drawio-skill to create a cloud architecture diagram.
```

```text
Use $drawio-skill to draw a Chinese-labeled order flowchart and export drawio + svg.
```

```text
Use $drawio-skill to create an animated LSTM architecture diagram.
```

## Repository Layout

```text
drawio-skill/
├── SKILL.md
├── README.md
├── LICENSE
└── agents/
    └── openai.yaml
```

## License

This repository is licensed under `MIT-0`.
