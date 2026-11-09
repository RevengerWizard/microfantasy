# microfantasy

A small game made with Teascript

## Tilemap editor

Press `F1` while running to switch between the game and the built-in tilemap
editor. The editor uses `asset/tileset/platformer.png`, paints on an 8x8 grid,
and exports a loader-compatible Teascript map to `tilemap/editor.tea`.

- Left mouse paints; right mouse erases.
- Hold `I` to hide the canvas grid overlay.
- Press `C` to toggle collision mode. In collision mode, left-click adds
  collision rectangles and right-click removes them.
- In collision mode, `T` cycles solid/platform/stair, `[` and `]` adjust
  width, and `-` and `=` adjust height. Dimensions are measured in 8x8 cells.
- Press `E` to enter entity mode. `T` cycles supported enemies and items;
  left-click places the selected entity on the grid and right-click removes it.
- `Torch` is a checkpoint entity. Touching its flame updates the player
  respawn position; its only visible representation is the fire particle effect.
- Click the palette to select a tile. When the pointer is over the palette,
  use `Up` and `Down` to reveal tiles below the visible section.
- When the pointer is over the canvas, use the arrow keys to pan the map in
  8-pixel tile increments.
- Press `Enter` in the editor to play the map currently being edited.
- `Tab` selects the next layer; `N` creates a layer.
- `Up` and `Down` scroll the map vertically.
- `Ctrl+S` writes the current map.

With the debug console focused (`F3`, then `F2`), `/load <name>` loads a
saved map from `tilemap/<name>.tea`, for example `/load editor`, and
synchronizes the editor view. The mouse coordinate marker is also shown only
while the F3 debug overlay is visible.