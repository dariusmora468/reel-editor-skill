# Reel editor skill: how to install it

Free from @buildwithdarius.ai. One file, SKILL.md, turns Claude Code or Codex into your video editor.

## Claude Code (the best way)

1. Install Claude Code: claude.com/claude-code (the desktop app is the easiest).
2. Put this folder, `reel-editor`, inside your skills folder:
   - Mac / Linux: `~/.claude/skills/reel-editor/SKILL.md`
   - Windows: `C:\Users\<you>\.claude\skills\reel-editor\SKILL.md`
   (Or, for one project only: `<your video folder>/.claude/skills/reel-editor/SKILL.md`.)
3. Make a folder for your video with a `raw` folder inside, and drop your raw video in it.
   Optional: a `style` folder with 2 or 3 reels whose editing you love, or their links in `style/links.txt`.
4. Open that folder in Claude Code and type: `/reel-editor`
5. Wait 15 to 20 minutes depending on the model. Want changes? Just tell it ("captions bigger", "faster intro").
   It saves every note, so the next video comes out right the first time.

## Codex (in the ChatGPT desktop app)

1. Open the ChatGPT desktop app and switch to Codex (included on every ChatGPT plan). The Codex CLI works too.
2. Put this folder, `reel-editor`, inside your skills folder:
   - Mac / Linux: `~/.agents/skills/reel-editor/SKILL.md`
   - Windows: `C:\Users\<you>\.agents\skills\reel-editor\SKILL.md`
   Restart Codex if the skill does not show up.
3. Make a folder for your video with a `raw` folder inside, and drop your raw video in it.
   Optional: a `style` folder with 2 or 3 reels whose editing you love, or their links in `style/links.txt`.
4. Open that folder in Codex and type: `$reel-editor edit my video`
5. Wait 15 to 30 minutes depending on the model. Want changes? Just tell it.

Plain ChatGPT chat will not work: it does not accept video uploads. Use Codex.

## Claude app (claude.ai)

Settings > Capabilities > Skills > upload `reel-editor.zip`. Then start a chat with your video and say
"Edit this with the reel editor skill."

## The connectors (Apify + Higgsfield)

Optional. Apify grabs reference reels Instagram blocks; Higgsfield makes any image or clip the edit needs.
Setup for Claude Code, Codex and the Claude app is in `CONNECTORS.md`. Quickest: paste this into Claude Code or Codex:
"Connect the Apify MCP server at https://mcp.apify.com and the Higgsfield MCP server at
https://mcp.higgsfield.ai/mcp, then walk me through signing in to both."

## Want the full version?

Cuttr AI Video Editing is the full set of editors that run inside Claude: drop in a raw video, say what you want,
get back a finished reel. https://getcuttr.com/?src=skill
