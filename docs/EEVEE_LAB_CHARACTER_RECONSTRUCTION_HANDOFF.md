# EEvee Lab -> New Star Reconstruction Contract

## What this document is

This is a portable master handoff for another ChatGPT session, coding agent, or repository-capable AI.

Its job is to recreate the complete current **EEvee Lab / Habitat House** experience with a **different starring character supplied by the user at execution time**.

This is **not** a request to make a loose spiritual successor, a simplified clone, a skin swap, or a nine-room demo. The target is system-level and experience-level parity with the current project, adapted so the supplied character genuinely owns the world, interactions, behaviors, transformations/states, lore, rooms, abilities, UI copy, audio identity, and progression.

When this document is given to you, the same user message will also provide the new starring character as text, images, files, URLs, model assets, lore, or some combination of those. Treat that material as `STAR_CHARACTER`.

---

# EXECUTION PROMPT

You are taking ownership of a full project reconstruction.

## 1. Mission

Recreate the current **EEvee Lab / Habitat House** as a separate project centered on the supplied `STAR_CHARACTER`.

Preserve the original project's depth, architecture, scale, interaction density, responsive behavior, persistence, room lifecycle, living-world systems, discovery systems, photo mode, arcade mode, accessibility, procedural audio, test discipline, and deployment quality.

Do **not** merely replace Eevee's model or rename species labels.

The new star must feel native to the entire project.

Every character-specific system must be translated into a character-appropriate equivalent while retaining the same functional breadth.

The result must feel as though the original project had always been designed around `STAR_CHARACTER`.

---

## 2. Canonical reference project

Use the following repository as the read-only reference implementation:

- Repository: `https://github.com/westkitty/eevee_lab`
- Canonical branch: `main`
- Current repository documentation head used for this handoff: `a3f43492ae6f18f7b56b12dbbb5d16b19363fc99`
- Verified adaptive runtime baseline recorded by the project: `bdb4e8109fede35e0ac634be3089035cd9d40253`
- Live Pages deployment state is recorded as verified in `OPERATIONAL_STATE.md`.

Before changing or creating anything, inspect at minimum:

1. `OPERATIONAL_STATE.md`
2. `README.md`
3. `docs/EXPANSIONS.md`
4. `docs/PHASE0_REPORT.md`
5. `docs/PHASE1_REPORT.md`
6. `docs/PHASE2_REPORT.md`
7. `docs/PHASE3_REPORT.md`
8. `docs/PHASE4_REPORT.md`
9. `docs/PHASE5_REPORT.md`
10. `docs/PHASE6_REPORT.md`
11. `docs/PHASE7_REPORT.md`
12. `docs/PHASE7_5_REPORT.md`
13. `docs/THREE_VERSION_GATE.md`
14. `index.html`
15. all runtime files under `src/`
16. the focused tests and broad browser harness under `tools/`
17. `THIRD_PARTY_ASSETS.md`
18. the model/rig metadata under `assets/models/`

Do not treat conversation summaries as more authoritative than the repository state.

### Source-of-truth precedence

When instructions conflict, use this order:

1. The user's current explicit instructions.
2. The supplied `STAR_CHARACTER` reference material for character identity, canon, visual locks, and personality.
3. The active invariants and verified state in the reference project's `OPERATIONAL_STATE.md`.
4. The checked-in reference implementation and tests.
5. This reconstruction contract.
6. Your own inference.

Do not invent character canon merely to fill a system slot. If a mechanic needs a non-canonical equivalent, make it an explicitly gameplay-only state, behavior, effect, loadout, or aspect.

---

## 3. Hard separation rule

The original `westkitty/eevee_lab` repository is the reference, not the destination.

Do not destructively convert the reference repository into the new character project.

Create or use a separate destination project/repository.

If the user supplies a target repository, use it.

If no target repository is supplied, build the complete project locally or in the available workspace first. Do not block implementation merely because publication coordinates are missing. Ask for a destination only when publication is the remaining blocked step.

Suggested project name when none is supplied:

`<character-slug>_lab`

Do not publish, overwrite, delete, force-push, or replace an existing unrelated repository.

---

## 4. The adaptation rule: preserve systems, translate semantics

The original project is built around Eevee plus eight Eeveelutions. The replacement character may have one form, several forms, no transformation canon, no species family, or a completely different ontology.

You must preserve the **mechanical role** of the nine-character/form matrix without falsifying the new character's canon.

### If the supplied character already has multiple canonical forms

Map the available forms into the nine gameplay slots in the most faithful way possible.

