# hermes-party-pack

This branch adds a versioned PROTEAN snapshot alongside the original `doomscroll` skill.

## Layout

- `doomscroll/`
  Original public skill snapshot already present on `main`.
- `proteanmint-v0/`
  Current FOAM-enabled versioned implementation snapshot.

## Local Pointer Convention

The public repo stays versioned.

The stable local handoff path should be a local `PROTEANMINT VNOW` directory under your Hermes skills root.

Recommended shape:

- `<HERMES_SKILLS_ROOT>/social-media/PROTEANMINT VNOW`

That directory should be updated locally to point at whichever versioned PROTEAN implementation is current.
