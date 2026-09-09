# Simple Brick Breaker

A classic, fast-paced 2D brick breaker arcade game built with vanilla HTML5 Canvas, CSS, and JavaScript. Zero dependencies, no build tools, and completely playable in any modern web browser.

---

## 🎮 Features

- **Zero Dependencies**: Pure vanilla JavaScript and HTML5 Canvas in a single file.
- **Dynamic Ball & Paddle Physics**: Realistic angle-based bouncing based on paddle impact location, preventing repetitive vertical loops.
- **Multi-Tiered Bricks**: Bricks spawn with randomized point values and color indicators.
- **Power-Up Drop System**: Destroying bricks has a chance to drop unique power-ups spanning 4 rarity tiers.
- **Laser Blasters**: Equip your paddle with dual laser cannons to blast through rows of bricks.
- **Lives & HUD System**: Real-time score tracking, remaining lives, and active power-up status indicators.
- **Responsive Canvas**: Automatically adapts to different screen sizes.

---

## 🕹️ Controls

| Action | Primary Key | Alternative Key |
| :--- | :--- | :--- |
| **Move Left** | `Left Arrow` (`←`) | `A` |
| **Move Right** | `Right Arrow` (`→`) | `D` |
| **Shoot Lasers** | `X` | *(Requires active Laser power-up)* |
| **Restart Game** | `Space` | *(On Game Over or Victory)* |

---

## 🧱 Game Mechanics

### Brick Types & Scoring
Every brick row has a randomized chance to spawn as a standard or high-value brick:

| Brick Type | Color | Spawn Chance | Points |
| :--- | :--- | :--- | :--- |
| **Standard** | Blue (`#3fa9f5`) | 80% | 1 pt |
| **Medium** | Yellow (`#ffd83d`) | 12% | 10 pts |
| **High Value** | Red (`#ff3b3b`) | 8% | 20 pts |

---

### Power-Ups & Rarity
When a brick is destroyed, there is a **25% chance** of dropping a power-up capsule. Power-ups fall toward the paddle and can be collected for temporary or permanent buffs:

| Power-Up | Badge | Rarity | Drop Share | Effect |
| :--- | :---: | :--- | :---: | :--- |
| **Wide Paddle** | `W` | Common (Silver) | 50% | Expands paddle width to 140px for 10s |
| **Extra Life** | `+1` | Uncommon (Green) | 25% | Grants +1 additional life |
| **Slow Ball** | `S` | Legendary (Orange) | 20% | Reduces ball speed by 40% for 10s |
| **Laser Blaster** | `L` | Epic (Purple) | 5% | Equips dual laser cannons for 12s (Press `X` to fire) |

> **Note:** Collecting duplicate timed power-ups extends their active duration.

---

## 🚀 Getting Started

No installation, build step, or web server required!

1. Clone or download this repository:
   ```bash
   git clone https://github.com/pmarkoulidakis/simple-brick-braker.git