# Nushell (AI-patched fork)

> [!NOTE]
> **This is a personal fork patched using AI** to fit personal needs, modal editing preferences modeled after the [Helix editor](https://helix-editor.com/), and per-instance session isolation for SQLite history.
>
> Official upstream project: **[nushell/nushell](https://github.com/nushell/nushell)**.

---

## Why this fork exists

This repository contains modifications tailored with AI assistance to address two specific workflows:

1. **Session-Isolated SQLite History**:
   - In upstream Nushell with SQLite history enabled, browsing command history in interactive sessions shares commands across all concurrently open shell instances, leading to unexpected history navigation.
   - This fork generates a unique `UUIDv7` session ID when each Nushell instance starts and isolates interactive command history lookups so that pressing `Up`/`Down` or searching history only recalls commands executed within that specific shell session.

2. **Native Helix Modal Editing & Custom Keybindings**:
   - Integrated with our patched [`reedline`](https://github.com/ken-morel/reedline) engine supporting full Helix modal editing (`edit_mode: helix`).
   - Supports selection-first editing (`w`, `b`, `e`, `W`, `B`, `E`), gotos (`gh`, `gl`, `gs`, `ge`, `gg`), selection extension (`H`, `L`), line and buffer selection (`x`, `V`, `%`), selection collapse to single cursor (`;`), cursor/anchor swapping (`Alt-;`), line deletion (`Ctrl-d`), inner text object selection (`SelectTextObject`), and seamless insert-mode navigation (`Alt-h`/`j`/`k`/`l`).

---

For standard Nushell documentation, book, and cookbooks, please refer to the official [nushell/nushell](https://github.com/nushell/nushell) project.
