# Eddie's Superpowers Fork

## Purpose

This repository is Eddie Huang's fork of
[`obra/superpowers`](https://github.com/obra/superpowers). Upstream remains the
source of general framework improvements; this fork keeps a small set of
deliberate workflow preferences.

When syncing upstream, preserve the intentions in this document rather than
blindly choosing either side of a merge conflict. Accept upstream fixes and
structural improvements whenever they do not change these behaviors. If upstream
reorganizes a skill, reapply the invariant in the new structure instead of
preserving stale local wording.

## Provenance

- Upstream remote: `https://github.com/obra/superpowers.git`
- Fork remote: `https://github.com/huangeddie/superpowers.git`

## Current Fork Policies

### 1. Brainstorming is terminal-only

`skills/brainstorming/SKILL.md` must conduct brainstorming in the terminal
conversation. Do not offer or launch the browser visual companion.

### 2. Approved designs proceed directly to planning

Brainstorming still presents design sections and obtains user approval before
writing the specification. After the approved specification is written,
committed, and self-reviewed, proceed directly to `writing-plans` without asking
the user for approval.

### 3. Local-only branch finishing

No remote publication and pull-request creations from branch finishing. Retain
an explicit local merge/keep/discard workflow, including destructive
confirmation and the then-existing cleanup protections.

### 4. The starting workspace is intentional

The checkout, branch, and worktree in which the session starts are the workspace
the user selected.

- Work in that workspace without checking whether another branch or worktree
  would be preferable.
- Do not ask whether to create or switch branches or worktrees.
- Do not invoke `using-git-worktrees` automatically before implementation.
- Use `using-git-worktrees` only after an explicit request for a new isolated
  workspace.
- A direct request for a new worktree authorizes its necessary initial branch
  creation. It does not authorize later switching, merging, deletion, cleanup,
  pull, fetch, push, or pull-request creation.

## Upstream Sync Procedure

1. Fetch upstream only when the maintainer explicitly starts a sync.
2. Review upstream commits and the complete three-dot diff before resolving
   conflicts.
3. Resolve structural changes in favor of useful upstream improvements.
4. Reapply each conflict invariant above to the resulting active skill text.
5. Do not restore files removed for terminal-only operation merely because
   upstream modified them.
6. Review the complete diff with the human maintainer before publishing.
