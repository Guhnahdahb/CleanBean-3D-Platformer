# 3D Platformer Template

Documentation for the 3D Platformer Template for Unreal Engine.

[🛒 Fab Listing](#) | [🎮 Download Demo](https://github.com/YOUR-USERNAME/YOUR-REPO-NAME/releases/latest) | [💬 Discord](#) | [📦 GitHub](https://github.com/YOUR-USERNAME/YOUR-REPO-NAME)

> **Current version: 0.5** — Core movement and juice. Version 1.0 will add advanced traversal. [See roadmap →](#roadmap)

## Overview

A game-ready 3D platformer controller built around one thing: **how it feels in your hands.** Responsive controls, procedural animations, particle effects, and sound design — all without requiring a humanoid character rig or pre-made animations. Drop it in and start building levels.

<!-- Add a screenshot or GIF here:
![Gameplay preview](images/preview.gif)
-->

## Requirements

| Requirement | Details |
|---|---|
| Engine Version | Unreal Engine 5.6+ |
| Plugins | None required |
| Project Type | Blueprint-only or C++ |
| Platform | Windows (Mac/Linux untested) |
| Input | Keyboard, Mouse, Gamepad |
| Multiplayer | Not supported |

## Installation & Setup

<!-- UPDATE THESE STEPS TO MATCH YOUR ACTUAL PROCESS -->

**1. Install from Fab**

Purchase and install the asset from the Fab Marketplace. Content appears in your Content Browser under `Content/YourFolderName`.

**2. Open the Example Map**

Navigate to `Content/YourFolderName/Maps/` and open the included example map. Hit Play to test.

**3. Use in Your Own Level**

Place `BP_PlatformerCharacter` into your scene and set it as the Default Pawn in your Game Mode. All effects and sounds are wired up automatically.

**4. Configure**

Select the character and check the Details panel. All parameters are exposed under labeled categories. See [Configuration](#configuration).

<!-- FILL IN: mention Enhanced Input / Input Mapping Context if applicable -->

## Movement

### Run

Standard ground movement with configurable max speed and acceleration. The character responds to input almost instantly with a subtle acceleration curve that adds weight.

<!-- FILL IN: details about your acceleration, sprint, etc. -->

### Jump

A single press launches the character with a punchy upward impulse. Gravity is increased on the downward arc for more satisfying arcs and better control at the peak.

<!-- FILL IN: coyote time, jump buffering if applicable -->

### Double Jump

A second jump mid-air with its own independent force value, tunable separately from the first jump.

<!-- FILL IN: does it reset velocity? Can you double jump after walking off a ledge? -->

## Procedural Animations

All character motion is driven procedurally in real time. No animation Blueprints, state machines, or blend trees.

<!-- FILL IN: brief explanation of how the system works technically -->

### Forward Tilt

Character tilts forward when running, proportional to speed. Gives a natural sense of momentum.

### Directional Lean

Character leans into strafes and turns. Lean angle, speed, and smoothing are all configurable.

### Squash & Stretch

Squashes on land, stretches on launch. Classic platformer juice.

### Using Your Own Mesh

The system operates on root component transforms, not bones. Swap in any mesh — static or skeletal — and it still works.

<!-- FILL IN: any gotchas, pivot requirements, etc. -->

## Particles & VFX

All particle systems are included and trigger automatically.

- **Jump Burst** — Fires from the character's feet on jump
- **Land Impact** — Plays on landing, scaled to fall distance
- **Walk Dust** — Subtle trails during ground movement

<!-- FILL IN: Niagara or Cascade? How to customize colors/scale? How to swap for custom effects? -->

## Sound Effects

Every action has audio feedback. Included SFX are punchy and genre-neutral.

- **Footsteps** — Rhythmic, synced to movement speed
- **Jump SFX** — Sharp launch sound
- **Land SFX** — Weighted thud on landing

<!-- FILL IN: how are footsteps triggered? How to swap in custom sounds? -->

## Character

A simple bean/capsule mesh with no humanoid rig required. Replace it with your own model — the procedural system works with any mesh since it animates the root transform, not bones.

<!-- FILL IN: collision setup, default dimensions, mesh swap steps, material customization -->

## Configuration

All parameters are exposed in the character Blueprint's Details panel.

<!-- FILL IN: replace with your actual parameter names and default values -->

### Movement

| Parameter | Description | Default |
|---|---|---|
| `MaxSpeed` | Maximum ground speed | `000` |
| `Acceleration` | How quickly the character reaches max speed | `000` |
| `Deceleration` | How quickly the character stops | `000` |
| `GroundFriction` | Friction during ground movement | `000` |
| `AirControl` | Steering control while airborne | `000` |

### Jump

| Parameter | Description | Default |
|---|---|---|
| `JumpForce` | Upward impulse on jump | `000` |
| `DoubleJumpForce` | Upward impulse on double jump | `000` |
| `FallGravityMultiplier` | Extra gravity when falling | `000` |
| `CoyoteTime` | Grace period after leaving a ledge | `000` |
| `JumpBuffer` | Input buffer window before landing | `000` |

### Animation

| Parameter | Description | Default |
|---|---|---|
| `TiltAngle` | Max forward tilt in degrees | `000` |
| `LeanAngle` | Max lean angle in degrees | `000` |
| `LeanSpeed` | How quickly lean responds | `000` |
| `SquashIntensity` | Compression on land | `000` |
| `StretchIntensity` | Stretch on jump | `000` |

### Effects & Sound

| Parameter | Description | Default |
|---|---|---|
| `ParticleScale` | Scale of all particle effects | `000` |
| `FootstepFrequency` | How often footsteps play | `000` |
| `SFXVolume` | Volume of all sound effects | `000` |
| `LandImpactThreshold` | Min fall distance for land effects | `000` |

## Roadmap

**Planned for v1.0:**

| Feature | Description | Status |
|---|---|---|
| Wall Running | Run along vertical surfaces with auto-detection | 🔲 Planned |
| Wall Jumping | Launch off walls with directional control | 🔲 Planned |
| Vaulting | Automatic vault over low obstacles | 🔲 Planned |
| Ground Slam | Mid-air downward slam with impact VFX | 🔲 Planned |
| Grinding | Rail grinding with speed mechanics | 🔲 Planned |

> **All updates are free** for existing owners.

<!-- Status key: ✅ Complete · 🔧 In Progress · 🔲 Planned -->

## Changelog

### v0.5 — Initial Release <!-- · FILL IN: Date -->

- Core movement system: run, jump, double jump
- Procedural animations: forward tilt, directional lean, squash and stretch
- Particle effects: jump burst, land impact, walk dust
- Sound effects: footsteps, jump SFX, land SFX
- Bean character mesh with customizable material
- All parameters exposed in Blueprint Details panel
- Example demo level

## FAQ

**Can I use my own character mesh?**
Yes. Swap in any static or skeletal mesh. The procedural system works on root transforms, not bones.

**Does this work with multiplayer?**
Not currently. Single-player only.

**What engine versions are supported?**
UE 5.6+. Earlier versions untested.

**Will v1.0 features be free?**
Yes. All updates are free for existing owners.

<!-- Add more FAQ entries as you get support questions -->

## Support

Having issues or found a bug?

- 💬 **Discord:** [Join the server](#)
- 📧 **Email:** [your@email.com](mailto:your@email.com)
- 🛒 **Fab:** Questions tab on the [store listing](#)

When reporting bugs, include your UE version, what happened, and steps to reproduce. Screenshots or video help a lot.
