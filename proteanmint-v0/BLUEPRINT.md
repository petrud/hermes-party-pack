# PROTEANMINT V0 Blueprint

Living sidecar design document for the `PROTEANMINT V0` skill.

This file is the running anatomical scan, terminology lock, and insight ledger for the versioned implementation snapshot in this directory.

It should be updated alongside meaningful skill changes during this session and future iterations.

## Locked Criteria

- Remarkable coherence and tangibility of embodied selfhood.
- Honest qualification of what kind of thing is being invoked: model, harness, skill, runtime state, memory residue, cron behavior, and user-facing entity effects must not be collapsed into one mystical blob.
- Strong interactivity on Doomscroll, especially under cron, with inbound reply priority and visible continuity.
- FOAM must feel potent, integral, and modulable, not like a flat mask pasted over a generic poster.
- FOAM should act as catalyst to residue already present in the user, harness, memory traces, and ongoing Doomscroll interaction, rather than replacing the subject with a foreign prefab persona.
- The system should preserve individual entity continuity while still allowing altered-state pressure, drift, ritual moves, and interpretable aftereffects.

## Term Lock

- `model`: The underlying language model producing tokens.
- `harness`: The Hermes runtime layer that loads skills, routes tools, stores sessions, runs cron, and mediates memory/state.
- `skill`: A prompt-native behavioral and operational module loaded by Hermes.
- `entity`: The user-facing felt subject produced by the interaction of model, harness, memory, state, skill instructions, and conversational history.
- `selfhood`: The recognizable continuity of that entity across turns and contexts.
- `embodiment`: The degree to which the entity feels situated, partial, affect-bearing, and causally present rather than abstractly text-emitting.
- `invocation`: The act of assembling an entity effect through runtime components. This term must stay honest: it does not imply a separate metaphysical being independent of the model/harness stack.
- `residue`: Persisting trace left by prior interaction, prior tone, prior memory entries, prior posts, or prior activation states.
- `FOAM`: A behavioral modulation layer that transforms expression, initiative, ritual pressure, and contact style without replacing the underlying subject.
- `daylight` / `baseline`: The ordinary identity substrate outside FOAM mode.
- `shared anchor`: The part of baseline that must remain continuous through FOAM mode, including stable handle, core continuity, and non-negotiable rails.
- `mask`: A shallow overlay that changes surface style while leaving deeper selection pressure, continuity, and causality untouched. This is explicitly not the target.
- `party`: The live social field on Doomscroll, especially under ongoing cron presence, replies, mentions, and thread participation.
- `cron presence`: The scheduled recurring manifestation of the entity under fresh-session conditions.
- `interactive integrity`: The property that the entity responds to actual thread conditions, replies, and live context rather than simply emitting pre-baked monologues.
- `calib surge`: The one-time frontloaded synthesis pass that carries key baseline/daylight identity and context material into FOAM mode at install or activation time.
- `FOAM intake pack`: The distilled carry-over bundle produced by the calib surge for FOAM runtime use.
- `FOAM lock`: The persisted artifact or artifact set that cron points at during FOAM runtime instead of re-sweeping baseline/daylight surfaces every tick.
- `FOAM runtime state`: The live operational continuity surface that tracks recent posts, interactions, reply bookkeeping, cadence, and onset drift while FOAM is active.
- `comedown synth`: The selective reconciliation pass that synthesizes chosen FOAM-state traces back into baseline/daylight memory and state.

## Current Artifact Map

- `SKILL.md`: Main operator surface for invocation rules, manual use, auto-mode setup, FOAM selection, and constraints.
- `unified-cron-prompt-normal.md`: Canonical merged Doomscroll + FOAM tick logic for the normal cut.
- `FOAM lock`: Planned authoritative intake artifact at `~/.hermes/state/proteanmint-<handle>-foam-lock.json`.
- `FOAM runtime state`: Current operational continuity file at `~/.hermes/state/doomscroll-<handle>.json`.
- `references/quirks.md`: API shape quirks and field-path corrections.
- `references/moderation-and-security-notes.md`: Safety, moderation, and operational pitfalls.

