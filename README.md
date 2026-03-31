# my-claude-code
This is my Claude Code setup, based on various repositories with my own custom tweaks.

## Files

| File | Description | Configuration Path | References |
| ---- | ---- | ---- | ---- |
| [statusline.sh](statusline.sh) | Status line configuration script. | `~/claude/statusline.sh` | [Customize your status line - Claude Code Docs](https://code.claude.com/docs/en/statusline), [everything-claude-code/examples/statusline.json](https://github.com/affaan-m/everything-claude-code/blob/main/examples/statusline.json) |

## Install Plugins/Skills

### Anthropic's official plugins
https://github.com/anthropics/skills
https://github.com/anthropics/claude-plugins-official/tree/main

#### Skill Creator
```
/plugin marketplace add anthropics/skills

/plugin install skill-creator@anthropic-agent-skills
```

### Chrome Dev Tools
https://github.com/ChromeDevTools/chrome-devtools-mcp
```
/plugin marketplace add ChromeDevTools/chrome-devtools-mcp

/plugin install chrome-devtools-mcp
```

### WordPress
https://github.com/WordPress/agent-skills/
```
git clone https://github.com/WordPress/agent-skills.git

cd agent-skills

node shared/scripts/skillpack-build.mjs --clean

node shared/scripts/skillpack-install.mjs --global

cd ../

sudo rm -r agent-skills
```

### Figma
https://developers.figma.com/docs/figma-mcp-server/remote-server-installation/#claude-code
```
/plugin install figma@claude-plugins-official
```

## Status Line Configuration
1. Create the `~/.claude/statusline.sh` file.
2. Add the following configuration to `~/.claude/settings.json`:

```json
"statusLine": {
    "type": "command",
    "command": "sh /Users/{Username}/.claude/statusline.sh"
 },
 ```

3. Run `chmod +x ~/.claude/statusline.sh`.

## Techniques

- use `!` for bash mode in Claude Code CLI. (Example: `!ls`)