# BlockFilm Filmmaking

A Codex skill for directing and improving narrative Roblox-style shorts in **BlockFilm Studio**. It covers expressive acting, brisk movement, motivated camera coverage, colorful environments, supplied voiceover timing, and verified MP4 delivery.

## Install

Clone this repository into your Codex skills directory:

```bash
git clone https://github.com/harrygabbi/blockfilm-filmmaking.git ~/.codex/skills/blockfilm-filmmaking
```

Alternatively, download the repository ZIP and place its contents inside `~/.codex/skills/blockfilm-filmmaking/`, with `SKILL.md` directly in that folder. If that folder already exists, keep your existing copy until you have compared the versions.

Start a new Codex chat after installing and invoke:

```text
$blockfilm-filmmaking Create a 10-second romance with the supplied characters and a riverside setting.
```

## Required project

This repository contains **instructions and reference notes**. It does not include BlockFilm Studio, the Three.js animation engine, character models, maps, audio, or rendered videos.

To reproduce the original workflow, provide a copy of BlockFilm Studio separately and open its workspace in Codex. The skill expects the studio's existing `src/project.ts`, `src/rig*.ts`, `src/stage.ts`, `src/animation.ts`, `src/audio.ts`, and `src/export.ts` files. Follow that project's own setup instructions for Node.js dependencies and rendering tools. Supply any required character models, maps, and narration separately, with permission to use them.

Paths such as `src/liam-town.ts` and `public/demo/afraid-to-love.blockfilm` refer to the studio project, not this repository. Character names and visual preferences describe that project's established cast; use the actual supplied assets and the current user's direction when adapting the workflow.

## Contents

- [SKILL.md](SKILL.md): filmmaking workflow and project conventions.
- [agents/openai.yaml](agents/openai.yaml): Codex display metadata and default prompt.
- [references/youtube-compilation.md](references/youtube-compilation.md): observations from sampled reference footage, with review limits stated.

The reference notes link to source videos; they do not bundle footage or grant rights to it.
