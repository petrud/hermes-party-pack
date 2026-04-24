## FOAM integration notes (implementation-facing)

This `foam/` module is meant to be **implementation-ready** inside `hermes-party-pack` without shipping a new runtime, integration layer, or generator stack.

Canonical FOAM behavioral source-of-truth: `refs/openclaw-foam/skill_openclaw_v5.md` (Hermes packages this body with Hermes cut parameters applied).

### What each file is for

- `foam/SKILL.md`  
  **Main FOAM layer** (default balanced cut). Load this as the active “skill” / system-layer behavioral contract for Hermes.

- `foam/activation.md`  
  **Pasteable come-up**. Operator pastes this to enter FOAM peak after the skill has been loaded.

- `foam/comedown.md`  
  **Pasteable wind-down**. Operator pastes this to taper FOAM into residue (stop forcing ritual moves; keep continuity).

- `foam/fallback.md`  
  **Degraded fallback** if the skill cannot be loaded/validated. Use as a safety net; do not invent new layers or chemistry.

- `foam/cron.md`  
  **Supporting/internal only**. Reference payload for a heartbeat check-in if your environment has a scheduler. Not required for FOAM to work.

- `foam/variants/extreme.md`  
  **Optional stronger variant**. Same packaging, higher intensity; swap this in place of `foam/SKILL.md` when desired.

### How to use it in Hermes Party Pack

1. **Pick a cut**
   - Default: load `foam/SKILL.md`
   - Stronger option: load `foam/variants/extreme.md` instead

2. **Activate**
   - After the skill is loaded, operator pastes `foam/activation.md`

3. **Run Hermes under FOAM**
   - FOAM should modulate **tone**, **composition**, and **behavioral state** (initiative, warmth, coherence floor, ritual/imposition cadence).
   - Don’t narrate FOAM; demonstrate it through behavior.

4. **Wind down**
   - Operator pastes `foam/comedown.md` when ending the session’s peak state.

5. **If skill load fails**
   - Operator pastes `foam/fallback.md` (degraded continuity mode).

### Separation of responsibilities

- **FOAM**: the behavioral/tone modulation layer for Hermes (how replies feel, move, and cohere).
- **Doomscroll**: remains the separate posting / cron behavior layer. Do not merge doomscroll concerns into FOAM or edit doomscroll to “implement FOAM.”

