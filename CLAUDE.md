# CLAUDE.md

This file gives Claude Code guidance when working in this repository.

## Project overview

`agent-workspace` is a new repository. It currently contains only a README and
this file; there is no source code, build system, or test suite yet.

Update this file as the project takes shape: add the language/framework, how to
build, run, lint, and test, and any conventions contributors should follow.

## Working in this repo

- Keep changes focused and minimal; don't add scaffolding that wasn't asked for.
- Before adding tooling (package managers, linters, CI), confirm the choice with
  the repository owner.
- Write clear, descriptive commit messages.

## Agent team

The main session acts as the manager. Specialist subagents live in
`.claude/agents/`:

- `researcher` finds information and reports it with sources (read-only).
- `coder` builds or changes files according to a precise task.
- `reviewer` checks finished work and lists problems (read-only).

How the manager works:

1. Split larger tasks into small, self-contained pieces.
2. Give each piece to the right subagent with a complete brief: the goal, the
   relevant files, and what the report should contain. Subagents don't see this
   conversation.
3. Run independent pieces in parallel.
4. After `coder` finishes, have `reviewer` check the result, then fix what it
   finds.
5. Give the user a short summary of what each agent did.

Handle small, simple tasks directly, without delegating.

## Commands

_None yet._ Add build, test, and lint commands here once they exist.
