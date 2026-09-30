# LM Arena — Build Squirtle Lab

You are taking ownership of the implementation of **Squirtle Lab**.

Repository:
https://github.com/westkitty/Squirtle_Lab

Canonical reference repository:
https://github.com/westkitty/eevee_lab

Your job is to BUILD THE PROJECT, not merely propose a plan, scaffold a demo, or describe what should be done.

## Mission

Reconstruct the complete Eevee Lab / Habitat House experience as a separate, polished **Squirtle-first interactive 3D world**.

Squirtle is the STAR_CHARACTER.

This must feel as though the entire application was originally conceived around Squirtle.

Do not make an Eevee reskin.
Do not merely replace the model.
Do not stop at a prototype.
Do not reduce the scope to one room or nine rooms.
Do not replace the established architecture because another framework is easier.

The source repository already contains the governing reconstruction contract and Squirtle source model bundle.

## READ THESE FIRST

Before modifying implementation files, inspect:

1. OPERATIONAL_STATE.md
2. docs/EEVEE_LAB_CHARACTER_RECONSTRUCTION_HANDOFF.md
3. docs/SQUIRTLE_ASSET_INTAKE.md
4. assets/source/squirtle/Archive.zip

Then inspect the canonical reference implementation:

westkitty/eevee_lab

Read its current:

- OPERATIONAL_STATE.md
- README.md
- expansion documentation
- phase reports
- index.html
- runtime files under src/
- tests and browser harnesses under tools/
- model/rig metadata
- asset provenance documentation

The checked-in reconstruction handoff is the principal implementation contract. Do not duplicate its contents into new planning documents instead of implementing them.

## Squirtle asset source

The supplied ZIP contains actual Pokemon X/Y Squirtle source assets including:

- Squirtle.FBX
- Squirtle.SMD
- Squirtle_ColladaMax.DAE
- Squirtle_OpenCollada.DAE
- normal Squirtle texture set
- shiny Squirtle texture set
- source provenance metadata

Ignore:

- __MACOSX/
- .DS_Store

Do not simply pick a model format blindly.

Inspect:

- skeleton/armature
- mesh hierarchy
- materials
- texture mappings
- animations, if present
- actual animation clip semantics
- bounding dimensions
- orientation
- origin
- scale
- browser suitability

Convert or derive a browser-ready representation only when necessary.

Preserve the original source assets and provenance.

Do not infer animation meanings merely from ambiguous bone or clip names.

## Squirtle identity

Squirtle must be the visual, behavioral, mechanical, and thematic center of the application.

Build character-specific behavior around recognizable Squirtle traits and capabilities where they are supported by the project and source material:

- aquatic affinity
- shell-based physical identity
- playful movement
- swimming/water behavior
- defensive shell behavior where feasible
- water interaction
- expressive idle behavior
- food/toy/touch preferences
- familiar/bonded gestures
- sleeping
- curiosity
- rare autonomous moments
- environment-sensitive behavior

Do not treat Squirtle as a generic blue mascot.

## Nine gameplay slots

The original project mechanically expects nine form/aspect slots.

Squirtle does not canonically have nine evolutionary forms.

DO NOT invent nine canonical Squirtle evolutions.

Instead use one Squirtle identity with nine clearly identified **Gameplay Aspects**.

Develop an internally coherent Squirtle-specific nine-aspect matrix.

A strong direction is to use aspects based on modes, affinities, environments, stances, cosmetic/material states, or behavioral emphases rather than invented species.

Each aspect must have a mechanically meaningful difference involving some combination of:

- visual treatment
- material accents
- movement cadence
- idle behavior
- touch preference
- toy preference
- bonded gesture
- native habitat affinity
- environmental ability
- sound motif
- setpiece reactions

Clearly distinguish canonical Squirtle traits from gameplay-only systems.

The normal and supplied shiny texture sets should inform the alternate-material system where technically suitable.

## World requirement

Build the entire habitat architecture defined by the reconstruction contract:

### Central structure

- one Squirtle-centered central Habitat House hub
- nine core habitat rooms
- four expedition regions
- one hub per expedition region
- nine habitat rooms per expedition region

