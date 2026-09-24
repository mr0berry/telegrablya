# SolBerry patch notes

## Current source repo
Repo was cleaned to keep only normal project source:
- build.gradle
- settings.gradle
- gradle.properties
- src/
- root .gitignore

Removed from source repo:
- custom build .bat files
- gradle.bat helper files
- config_examples folders
- tools folders
- old multiloader_workspace copy
- README / TODO / patch notes from source repo

Project notes now live here in telegrablya/solberry.

## Recent 1.21.11 Fabric render work
Latest source line includes work on:
- GUI motion blur
- starvation motion blur
- black hole render
- cloud spin transitions
- player skin second-layer render
- starvation hallucination render

Latest intended behavior:
- black hole behind falling food
- food stays in foreground
- GUI cloud blur affects only cloud area
- starvation blur affects world and does not blur GUI
- no full-screen black/dark frame from motion blur
- food changes smoothly during cloud spin
- second skin layer stays attached to player model

These render changes still need normal gameplay verification before calling them fully done.

## Other work already added during 0.5 development
- setup wizard and large settings UI rework
- category editor and food picker
- presets and full settings reset
- craving unlock system
- advancement and FTB quest integration work
- food detection / recipe safety
- NBT-safe food handling
- configurable hunger drain and fractional hunger
- full-hunger healing options
- post-eating regeneration
- dimension rules
- streak rewards
- reroll system and reroll animations
- jackpot rules
- starvation effect and starvation rules
- starvation visuals
- player eating mechanic
- player eating progress UI
- old/new cloud textures
- localization updates
- loader/version ports and parity fixes

## Important version history around latest sources
- v25: UI multiselect work and shared source baseline
- v26: NeoForge 1.21.1 / Fabric 1.20.1 UI fixes
- v27: Fabric 1.20.1 compile fix
- v28-v30: Fabric 1.21.11 visual/render/starvation fixes
- v31-v33: Fabric 1.21.11 render, motion blur, black hole, transition and layer fixes
