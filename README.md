# Claude Code Animations — Lemo-Opuscar Prompt

> The exact prompt used in the YouTube video **[Claude Code Can Now Create INSANE Animations (2026)](https://youtu.be/uVHWzzNR-54)**.

[![Watch the video](https://img.youtube.com/vi/uVHWzzNR-54/maxresdefault.jpg)](https://youtu.be/uVHWzzNR-54)

Claude Code can create motion graphics and animated videos from a single prompt. You don't need After Effects or manual keyframing. This repo has the creative brief I used with **[Lemo-Opuscar](https://github.com/lemomo-ai/lemo-opuscar)**, a free, open-source Claude Code plugin, to make a ~40-second cinematic explainer about **how AI agents work**.

👉 **The prompt is here: [`lemo-opuscar-prompt.md`](lemo-opuscar-prompt.md)**

---

## What is Lemo-Opuscar?

Lemo-Opuscar is an open-source plugin that adds AI-assisted video production to Claude Code. Claude:

1. **Plans** the scenes
2. **Writes** the animation code
3. **Renders** the final video, with sound effects from the plugin's built-in library

It comes with several visual styles and directing instructions. It works well for motion graphics, animated explainers, product demos, and educational videos.

### Is this AI video generation?

**No.** Tools like Sora or Veo generate video frames from a text prompt. Here, Claude Code writes the animation itself, so you get an **editable, repeatable animation project** instead of a flat MP4. You can change timing, text, layout, or transitions with a follow-up prompt.

---

## Requirements

| Tool | Link |
| --- | --- |
| Claude Code | [claude.com/claude-code](https://claude.com/claude-code) |
| Node.js | [nodejs.org](https://nodejs.org) |
| FFmpeg | [ffmpeg.org](https://ffmpeg.org) |
| Python or uv | [docs.astral.sh/uv](https://docs.astral.sh/uv/) |

## Install the plugin

**Option A: Claude Code UI**

1. Open Claude Code in the folder where you want to make the video.
2. Click **+** → **Plugins** → **Manage plugins**.
3. Click **Add** (top right) → **Add marketplace** → **From repository**.
4. Paste `https://github.com/lemomo-ai/lemo-opuscar`, press Enter, then click **Sync**.
5. Find the plugin, click the arrow, and choose **Install for this project**.
6. Reload plugins.

**Option B: Terminal**

```bash
claude plugin marketplace add lemomo-ai/lemo-opuscar
```

```bash
claude plugin install lemo-opuscar@lemolab
```

## Use the prompt

1. Start the plugin inside Claude Code:

   ```text
   /lemo-opuscar:lemo-opuscar
   ```

2. Copy everything in [`lemo-opuscar-prompt.md`](lemo-opuscar-prompt.md) and paste it in.
3. Claude reviews the plugin's docs, writes a storyboard, and makes **preview frames**. Then it **stops and waits for your approval**.
4. Approve the direction (or ask for changes), and Claude builds and renders the full video.
5. Keep refining it in plain English, for example *"slow down scene 3"* or *"make the final title bigger"*.

---

## What's in the prompt

You *could* just type "create an animation explaining AI agents", but a detailed creative brief gets much better results. This one defines:

- **The video:** 40–45 s, 16:9, 1920×1080, 30 FPS, H.264 MP4
- **Creative direction:** dark premium tech look, typography, and a meaningful color system (blue = reasoning, violet = planning, cyan = tools, green = success)
- **A six-scene storyboard:**

  | # | Scene | Time | On-screen text |
  | --- | --- | --- | --- |
  | 1 | The user request | 0:00–0:06 | ONE REQUEST. |
  | 2 | Understanding & planning | 0:06–0:13 | REASON → PLAN |
  | 3 | Tool selection | 0:13–0:20 | SELECT TOOLS |
  | 4 | Executing the workflow | 0:20–0:30 | EXECUTE → OBSERVE → CONTINUE |
  | 5 | The final result | 0:30–0:38 | TASK COMPLETED |
  | 6 | The big picture | 0:38–0:45 | AI AGENTS — Reason. Act. Deliver. |

- **Shared-element transitions,** so the same UI elements move and transform between scenes and the video feels like one continuous shot, not a slideshow
- **Technical requirements and project structure,** so the output is an organized, editable project with docs and a reproducible render command
- **A production workflow** with a **preview-and-approve checkpoint** and a QA pass on the rendered video

### Tips for writing your own brief

- **Describe how scenes connect,** not just what's in them. That's what makes the video feel cinematic.
- **Give color and motion a meaning,** so every choice communicates something.
- **Ask for previews first.** It's much cheaper to fix the direction before the full render.
- **Tell Claude not to invent plugin features,** and to use the plugin's documented styles and commands.
- **Ask for a QA pass** on the rendered frames, not just the source code.

---

## Video chapters

| Time | Chapter |
| --- | --- |
| [00:00](https://youtu.be/uVHWzzNR-54?t=0) | Claude Code Can Create Animations? |
| [00:37](https://youtu.be/uVHWzzNR-54?t=37) | What Is Lemo-Opuscar? |
| [01:33](https://youtu.be/uVHWzzNR-54?t=93) | The Experiment: Animated AI Agents Explainer |
| [02:00](https://youtu.be/uVHWzzNR-54?t=120) | Installing the Lemo-Opuscar Plugin |
| [03:11](https://youtu.be/uVHWzzNR-54?t=191) | Launching the Plugin |
| [03:38](https://youtu.be/uVHWzzNR-54?t=218) | Writing the Creative Brief |
| [04:32](https://youtu.be/uVHWzzNR-54?t=272) | How Claude Builds the Animation |
| [05:01](https://youtu.be/uVHWzzNR-54?t=301) | Final Animation Result |
| [05:51](https://youtu.be/uVHWzzNR-54?t=351) | Why This Changes Motion Graphics Workflows |
| [06:26](https://youtu.be/uVHWzzNR-54?t=386) | Resources & Final Thoughts |

## FAQ

**Can Claude Code make animations?**
Yes. With the Lemo-Opuscar plugin, Claude Code plans scenes, writes animation code, and renders a finished video with sound effects.

**Do I need After Effects?**
No. The animation is generated and rendered from code using Claude Code and open-source tools.

**Is Lemo-Opuscar free?**
Yes. It's an open-source plugin [on GitHub](https://github.com/lemomo-ai/lemo-opuscar).

**Can I edit the video after it's generated?**
Yes. It's a real animation project, so you can keep refining it with natural-language prompts.

## Resources

- 🎬 Video: [Claude Code Can Now Create INSANE Animations (2026)](https://youtu.be/uVHWzzNR-54)
- 🧩 Lemo-Opuscar: [github.com/lemomo-ai/lemo-opuscar](https://github.com/lemomo-ai/lemo-opuscar)
- 📝 Prompt: [`lemo-opuscar-prompt.md`](lemo-opuscar-prompt.md)
- 💼 Work with me: [vivekshetye.com](https://vivekshetye.com)

---

If this helped, ⭐ star the repo, like the video, and subscribe for more on Claude Code, AI agents, and automation workflows.

*This repo isn't affiliated with Anthropic or the Lemo-Opuscar maintainers. Feel free to use and adapt the prompt for your own videos.*
