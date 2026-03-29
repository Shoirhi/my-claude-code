# my-claude-code
This is my Claude Code setup, based on various repositories with my own custom tweaks.

## Files

| File | Description | Configuration Path | References |
| ---- | ---- | ---- | ---- |
| [statusline.sh](statusline.sh) | Status line configuration script. | `~/claude/statusline.sh` | [Customize your status line - Claude Code Docs](https://code.claude.com/docs/en/statusline), [everything-claude-code/examples/statusline.json](https://github.com/affaan-m/everything-claude-code/blob/main/examples/statusline.json) |

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