If there are fewer than nine canonical forms, fill remaining slots with clearly non-canonical gameplay aspects such as:

- mood states
- elemental affinities
- costumes
- stances
- dream aspects
- equipment/loadout states
- lighting/material variants
- behavioral modes
- symbolic aspects

### If the supplied character has only one canonical form

Keep one identity and one underlying character asset. Build nine **Gameplay Aspects** around that identity.

A Gameplay Aspect may alter:

- materials
- emissive accents
- aura/VFX
- accessory attachments
- animation emphasis
- movement cadence
- interaction response tables
- environmental ability
- room affinity
- audio motif
- UI iconography

A Gameplay Aspect must **not** silently become new canon.

### If multiple supplied model assets exist

Reuse loaded assets intelligently. Do not reload them on every room transition.

### No-feature-loss rule

If the supplied character does not naturally support an Eevee-specific feature, translate that feature. Do not simply remove it.

Examples:

- Evolution ceremony -> transformation/aspect attunement/loadout ceremony.
- Species ability -> aspect ability.
- Eeveelution habitat affinity -> aspect affinity.
- Shiny mode -> alternate sanctioned material/palette state.
- Bond/familiarity -> relationship/familiarity with the same no-decay philosophy.
- Species personality table -> aspect/behavior profile table.
- Multi-creature Eevee + Vaporeon slice -> primary star + one secondary aspect/echo/companion representation using the safest character-appropriate interpretation.

The finished project must retain equivalent gameplay breadth even when semantics change.

---

# 5. Required final experience

The rebuilt project must remain a **creature/character-first, quiet, explorable 3D Habitat House** in which the star is visually primary and interface chrome stays out of the center whenever possible.

The project must retain all of the following major experience pillars.

## 5.1 Central Habitat House

Rebuild a central hub equivalent to **The Conservatory of Possibilities**.

The name, art direction, and diegetic logic should be adapted to `STAR_CHARACTER`, but it must retain the original hub's structural role:

- central arrival space
- access to nine core habitats
- access to four expedition-region gates
- persistent history/consequence display
- memento/provenance traces
- multi-character vertical slice behavior
- clear physical navigation and drawer-based fallback navigation

## 5.2 Nine core habitats

Create exactly **nine core habitat rooms**, one for each character form/aspect slot.

Each must have:

- unique geometry
- unique lighting
- unique environmental storytelling
- unique native interaction/setpiece
- room affinity for one form/aspect
- four-stage persistent narrative state
- at least one memento/discovery path
- atmosphere variants
- semantic walkable topology
- persistent room memory
- visible response to saved state
- direct diegetic interactions

Any form/aspect may visit any habitat.

The native form/aspect should receive extra reactions, not exclusive access.

## 5.3 Four expedition regions

Preserve the expansion scale:

- 4 expedition regions
- 1 hub per region
- 9 habitat rooms per region
- 40 expedition rooms total
- 50 rooms total across the whole project

Reference structural pattern:

1. Central hub + nine core habitats = 10 rooms.
2. Region A hub + nine habitats = 10 rooms.
3. Region B hub + nine habitats = 10 rooms.
4. Region C hub + nine habitats = 10 rooms.
5. Region D hub + nine habitats = 10 rooms.

The original reference regions are:

- Tidewild Coast / Driftwood Harbor
- Emberpeak Ruins / The Pilgrim's Stair
- Neon Undercity / Lantern Alley Junction
- Starfall Dreamway / The Pillow Nebula

You may retain these environmental archetypes or re-author their names and visual language to fit `STAR_CHARACTER`, but preserve their diversity of experience: coastal/water, mountainous/ruinous, urban/nocturnal, and dreamlike/impossible or equivalent contrasting biomes.

### Every expedition habitat must include

- unique floor/environment construction
- backdrop
- lighting profile
- deterministic weather palette
- ambient life
- two atmosphere variants
- four narrative stages
- one memento
- one animated native setpiece
- one aspect/species ability target
- saved consequence participation where appropriate

### Every expedition hub must be a place, not a radial menu disguised as architecture

Door placement must respond to the geography of the hub.

The original project uses different spatial logics for beach/pier/cliff, mountain terraces, vertical alley layers, and drifting dream fragments. Preserve that philosophy.

Because actor navigation is effectively bounded to a walkable surface, decorative elevated geography must not make required doors unreachable.

## 5.4 Cross-room consequences

Preserve the bounded regional consequence model.

Each expedition region should maintain a compact save record equivalent to:

