# Changelog
All notable changes to this project will be documented in this file.
The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).
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