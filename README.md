# Simple Brick Breaker

A classic, fast-paced 2D brick breaker arcade game built with vanilla HTML5 Canvas, CSS, and JavaScript. Zero external dependencies, no build tools, and completely playable in any modern web browser.

---

## 🎮 Features

- **Zero Dependencies**: Pure vanilla JavaScript and HTML5 Canvas in a single standalone file.
- **Web Audio Sound Effects**: Built-in 8-bit retro sound synthesizer using the native browser Web Audio API.
- **Visual Juice & Effects**: Dynamic particle explosions, glowing ball trails, camera screen shake, and floating score numbers.
- **Multi-Level Progression**: 3 handcrafted stages with unique brick formations (Standard Grid, Pyramid, and The Fortress).
- **Multi-Ball Power-Up**: Split your active balls into multiple simultaneous projectiles.
- **Multi-Tier & Reinforced Bricks**: Standard, High-Value, and Durable Silver Bricks requiring multiple hits with visible crack states.
- **Ball Launch on Demand**: Aim and launch the ball from your paddle at your own pace.
- **Mouse & Touch Support**: Fluid desktop mouse tracking and mobile touch dragging support.
- **Pause & High Score System**: Persistent local high scores (`localStorage`) and pause/resume functionality.

---

## 🕹️ Controls

| Action | Primary Key | Alternative Key / Input |
| :--- | :--- | :--- |
| **Move Paddle** | `←` / `→` | `A` / `D` or **Mouse / Touch Drag** |
| **Launch Ball** | `Space` | `↑` (Up Arrow) or **Click / Tap** |
| **Shoot Lasers** | `X` | *(Requires active Laser power-up)* |
| **Pause / Resume** | `P` | `Esc` |
| **Mute / Unmute Sound** | `M` | HUD Audio Indicator |
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

---

### Power-Ups & Rarity

When a brick is destroyed, there is a **28% chance** of dropping a power-up capsule:

| Power-Up | Badge | Rarity | Drop Share | Effect |
| :--- | :---: | :--- | :---: | :--- |
| **Wide Paddle** | `W` | Common (Silver) | 40% | Expands paddle width to 135px for 10s |
| **Extra Life** | `+1` | Uncommon (Green) | 25% | Grants +1 additional life |
| **Multi-Ball** | `3X` | Rare (Blue) | 15% | Multiplies active balls |
| **Slow Ball** | `S` | Legendary (Orange) | 15% | Reduces ball speed by 38% for 10s |
| **Laser Blaster** | `L` | Epic (Purple) | 5% | Equips dual laser cannons for 12s (Press `X` to fire) |

> **Note:** Collecting duplicate timed power-ups extends their active duration.

---

## 🚀 Getting Started

No installation, build step, or web server required!

1. Clone or download this repository:
   ```bash
   git clone https://github.com/pmarkoulidakis/simple-brick-braker.git
   ```
2. Open `index.html` directly in any modern web browser (Chrome, Firefox, Safari, Edge).