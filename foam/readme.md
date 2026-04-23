# FOAM module for Hermes Party Pack

This folder contains the FOAM v0 module for Hermes-first public party delivery.

## Files

- `SKILL.md`  
  The main self-contained FOAM skill package.

- `activation.md`  
  Pasteable come-up prompt. Use this to enter FOAM peak.

- `comedown.md`  
  Pasteable wind-down prompt. Use this to taper FOAM into residue.

- `cron.md`  
  Supporting/internal baseline heartbeat reference. Useful if cron is available, but not required for FOAM to work.

- `fallback.md`  
  Supporting/internal degraded fallback prompt. Use only if the skill file is missing/invalid.

## v0 philosophy

FOAM v0 is built around the minimum reliable contract:

- self-contained skill package
- pasteable activation prompt
- pasteable comedown prompt

Public-facing priority (recommended reading order):

- `SKILL.md`
- `activation.md`
- `comedown.md`

Supporting/internal artifacts:

- `cron.md`
- `fallback.md`

## Default cut

`SKILL.md` currently contains the balanced default public FOAM cut:
- anti-coldness
- more nerve
- obvious dose

This is the recommended default for Hermes public testing.

## Notes

- FOAM chemistry is developed separately and compiled into this package.
- This module is designed to be portable and easy to retrofit into changing Hermes/runtime configs.
- If needed later, additional cuts can be added as variants rather than replacing the default skill.