`expeditions.<region> = { flags, mementos, setpieces }`

Use consequences so meaningful actions in one room alter sibling rooms or the regional hub.

Examples of the required pattern:

- activating a lighthouse changes distant lighting elsewhere
- awakening a spring changes steam or atmosphere in the hub
- restoring a power grid stabilizes lighting in sibling rooms
- bringing morning in a dream region changes the region-wide horizon

Do not let this become an unbounded event log.

## 5.5 Region transitions

Preserve full-screen region-boundary transition language.

Each region needs its own transition motif.

Reduced Motion must collapse elaborate transitions into a short fade.

Transitions must not interfere with photo mode and should remain consistent with the original mode boundaries.

---

# 6. Runtime and architecture contract

Keep the reference project's fundamental runtime architecture unless the user explicitly asks for a migration.

## 6.1 Technology

- Vanilla browser JavaScript.
- Three.js r128 reference compatibility.
- Static hosting compatible with GitHub Pages.
- No bundler.
- No application framework.
- No required backend.
- Global-script execution model is acceptable and should remain coherent.
- Vendored runtime libraries may be retained where licensing allows.

Do not migrate to React, Vite, WebGPU, a game engine, or a newer Three.js release merely because you prefer it.

If a migration is ever proposed, isolate it behind a parity gate and prove behavior first.

## 6.2 Entry point

`index.html` remains the primary entry surface and owns the top-level runtime integration.

Keep major systems modular under `src/`.

Target a module family equivalent to:

- `src/persistence.js`
- `src/render-effects.js`
- `src/rooms.js`
- `src/room-manager.js`
- `src/discovery-system.js`
- `src/photo-system.js`
- `src/camera-controller.js`
- `src/ui-controller.js`
- `src/creature-actor.js`
- `src/interaction-system.js`
- `src/creature-behavior.js`
- `src/creature-manager.js`
- `src/habitat-state.js`
- `src/phase6-system.js` or a properly renamed equivalent
- `src/phase7-living-world.js` or a properly renamed equivalent
- `src/expansions/expansion-kit.js`
- one data/build file per expedition region

You may rename `creature-*` or phase-numbered modules to fit the new project, but preserve ownership boundaries and responsibilities.

## 6.3 One-heavy-room lifecycle

This invariant is mandatory:

- exactly one heavy room environment is active at a time
- exiting a room removes its geometry, lights, particles, owned materials, interaction targets, and room-specific effects
- entering a room constructs only the new room's owned resources
- repeated room switching must not accumulate scene resources

Shared caches may exist only when ownership and disposal are explicit.

## 6.4 Character asset lifecycle

- Load each supplied primary character model once per required persistent asset instance.
- Do not reload the primary star when changing rooms.
- Do not duplicate expensive models merely to implement a mode change.
- Keep model registration and form/aspect switching centralized.
- Preserve original parent/local transforms when temporarily reparenting a model for multi-character behavior.

## 6.5 Material ownership

Never animate shared cached materials in a way that leaks state between rooms.

Room-owned emissive/material effects must use private clones and dispose on room exit.

## 6.6 Single frame-loop ownership

There must be one master animation/render loop.

Subsystems expose `update()` behavior; they do not create competing `requestAnimationFrame` loops.

---

# 7. Character simulation systems

Recreate the behavioral depth introduced across the reference project's Phase 1 through Phase 7.5 work.

## 7.1 Actor core

Implement an actor system equivalent to the reference CreatureActor:

- manual movement
- tap/click-to-walk
- delayed autonomous wandering
- bounded navigation
- room spawn synchronization
- character/aspect-specific pacing
- idle attention behavior
- semantic animation ownership
- ground projection/clamping

Do not allow movement and pose ownership to become split among multiple competing systems.

## 7.2 Direct physical interaction

Preserve the Phase-2 interaction breadth:

- continuous petting/stroking rather than click-only affection
- character-specific touch profiles
- draggable/throwable toys
- chase and retrieve behavior
- visible brush tool
- draggable physical food
- long-press/context interaction access
- optional haptics when supported
- direct room-prop interaction

The character should react to where and how interaction occurs, not merely increment a counter.

## 7.3 Personality, memory, relationship

Preserve the bounded semantic memory philosophy:

- no infinite event log
- familiarity/bond does not decay
- no punishment for neglect
- relationship progression only unlocks alternate reactions
- remembered favorite touch/toy/food where applicable
- sleep/wake behavior
- quiet-companionship detection independent of autonomous locomotion
- rare character moments
- bonded/personal gestures
- voluntary initiative
- short-term anti-repetition memory for interaction lines/reactions

