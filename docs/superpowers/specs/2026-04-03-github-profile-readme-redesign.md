# GitHub Profile README Redesign

Date: 2026-04-03
Repo: `c:\Users\Fitel\Documents\git-profile\Git-profile`
Primary file: `README.md`

## Goal

Update the GitHub profile README so it reflects current published work instead of mixing live projects with unpublished ideas.

## Approved Direction

Keep the existing centered visual language and preserve the current top-level sections:

- About
- Toolkit
- Projects
- Connect

Do not redesign `banner.svg` or `typing.svg`.

## Project Section Redesign

Replace the current mixed project grid with two distinct groups:

### Published

Show only work that is already public and reachable by link.

Approved published entries:

1. Ommetrickz Portfolio
   - Link: `https://ommetrickz.vercel.app/`
   - Positioning: cinematic motion design portfolio
2. RadarMed
   - Link: `https://radarmed.vercel.app/`
   - Positioning: public-data blood search product
3. AE Scripts
   - Link: `https://github.com/ommetricksz/AFter_Effect_SC`
   - Positioning: After Effects ExtendScript toolkit

### Seeding

Keep a smaller, quieter section below published work.

Rules:

- Names only
- No links
- No fake launch status
- No presentation that implies the work is already live

Approved seeding entries:

- Zero Sleep Studio
- Career Agent
- Launch India

Framing rules:

- Zero Sleep Studio is a studio in formation, not a launched product.
- Career Agent and Launch India are ideas in development.

## Toolkit Section Redesign

Simplify the current toolkit block so it does not rely on broken or unsupported icon combinations.

Remove:

- Cinema 4D
- unsupported or broken top-strip icon entries

Use three grouped headings:

### Motion and VFX

- After Effects
- Premiere Pro
- Nuke
- Blender

### Design

- Photoshop
- Illustrator

### IDE and Vibe Code

- Claude
- Ollama

## Content Rules

- Published work must always have a real destination link.
- Seeding work must not have a link.
- The README should stop using mixed status labels like "building" or "launching" inside the main project cards.
- Published work should feel production-ready.
- Seeding work should feel intentionally separate.

## External Inspiration Repo Decision

The repository `EddieHubCommunity/awesome-github-profiles` was reviewed before use.

Result:

- Safe enough to use for inspiration and static README ideas
- Not approved for direct workflow reuse

Reason:

- No malware or obfuscated payloads were found in the cloned repo
- The repo contains third-party GitHub Actions pinned to mutable refs, so those workflow files should not be copied as-is

## Verification Plan

After editing `README.md`, verify:

1. Section anchors still match the nav links.
2. The published section contains exactly three linked items.
3. The seeding section contains exactly three unlinked items.
4. Toolkit labels and badges render without obviously broken entries.
5. Markdown structure remains valid and readable in GitHub rendering.

## Non-Goals

- No changes to `banner.svg`
- No changes to `typing.svg`
- No adoption of files, workflows, or automation from `awesome-github-profiles`
- No broader brand rewrite outside the approved README sections
