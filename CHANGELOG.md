# Changelog

All notable changes to Blocking Tool are documented here.

## [0.2.0] - 2026-07-03

### Added
- Articulated character rig: shoulder, elbow, hip, knee and neck joints, each with its own slider to pose it by hand
- Stand / Sit / Lie pose presets built on that same joint system — Sit folds the hip/knee joints to roughly seat height instead of squashing the leg mesh, Lie tilts the whole body flat on the floor
- Characters now have two independent legs (each with its own knee), instead of a single shared leg mesh
- Skeleton view (characters only): swaps the solid mesh for colored bone cylinders and joint dots that track the live pose every frame — hands and face excluded
- "Save image" — export a JPEG of the main view at the current playhead position, cropped to the selected Frame ratio (buttons in both the Export panel and the timeline toolbar)
- 1:1 and 9:16 frame ratios
- `G` shortcut to toggle the floor grid
- App logo in the toolbar menu button (heading text moved into the opened dropdown), header/menu styling matched to storyboard.arnofaure.com
- Favicons, web app manifest, SEO/Open Graph meta tags, a dedicated Open Graph share image, and a screenshot in the README

### Changed
- Panel section headers: full color when collapsed, dimmed when expanded so slider/button content stays readable; white title text that dims on hover; icon moved onto its own dark badge, separate from the colored label
- Stronger hover outline on panel sections and a more visible white outline on the camera HUD
- Camera HUD repositioned away from the corner

### Fixed
- Elbow joint bent in the anatomically wrong direction
- Neck pivot was positioned at the head's center instead of its base, collapsing the skeleton view's neck bone to ~zero length

## [0.1.3] - 2026-07-02

### Fixed
- With "Smooth" curves on (the default), a move between just two keyframes — the most common case, e.g. a camera pan from A to B — had a constant, non-eased speed right from the first frame instead of easing in and out. Caused by the Catmull-Rom spline's phantom duplicate-point tangent at the very first/last keyframe of a track not actually being zero. The first and last segment of every track now use a proper ease in/out instead; interior segments (3+ keyframes) still blend through a smooth spline as before.

## [0.1.2] - 2026-07-02

### Added
- "Storyboard App" link in the menu, opening [storyboard.arnofaure.com](http://storyboard.arnofaure.com/) in a new tab

### Fixed
- Camera path line/markers were the same orange as the default first character color, making the path hard to spot in the scene. Changed to red.

## [0.1.1] - 2026-07-02

### Added
- "Shortcuts" menu item and modal listing every keyboard and mouse shortcut in the app
- Separate Width and Depth sliders for props (previously one "Width" slider scaled both X and Z together)

### Fixed
- Help modal's close button rendered outside the dialog, to the left of it — caused by the global button style's `width:100%` combined with `position:absolute; right:12px` pushing it past the left edge. Fixed by resetting width/margin on the close button.
- Missing visual space between "by" and "Arno Faure" (and "under" and the license link) in the page footer — replaced the plain space before each link with a non-breaking space

## [0.1.0] - 2026-07-02

Initial release.

### Added
- Main perspective view and top-down view of a 3D scene, with orbit/pan/zoom camera controls in both
- Characters (with stand/sit pose) and simple props (car, bus, wall, house, table, chair) — add, drag to move, rotate, scale
- Real-world size units for props (meters, feet & inches, inches)
- Double-click any name in the Characters/Objects list to rename it
- Lock a character/object in place with `L` to prevent accidental dragging
- Group two or more characters/objects (checkbox or Ctrl/Cmd-click) to move and keyframe them together; "Group selected" / "Ungroup"
- Camera height/tilt/pan controls and 14mm–200mm lens presets, mirrored in an on-screen HUD over the main view
- Aspect-ratio crop guides (16:9, 1.43, 1.85, 2.39) and a phi (golden ratio) composition grid overlay
- Camera path drawing (Shift-drag on the floor, in either view) with adjustable height and "follow path" playback
- Multi-track keyframe timeline per character/object/camera — add/delete keyframes, drag keyframes to retime them, color-tinted rows matching each object, smooth spline or per-segment easing
- Collapsible left-panel sections, with a "Collapse/Expand all" toggle
- Save/export/import shot lists as JSON
- Record timeline playback to a WebM video
- Undo (Ctrl/Cmd+Z)
- In-app Help overlay and GitHub link in the menu; page footer
