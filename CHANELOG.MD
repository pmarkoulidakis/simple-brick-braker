# Changelog
All notable changes to this project will be documented in this file.
The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.1.0] - 2026-09-09
### Added
- **Dynamic Combo Multiplier System**:
  - Chaining brick breaks without hitting the paddle builds an active combo streak with scaling multipliers (`x2`, `x3`, `x4`, up to `x5`).
  - Added dynamic pitch-scaling audio feedback on consecutive brick hits and destruction.
  - Added on-screen fiery combo badge and floating score tags (`+40 (2X!)`).
- **TNT & Titanium Brick Mechanics**:
  - Added **TNT Explosive Bricks** that trigger a radial 3x3 chain detonation damaging adjacent bricks with custom explosions and heavy screen shake.
  - Added **Titanium Bricks** functioning as indestructible metallic obstacles with glancing spark physics, destructible only via the Fireball power-up.
- **Fireball & Safety Shield Power-Ups**:
  - Added **Fireball** (`F` - Flame Red tier) that engulfs the ball in fiery embers and punches straight through bricks without deflecting.
  - Added **Safety Shield** (`B` - Cyan Barrier tier) that deploys a glowing bottom laser floor to catch and rebound dropped balls.
- **Procedural 8-Bit Chiptune BGM**:
  - Built-in zero-dependency 16-step arpeggiated retro bassline synthesizer generated via the Web Audio API.
  - Added `B` keyboard shortcut and interactive HUD click toggle for music playback.
- **Trajectory Aim Guide**:
  - Added a predictive dashed trajectory line and target reticle when a ball is docked on the paddle.
- **Stage 4: The Demolition Citadel**:
  - Handcrafted master stage combining layered titanium defenses, TNT chains, silver reinforcements, and high-value targets.

---

## [2.0.0] - 2026-09-09
### Added
- **Web Audio Sound Effects Synthesizer**:
  - Implemented synthesized 8-bit sound effects using the native browser `AudioContext` (paddle hit, brick hit, brick destruction, laser shot, power-up pickup, life lost, level clear, game over, victory).
  - Added sound mute toggle (`M` key and HUD indicator) and auto-initialization on first user interaction.
- **Visual Juice & Particle Engine**:
  - Added dynamic particle explosions upon brick destruction, color-matched to the brick destroyed.
  - Added glowing trailing motion blur behind moving balls.
  - Added camera screen shake effect on high-value brick destruction and life loss.
  - Added rising floating point indicators (`+10`, `+20`, power-up tags) on brick breaks and buffs.
  - Updated UI styling with rounded glowing paddle and modern HUD typography.
- **Gameplay Enhancements & Multi-Ball**:
  - Refactored single ball system into a multi-ball array (`balls[]`).
  - Added **Multi-Ball** power-up (`3X` - Rare tier) that splits active balls into 3 balls simultaneously.
  - Added **Reinforced Silver Bricks** (2 HP) displaying realistic crack textures upon taking damage.
  - Added ball launch on demand (ball docks on paddle and launches upon pressing `Space`, `↑`, or clicking/tapping).
- **Multi-Level Progression System**:
  - Added 3 handcrafted stages (Level 1: Grid, Level 2: Diamond / Pyramid, Level 3: The Fortress).
  - Added level transition fanfare and automatic level progression upon clearing all destructible bricks.
- **Controls & Accessibility**:
  - Added mouse tracking and mobile touch dragging support on canvas.
  - Added pause/resume functionality (`P` or `Escape` key).
  - Added persistent local high score tracking via `localStorage`.

---

## [1.2.0] - 2026-09-09
### Fixed
- **Refresh Rate & Game Speed Consistency**:
  - Implemented a fixed-timestep accumulator loop (60 updates/sec) in `gameLoop`.
  - Decoupled game physics and movement from display refresh rates and browser `requestAnimationFrame` timing.
  - Resolved hyperspeed gameplay issues on Chrome and high refresh rate monitors (120Hz, 144Hz, 240Hz+).
  - Added elapsed time clamping to prevent spiral-of-death catch-up loops when tab is unfocused or backgrounded.

---

## [1.1.0] - 2026-09-09
### Added
- **Power-Up System**:
  - Implemented 25% drop rate upon brick destruction.
  - Added 4 power-up types with distinct rarity tiers:
    - **Wide Paddle** (`W` - Common): Widens paddle for 10 seconds.
    - **Extra Life** (`+1` - Uncommon): Adds +1 life immediately.
    - **Slow Ball** (`S` - Legendary): Decreases ball velocity by 40% for 10 seconds.
    - **Laser Blaster** (`L` - Epic): Equips paddle with laser cannons for 12 seconds.
  - Added power-up stacking/duration extension when collecting matching active buffs.
- **Laser Shooting Mechanic**:
  - Added dual laser projectiles fired using the `X` key (with a 300ms cooldown) during active laser buff.
  - Added collision detection for laser projectiles against active bricks.
- **Brick Variety & Tiered Scoring**:
  - Added multi-tier bricks with distinct colors and point values (Blue = 1pt, Yellow = 10pts, Red = 20pts).
- **HUD & Status Displays**:
  - Added top-right active effects indicator showing remaining power-up statuses.
  - Added on-screen controls description below canvas.
- **Lives System**:
  - Implemented 3-life pool before reaching Game Over.
  - Added ball & paddle repositioning on life loss.
### Changed
- Improved paddle rebound physics with dynamic angular deflection based on hit position.
- Added minimum horizontal velocity check to prevent infinite vertical bounces.

---

## [1.0.0] - 2026-09-08
### Added
- Initial release of the 2D canvas brick breaker game.
- Single-file setup (`index.html`) using vanilla JavaScript and HTML5 canvas.
- Basic brick layout, paddle movement (`A`/`D` and `Arrow` keys), and ball physics.
- Win, Game Over, and restart (`Space`) screen states.
- Responsive canvas scaling.