---
name: jsdss-process-docs
description: >-
  Maintains the JSDSS review-process documents: instructions-all.md as the full
  source of truth, plus role-specific instructions-authors.md,
  instructions-reviewers.md, and instructions-aes.md. Use when editing
  instructions-all.md, splitting the process by role, writing or updating 
  author / reviewer / AE instructions, or when the user mentions wait-for handoffs
  in the JSDSS workflow.
---

# JSDSS process documents

`instructions-all.md` describes the entire process for authors, reviewers, and AEs.
Keep that main process document. Do not replace it with the role files.

Also maintain three role documents:

- `instructions-authors.md` — what authors should do
- `instructions-reviewers.md` — what reviewers should do
- `instructions-aes.md` — what AEs should do

Each of these three documents should include "Wait for so-and-so to do such-and-such."

## When to use

- Creating or regenerating the three role documents
- Editing `instructions-all.md` (update the matching role docs in the same pass)
- The user asks what authors, reviewers, or AEs should do

## Source of truth

1. Read `instructions-all.md` and all three `instructions-*.md` files.
2. Look both ways. `instructions-all.md` is the full process, but a role doc may contain a policy change that should be copied into `instructions-all.md` rather than overwritten.
3. Do not invent policy, GitHub settings, or decision types.
4. Skip internal editorial notes (`ZZZ`, named callouts) in the role docs.
5. If it is unclear who acts, write a Wait for line rather than guessing.

## Role-doc rules

- Second person ("you") for the named role.
- Only that role's actions, plus Wait for lines for everyone else (Editor, AE, reviewers, authors).
- Every handoff is a Wait for line: Wait for [role] to [action]. Do not bold Wait for.
- Link back to [instructions-all.md](instructions-all.md) at the top.
- Keep the same decision vocabulary: **Decline**, **Request Revisions**, **Invite to GitHub Review Process**, **Accept**.
- Keep GitHub names: journal fork in `jsds-sports`, `R0` / `R1` / `final`, Reviewers vs Assignees, only AEs merge.

## After editing instructions-all.md

Update all three `instructions-*.md` files so they stay in sync. Do not leave a role doc describing a step that `instructions-all.md` no longer has.
