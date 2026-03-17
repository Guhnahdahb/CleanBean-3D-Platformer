# Configuration

All parameters are exposed in the character Blueprint's Details panel, organized under labeled categories.

## Movement

<!-- FILL IN: replace with your actual parameter names and defaults -->

| Parameter | Description | Default |
|---|---|---|
| `MaxSpeed` | Maximum ground speed | `000` |
| `Acceleration` | How quickly the character reaches max speed | `000` |
| `Deceleration` | How quickly the character stops | `000` |
| `GroundFriction` | Friction during ground movement | `000` |
| `AirControl` | Steering control while airborne | `000` |

## Jump

| Parameter | Description | Default |
|---|---|---|
| `JumpForce` | Upward impulse on jump | `000` |
| `DoubleJumpForce` | Upward impulse on double jump | `000` |
| `FallGravityMultiplier` | Extra gravity when falling | `000` |
| `CoyoteTime` | Grace period after leaving a ledge | `000` |
| `JumpBuffer` | Input buffer window before landing | `000` |

## Animation

| Parameter | Description | Default |
|---|---|---|
| `TiltAngle` | Max forward tilt in degrees | `000` |
| `LeanAngle` | Max lean angle in degrees | `000` |
| `LeanSpeed` | How quickly lean responds | `000` |
| `SquashIntensity` | Compression on land | `000` |
| `StretchIntensity` | Stretch on jump | `000` |

## Effects & Sound

| Parameter | Description | Default |
|---|---|---|
| `ParticleScale` | Scale of all particle effects | `000` |
| `FootstepFrequency` | How often footsteps play | `000` |
| `SFXVolume` | Volume of all sound effects | `000` |
| `LandImpactThreshold` | Min fall distance for land effects | `000` |
