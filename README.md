# Dinoctor downloads

The installers for Dinoctor, a video maker for faceless creators. This project holds only the installers, no source code.

Get the latest version from [Releases](https://github.com/Dinoctor/dinoctor-downloads/releases/latest).

- **Mac:** Apple chip (M1 or newer), macOS 12 or newer.
- **Windows:** Windows 10 or 11, 64-bit.

This is a beta. It isn't signed yet, so the first time you open it:
- **Mac:** System Settings, Privacy & Security, Open Anyway.
- **Windows:** on "Windows protected your PC", click More info, then Run anyway.

## Use Dinoctor from Claude, Claude Code or Cursor (MCP)

Dinoctor has a built-in [MCP](https://modelcontextprotocol.io) server. With it, an AI app on your computer can make and change videos in the open Dinoctor window while you watch: write the script, add scenes and shots, pick places, characters, camera moves and lights, add voice and music, and render the MP4.

There is nothing extra to install. The app itself is the server: it runs as `Dinoctor --mcp` over stdio.

**Easiest:** in Dinoctor, open **Help → Connect to Claude or Cursor...** (on Mac also in the Dinoctor menu) and click **Add to Claude Desktop**, or copy the ready-made line for Claude Code or Cursor.

**By hand** (Claude Desktop `claude_desktop_config.json`, Cursor `mcp.json`):

Mac:
```json
{ "mcpServers": { "dinoctor": { "command": "/Applications/Dinoctor.app/Contents/MacOS/Dinoctor", "args": ["--mcp"] } } }
```

Windows (installer):
```json
{ "mcpServers": { "dinoctor": { "command": "C:\\Users\\YOU\\AppData\\Local\\Programs\\Dinoctor\\Dinoctor.exe", "args": ["--mcp"] } } }
```

Claude Code:
```bash
claude mcp add dinoctor --scope user -- /Applications/Dinoctor.app/Contents/MacOS/Dinoctor --mcp
```

Anything that would spend credits (AI pictures, voices) returns a price and waits for you to confirm, and every change can be undone in the app.
