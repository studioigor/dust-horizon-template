# MASTER GAME PROMPT — Пыльный горизонт

Create a polished short cinematic first-person survival game in Godot 4 using prebuilt Blender environment assets exported as GLB.

## Environment workflow
Do NOT procedurally invent the main architecture.

Use a hybrid workflow:
- handcrafted Blender hero assets for everything close to the player;
- modular architecture for bunker interiors;
- terrain system for the desert;
- procedural scattering only for repeated natural/environmental objects;
- manually composed hero areas;
- MultiMesh or equivalent instancing for repeated rocks, debris and distant props;
- decals, particles, lighting and fog for richness;
- simplified distant geometry for a huge-world illusion.

The three previously generated object sheets are authoritative visual references for props and interactive objects:
1. bunker props;
2. wasteland/gas-station props;
3. interactive gameplay items.
Use the 3D props modeled from these sheets inside the final level rather than regenerating them in-engine.

## Game overview
10–15 minute cinematic first-person post-apocalyptic game.

Flow:
1. Intro in bunker.
2. Short bunker exploration.
3. Giant blast door interaction.
4. Short cinematic reveal outside.
5. Walk through wasteland along destroyed highway.
6. Discover abandoned gas station and repairable car.
7. Search for BATTERY, FUEL, IGNITION COMPONENT.
8. Install items.
9. Start car; engine startup takes 90–120 seconds.
10. Survive increasingly difficult monster attack.
11. At 100%, objective changes to GET IN!
12. Sprint to vehicle while enemies continue attacking.
13. Cinematic escape down road.
14. Beautiful sunset driving montage.
15. Fade to title and credits.

## Production limits
Only two major playable locations:
A. Underground shelter.
B. Wasteland + highway + gas station.

No cities, crowds, complex NPC dialogue, open-world quest systems, deep crafting or large inventory.

## Player
First-person controller:
- WASD;
- mouse look;
- sprint;
- crouch;
- jump;
- interact;
- pickup/carry;
- firearm;
- reload;
- optional flashlight.

Movement slightly heavy and physical. Add subtle head bob, footsteps, breathing, landing motion and weapon sway.

## Bunker
1–2 minutes.
Use modular Blender corridor assets. Start in a small shelter room, move through industrial corridors, machinery and empty maintenance spaces, then reach blast-door chamber.
Environmental storytelling only. Minimal text.

Objective: REACH THE SURFACE.

Use warm emergency lights, cold fluorescent lights, machinery audio, ventilation, dripping water, electrical hum, occasional sparks and steam.

## Blast door
Hero moment.

Player:
1. activates console;
2. restores power;
3. pulls emergency lever;
4. waits for locks;
5. hydraulic systems move;
6. huge door opens.

Use separate animated door parts. Add low-frequency mechanical audio, subtle camera vibration, dust, steam, warning lights and a thin line of exterior sunlight growing into a blinding opening.

## Exterior reveal
Briefly reduce player control for 10–20 seconds.
Exposure adapts from dark bunker to bright desert.

Reveal:
- vast wasteland;
- cracked highway;
- dead pylons;
- abandoned vehicles;
- distant mountains;
- distant ruins;
- huge sky;
- dust and heat haze.

No combat.

Objective: FIND TRANSPORTATION.

## Desert
Compact playable area, visually huge.
Hand-author the route. Use procedural scatter only for rocks, small debris, sparse dry vegetation and roadside scrap.

Rule:
0–10 m = manual placement.
10–50 m = manual + scatter.
50+ m = LOD/MultiMesh/distant decoration.
Horizon = cheap silhouette geometry.

## Highway
Use modular road GLBs.
Road visually connects bunker → gas station → sunset destination.
Use decals/sand overlays to hide repetition.

## Gas station
Main hero arena, entirely art-directed by hand.

Include:
- shop;
- garage;
- canopy;
- pumps;
- roadside sign;
- wrecked vehicles;
- workshop;
- generator;
- radio antenna;
- escape vehicle.

Strong compositions:
1. first distant view;
2. vehicle discovery;
3. combat at dusk/night;
4. departure onto highway.

## Repair loop
Interact with vehicle. It will not start.

Display:
BATTERY
FUEL
IGNITION COMPONENT

Battery: remove from abandoned car.
Fuel: find canister in storage/rear area.
Ignition component: retrieve from workshop/electrical cabinet/generator room.

Each item uses simple tactile interactions:
open, pull, remove, carry, insert.

No complex inventory.

## Tension
After item 1: mostly safe.
After item 2: strange sounds/radio interference.
After item 3: silhouettes and movement appear.

Use tracks, distant noises, shadows, damaged remains and dust movement.

## Engine startup
After all items are installed:
car fails to start several times, then automatic startup begins.

Display:
ENGINE STARTING — 0%

Duration: 90–120 sec.

The player only needs to survive until 100%.

## Monsters
Use only 2–3 archetypes.

FAST CREATURE:
low health, fast, attacks in groups.

HEAVY CREATURE:
slow, high health, strong impact.

OPTIONAL STALKER:
rare flanker.

Keep AI simple but reliable:
detect, navigate, attack, react to damage, die, use several approach routes.

Create horde illusion through fog, dust, distant silhouettes, monster audio, staged spawning and multiple directions rather than huge simultaneous counts.

## Combat
Simple firearm:
shotgun, revolver or crude rifle.
Optional melee.

Limited ammo. Extra ammo placed around arena.
Player must move between shop, garage, pumps, wrecks and barriers.

Environmental options:
- explosive fuel container;
- temporary floodlight;
- electrical trap;
- destructible barricade.

No crafting.

## Escalation
0–25%: small fast enemies.
25–50%: more enemies, multiple directions.
50–75%: heavy enemy, lighting issues, stronger wind.
75–95%: high pressure, low ammo.
95–100%: near-overwhelming final wave.

Game should become genuinely difficult near the end.

## Escape
At 100%:
engine roars, headlights turn on.

Objective:
GET IN!

Do not stop enemies.
Player sprints to vehicle.
Large creature may almost reach vehicle.

On interaction, immediately trigger escape cinematic.

## Final cinematic
Shots:
1. first-person windshield;
2. low wheel shot;
3. side tracking;
4. rear shot of gas station disappearing;
5. wide desert shot.

Combat music fades into emotional atmospheric track.

Vehicle drives through destroyed highway, pylons, distant ruins and mountains toward orange sunset.

Destination remains unexplained.

Final wide shot: tiny car moving through enormous dead world.

Fade to black.
Show title.
Credits.

Optional final radio transmission hinting that another survivor or settlement exists.

## Rendering/art direction
High-quality stylized low-poly, not PS1.
Use:
- strong silhouettes;
- PBR materials;
- decals;
- DirectionalLight3D;
- WorldEnvironment;
- volumetric fog where useful;
- GPU particles for dust/sparks/steam;
- heat haze;
- LOD;
- simplified collisions;
- MultiMesh for repeated props.

Visual priorities above extra content.

The four most important shots:
1. blast door opening;
2. first wasteland view;
3. first gas station view;
4. car driving into sunset.

The final experience should feel like a polished playable cinematic episode, not an unfinished RPG.