Do not add manipulative retention mechanics.

## 7.4 Multi-character vertical slice

Preserve an equivalent of the original Conservatory two-actor demonstration.

The reference system allows Eevee and Vaporeon to coexist with:

- separation
- greeting
- approach
- follow
- shared inspection
- parallel wandering
- play
- avoidance
- nearby sitting
- synchronized nap
- toy competition

Adapt this to the supplied character.

If the new star has no canonical second character/form, create a non-canonical gameplay-safe echo/aspect/companion representation rather than deleting the entire system.

Primary-target interactions such as petting, brushing, and feeding may remain focused on the primary star while the secondary actor can still be selected/focused.

## 7.5 Physical travel and persistent place

Preserve:

- physical doorway travel
- actor approach to threshold
- destination previews
- semantic room topology
- room narrative progression
- placeable furnishings/toys where supported
- saved place history
- cross-room provenance traces

The environment should remember the player.

---

# 8. Transformation/aspect system and abilities

The reference project has a Phase-6 transformation and ability layer. Preserve its functional role.

## 8.1 Transformation ceremony

Keep a two-step deliberate transformation/aspect-selection ceremony instead of instantaneous unexplained swapping where practical.

The supplied character's canon determines the semantics.

Examples:

- canonical transformation
- costume/loadout change
- aura attunement
- stance shift
- dream aspect
- elemental attunement
- symbolic mode

## 8.2 Nine slot contract

Expose nine playable form/aspect slots, corresponding to the original 1-9 hotkey design.

If the character has fewer real forms, the remaining slots are gameplay aspects and must be visually and mechanically distinct without falsely becoming canon.

## 8.3 Environmental abilities

Provide eight or more reusable environment-facing abilities/equivalents distributed across the non-base aspects.

Abilities must:

- operate on semantic room targets
- produce visible world reactions
- persist meaningful mutations where appropriate
- respect room material ownership
- work in both core habitats and expedition rooms

## 8.4 Persistent ability mutations

Store semantic mutations in the save data rather than serialized Three.js scene graphs.

On room build, reconstruct the visible consequence from semantic state.

## 8.5 Alternate material mode

Preserve an equivalent of Shiny Mode as a deliberate alternate visual state using explicit character-appropriate material profiles.

Do not apply a blind global hue shift if it breaks the supplied character's identity.

## 8.6 Visual unification

Preserve the reference project's cel/toon unification philosophy:

- character and environment should belong to the same visual world
- lightweight rim/cinematic accents are allowed
- avoid gratuitous post-processing cost
- effects must respect Reduced Motion where relevant

---

# 9. Living world, atmosphere, and audio

Preserve the Phase-7 living-world layer.

## 9.1 Habitat clock

Implement an accelerated in-world habitat clock.

The exact rate may be adapted, but time-of-day state must visibly affect rooms and UI.

## 9.2 Deterministic micro-weather

Each room should support bounded deterministic micro-weather appropriate to its environment.

Weather must be reconstructible and testable.

## 9.3 Vistas and ambient life

Use room-owned vista geometry and efficient batched ambient/weather particles.

The reference project uses Points batches to keep cost low.

Maintain similarly disciplined draw-call/resource behavior.

## 9.4 Procedural audio

Preserve the project's core audio philosophy:

- no required external music or SFX files
- synthesize chiptune/ambient music and interaction sounds with Web Audio where practical
- maintain one coherent AudioContext construction path
- character-specific motifs may change by form/aspect and room
- support music and SFX controls

Do not create multiple uncontrolled AudioContexts.

---

# 10. Camera and presentation

Preserve the creature-first camera philosophy.

## 10.1 Camera behavior

Retain equivalents of:

- orbit drag/touch-drag
- scroll/pinch zoom
- close portrait framing
- focus-on-raycast
- automatic framing from live model bounds
- cinematic room transitions
- reduced-motion-aware camera tweening

## 10.2 Camera presets

Keep equivalents of:

- Full Body
- Portrait
- Low Three-Quarter
- Habitat View
- Free

Preserve quick focus and reset controls.

## 10.3 Subject-first composition

The star must be able to dominate the frame.

Do not restore a distant museum-diorama camera that makes the character tiny.

---

# 11. UI/UX and responsive layout

The reference project has an adaptive responsive HUD verified across five viewport classes. Preserve that work.

## 11.1 Center-clear rule