Total:

**50 rooms**

Do not fake these as menu entries.

Rooms must be actual distinct explorable environments.

Every core habitat needs meaningful distinctions in:

- geometry
- lighting
- environmental storytelling
- interactions
- Squirtle/aspect affinity
- four-stage narrative state
- memento/discovery
- atmosphere variants
- persistent memory
- world response

Every expedition habitat must likewise provide its required:

- unique environment
- lighting
- weather
- ambient life
- narrative states
- memento
- native setpiece
- ability target
- atmosphere variants
- consequence participation

## Squirtle-specific world authorship

Do not copy Eevee's room concepts and rename them.

Translate the world around Squirtle.

Use water, rain, ponds, streams, pools, mist, shorelines, fountains, flooded structures, shell-scale architecture, reflections, currents, bubbles, submerged spaces, wet stone, aquatic life, and other fitting ideas where appropriate — but maintain environmental diversity.

Do not make all 50 rooms blue water rooms.

The project must still have strong biome contrast.

The four expedition regions should retain the structural diversity of:

- coastal/water
- mountainous/ruinous
- urban/nocturnal
- dreamlike/impossible

but should be re-authored strongly enough to belong to Squirtle Lab.

The dream region must preserve the requirement that every room contains one internally consistent impossible rule the player learns by observing it.

## Squirtle interaction depth

Port and adapt the full physical interaction breadth.

Squirtle must support meaningful equivalents of:

- petting/stroking
- brushing
- feeding
- draggable food
- toys
- throwing toys
- chase/retrieve behavior where appropriate
- direct environmental interactions
- long-press/context interaction
- call/reaction
- playful/comic interaction
- rest/loaf equivalent
- dance/play behavior
- autonomous wandering
- click/tap movement
- bonded reactions
- quiet companionship
- sleep/wake
- rare moments
- short-term anti-repetition memory

Interactions should affect Squirtle based on how and where the interaction occurs rather than functioning as dumb counters.

There must be no punishment for neglect and no manipulative retention mechanics.

## Multi-character system

Preserve the original multi-character vertical-slice capability.

If the implementation needs a secondary actor and no additional canonical Pokemon is explicitly provided, use a clearly gameplay-only Squirtle echo/aspect representation rather than inventing a new canonical character.

Preserve meaningful behaviors such as:

- approach
- greeting
- following
- parallel wandering
- play
- avoidance
- nearby sitting
- shared inspection
- synchronized rest
- toy competition

## Environmental abilities

Provide at least eight environment-facing abilities distributed across the non-base gameplay aspects.

Abilities must act on semantic targets in the environment.

They should visibly change rooms.

Persistent changes must be stored semantically and reconstructed when the room is rebuilt.

Do not serialize Three.js scenes into saves.

Squirtle-specific examples may involve water pressure, current manipulation, extinguishing, filling, rinsing, reflective surfaces, bubbles, aquatic traversal effects, shell interactions, or related mechanics — but choose final abilities based on coherence and implementation feasibility.

## Runtime architecture

Preserve the reference project's fundamental architecture unless the governing contract explicitly allows otherwise.

That means:

- vanilla browser JavaScript
- Three.js r128 compatibility unless parity proves a migration
- static GitHub Pages compatibility
- no required backend
- no React migration
- no Vite migration
- no game-engine rewrite
- no bundler added for convenience
- modular systems under src/
- one master render/update loop

### Mandatory lifecycle invariant

Exactly one heavy room environment should be active at once.

When leaving a room, dispose its:

- geometry
- lights
- particles
- cloned materials
- room interactions
- room effects
- owned resources

Repeated room changes must not increase resource counts indefinitely.

Squirtle's persistent model asset should not be reloaded on every room transition.

Shared assets and caches require explicit ownership.

Do not animate shared cached materials if doing so leaks state between rooms.

## Living world

Implement the living-world systems defined in the contract:

- accelerated habitat clock
- deterministic room weather
- vistas
- ambient life
- efficient batched particles
- procedural audio
- Squirtle/aspect-specific motifs
- room-aware atmosphere
- saved regional consequences

Use one coherent AudioContext path.

