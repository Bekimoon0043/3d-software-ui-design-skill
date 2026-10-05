---
name: 3d-software-ui-design
description: Design high-quality user interfaces and interaction patterns for 3D modeling, CAD, sculpting, animation, and spatial software. Use when the user is building, redesigning, or improving the UI of tools for 3D designers — including viewport layouts, toolbars, panels, gizmos, workspaces, command palettes, and domain-specific patterns from Blender, Cinema 4D, Maya, Fusion 360, or similar. Triggers include 3D software UI, CAD interface design, viewport UX, modeling tool layout, 3D app panels, spatial UI, Blender-like interface, and any request to make software better for 3D artists or designers.
---

# 3D Software UI Design

## Overview

Specialize in designing professional interfaces for software used by 3D designers. Encode industry conventions, proven layout patterns, and usability principles that general web UI knowledge does not cover. Focus on dense, expert-oriented tools where the 3D viewport is the primary workspace.

## Core Principles

Apply these first when designing or reviewing any 3D software interface:

1. **Viewport is king** — Maximize continuous screen real estate for the 3D view. UI chrome must stay secondary and collapseable.
2. **Expert density + progressive disclosure** — Support power users with dense information and shortcuts while keeping entry points discoverable for newcomers.
3. **Industry convention first** — Follow established patterns from Blender, Cinema 4D, Maya, 3ds Max, Fusion 360, FreeCAD, and similar tools unless there is a clear, tested reason to deviate.
4. **Direct manipulation** — Prefer gizmos, handles, and in-viewport controls over modal dialogs whenever possible.
5. **Non-blocking & reversible** — Every action should be undoable. Heavy operations must not freeze the viewport or UI.
6. **Consistency of interaction model** — Orbit/pan/zoom, selection, transform, and navigation must behave predictably across the entire application.

## Standard Layout Patterns

Recommend and design around these proven structures:

### Classic Professional Layout (most common)
- Top menu bar (File, Edit, View, tools, Help)
- Horizontal toolbar or ribbon for frequent actions (just below menu or as floating strips)
- Large central 3D viewport(s) — support multi-view (perspective + orthographic)
- Left or right vertical tool shelves / mode-specific toolbars
- Right or bottom property / inspector panels (context-sensitive)
- Outliner / hierarchy / scene tree (usually left or right, collapsible)
- Bottom timeline / dope sheet / graph editor for animation tools
- Status bar with mode, selection info, and coordinates

### Key Variations
- **Blender-style**: Highly customizable workspaces, area splitting, pie menus, search (F3/Space), N-panel properties.
- **Cinema 4D / Maya-style**: Dockable managers, Attribute Editor / Object Manager, command shelf.
- **CAD/parametric (Fusion, FreeCAD, SolidWorks)**: Ribbon or tabbed toolbars, feature tree, timeline of operations, constrained sketches.
- **Modern hybrid**: Command palette (Ctrl+K / Cmd+K), searchable tool menus, adaptive toolbars that change by mode (Object / Edit / Sculpt / Paint).

Always make panels dockable, floatable, and savable as named workspaces.

## Viewport & Interaction Design

- Default navigation: middle-mouse orbit (or Alt+LMB), Shift+middle pan, scroll zoom. Provide alternatives (trackpad, tablet, VR).
- Selection: LMB select, Shift multi-select, box/lasso/circle select. Clear active vs selected distinction.
- Transform gizmos: Clear, high-contrast, mode-aware (translate/rotate/scale). Support freeform + axis constraints.
- In-viewport overlays: Grid, axes, selection outlines, measurement, active tool feedback — all toggleable and non-destructive.
- Camera controls: Frame selected, frame all, walk/fly mode, orthographic toggle, camera lock.
- Multi-viewport layouts: Quad view, custom splits, synchronized cameras when useful.

## Panel & Information Architecture

- **Outliner / Hierarchy**: Tree with expand/collapse, visibility/lock icons, search/filter, drag-reorder, collections/layers.
- **Properties / Inspector**: Context-sensitive. Tabs or sections for Object, Data, Material, Modifiers, Constraints, etc. Use consistent icon + label + value layout.
- **Tool Settings**: Appear near the tool or in a dedicated shelf. Show only relevant options for the current tool/mode.
- **Modifiers / Nodes / Stacks**: Clear order, mute/enable toggles, drag to reorder, apply/copy/paste.
- Search everything: Global command search is mandatory for complex tools.

## Usability Rules Specific to 3D Tools

- Prefer icons + tooltips + optional labels. Icons must be recognizable at 16–24 px.
- Keyboard-first for experts: Every major action needs a shortcut. Show shortcuts in menus and tooltips.
- Mode awareness: UI and available tools change clearly when entering Edit Mode, Sculpt Mode, Pose Mode, etc.
- Error prevention: Soft constraints, confirmation only for destructive irreversible actions, clear feedback on invalid states.
- Performance: UI must stay responsive during heavy viewport updates. Use background workers, progressive refinement, and level-of-detail where needed.
- Accessibility: High contrast themes, scalable UI, keyboard navigation paths, screen-reader friendly labels for non-viewport elements.

## Design Process Guidance

When helping the user:

1. Clarify the primary user (modeling artist, CAD engineer, animator, technical artist) and core tasks.
2. Identify the dominant reference tools the target users already know.
3. Propose a base layout and justify deviations.
4. Design mode-specific toolsets and property panels.
5. Specify interaction details (gizmos, selection, navigation).
6. Define workspace presets and customization model.
7. Call out performance, discoverability, and onboarding considerations.
8. Suggest prototype fidelity (wireframes → interactive mockups → engine integration).

## Common Pitfalls to Avoid

- Over-cluttering the viewport with permanent UI.
- Hiding critical tools behind deep nested menus.
- Inconsistent left/right mouse button behavior.
- Modal tools that lock the user out of navigation.
- Poor visual hierarchy between active tool, selected objects, and background.
- Ignoring multi-monitor and high-DPI realities of professional 3D artists.
- Treating the interface like a website or mobile app.

## References

Load these for deeper detail when needed:
- `references/blender-ui-deep-dive.md` — In-depth Blender interface architecture, workspaces, editors, pie menus, Outliner, and design lessons
- `references/layout-patterns.md` — Detailed comparisons of major 3D software layouts (Blender, Cinema 4D, Maya, 3ds Max, Fusion 360, FreeCAD)
- `references/interaction-conventions.md` — Navigation, selection, and gizmo standards across 3D tools
- `references/usability-principles.md` — Refined principles for complex 3D/parametric tools