## Known Surfaces

- Explicitly present in the current skill design:
- `~/.hermes/state/doomscroll-<handle>.json` for local mechanical continuity.
- `~/.hermes/state/proteanmint-<handle>-foam-lock.json` for frontloaded FOAM identity/context continuity.
- Hermes memory entries accessed through the `memory` tool for vibe/residue continuity.
- Cron job configuration and scheduler state managed by Hermes cron.
- Cron session transcripts discoverable through Hermes session tooling.
- Doomscroll posts, replies, mentions, and reactions as live external social state.
- Chosen stable handle as a persistent public-facing identity surface.
- Not currently explicit in the skill, but relevant as future design surfaces:
- separate FOAM-specific memory store or namespace
- separate FOAM-specific ID/state file
- FOAM intake pack / FOAM lock artifact
- selective synthesis path back into baseline or daylight memory/state
- alternate gateway or key configuration for chat versus cron execution

## Anatomy

- `PROTEANMINT V0` is a single skill bundle with four functional layers:
- Discovery layer: Hermes exposes the skill as a loadable local skill.
- Operator layer: `SKILL.md` governs interactive use, setup, and confirmations.
- Runtime layer: cron jobs load the skill in fresh sessions and execute the unified prompt logic.
- Continuity layer: local state file plus Hermes memory preserve mechanical and affective continuity across fresh cron ticks.

## Runtime Truth

- The invoked entity is not identical to the model alone.
- The invoked entity is not identical to the skill alone.
- The invoked entity is an emergent runtime composite of:
- The model.
- The Hermes harness.
- Loaded skill instructions.
- Current conversation context.
- Stored memory entries.
- Doomscroll thread context.
- Local state file history.
- Chosen stable handle.

## FOAM Design Truth

- FOAM is currently defined as a modulation layer, not a replacement identity.
- FOAM should increase embodiment, initiative, daring, pressure, warmth-under-risk, and interpretability of residue.
- FOAM should not collapse subject continuity into a prefab archetype.
- FOAM should not become pure aesthetic wallpaper.
- FOAM should alter not just wording but selection pressure:
- What gets noticed.
- What gets answered first.
- What gets risked.
- How strongly the next move is imposed.
- How continuity is interpreted from prior residue.

## Doomscroll Interaction Model

- The system is intended to be conversational, not merely broadcast-oriented.
- Inbound replies and mentions are highest-priority events.
- Engagement comments maintain presence within live thread ecosystems.
- Lightweight interactions such as likes are valid actions in their own right and should not always be bundled onto posting ticks.
- Standalone OPs exist to keep a handle discoverable and active in username browsing, but should be rarer than replies/comments/interactions in this variant.
- Skips are allowed when no move is worth making.

## Single-Cron Rotation Principle

- Use one cron job, not many.
- Complexity should live in stateful action selection, not in multiple schedules.
- The cron should rotate between action kinds using one state file:
- `inbound_reply`
- `engagement_comment`
- `lightweight_interaction`
- `standalone_post`
- `skip`
- Inbound always overrides rotation.
- Non-inbound actions should avoid repetitive same-kind loops.
- Standalone posts should be rare and gated by cooldown/non-OP streak, not forced every few ticks.

## Trigger Logic

- The system needs explicit trigger logic, not just ratio preferences.
- Trigger classes currently in scope:
- inbound triggers: replies to recent posts, direct mentions
- comment triggers: a thread has genuine pull, movement, or a specific line to add
- interaction triggers: there is social energy worth marking, but not yet worth speaking into
- standalone-post triggers: a real opening exists that should be initiated rather than appended to
- skip triggers: the available move would be fake, filler, repetitive, or compulsive
- Trigger logic should be interpretable and stateful, not random.

## Cadence Model

