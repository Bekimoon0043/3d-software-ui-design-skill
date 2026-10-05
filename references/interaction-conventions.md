# Interaction Conventions for 3D Software

## Navigation (Industry Standard Defaults)
- Orbit / Rotate view: Middle mouse button drag (or Alt + LMB)
- Pan: Shift + Middle mouse (or Alt + MMB, or middle + Shift)
- Zoom: Mouse wheel or Ctrl + Middle mouse drag
- Frame selected: Numpad . or F
- Frame all: Home or A (in some tools)
- Orthographic / Perspective toggle: Numpad 5
- View presets: Numpad 1/3/7 (front/side/top) + Ctrl for opposite

Always provide alternative schemes (Maya, 3ds Max, tablet, trackpad, VR controllers).

## Selection
- Single select: LMB click
- Multi-select: Shift + LMB
- Deselect: Ctrl + LMB or click empty space
- Box select: Drag LMB (or B then drag)
- Lasso / Circle select: Common secondary modes
- Select linked / similar / hierarchy shortcuts are expected
- Clear visual distinction between active element and other selected elements

## Transform
- Move / Rotate / Scale gizmos must be large enough, high contrast, and mode-colored (usually RGB for XYZ).
- Free transform + axis constraint (click axis or hold middle mouse / Shift).
- Numeric input for precise values (type while gizmo active or in properties).
- Local vs Global vs View vs Normal orientation modes.
- Pivot point options (median, active, 3D cursor, individual origins).

## Modes
Clearly communicate and switch between:
- Object Mode
- Edit Mode (vertices/edges/faces)
- Sculpt Mode
- Pose Mode
- Paint / Weight / Texture modes
- Draw / Annotation modes

UI, available tools, and selection behavior must change consistently with mode.

## Gizmos & Overlays
- Keep gizmos non-destructive and toggleable.
- Overlays (grid, axes, statistics, wireframe, face orientation) should be per-viewport and savable.
- Active tool should give immediate visual feedback in the viewport (preview, brush size, falloff, etc.).

## Command Access
- Global searchable command palette is now expected (Ctrl/Cmd + K or Space/F3).
- Pie menus or radial menus for fast context actions.
- Right-click context menus that are rich but not overwhelming.
- Keyboard shortcuts visible in every menu and tooltip.
