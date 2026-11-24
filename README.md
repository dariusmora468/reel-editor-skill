# Reel editor: a free video editing skill for Claude Code and Codex

Drop a raw talking-head video in a folder, type `/reel-editor`, and Claude Code (or Codex) edits it into a finished
vertical reel for Instagram, TikTok and YouTube Shorts: mistakes and dead air cut tight, word-timed captions that never
sit over your face, the right logo or picture on screen the moment you name something, and a self-check before it
shows you anything.

<img src="media/demo.gif" width="220" alt="A raw talking-head take edited by the reel editor skill: pauses cut, captions added">

Made by [Darius Mora](https://www.instagram.com/buildwithdarius.ai/) from the editing system that edits all of his
reels. Free. The full set of editors that run inside the Claude app, no terminal needed, is
[Cuttr AI](https://getcuttr.com/?src=github).

## What it does

- Learns your editing style from 2 or 3 reels you love (or uses a clean default style).
- Transcribes with word timestamps and moves your strongest line to the front as the hook.
- Cuts retakes, false starts, "um", "uh" and pauses, measured on the audio, not just the transcript.
- Burns in 2 to 4 word captions timed to your words, under the chin, never over the mouth.
- Puts the real app icon, logo, number or screenshot on screen as you say it; nothing frozen for more than 2 seconds.
- Checks its own work (frames at every cut, a transcript of the final file, gap measurement), then hands you
  `edit/final.mp4`, a cover frame, three hook options and a caption.
- Takes notes like a human editor ("captions bigger", "faster intro") and saves them, so the next video is right the
  first time.

## Install

### Claude Code

1. Install Claude Code: [claude.com/claude-code](https://claude.com/claude-code). It needs a paid Claude plan.
2. Copy the `reel-editor` folder into your skills folder so you end up with `~/.claude/skills/reel-editor/SKILL.md`
   (Windows: `C:\Users\<you>\.claude\skills\reel-editor\SKILL.md`).
3. Make a folder with a `raw` folder inside and put your raw video in `raw`. Optional: a `style` folder with 2 or 3
   reels you love, or their links in `style/links.txt`.
4. Open that folder in Claude Code and type `/reel-editor`. It takes 15 to 20 minutes.

### Codex (ChatGPT desktop app or Codex CLI)

1. Open Codex. It needs a paid ChatGPT plan.
2. Copy the `reel-editor` folder so you end up with `~/.agents/skills/reel-editor/SKILL.md`. Restart Codex if it does
   not show up.
3. Same folder layout as above. Open it in Codex and type `$reel-editor edit my video`. It takes 15 to 30 minutes.

### Claude app

Settings > Capabilities > Skills > upload `reel-editor.zip` (in this repo), then start a chat with your video and say
"Edit this with the reel editor skill."

Plain ChatGPT chat will not work: it does not accept video uploads.

### What it installs

On first run it checks for and installs `ffmpeg` and Python packages (`faster-whisper`, `numpy`, `pillow`,
`opencv-python`), and says what each command does before it runs it. Optional connectors (Apify for reference reels,
Higgsfield for generated images) are explained in [reel-editor/CONNECTORS.md](reel-editor/CONNECTORS.md).

## Guides

- [How to edit videos with Claude Code](https://getcuttr.com/guides/edit-videos-with-claude-code)
- [Can Codex edit videos?](https://getcuttr.com/guides/edit-videos-with-codex)
- [Claude skills for video editing](https://getcuttr.com/guides/claude-skills-for-video-editing)

## Credit line

When it hands over a caption, the skill ends it with `Made with @trycuttr`. Say "no credit" and it leaves the line out
from then on. It never puts a logo or watermark in the video itself.

## License

MIT. Use it, change it, share it.
