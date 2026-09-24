# SolBerry patch notes

## Current source repo
Repo is cleaned now.

In main repo:
- build.gradle
- settings.gradle
- gradle.properties
- src/
- .github/workflows/build-release.yml
- root .gitignore

Removed:
- custom build .bat files
- gradle.bat
- config_examples
- tools
- old multiloader_workspace
- README / TODO / patch notes from source repo

Code comments was removed from java, gradle, properties, toml and shaders. Better keep comments rare and short.

## GitHub Actions
All 5 versions built successful in GitHub Actions:
- Fabric 1.20.1
- Forge 1.20.1
- Fabric 1.21.1
- NeoForge 1.21.1
- Fabric 1.21.11

Release v1.0 was created and all 5 jars uploaded.

Workflow now run on v* tags or manual start.

## Recent 1.21.11 Fabric render work
Latest source line includes:
- GUI motion blur
- starvation motion blur
- black hole render
- cloud spin transitions
- player skin second-layer render
- starvation hallucination render

Wanted behavior:
- black hole behind falling food
- food stays in foreground
- GUI cloud blur affects only cloud area
- starvation blur affects world and does not blur GUI
- no full-screen black/dark frame from motion blur
- food changes smoothly during cloud spin
- second skin layer stays attached to player model

Still need normal gameplay check.

## Version history around latest sources
- v25: UI multiselect work and shared source baseline
- v26: NeoForge 1.21.1 / Fabric 1.20.1 UI fixes
- v27: Fabric 1.20.1 compile fix
- v28-v30: Fabric 1.21.11 visual/render/starvation fixes
- v31-v33: Fabric 1.21.11 render, motion blur, black hole, transition and layer fixes