No AudioContext-per-sound nonsense.

## Camera

Squirtle should dominate the frame when appropriate.

Preserve/adapt:

- orbit camera
- pinch/scroll zoom
- live model-bound framing
- portrait focus
- habitat view
- low three-quarter
- full-body
- free camera
- focus-on-raycast
- smooth room transitions
- Reduced Motion alternatives

Do not regress into a distant museum-diorama camera.

## UI

Preserve the reference project's center-clear interface philosophy.

The player is there to interact with Squirtle, not stare at chrome.

Support:

- phone portrait
- phone landscape
- tablet portrait
- tablet landscape / small desktop
- wide desktop
- safe areas
- dynamic viewport height
- coarse pointers
- hybrid devices
- ultrawide screens

No horizontal page overflow.

Drawers and panels must remain within and scroll inside the viewport.

Keyboard functionality may not be hidden behind pointer-only interaction.

## Accessibility

Preserve:

- keyboard navigation
- visible focus states
- adequate touch targets
- Reduced Motion
- automatic prefers-reduced-motion
- deterministic Escape/back dismissal
- graphics controls
- music control
- SFX control
- camera sensitivity
- ambience controls
- UI density controls

## Photo / observation system

Preserve full photo mode:

- hide UI
- reframe camera
- capture PNG
- no UI contamination
- deterministic observation/Moment scoring

Score using actual measurements such as:

- subject framing
- centering
- facing
- active behavior
- fresh discovery context

Store bounded metadata, not giant screenshot blobs in normal save data.

## Discovery / progression

Progression must make the environment feel increasingly interconnected.

Preserve:

- aspect-specific behavior
- discovery combinations
- Journal/Lore system
- mementos
- cross-room traces
- persistent room history
- regional consequences
- familiarity/bond without decay

## Arcade mode

Rebuild the reference project's Stone Dash feature at parity, but make it belong to Squirtle.

Retheme it appropriately.

Preserve:

- left/right steering
- jump
- touch/drag input
- aspect items
- temporary power-ups
- hazards
- score
- high score
- environment-driven palette changes
- clean entry/exit
- compatibility with model and room lifecycle ownership

Give the Squirtle arcade mode its own fitting title rather than leaving an obviously Eevee-derived title unless the original name remains genuinely appropriate.

## Persistence

Use a Squirtle-specific versioned persistence key, for example:

squirtle_habitat_save

Never reuse Eevee Lab's save key.

Persist semantic state for:

- active aspect
- shiny/alternate material state
- room
- discoveries
- mementos
- familiarity
- atmosphere
- room state
- placeables
- narrative progression
- ability mutations
- expedition consequences
- camera preferences
- UI/accessibility settings
- graphics/audio settings
- arcade score
- bounded photo metadata

Create migrations when schema changes require them.

## Expansion architecture

Retain the declarative expansion registry.

Adding a fifth region later should require approximately:

1. a new region definition
2. its hub plus nine rooms
3. one registration entry

It must not require rewriting the major subsystems.

## Testing

Do not declare completion because the page loads.

Port or rebuild the reference validation strategy.

### Focused tests

Cover:

- actor core
- physical interaction
- behavioral memory
- multi-character management
- persistence
- room lifecycle
- doors
- aspects/transformation
- abilities
- living world
- weather
- procedural audio
- expansions

### 50-room lifecycle verification

Exercise every room.

Prove:

- all 50 construct
- all can update
- required doors function
- room disposal occurs
- repeated reconstruction remains stable
- expedition setpieces work
- expedition mementos work
- regional consequences persist
- saved state reconstructs correctly
- door destinations remain reachable

### Browser journey

Use a real browser harness such as Playwright when available.

Exercise meaningful versions of:

- Squirtle load
- all nine gameplay aspects
- shiny/alternate mode
- pet
- feed
- brush
- toys
- rest
- comic interaction
- dance/play
- call
- movement
- multi-character slice
- room travel
- room cleanup
- aspect ceremony
- environmental abilities
- weather/time
- photo mode
- observation score
- Chill Mode
- arcade mode
- persistence reload
- expedition travel
- region transitions
- responsive drawers

