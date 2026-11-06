# Pixel Playground

**CTRL + PLAY · AI Game Development Workshop · NIT Calicut**

Collect sparks, dodge moving drones, and beat your best score. Every five sparks adds a level. Four drones start each round. Another spawns every three seconds, up to twelve active drones. Drone speed rises with level.

## Play locally

1. Extract the ZIP. Keep its folders together.
2. Double-click `index.html` to open it in a browser.
3. Select **Start game**. Move with **WASD** or the **arrow keys**. On a touch screen, hold the direction buttons under the arena.
4. Aim with the mouse and click the arena to shoot drones. Collecting a spark or destroying two drones in a row locks the gun for five seconds. A shot that leaves the arena without hitting a drone breaks the streak. Watch the Gun countdown above the arena.
5. If you hit a drone, choose **Play again**. Each new round resets the score and level. The best score is saved where the browser permits local storage.

The game runs offline. You only need a browser and a text editor. After editing a file, save it and refresh the browser.

## Find your way around

| File | What to edit |
| --- | --- |
| `index.html` | Title, mission, controls and legend |
| `style.css` | Page palette and layout, with colors grouped at the top |
| `game.js` | Arena colors in `THEME`, movement and difficulty in `RULES`, art in `draw()` |
| `starter/index.html` | Movement-only demo for the instructor or participants |
| `starter/starter.js` | Short game loop and two marked pickup exercise hooks |
| `EXERCISES.md` | Live demo sequence, Codex prompt and test checkpoints |

In the full game, `frame()` repeatedly calls `update()` and `draw()`. The update moves the objects, checks for collisions and changes the score or game state. The draw function paints the current state. `dt` is elapsed time in seconds, so speeds are expressed in pixels per second. Full-game positions are object centers. The starter uses top-left positions to match Canvas's `fillRect()`.

## Remix after the roulette

For an underwater theme, make the player a diver, sparks into pearls, and drones into jellyfish. Change the palette in `THEME` and `style.css`, set `collectiblePlural` to `"pearls"`, and update the mission and legend in `index.html`. Edit the collision headline in `endRound()`. Once the theme reads consistently, change one rule and play a round to see its effect.
