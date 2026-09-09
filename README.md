# Simple Brick Breaker

A classic, fast-paced 2D brick breaker arcade game built with vanilla HTML5 Canvas, CSS, and JavaScript. Zero external dependencies, no build tools, and completely playable in any modern web browser.

---

## 🎮 Features

- **Zero Dependencies**: Pure vanilla JavaScript and HTML5 Canvas in a single standalone file.
- **Web Audio Sound Effects & Procedural BGM**: Built-in 8-bit retro sound synthesizer and procedural chiptune background music player using the native browser Web Audio API.
- **Dynamic Combo Multiplier**: Chain consecutive brick breaks before the ball returns to the paddle to rack up multipliers (`x2`, `x3`, `x4`, `x5`) with rising audio pitches and floating combo badges.
- **Visual Juice & Effects**: Dynamic particle explosions, glowing ball trails, camera screen shake, and floating score numbers.
- **Trajectory Aim Guide**: Predictive dashed trajectory guide when the ball is docked on the paddle for precise aim.
- **Multi-Level Progression**: 4 handcrafted stages with unique brick formations (Standard Grid, Pyramid, The Fortress, and The Demolition Citadel).
- **Power-Up Arsenal**:
  - **Fireball (`F`)**: Turns balls into blazing fireballs that melt clean through bricks (and titanium) without deflecting.
  - **Safety Shield (`B`)**: Deploys a bottom energy barrier that catches and deflects lost balls back into play.
  - **Multi-Ball (`3X`)**: Multiplies active balls into multiple simultaneous projectiles.
  - **Laser Blaster (`L`)**: Mounts dual plasma cannons on the paddle.
  - **Wide Paddle (`W`)**: Widens paddle for easier deflections.
  - **Slow Ball (`S`)**: Reduces ball speed for high-precision maneuvering.
  - **Extra Life (`+1`)**: Grants immediate bonus lives.
- **Diverse Brick Roster**: Standard, Medium, High-Value, Reinforced Silver (with crack states), **TNT Explosives** (radial detonations), and **Titanium** (unbreakable deflectors).
- **Mouse & Touch Support**: Fluid desktop mouse tracking, mobile touch dragging support, and interactive HUD toggles.
- **Pause & High Score System**: Persistent local high scores (`localStorage`) and pause/resume functionality.

---

## 🕹️ Controls

| Action | Primary Key | Alternative Key / Input |
| :--- | :--- | :--- |
| **Move Paddle** | `←` / `→` | `A` / `D` or **Mouse / Touch Drag** |
| **Launch Ball** | `Space` | `↑` (Up Arrow) or **Click / Tap** |
| **Shoot Lasers** | `X` | *(Requires active Laser power-up)* |
| **Toggle Music (BGM)** | `B` | Click BGM in HUD |
| **Mute / Unmute SFX** | `M` | Click SFX in HUD |
| **Pause / Resume** | `P` | `Esc` |
| **Restart Game** | `Space` | **Click / Tap** *(On Game Over or Victory)* |

---

## 🧱 Game Mechanics

### Brick Types & Scoring

| Brick Type | Color | Hits | Points | Details |
| :--- | :--- | :---: | :---: | :--- |
| **Standard** | Blue (`#3fa9f5`) | 1 | 1 pt | Basic foundation brick |
| **Medium** | Yellow (`#ffd83d`) | 1 | 10 pts | Mid-tier score booster |
| **High Value** | Red (`#ff3b3b`) | 1 | 20 pts | High-value target causing screen shake |
| **Reinforced** | Silver (`#d1d5db`) | 2 | 15 pts | Sturdy brick that cracks upon first hit |
| **TNT Explosive** | Orange-Red (`#ff471a`) | 1 | 15 pts | Detonates in a 3x3 radius damaging all adjacent bricks |
| **Titanium** | Slate (`#555d70`) | &infin; | 0 pts | Indestructible obstacle (can only be obliterated by Fireball) |

---

### Power-Ups & Rarity

When a brick is destroyed, there is a **28% chance** of dropping a power-up capsule:

| Power-Up | Badge | Rarity | Drop Share | Effect |
| :--- | :---: | :--- | :---: | :--- |
| **Wide Paddle** | `W` | Common (Silver) | 28% | Expands paddle width to 135px for 10s |
| **Extra Life** | `+1` | Uncommon (Green) | 14% | Grants +1 additional life |
| **Safety Shield** | `B` | Shield (Cyan) | 16% | Deploys a bottom energy barrier that saves 1 lost ball |
| **Multi-Ball** | `3X` | Rare (Blue) | 16% | Triples active balls on the screen |
| **Slow Ball** | `S` | Legendary (Orange) | 10% | Reduces ball speed by 38% for 10s |
| **Fireball** | `F` | Fire (Flame Red) | 10% | Pierces straight through bricks without deflecting for 8s |
| **Laser Blaster** | `L` | Epic (Purple) | 6% | Equips dual laser cannons for 12s (Press `X` to fire) |

> **Note:** Collecting duplicate timed power-ups extends their active duration.

---

## 🚀 Getting Started

No installation, build step, or web server required!

1. Clone or download this repository:
   ```bash
   git clone https://github.com/pmarkoulidakis/simple-brick-braker.git
   ```
2. Open `index.html` directly in any modern web browser (Chrome, Firefox, Safari, Edge).