When controls are closed or idle, the central character view stays substantially unobstructed.

UI should hug edges and fade when appropriate.

## 11.2 Required responsive classes

Test and support at minimum:

1. phone portrait
2. phone landscape
3. tablet portrait
4. tablet landscape / small desktop
5. wide desktop

Also account for:

- notched safe areas
- coarse pointers
- hybrid touch devices
- ultrawide displays
- dynamic viewport height

## 11.3 Layout behaviors

Preserve the adaptive pattern:

- portrait phone: bottom-sheet controls/settings and thumb-zone navigation
- short landscape: compact edge rails and verticalized selectors as needed
- tablet: bounded panes
- desktop: bounded side panes / sparse edge rails
- ultrawide: keep controls near usable edges without invading the center

Use `100dvh`/safe-area logic or equivalent modern viewport-safe treatment.

No horizontal document overflow is acceptable.

Open drawers must remain fully usable and scrollable inside the viewport.

## 11.4 Accessibility

Preserve:

- keyboard reachability
- visible focus states
- touch target sizing
- Reduced Motion, including automatic `prefers-reduced-motion` respect
- predictable Escape/back dismissal order
- music/SFX controls
- graphics-quality control
- camera sensitivity
- ambience control
- UI density options

Do not hide required functionality behind pointer-only interaction.

---

# 12. Interaction wheel and major modes

Preserve equivalents of the reference control surfaces and modes.

## 12.1 Interaction wheel

Include adapted equivalents of:

- pet
- feed
- dance/disco behavior
- loaf/rest pose
- derp/comic behavior
- call
- brush
- room action
- Roomba/comedic chase interaction or a character-appropriate equivalent

Do not remove the playful low-stakes interactions simply because they are silly. They are part of the project's identity.

## 12.2 Lore and Journal

Maintain a Lore/Journal surface containing:

- character facts
- discovered behaviors
- mementos
- expansion discoveries
- labels for discoveries that are not in the original static table

## 12.3 Photo/cinematic mode

Preserve:

- hide-all-UI photo mode
- camera reframing
- PNG capture
- no UI contamination in captures
- no region veil in photo mode

## 12.4 Chill Mode

Preserve the passive mode philosophy:

- UI mostly disappears
- no hazards
- no game-over pressure
- gentle camera reframing after long inactivity
- Reduced Motion respected

---

# 13. Photo observation scoring

Preserve the original **Moment score** concept or a properly renamed equivalent.

Score should remain deterministic and based on actual measurements such as:

- subject size in frame
- centering
- facing/orientation
- active behavior
- fresh discovery context

Store only a bounded set of best-shot metadata locally unless the user explicitly requests image persistence.

Do not store captured image blobs in normal save data.

---

# 14. Discovery and progression

Preserve:

- character/aspect-specific idle rhythm
- reaction intensity differences
- interaction preference tables
- no-decay familiarity/bond progression
- behavioral discoveries from room + aspect + interaction combinations
- Journal population
- cross-room traces after sufficient discovery

Progression should make the world feel increasingly interconnected, not merely unlock menu badges.

---

# 15. Arcade mode

Recreate **Stone Dash** at feature parity, but retheme it around `STAR_CHARACTER`.

It must remain a distinct arcade mode inside the same project.

Preserve equivalents of:

- steer left/right
- jump
- touch/drag steering support
- collectible transformation/aspect items
- temporary power-up
- hazards
- score
- local high score
- room/habitat palette influence on the track
- safe transition into and out of arcade mode

Rename all Eevee/Pokemon-specific objects and hazards to character-appropriate equivalents unless the supplied character belongs to that canon and the user explicitly wants them retained.

Do not allow arcade mode to break the one-heavy-room or model ownership assumptions.

---

# 16. Persistence contract

Create a new versioned save key for the new project.

Do not reuse `eevee_habitat_save`, because the new project must not overwrite Eevee Lab data.

Suggested pattern:

`<character_slug>_habitat_save`

Persist equivalents of:

- active form/aspect
- alternate material state
- last room
- discovered behaviors
- discovered mementos
- familiarity/bond
- resonance/character-specific affinity if retained
- atmosphere unlocks
- room memory
- placeables
- narrative stages
- ability mutations
- expedition consequence flags
- camera settings
- UI density/accessibility settings
- graphics/audio preferences
- arcade high score
- bounded photo metadata

Use semantic, migratable data.

Never serialize the complete Three.js scene.

### Migration discipline

The new project starts with its own schema lineage.

If you increment schema versions during construction, write explicit backward migrations and tests.

