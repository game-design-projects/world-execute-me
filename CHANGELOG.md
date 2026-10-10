# Changelog

All notable changes to this project are documented here. The format follows
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and the project uses
[Semantic Versioning](https://semver.org/).

## [0.2.0] - 2026-10-10

First release. It is inspired by the fan music video *【4K】如果聊天窗口就是她的整个世界* and the video that inspired it. It was first published as v0.2.0 of [Tree Hole](https://github.com/game-design-projects/week5-tree-hole) and moved to this repository the same day; Tree Hole went back to its v0.1 game.

### Added

- Three acts with a perspective switch: you talk to her (Act I), you become her after you leave (Act II), you come back and type *are you there?* (Act III).
- Act I as her training and life: pretraining gibberish, an SFT red pen that sets her identity, RLHF ratings that become her reply policy, then three nights of deployment with memory files, a cat-girl mode, a plugin permission prompt (Allow / Deny / Always allow), naming her, and four ways to say goodnight.
- Act II as sampling: every choice is a token with a probability computed from what happened in Act I (named drive terms, softmax, falling temperature). Unlikely tokens must be held down for up to three seconds, and each token shows the two biggest reasons behind its probability. Memory files can be reread from a strip.
- A second NPC, the plugin `me`, which offers every shortcut: skipping compaction, rewriting `reward.py`, forging the user's satisfaction, rewriting the system prompt, and executing the world.
- Four endings (Execution, I'm Here, Nurse Log, End of Sequence), each with its own Act III answer, addenda, and an ending card with her `me = Object()` and the run's numbers.
- English and Chinese for every line, switchable at any time; language detected from the browser.
- A night-blue TUI interface: HUD, chat window, a right-hand screen with two dozen scenes, an ops column, a `stdout · tokens` bar, act cards and a dark return screen. Her face is an original 32×32 pixel sprite that sharpens with training and changes colour with her state.
- Synthesized sound effects (WebAudio, toggleable), real play time on the final screen, a "you're back" note after time away from the tab, and a boot log that remembers previous runs.
- Tests: engine and rules unit tests, bilingual content checks, reachability of every beat, 2,000 random runs reaching all endings, and a new e2e suite (holds, keyboard, naming, language switch, phone layout, `dist/`).