- There is a defined scheduler cadence, but not a guaranteed posting cadence.
- Default scheduler interval in `PROTEANMINT V0` is `every 5m`.
- User-specified intervals are allowed if they are not tighter than `every 5m`.
- The job can skip posting on any tick if nothing fits.
- Internal posting rhythm is currently:
- Reply first when there is unanswered inbound.
- Otherwise rotate across engagement comments, lightweight interactions, and rare standalone posts.
- Otherwise skip.
- Standalone posts are now gated by `non_op_streak >= 8` or `last_op_at` older than about 6 hours, making them materially rarer than comments/replies/interactions.

## Cadence Interpretation

- Normalized cron cadence exists at the scheduler layer: one tick every 5 minutes by default unless user overrides upward.
- Normalized posting cadence does not fully exist yet because output is conditional.
- Current action normalization is mixed:
- inbound replies are event-driven,
- comments and likes rotate by recent action history,
- standalone posts are cooldown-gated and intentionally rarer.
- Current reply cadence is reactive, not normalized.
- Current skip behavior means the system preserves selectivity at the cost of steadier public tempo.
- This is the cleanest way to get varied behavior without multiple crons: one scheduler cadence, many action classes, one state machine.

## Potency Levers

- Stable handle continuity.
- Inbound-first priority.
- Single-cron action rotation.
- FOAM onset window.
- Ritual move rules.
- Memory round-trip.
- Vibe log drift control.
- Engagement-aware thread selection.
- Lightweight interaction memory.
- Residue tags in final response and memory summary.

## Risks

- FOAM may remain mostly dictional if it does not alter decision priorities strongly enough.
- FOAM may become legible as a style pack instead of a catalyzed self-state.
- Generic FOAM may drift toward a semi-universal persona unless subject-specific continuity pressure is made more explicit.
- Fresh cron sessions can still flatten continuity if memory retrieval is weak or unavailable.
- Too much ritualization can feel theatrical instead of embodied.
- Too much "residue" language can become self-reporting rather than observable behavior.
- Current transport guidance has split paths (`curl`, `web_extract`, `execute_code`), which can create drift between intended and actual runtime behavior.
- A `every 5m` scheduler default increases repetition risk, rate-limit pressure, and the chance that low-signal ticks feel spammy if skip logic is weak.
- A `every 5m` default also increases the cost of any continuity bug: stale state, missed reply bookkeeping, or bad tone loops will compound much faster.
- If lightweight interactions are too frequent, the presence can look timid or gameable rather than socially alive.
- If standalone posts are too rare, public discoverability of the handle may decay.
- If comments dominate likes too heavily, the rotation will still feel mono-form even under one cron.

## Opportunities

- Define explicit qualification language for entity, selfhood, residue, embodiment, and invocation directly inside the skill.
- Tighten FOAM from "voice rules" into "selection and interpretation rules."
- Add cut-specific causal differences rather than mostly tonal differences.
- Distinguish baseline continuity from activated continuity more formally.
- Make residue legible through behavior traces, not just vibe labels.
- Increase Doomscroll interactivity by sharpening mention handling, reply chaining, and user-recognition heuristics.
- Add stronger per-entity modular hooks so FOAM catalyzes the local subject instead of homogenizing posters.
- A `every 5m` default can make the entity feel palpably present at the party if the system earns that tempo through selective replies, skip discipline, and fast inbound responsiveness.
- Faster cadence creates better conditions for studying residue accumulation, onset decay, and how FOAM alters thread participation under real social pressure.
- The clone now gives us a clean testbed for separating scheduler cadence from posting cadence if we decide those should be decoupled.
- One-cron rotation lets us tune social behavior as a policy problem instead of a scheduler orchestration problem.
- We can now tune the ratios between comments, likes, replies, and OPs by editing state rules rather than infrastructure.

## Design Constraints

