# vwm - Vitt's Window Manager
My dwm build and configuration.

## Patches
- **dwm-systray-6.8** - system tray support
- **EWMH support** - `_NET_ACTIVE_WINDOW`, `_NET_CLIENT_LIST`,
  `_NET_CURRENT_DESKTOP`, `_NET_DESKTOP_NAMES`, `_NET_NUMBER_OF_DESKTOPS`,
  `_NET_DESKTOP_VIEWPORT`, `_NET_WM_DESKTOP`, `_NET_WM_WINDOW_TYPE`,
  `_NET_WM_WINDOW_TYPE_DIALOG`, `_NET_SUPPORTING_WM_CHECK`

## Modifications
### Mouse drag behavior (`movemouse` / `resizemouse`)
- Removed auto-float on grab: dragging a tiled window no longer automatically toggles it to floating
- Tiled windows move visually during drag and re-tile on release (via `arrange`)
- Dragging across monitors works: drop on another monitor to send it there and tile it

### Floating toggle (`togglefloating`)
- Explicit `togglefloating` (Mod+v) shrinks the window to 75% and centers it on the mouse cursor
- Size/position changes only happen on explicit float toggle, not on drag

### Focus monitor (`focusmon`)
- Warps cursor to the center of the target monitor on focus switch (Mod+h/l)

### Configure event handling
- Floating windows that resize off-screen are re-centered within the monitor
