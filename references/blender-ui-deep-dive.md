# Blender UI Deep Dive

Blender is the most influential open reference for modern 3D software interface design. Study it closely when designing for 3D artists.

## Core Architecture

### Areas and Editors
- The entire window is divided into non-overlapping **Areas**.
- Each Area contains exactly one **Editor** type (3D Viewport, Outliner, Properties, Timeline, Shader Editor, etc.).
- Users can split, join, and change the editor type of any area at any time.
- This extreme flexibility is both Blender’s greatest strength and the source of its learning curve.

### Workspaces
- Top-level tabs that switch the entire screen layout.
- Default workspaces: Layout, Modeling, Sculpting, UV Editing, Texture Paint, Shading, Animation, Rendering, Compositing, Scripting, Geometry Nodes, etc.
- Users can create, duplicate, and rearrange workspaces.
- Best practice when designing similar systems: provide sensible defaults + easy customization.

### Headers, Toolbars, and Sidebars
- Every editor has a **Header** (top bar with menus and mode selectors).
- **Toolbar** (T key) on the left of the 3D Viewport — contains active tools.
- **Sidebar** (N key) on the right — contains panels for Item, Tool, View, and add-on panels.
- Properties Editor (usually on the right) is tabbed and context-sensitive (Object, Modifier, Material, Render, etc.).

## Key Interaction Patterns Unique to Blender

- **Pie Menus**: Radial menus triggered by keys (e.g. ~ for view pie, Tab for mode pie in some configurations). Extremely fast for experts.
- **Search (F3)**: Global operator search. Essential for discoverability in a dense interface.
- **Right-click context menus** and **Quick Favorites**.
- **Modal operators**: Many tools enter a modal state (e.g. extrude, bevel) with on-screen help and numeric input.
- **Gizmos**: Transform gizmos, light gizmos, camera gizmos, force field gizmos — all toggleable.
- **Overlays**: Extensive per-viewport overlay system (wireframe, face orientation, statistics, annotations, etc.).

## Outliner & Collections
- Hierarchical scene organization via Collections (replacing older layers).
- Visibility, selectability, and renderability toggles per collection and object.
- Drag-and-drop parenting and collection assignment.
- Search and filtering are critical.

## Properties Editor Structure
Typical tabs (icons):
- Active Tool and Workspace settings
- Render Properties
- Output Properties
- View Layer
- Scene
- World
- Object
- Modifier
- Particles
- Physics
- Object Data (mesh, curve, armature, etc.)
- Material
- Texture
- Constraints
- etc.

Design lesson: Group properties by context and keep the most-used ones one click away.

## Strengths to Emulate
- Maximum screen real-estate for the 3D view.
- Extremely high customization without leaving the application.
- Consistent keyboard-driven workflow.
- Non-destructive modifiers and geometry nodes.
- Excellent multi-monitor support via multiple windows.

## Weaknesses to Improve Upon
- Initial overwhelm for new users (too many panels and options visible by default).
- Inconsistent discoverability of some features.
- Some older panels still feel dense and text-heavy.
- Theme and scaling can still be improved for high-DPI and accessibility.

## Design Recommendations Inspired by Blender
1. Make the viewport the undisputed primary surface.
2. Provide named, switchable workspaces as the top-level organization.
3. Allow free splitting and editor-type changing if the target users are professionals.
4. Always include a powerful global search.
5. Use pie menus or radial menus for high-frequency actions.
6. Keep tool settings and properties context-sensitive and close to the action.
7. Support saving and sharing custom layouts.