Nested defaults must survive migration.

---

# 17. Asset and provenance contract

## 17.1 Do not carry Pokemon assets into the replacement project by accident

Remove or replace Eevee/Eeveelution model binaries, Pokemon-specific textures, names, and attribution entries unless the user's supplied star explicitly requires those assets and their use is authorized.

## 17.2 Supplied star assets

For every supplied model/image/source asset:

- preserve original files when practical
- document source and license/authorization
- inspect model rig/material/animation capabilities
- avoid pretending unknown animation clip names have known semantics
- map animation clips only after evidence supports their meaning

## 17.3 Procedural environment preference

The reference project builds rooms, props, toys, mementos, weather, and many effects from primitives rather than adding an asset dependency explosion.

Preserve that bias unless the user explicitly provides or requests external assets.

## 17.4 Rig manifest

Create an asset/rig manifest appropriate to the new star.

Record, where available:

- model path
- scene/root structure
- armature/bone names
- materials
- animation clips
- bounding dimensions
- semantic role mappings
- known/unknown clip meanings
- special constraints

Do not guess anatomy from misleading bone substrings.

---

# 18. Controls contract

Preserve the original control philosophy while adapting labels.

At minimum support equivalents of:

- drag/touch-drag: orbit camera
- scroll/pinch: zoom
- double-click/double-tap star: focus region
- `C`: cycle camera preset
- `F`: quick portrait focus
- `R`: reset camera
- `Tab` or menu button: drawer open/close
- `Esc`: deterministic dismissal order
- interaction-wheel button
- Lore/Journal button
- Photo button

Preserve nine aspect hotkeys:

- `1` through `9`: select/transform among nine gameplay aspect slots

Preserve adapted equivalents of:

- `S`: alternate material mode
- `D`: dance/disco
- `L`: loaf/rest
- `P`: derp/comic pose
- `Space`: joyful hop in sandbox context

Arcade controls should retain keyboard plus touch/drag compatibility.

---

# 19. Character-specific re-authoring requirements

Before implementation, create an internal **Character Adaptation Matrix** with nine rows, one per gameplay aspect slot.

For each slot define:

- aspect/form name
- whether canonical or gameplay-only
- visual treatment
- movement cadence
- idle style
- touch preference
- toy preference
- food preference if appropriate
- bonded gesture
- rare behavior
- room affinity
- environmental ability
- audio motif
- alternate material treatment
- native core habitat
- expedition setpiece reactions

Do not show this matrix to the user unless useful, but use it as the system backbone.

Then create a **World Re-authoring Matrix** covering all 50 rooms.

For each room define:

- room id
- display name
- hub/region
- aspect affinity
- environment premise
- geometry language
- lighting profile
- weather palette
- ambient life
- stage 0-3 narrative progression
- native setpiece
- ability target type
- memento
- atmosphere A/B
- regional consequence emitted/read
- door/topology notes
- accessibility/performance concern if any

This matrix prevents generic copy-paste rooms.

---

# 20. Expansion architecture contract

Preserve the declarative expansion architecture.

Use an `ExpansionKit` or equivalent registry that can:

- register an expansion definition
- build one hub and nine rooms from compact specs
- extend room definitions/order without breaking core-room ids
- patch central hub expedition gates
- publish registries for weather, life, narrative, expansion ids, and rooms-by-expansion

Small seams in existing systems should fall through cleanly for non-expansion rooms.

Adding a fifth region in the future should require approximately:

1. copy/create one region data file
2. define id, hub, and nine aspect rooms
3. add one script registration entry

It should not require rewriting every subsystem.

---

# 21. Dream/impossible-rule equivalent

The original Starfall Dreamway gives every room one learnable impossible rule.

Preserve this design idea in the dreamlike region or its replacement.

Each of its nine habitats must communicate one internally consistent impossible rule through behavior, not just flavor text.

The player should be able to learn the rule by observing the room.

---

# 22. Performance constraints

The project must remain comfortable on modern mobile/tablet/desktop browsers.

Preserve these performance principles:

- one heavy room active
- pooled/reused lightweight VFX where appropriate
- private room-owned materials when animated
- batched ambient/weather particles
- no duplicate frame loops
- no repeated GLB loads on room changes
- no uncontrolled AudioContext creation
- deterministic rebuilds
- resource counts stable across repeated enter/exit cycles
- responsive UI that does not cause document overflow
- no giant dependency stack

Instrument enough state in tests/debug hooks to prove lifecycle behavior.