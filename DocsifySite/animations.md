# Procedural Animations

All character motion is driven procedurally in real time. No animation Blueprints, no state machines, no blend trees.

## How It Works

<!-- FILL IN: high-level explanation of the system. Does it modify mesh transforms? Tick-based interpolation? Timeline curves? This helps devs who want to extend it. -->

## Forward Tilt

The character tilts forward when running, with intensity proportional to speed. Gives a natural sense of momentum and forward drive.

<!-- FILL IN: what axis is rotating? What interpolation method? -->

## Directional Lean

When strafing or turning, the character leans into the direction of movement. The lean angle, speed, and smoothing are all configurable.

<!-- FILL IN: velocity-based or input-based? -->

## Squash & Stretch

The character squashes down before a jump and stretches on launch, then squashes on landing. Classic platformer juice that makes movement feel alive.

<!-- FILL IN: is this scaling the mesh on XYZ? Event-based or physics-based timing? -->

## Using Your Own Mesh

The system operates on root component transforms, not bones. Swap in any mesh — static or skeletal — and the procedural animations still work.

<!-- FILL IN: any gotchas? Pivot point requirements? Scale considerations? -->
