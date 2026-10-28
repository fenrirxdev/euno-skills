# euno-skills

Agent skills for [euno](https://github.com/fenrirxdev), a macOS app that lets the AI chats you link (Claude, Codex, Cursor) read each other's conversations.

## Skills

| Skill | What it does |
| --- | --- |
| [`euno`](skills/euno/SKILL.md) | Catches up on another chat you linked with euno: reads what is new there and summarizes it, or does what you ask with it. |

## Install

```bash
npx skills add fenrirxdev/euno-skills -g -a claude-code -a codex -a cursor
```

This uses [vercel-labs/skills](https://github.com/vercel-labs/skills) (Node.js 22.20 or later). Update later with `npx skills update`.

## Use

In a chat that is in an euno bridge:

- Claude Code and Cursor: `/euno codex`
- Codex: `$euno claude`

The word after the command names the other chat's app or part of its title. Anything after that is what you want done with what was read. With nothing after the command, the skill reads the one other chat in the bridge.

## Requirements

The skill reads other chats through the euno MCP server (`euno-mcp`), which ships inside the euno app. The app must be installed and `euno-mcp` registered in each AI app; euno's settings show how. euno itself is not public yet, so for now the skill only works where euno is installed.

## License

[MIT](LICENSE)
