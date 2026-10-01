# Awesome Spec-Driven Development [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of frameworks, tools, and resources for **Spec-Driven Development (SDD)**: writing a durable specification *before* code, and using it (not the chat history) as the source of truth that AI coding agents build against.

Spec-Driven Development emerged in 2025–2026 as the answer to "vibe coding": instead of improvising code from a single prompt, you describe *what* to build, plan *how*, break it into tasks, and only then let the agent implement, with the spec persisting across sessions, team members, and agent runs.

> **A note on scope.** "SDD" is a fuzzy, still-forming category. The tools below sit at *different layers*: some treat a written spec as the source of truth (core SDD); others are adjacent layers (context engineering, skills/methodology enforcement, orchestration) that are commonly grouped with SDD but are not spec formats themselves. Sections are split accordingly so the distinction stays honest.

⭐ Star counts checked on **2026-10-01**. They move fast, so always check the repo.

## Contents

- [Core SDD Frameworks](#core-sdd-frameworks)
- [Adjacent Layers (grouped with SDD, but not spec formats)](#adjacent-layers-grouped-with-sdd-but-not-spec-formats)
- [Articles, Comparisons & Research](#articles-comparisons--research)
- [Contributing](#contributing)

## Core SDD Frameworks

Tools where a written specification is the central, durable artifact that feeds plans, tasks, and implementation.

- **[GitHub Spec Kit](https://github.com/github/spec-kit)** — ~139k ⭐. GitHub's official, agent-agnostic SDD toolkit. Ships the `specify` CLI, templates, a project-wide `constitution.md`, and agent skills / slash commands (`/speckit-constitution`, `/speckit-specify`, `/speckit-plan`, `/speckit-tasks`, `/speckit-implement`, `/speckit-converge`; exact syntax varies by agent). Optional extensions add bug fixing and idea assessment. Works across 30+ agents (Copilot, Claude Code, Gemini CLI, Cursor, Codex, Windsurf…). Best all-round choice for greenfield, single-repo work.
- **[OpenSpec](https://github.com/Fission-AI/OpenSpec)** — ~66.9k ⭐. Lightweight, vendor-neutral spec format with a fluid `explore → propose → apply → archive` change lifecycle (`/opsx:*`). Writes *delta* specs (only what changes) that archive into a single source-of-truth doc. Node/TypeScript CLI, `openspec init`; supports 30+ tools. Strong on brownfield.
- **[Spec Kitty](https://github.com/Priivacy-ai/spec-kitty)** — ~1.6k ⭐. SDD workflow (`spec → plan → tasks → next → review → accept → merge`) with a Kanban dashboard, git-worktree isolation, review gates, and auto-merge; keeps specs, plans, work packages, and merge state in Git as the source of truth. Inspired by the Spec Kit idea, aimed at teams running a "governed software factory."

## Adjacent Layers (grouped with SDD, but not spec formats)

Frequently listed alongside SDD and pair well with it, but they operate at a different layer (context engineering, skills/methodology enforcement, or orchestration) rather than defining a spec as the source of truth.

- **[Superpowers](https://github.com/obra/superpowers)** — ~293k ⭐. By Jesse Vincent / Prime Radiant. A *skills* and methodology-enforcement layer: auto-triggering skills shape how the agent brainstorms → plans → implements (TDD) → reviews, with subagent-driven development and code review between tasks. Explicitly *not* a spec format. Distributed through the official Claude plugin marketplace and many other harnesses (Codex, Cursor, Gemini CLI, Copilot CLI, OpenCode…).
- **[GSD Core (Open GSD)](https://github.com/open-gsd/gsd-core)** — ~10k ⭐. Context-engineering and spec-driven framework: a `discuss → plan → execute → verify → ship` phase loop that runs heavy work in fresh-context subagents to beat "context rot." Install: `npx @opengsd/gsd-core@latest`. This is the active successor of **Get Shit Done**; the original [gsd-build/get-shit-done](https://github.com/gsd-build/get-shit-done) (~64.4k ⭐) was **archived on 2026-06-26** and points here.

## Articles, Comparisons & Research

> All links checked on 2026-10-01.

- **[Spec-driven development with AI: get started with a new open source toolkit](https://github.blog/ai-and-ml/generative-ai/spec-driven-development-with-ai-get-started-with-a-new-open-source-toolkit/)** — GitHub Blog's Spec Kit launch post and the case for SDD.
- **[Diving Into Spec-Driven Development With GitHub Spec Kit](https://developer.microsoft.com/blog/spec-driven-development-spec-kit/)** — Microsoft for Developers walkthrough.
- **[spec-compare](https://github.com/cameronsjo/spec-compare)** — ~66 ⭐. Comparison of six SDD tools with decision frameworks and scoring matrices.

## Contributing

Contributions welcome. Add a tool only if it fits one of the layers above, include a one-line description, and say which layer it belongs to.
