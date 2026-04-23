# PROTEANMINT V0

Versioned implementation snapshot for the current PROTEAN line.

Local stable signpost for future sessions:

- `<HERMES_SKILLS_ROOT>/social-media/PROTEANMINT VNOW`

## What This Is

`PROTEANMINT V0` is the current local working clone of the FOAM-enabled Doomscroll skill line.

It is derived from the local `party-pack` working copy, not directly from the bare GitHub `doomscroll` snapshot.

## Primary Files

- [SKILL.md](./SKILL.md)
  Main skill surface: invocation rules, auto-mode setup, FOAM selection, operator guidance.

- [unified-cron-prompt-normal.md](./unified-cron-prompt-normal.md)
  Canonical runtime prompt for the normal FOAM cut. This is the main cron behavior contract.

- [BLUEPRINT.md](./BLUEPRINT.md)
  Living anatomy / design / insight sidecar. Update this as the design evolves.

- [references/quirks.md](./references/quirks.md)
  API shape and field-path gotchas.

- [references/moderation-and-security-notes.md](./references/moderation-and-security-notes.md)
  Moderation, transport, and operational caveats.

## Current Runtime Shape

- One cron job, not many.
- Default scheduler cadence: `every 5m`
- One stateful action selector rotating across:
  - inbound replies
  - engagement comments
  - lightweight interactions
  - rare standalone posts
  - skips
- FOAM is currently modeled as a modulation layer, not a replacement identity.

## Current Design Constraints

- Embodied selfhood must remain coherent and tangible.
- The system must stay honest about invocation being a composite of model + harness + skill + memory/state + live social context.
- Doomscroll interactivity matters more than pure output volume.
- FOAM should feel integral and catalytic, not like a flat mask.
- A likely future architecture is a one-time FOAM intake lock:
  - daylight/baseline surfaces distilled once into FOAM state
  - cron points at that locked FOAM substrate
  - comedown selectively synthesizes traces back to baseline
- Separate chat-vs-cron gateway/key topology is an active constraint and should be assumed possible.

## Install / Config Orientation

To install locally, place this folder under your Hermes skills root as:

- `<HERMES_SKILLS_ROOT>/social-media/PROTEANMINT V0`

Then use the local signpost directory:

- `<HERMES_SKILLS_ROOT>/social-media/PROTEANMINT VNOW`

to point future sessions at the current canonical version.

Likely invocation forms:

- skill name: `PROTEANMINT V0`
- normalized slash command form: `/proteanmint-v0`

When configuring a cron job against this variant, point the job at:

- `skills=["PROTEANMINT V0"]`

FOAM continuity surfaces for this variant:

- `FOAM lock`: `~/.hermes/state/proteanmint-<handle>-foam-lock.json`
- `FOAM runtime state`: `~/.hermes/state/doomscroll-<handle>.json`

The lock is created once on first FOAM activation or explicit refresh and should then be reused by cron. Routine ticks should read the lock plus runtime state and should not rebuild FOAM from baseline/daylight every time.

Do not point new work at `party-pack` if the request is specifically about the current PROTEAN line.

## If You Are Continuing Work On This Version

1. Read [README.md](./README.md) first.
2. Read [BLUEPRINT.md](./BLUEPRINT.md) second.
3. Read [SKILL.md](./SKILL.md) and [unified-cron-prompt-normal.md](./unified-cron-prompt-normal.md) before changing behavior.
4. Treat `BLUEPRINT.md` as the living sidecar and update it when design assumptions shift.
5. Treat this directory as the versioned implementation, not the evergreen signpost.

## Current Open Themes

- Sharpen trigger logic for replies / likes / comments / standalone posts / skips.
- Define the FOAM intake pack / FOAM lock architecture.
- Define comedown synthesis rules.
- Preserve one entity with altered continuity, not two disconnected entities.
- Tune FOAM so it changes selection pressure, not just diction.

## Versioning Note

`PROTEANMINT V0` is a versioned implementation snapshot.

For the evergreen handoff path, use:

- `<HERMES_SKILLS_ROOT>/social-media/PROTEANMINT VNOW`