Require zero unexplained page errors and zero unexplained console errors.

### Responsive matrix

Test:

- phone portrait
- phone landscape
- tablet portrait
- tablet landscape
- desktop/wide

Verify:

- center clear when controls close
- no document overflow
- panels stay within viewport
- contents scroll
- touch targets remain usable
- safe areas work

### Rendered QA

Actually inspect screenshots from representative modes and rooms.

Do not claim visual QA from source inspection alone.

## Visual target

Aim for a polished, deliberate, cohesive Three.js experience.

Squirtle and the environments should feel visually unified.

Use a strong stylized/cel-rendered presentation compatible with the source model while preserving Squirtle's recognizable appearance.

Avoid:

- generic AI-dashboard aesthetics
- excessive glass panels
- giant text overlays
- generic blue gradients everywhere
- cheap Pokemon UI imitation
- visual clutter over Squirtle
- effects that obscure interaction

The world should feel playful, inhabited, tactile, calm, strange, and occasionally spectacular.

## Git rules

You are authorized to modify westkitty/Squirtle_Lab.

Do not modify westkitty/eevee_lab.

Work on the existing main branch unless repository state establishes a safer implementation branch.

Before edits:

- verify repository identity
- read OPERATIONAL_STATE.md
- inspect current status

When the implementation is genuinely complete and validated:

1. inspect the full changed-file set
2. ensure unrelated files were not modified
3. update README.md
4. update OPERATIONAL_STATE.md
5. update provenance/asset documentation if derived assets were produced
6. stage intended files
7. commit with a clear message
8. push without force

Do not force-push.

Do not rewrite repository history.

## GitHub Pages

When the implementation is ready and permissions permit:

- configure GitHub Pages
- deploy
- verify the actual public route
- verify JS, model, texture, and other important assets load from the live route

A successful git push does NOT prove deployment.

Do not report Pages as working until the public build was actually opened and checked.

## Implementation strategy

Do not burn agent budget repeatedly rediscovering requirements.

1. Read the three governing Squirtle Lab documents.
2. Inspect the supplied Squirtle archive.
3. Inspect the named reference repository.
4. Build the internal nine-aspect Squirtle adaptation matrix.
5. Build the internal 50-room re-authoring matrix.
6. Establish model loading and prove Squirtle renders.
7. Port architecture and character simulation.
8. Build the core habitat.
9. Build living-world/presentation systems.
10. Build expedition architecture and rooms.
11. Adapt arcade mode.
12. Complete responsive UI.
13. Run focused validation.
14. Run broad validation.
15. Perform one bounded repair pass for proven failures.
16. Re-run affected validation.
17. Update project state/docs.
18. stage, commit, push.
19. Deploy and verify Pages if available.

Do not stop after generating the matrices or a plan.

They are implementation tools, not the deliverable.

## Definition of done

The result is complete only when there is a separate, polished Squirtle habitat project with the system depth, world scale, character interaction, lifecycle discipline, persistent simulation, living world, discovery, responsive UI, accessibility, photo systems, arcade mode, expansion architecture, validation rigor, and deployment honesty required by the checked-in reconstruction contract.

Squirtle appearing in a room is not success.

A nine-room prototype is not success.

A renamed Eevee Lab is not success.

The final project must feel unmistakably like **Squirtle Lab**.

## Final report

Return a concise evidence-based report containing:

### Reconstruction result
- repository
- branch
- final commit
- Squirtle model/runtime asset used
- nine aspect names
- room count
- four expedition regions
- arcade title
- persistence key/schema

### Validation
- tests actually run
- exact results
- 50-room lifecycle result
- browser journey result
- viewport matrix result
- console/page error count
- rendered screenshot QA status

### Deployment
- Pages status
- live route checked
- key assets verified

### Git
- final commit
- pushed/not pushed
- working tree status

### Remaining uncertainty
List anything not actually proven.

Never substitute "should work," "appears complete," or similar language for evidence.

Begin now by reading OPERATIONAL_STATE.md, the reconstruction contract, the Squirtle asset intake document, and the supplied model ZIP. Then implement the project through validation and publication rather than stopping at a plan.