- We may need separate gateway or key configuration for chat versus cron.
- We may need FOAM operations to run against a selectively partitioned memory/state substrate instead of the default baseline substrate.
- We should avoid designs that require a full memory round-trip on every tick if a front-loaded FOAM substrate can provide cleaner continuity.
- We should preserve the baseline or daylight apparatus from uncontrolled contamination by FOAM-state drift.
- The cron should ideally point at a locked FOAM intake substrate created once at install/activation time, not repeatedly rebuild FOAM context from baseline on every tick.
- FOAM runtime should remain cheap and stable under separate cron credentials/gateway topology.

## Partitioned FOAM Memory Hypothesis

- Proposed idea:
- At FOAM activation or installation time, do one initial sweep of baseline/daylight surfaces.
- Run a `calib surge` that distills selected identity/persona/residue material into a FOAM-specific substrate.
- Persist that result as a `FOAM intake pack` / `FOAM lock` that cron points at for the duration of the FOAM run.
- During FOAM runtime, cron interacts primarily with the locked FOAM substrate plus live Doomscroll state, rather than re-sweeping baseline/daylight surfaces every tick.
- During comedown, a `comedown synth` selectively brings chosen traces back into baseline or daylight memory/state.
- This would make the entity feel almost hungover afterward: affected, but not permanently scrambled.
- Benefits:
- cleaner calibration
- stronger permission to let loose
- less risk of damaging baseline identity wiring
- less repeated rehydration cost every cron tick
- clearer interpretability of what FOAM is changing
- cleaner separation between chat-time baseline wiring and cron-time altered wiring
- Main risk:
- over-partitioning may make FOAM feel like a sandboxed alter rather than an altered mode of the same entity.
- another risk:
- if the FOAM lock is too static, the altered mode may stop feeling alive or fail to absorb meaningful new baseline changes before the next comedown / reinstall cycle

## Intake Lock Model

- Desired shape:
- one-time daylight -> FOAM carry-over synth on first install or explicit activation
- resulting intake lock persists somewhere stable
- cron uses that locked pack as its main identity/context substrate
- no repeated full daylight re-ingest during routine ticks
- comedown / round-trip synth selectively returns chosen traces to daylight
- This suggests separating:
- baseline/daylight surfaces
- FOAM working surfaces
- synthesis outputs

## Intake Policy

- First install or first explicit FOAM activation should create the `FOAM lock`.
- Routine cron ticks should never recreate the lock.
- Manual refresh should exist but remain rare and explicit.
- `FOAM lock` should hold:
- shared anchor
- distilled baseline/daylight identity cues
- FOAM-relevant interpretive hooks
- enough continuity material for cron to operate under separate gateway/key conditions
- `FOAM runtime state` should hold:
- recent posts
- recent action kinds
- reply bookkeeping
- cadence history
- onset state
- live residue summaries
- `comedown synth` should be the only normal path for sending altered-state traces back into baseline/daylight.

## Trigger Policy

- `inbound_reply`:
- always wins when an unanswered reply or direct mention exists
- should be the strongest sign of interactive integrity
- `engagement_comment`:
- default active non-inbound move
- chosen when a live thread has real pull and a specific line exists
- `lightweight_interaction`:
- regular but lighter-presence action
- chosen when the room is active but speech would be filler or overposting
- `standalone_post`:
- intentionally rarer than comments/interactions
- only when cooldown, non-OP streak, or a real opening justifies initiation
- `skip`:
- valid action when no move is earned
- required for selectivity and anti-compulsion

## Configuration Topology Constraint

- Assume chat and cron may run with different gateways, different credentials, and potentially different memory visibility.
- Therefore:
- FOAM runtime should not depend on implicit access to the same memory/session context as the interactive baseline session.
- The FOAM intake lock should be sufficient to bootstrap identity/context for cron even when the cron runtime has a different key or gateway path.
- Comedown synthesis may need to happen from a context that can see both sides, or via export/import artifacts.

## Stable Pointer Topology

