# Ghostman: Custom Sandbox & Enemy Builder

A standalone, single-file HTML5 Canvas combat sandbox and playtesting lab for **Ghostman**, featuring real-time enemy spawners, customizable parameters, stopwatch timer, debug tools, and procedural Web Audio sound effects.

🎮 **Play directly on GitHub Pages**: [Launch Sandbox](https://mmalone3.github.io/Ghostman/) *(or your deployed repository URL)*

---

## ⚡ Core Features

- **Endless Arena Sandbox**: No floor timers, transitions, or level gates. Test combat mechanics continuously in a single persistent arena.
- **Stopwatch & PB Tracker**: Live counting timer (`MM:SS.ms`) with Pause, Resume, Reset, and local-storage Personal Best tracking.
- **All 7 Enemy Archetypes**:
  1. 💣 **Bombs**: Green (3.0s fuse), Yellow (2.0s fuse), and Red (1.2s rapid blast) with expanding telegraph rings and radial explosions.
  2. 🔷 **Diamond Sparks**: Fast cardinal laser projectiles launched from arena walls.
  3. ⭕ **Singer Rings**: Giant collapsing waves contracting to an inner sweet spot.
  4. 🎯 **Orbital Pouncers**: Multi-phase enemies (Orbit ➔ Telegraph Windup ➔ High-speed Lunge) in Physical (orange) and Void (purple) variants.
  5. ⚡ **Kinetic Lance**: High-velocity azure beam that pierces Vanish (must be shielded/parried or dodged).
  6. 🌌 **Phasing Void Beam**: Heavy violet beam and room sweep that pierces shields (must be Vanished or dodged).
  7. 🌐 **Static Cardinal Grid**: Electric grid hazard lines (Cross, Hash, Perimeter) with pre-activation glow.
- **Interactive Builder Panel**:
  - **Quick Spawn**: 1-click buttons for every enemy variant, combinations, and clusters.
  - **Parametric Spawner**: Fine-tune telegraph duration, projectile speed, blast radius/beam thickness, damage, and spawn count.
  - **Continuous Wave Generator**: Auto-spawn enemies at configurable intervals with customizable enemy pool toggles.
  - **Debug Suite**: God Mode (Invincibility), No Cooldowns (infinite shield/vanish), Freeze/Slow Motion (0.25x - 2x), Hitbox visualizers, HP refill/max sliders, and Partner switcher (Rock / Healer / Speed).
- **Audio & Visuals**: Fully procedural Web Audio API sound effects (no external audio assets needed), dynamic particle burst engine, and crisp high-DPI canvas rendering.

---

## 🕹️ Controls

| Action | Input | Mechanics & Counterplay |
|---|---|---|
| **Move** | `WASD` / Arrow Keys | Responsive directional movement with acceleration & friction |
| **Directional Shield / Parry** | `Spacebar` | Blocks & parries Bombs, Diamonds, Kinetic Lances, and Physical Pouncers. *Vulnerable to Void Beams & Singer Rings.* |
| **Vanish / Phase Shift** | `J` Key | Ethereal phase shift granting invulnerability to Void Beams, Singer Waves, and Grid hazards. *Vulnerable to Kinetic Lances.* |
| **Pause Game** | `P` Key / UI Button | Freezes gameplay & stopwatch timer |

---

## 👥 Selectable Partners

- 🛡️ **Rock**: Expanded shield angle and defensive counter-shockwaves that clear nearby hazards on parry.
- 💖 **Healer**: Emergency auto-revive heal trigger when dropped into critical health (<25% HP).
- ⚡ **Speed**: Faster movement velocity and significantly reduced Vanish cooldown.

---

## 🚀 GitHub Pages Deployment

This repository is ready for immediate deployment on GitHub Pages:

### Option 1: Deploy from Branch (Recommended)
1. Go to your repository **Settings** on GitHub.
2. Under **Code and automation**, click **Pages**.
3. Under **Build and deployment** > **Source**, choose **Deploy from a branch**.
4. Select branch `main` (or your preferred branch) and `/ (root)`, then click **Save**.
5. Your game will be live at `https://<username>.github.io/<repository-name>/`.

### Option 2: Deploy via GitHub Actions
A GitHub Actions workflow is included at `.github/workflows/deploy-pages.yml` to automatically publish `index.html` on every push to `main`.
