# Squirtle asset intake

The supplied source bundle is `Archive.zip`.

SHA-256: `f7c767ab46286d1bde6791157ddfb797643eba7dccae602cca14b8b3c92ac5a6`

## Canonical source contents

- `source/Pokemon XY/Squirtle/Squirtle.FBX`
- `source/Pokemon XY/Squirtle/Squirtle.SMD`
- `source/Pokemon XY/Squirtle/Squirtle_ColladaMax.DAE`
- `source/Pokemon XY/Squirtle/Squirtle_OpenCollada.DAE`
- normal texture set under `source/Pokemon XY/Squirtle/images/`
- shiny texture set under `source/Pokemon XY/Squirtle/images_shiny/`
- provenance note in `source/Pokemon XY/Squirtle/Tag.txt`

The outer ZIP also contains a nested original archive and duplicate convenience textures. Ignore `__MACOSX/` and `.DS_Store`.

## Provenance recorded in Tag.txt

- Game: Pokémon X/Y
- Subject: #007 Squirtle
- Copyright: Nintendo, Game Freak, Creatures Inc.
- Model ripper: Random Talking Bush
- Hosting permissions: The Models Resource
- Note credits Ploaj for supplying the necessary files.

## Integration rule

Treat these files as source/reference assets. Inspect rig, materials, animation clips, scale, orientation, and browser compatibility before choosing the runtime format. Do not invent animation semantics from clip or bone names. Preserve the original source bundle/provenance and create browser-ready derivatives only as needed.

The binary ZIP could not be transferred through the GitHub connector used to seed this repository. The authoritative archive is preserved separately; attach `Archive.zip` to the implementation agent/session when building the project.
