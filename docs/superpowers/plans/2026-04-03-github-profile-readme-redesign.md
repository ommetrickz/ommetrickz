# GitHub Profile README Redesign Implementation Plan

> **For agentic workers:** REQUIRED: Use superpowers:subagent-driven-development (if subagents available) or superpowers:executing-plans to implement this plan. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Update the profile README so it highlights only published work, separates seeding ideas, fixes toolkit labels/icons, and removes the local inspiration clone from the workspace.

**Architecture:** Keep the existing centered README structure and SVG assets, but replace the mixed projects table with a published plus seeding split and simplify the toolkit block to stable badge groups. Treat the untracked `awesome-github-profiles/` directory as local research debris and delete it after confirming the absolute path is inside the repo workspace.

**Tech Stack:** Markdown, HTML-in-Markdown, Git, PowerShell

---

## Chunk 1: README Rewrite

### Task 1: Restructure the toolkit and projects sections

**Files:**
- Modify: `README.md`
- Reference: `docs/superpowers/specs/2026-04-03-github-profile-readme-redesign.md`

- [ ] **Step 1: Rewrite the toolkit block**

Replace the current `skillicons.dev` strip and software rows so the section shows:

- `Motion & VFX`: After Effects, Premiere Pro, Nuke, Blender
- `Design`: Photoshop, Illustrator
- `IDE & Vibe Code`: Claude, Ollama

Remove `Cinema 4D` and unsupported icon entries.

- [ ] **Step 2: Rewrite the projects block**

Replace the four-card mixed project table with:

- `Published`: Ommetrickz Portfolio, RadarMed, AE Scripts
- `Seeding`: Zero Sleep Studio, Career Agent, Launch India

Published entries must have live links. Seeding entries must have no links.

- [ ] **Step 3: Keep the rest of the README stable**

Preserve:

- top navigation
- `About`
- `Connect`
- `banner.svg`
- `typing.svg`

### Task 2: Verify markdown structure

**Files:**
- Verify: `README.md`

- [ ] **Step 1: Re-read the final README**

Check that:

- anchors still match nav targets
- headings remain centered consistently
- links for published projects are correct
- seeding items are plain text only

- [ ] **Step 2: Check git diff**

Run: `git diff -- README.md`
Expected: Only approved README restructuring changes

## Chunk 2: Workspace Cleanup

### Task 3: Remove the cloned inspiration repo

**Files:**
- Delete: `awesome-github-profiles/`

- [ ] **Step 1: Resolve the absolute path**

Run: `Resolve-Path .\awesome-github-profiles`
Expected: Path resolves under `c:\Users\Fitel\Documents\git-profile\Git-profile`

- [ ] **Step 2: Delete the directory**

Run: `Remove-Item -LiteralPath .\awesome-github-profiles -Recurse -Force`
Expected: Directory removed locally

- [ ] **Step 3: Verify repo state**

Run: `git status --short --branch`
Expected: No `awesome-github-profiles/` entry remains

## Chunk 3: Final Verification

### Task 4: Fresh verification before reporting

**Files:**
- Verify: `README.md`

- [ ] **Step 1: Show final diff summary**

Run: `git diff --stat`
Expected: `README.md` changed, plan/spec files retained, no cloned repo directory

- [ ] **Step 2: Confirm exact remote-safe state**

Run: `git status --short --branch`
Expected: Clean summary except intended local modifications
