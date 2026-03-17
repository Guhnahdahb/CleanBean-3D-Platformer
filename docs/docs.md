# Documentation for CleanBean 3D Platformer



> **Current version: 0.5** — Core movement and juice. Version 1.0 will add advanced traversal. See roadmap

## Overview

A game-ready 3D platformer controller built around one thing: **how it feels in your hands.** Responsive controls, procedural animations, particle effects, and sound design — all without requiring a humanoid character rig or pre-made animations. 

## Requirements

Unreal engine 5.6+.

## Design Philosophy

My intent with this project is to keep things really simply but still have a good feeling player controller. I use this even when not making a 3D platformer. It's a good way to test out multiple different levels or game systems with a simple character controller. 

It's built using the default Unreal Engine Character Movement Component (CMC). This is great for a lot of reason, and not so great for a few. A lot of custom movement has to fight against the CMC. Ideally for an in depth or completely custom movement system, it would be built up from the ground up. For simplicity and familiarity, I decided to stick with CMC for this.

## Specific things of note for this project

A few spring arms are used in the player blueprint. This isn't standard for characters, and I'm not using them in a typical way. Spring Arms are typically meant for cameras. They use arm length, target offset and a few other things. The main thing I use is "Enable Camera Lag" and "Enable Camera Rotation Lag." It's a type of short cut to apply some smoothing to the character movement and it's different components. Most of the components are child-ed under the "Visuals Spring Arm." With camera lag enabled on this spring arm, the visual part of the characters slightly lags (smooths) behind the true player capsule. Visually, this makes things like the landing, sliding (yet to be implemented) and even idle bob and walking bob smoother without writing a bunch of extra code or using a ton of timelines to smooth everything out. It's performant and a simple way to implement smoothing in a lot of ways.

## Procedural Animations

### Idle Bob and Movement Bob

The bobbing "animation" is really just a scaling value of the visuals spring arm. Depending on the players horizontal speed, it scales the speed of the timeline played that controls it's Z scale value.

### Forward tilt and L/R lean

All character motion is driven in real time. It is called on event tick. You may have heard to never use Event tick, and that's simply not true. There are use cases for it, but obviously building everything off of Event Tick is a bad idea and bad practice. In the CleanBean 3D, only what needs to be is off Event Tick. 

Essentially what this means for the bean is it calculates the players horizontal velocity, and applies a rotational effect depending on the local orientation of the bean. 

### Squash & Stretch

When jumping and landing, it sets the spring Arm Target variable. This variable is fed into a function that is always trying to smooth two vectors together. In this case, the two vectors that are being smoothed are the Spring arm Target and the beans actual scale. The end results is smooth interpolation of the bean, regardless of it's value. In extreme cases, the interp value might be too small, but there aren't many extreme cases so I've omitted a solution to this for now.

## Particles & VFX

All particle systems are included and trigger automatically.

They are all based from simple Niagara particle systems that render 3D meshes of circle and emit them based on distance or space.
## Sound Effects

Most things have sound effects.
"Footsteps" (the bean doesn't have feet), jump, and land. 

`At this time, I'm aware of a bug with the visual dust and sound footstep going off even if the bean is in the air. This will be fixed in the next update.`

## Roadmap

**Planned for v0.6**
	Collectable / Pick-up item class

**Planned for v1.0:**
	- Wall running
	- Wall jumping
	- Vaulting
	- Ground slam

> **All updates are free** for existing owners.

## Changelog

### v0.5 — Initial Release 

- Core movement system: run, jump, double jump
- Procedural animations: forward tilt, directional lean, squash and stretch
- Particle effects: jump burst, land impact, walk dust
- Sound effects: footsteps, jump SFX, land SFX
- Bean character mesh with customizable material
- Example demo level

## FAQ

**Can I use my own character mesh?**
Yes. Swap in any static or skeletal mesh. The procedural system works on root transforms, not bones. That means if you want actual animations, other animation solutions will be needed.

**Does this work with multiplayer?**
Not currently. Single-player only. Because of the simplicity of the system, I'm considering coding for multiplayer, but at this time it's not planned.

**What engine versions are supported?**
UE 5.6+. Earlier versions untested, although I don't see many conflicts since I'm not using any fancy 5.6+ features.

**Will v1.0 features be free?**
Yes. All updates are free for existing owners.

## Support

Having issues or found a bug?

	Github repo [[https://github.com/Guhnahdahb/CleanBean-3D-Platformer/tree/main]]


