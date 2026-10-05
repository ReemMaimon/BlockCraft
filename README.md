# BlockCraft

A Minecraft-style voxel sandbox that lives in **one HTML file** (`index.html`) — no build step, no
dependencies, no image/audio assets. Open it in a modern browser (WebGL2) and play.

## Highlights

* **Infinite procedural world** – chunked terrain streamed around you (render distance 2–16 chunks),
  16 biomes (oceans, rivers, beaches, plains, forests, birch forests, taiga, tundra, deserts, badlands,
  swamps, mountains with snow caps), caves, lava lakes, ores, trees, cacti, flowers.
* **Real lighting** – flood-fill sky + block light with smooth per-vertex light and ambient occlusion,
  torches / glowstone / lava / lit furnaces, day–night cycle with sun, moon, stars and clouds, rain & snow.
* **Survival** – health, hunger, armour, fall / drowning / lava / cactus damage, tool tiers and durability,
  break times like the real game, item drops, progression from wood to stone to iron to diamond.
* **Crafting & smelting** – 2×2 and 3×3 shaped / shapeless recipes, furnaces with fuel, chests, stairs,
  slabs, tools, armour, bow & arrows, TNT, farming (hoe → farmland → wheat → bread).
* **Mobs** – cows, pigs, sheep, chickens, zombies, skeletons (they shoot!), creepers (they explode!),
  spiders. Hostiles spawn in the dark (caves and night), burn in daylight, drop loot.
* **Creative mode** – flying (double-tap Space), instant breaking, full block palette.
* **Saving** – worlds, edited chunks, chests, furnaces, inventory and time are stored in IndexedDB.
* Procedural pixel-art textures, synthesized sound effects and ambient music (Web Audio).

## Controls

| Key | Action |
| --- | --- |
| `W` `A` `S` `D` | Move (`D` = right, `A` = left) |
| `Space` | Jump / swim up / fly up |
| `Shift` | Sprint (or double-tap `W`) |
| `C` | Sneak (hold) – you won't fall off edges |
| Mouse | Look · **LMB** mine / attack · **RMB** place / use / eat / draw bow |
| `1`–`9`, wheel | Hotbar |
| `E` | Inventory / 2×2 crafting (creative palette in creative mode) |
| `Q` | Drop item (`Shift+Q` whole stack) |
| `V` | Third-person camera |
| `T` or `/` | Chat & commands (`/help`) |
| `F3` / `F1` / `F2` | Debug info / hide HUD / screenshot |
| `Esc` | Pause |

Handy commands: `/gamemode creative`, `/time set day`, `/give diamond_pickaxe`, `/tp x y z`,
`/summon creeper`, `/weather rain`, `/difficulty 0-3`.

## Notes

* Needs a browser with WebGL2 (any current Chrome, Edge, Firefox or Safari). A discrete / modern GPU
  is recommended for render distances above 8; the game lowers the distance automatically if it
  runs very slowly (toggle in the source via `settings.autoQuality`).
* The game uses `localStorage` for settings and `IndexedDB` for worlds. Private windows may not keep saves.
