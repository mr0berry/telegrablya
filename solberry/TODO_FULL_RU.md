# SolBerry TODO

## Versions
Keep same features on all supported versions:
- 1.20.1 Fabric
- 1.20.1 Forge
- 1.21.1 Fabric
- 1.21.1 NeoForge
- 1.21.11 Fabric

Do not fix only one version if change is supposed to be shared.

## 1.21.11 Fabric render check
Latest render patch still need full in-game check:
- black hole must be behind food, food must stay on foreground
- cloud motion blur only on cloud, never darken whole screen
- starvation motion blur only on world, GUI must stay normal
- cloud spin food transition must be smooth, not disappear/appear
- skin second layer must not split from player model
- black hole must be shader/GL effect, not generated texture

## Known version problems to keep checking
### 1.21.11 NeoForge
- motion blur parity
- skin layer splitting
- black hole
- smooth food change while cloud spins
- crash when looking at player

### 1.20.1 Fabric / Forge
- last item in some lists was not selectable
- world motion blur must not blur opened GUI

## Starvation
- starvation effect immediately at 0 hunger
- health damage starts from next day, configurable
- recovery target configurable, default half hunger bar
- no starvation phases
- first person hand shake
- bent player pose
- darkening from top to bottom
- eating sound
- other players/animals can look like food while starving
- hallucination model must not blink/disappear
- animal / food / stretched steak / fixed random modes
- optional rerandomize
- starvation potion around 10/15 sec and lower recovery
- disabling starvation must return hand smoothly

## Eating players
Off by default.
- hold RMB
- gradual damage mode with hunger recovery
- instant eat mode with warning
- configurable duration and hunger recovery
- can kill / damage / affect hunger depending settings
- optional player head
- only while starving
- cannot eat self without starvation
- eating removes starvation
- death messages without final dot
- pixel circle progress indicator with starvation icon
- smooth circle then pixelized look

## Reroll
- lever inside cloud
- lever reward modes: morning / completed craving / completed sheet
- jackpot 5%, only first spin
- jackpot freezes hunger like full sheet
- reroll can reset completed cravings
- option to keep completed cravings
- roulette must actually stop on selected food
- sounds must match animation
- food must move away smoothly, not just disappear
- wind-up before spin

Animations:
- revolver
- magician
- portal
- UFO
- theater
- cane
- shadow
- black hole from side

## Cloud and UI
- old/new textures switch, new by default, with preview
- category + food mode must show both
- category cloud parity on all loaders
- motion blur while cloud spins
- custom values in wizard
- dropdowns where needed
- multiselect animation picker
- text must not cover buttons
- all bottom buttons clickable
- scrolling questions, can jump to later question
- discovered food from inventory / ingredients
- hunger spending speed presets + custom
- refresh time morning / timer

## Unlocks
- craving unlock editor
- advancements picker instead of manual IDs where possible
- show unlocks in advancement screen on Shift
- toast with newly unlocked cravings
- FTB Quests support
- BetterQuesting support where version allows it
- food/category picker instead of manual typing

## Food pool
- food can unlock when player got all ingredients
- cooked-food requirement on by default
- avoid raw food when cooked version is the intended one
- mob-drop progression can unlock related cooked food
- custom food items and changed food values saved in presets

## Localization
Keep every language file in parity after UI/settings changes.
German currently has 365 translated keys in the tracked set.

## Build / testing
- check every supported project after shared changes
- do not assume one loader fix works on another
- keep source repo clean, no build output or logs

## Raven trials / Halloween (WIP branch)

Source branch: mr0berry/SOLberry / feature/raven-trials-candy-scaffold

- [x] 12 stationary candy placeholders (NeoForge 1.21.1 only)
- [x] 2 active candy slots, third only if current cravings completed
- [x] death resets candy selections; basic hunger costs
- [x] separate flat raven_trials dimension placeholder
- [x] basic raven sack block (dialogue placeholder)
- [ ] move candies to Fabric 1.20.1, Forge 1.20.1, Fabric 1.21.1 and Fabric 1.21.11 after compile checks
- [ ] real candy models/textures supplied by user
- [ ] build 12 arenas, difficulty progression and candy rewards (no crafting or random drops)
- [ ] raven sack village spawn, villagers' dialogue and crow cutscene
- [ ] player jumps into sack, raven loading animation and game selection
- [x] per-player server SavedData for 12 trials: attempts, wins, candy unlocks
- [x] clickable sack trial picker, server-only win callback, OP debugwin
- [x] ordinary inventory snapshot (main slots, armor, offhand); deny held cursor/crafting items
- [x] restore hooks for death, logout/relogin, escape, time limit and failed entry
- [x] fail-closed guard for known extra-slot mods (Curios, Accessories, Trinkets, etc.)
- [x] basic guards for breaking blocks, items, pickup, attacks and gamemode
- [ ] validate inventory escrow under restart/crash, full inventory, keepInventory and mod removal
- [ ] full modded inventory/ability/remote storage + multiplayer anti-cheese, no bypasses
- [ ] full dynamic arena instancing for several players in the same minigame
- [ ] in-world victory conditions for all 12 games (currently OP test only)
- [ ] witch iris: single dream splash bottle per life, sleep effect for enemies, player dream traversal
- [ ] spider caramel: triple shift, real wall/ceiling movement with camera/accessibility mode
- [ ] crow transformation: actual model/flight, invulnerability, totem/cooldown order tests
- [ ] true projectile reflection, rubber safe-place rebound, balancing
- [ ] candy status UI, translations in all supported languages
- [x] NeoForge 1.21.1 compile-only CI and asset checks (first GitHub run passed)
- [ ] client/server gameplay and multiplayer regression tests before merging; no JAR release in this prototype

