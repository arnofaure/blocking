# Changelog

All notable changes to Blocking Tool are documented here.

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