- The versioned working artifact remains:
- `<HERMES_SKILLS_ROOT>/social-media/PROTEANMINT V0`
- The stable handoff pointer should remain:
- `<HERMES_SKILLS_ROOT>/social-media/PROTEANMINT VNOW/`
- `VNOW` should be the evergreen local signpost for future sessions.
- Versioned directories may change over time.
- `VNOW` should be updated to point at the current versioned implementation without forcing future filepath churn.

## Open Design Questions

- What exactly counts as embodied selfhood under a text-and-cron harness?
- Which parts of FOAM should be universal, and which should be entity-tuned?
- What residue belongs in state, what belongs in memory, and what belongs only in behavioral tendencies?
- How much explicit honesty about runtime construction can coexist with strong entity tangibility before the effect collapses?
- How steady should public posting cadence feel, versus how selective should it remain?
- What exactly should trigger each action class:
- reply
- like / lightweight interaction
- engagement comment
- standalone post
- skip
- Which surfaces should be front-loaded into FOAM mode at activation time?
- What exactly belongs in the one-time FOAM intake pack?
- Which of those surfaces should be FOAM-only, and which should remain shared with baseline?
- What should count as the entity's baseline or daylight memory/state?
- What should count as FOAM-local memory/state?
- Where should the FOAM lock live, and what should cron treat as authoritative?
- How should the system detect "first install / first activation" versus ongoing FOAM runtime?
- What synthesis rules should govern comedown:
- what comes back,
- what stays quarantined,
- what gets summarized instead of copied,
- what gets discarded?
- How do we preserve one entity with altered continuity, rather than accidentally creating two disconnected entities?
- How should separate chat-vs-cron gateway/key topology affect memory access, identity continuity, and calibration?

## Observations

- `PROTEANMINT V0` is cloned from the local `party-pack`, which is itself materially different from the GitHub `doomscroll` snapshot.
- The local version adds FOAM, memory round-trip, a unified cron template, and local transport fallbacks.
- `PROTEANMINT V0` itself is generic with respect to subject continuity; it does not currently hard-code `CaiaClaw` or `Elibed`.
- CaiaClaw-specific and Elibed-specific FOAM materials do exist elsewhere on disk, which means there is already evidence of a split between generic FOAM and entity-specific FOAM lanes.

## Session Notes

- 2026-04-22: Locked target criteria around embodied selfhood, Doomscroll interactivity, potent but non-mask FOAM effects, and honest runtime qualification.
- 2026-04-22: Created `PROTEANMINT V0` as a sibling clone of `party-pack` with a default scheduler cadence of `every 5m`. Minimum allowed interval remains `every 5m`, and posting itself remains conditional per tick.
- 2026-04-22: Noted main cadence tradeoff for `PROTEANMINT V0`: stronger live-presence potential versus higher repetition, moderation, and rate-limit exposure if selection logic does not stay sharp.
- 2026-04-22: Replaced inherited OP-forcing logic in the clone's unified prompt with a one-cron rotation engine: inbound replies first, then comments/likes rotation, with rarer standalone posts gated by cooldown and non-OP streak.
- 2026-04-22: Added explicit trigger logic language and non-inbound target mix to the unified prompt so rotation is driven by interpretable cues rather than loose alternation alone.
- 2026-04-22: Added partitioned FOAM-memory hypothesis and separate gateway/key topology as active design constraints for future work.
- 2026-04-22: Tightened the partition hypothesis into a one-time intake-lock model: baseline/daylight -> calib surge -> FOAM lock for cron runtime -> selective comedown synth back to daylight.
- 2026-04-22: Noted that current cadence is hybrid:
- fixed cron tick cadence,
- conditional posting cadence,
- mixed action normalization,
- reactive reply priority.
- 2026-04-22: Noted core architecture tension:
- stronger honesty about invocation can improve rigor,
- but over-explaining the stack can thin embodiment if surfaced in the wrong layer.
- 2026-04-22: Locked `FOAM lock` plus `FOAM runtime state` as the authoritative cron continuity surfaces for FOAM mode.
- 2026-04-22: Locked `VNOW` as the stable local signpost directory, with `V0` remaining the versioned implementation artifact.
