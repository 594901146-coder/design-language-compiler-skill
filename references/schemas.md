# Output Schemas

## Shared Rules

- Include `schema_version`.
- Use stable semantic IDs.
- Keep outputs semantic only.
- Include diagnostics when evidence is incomplete.
- Organize browser evidence and summaries into four layers: Visual Layer, DOM Structure, Layout Geometry, and Interaction Signals.

## Required Outputs

- `report.md`
- `report.zh.md` when Chinese output is useful or requested
- `design_language.json`
- `scene_graph.json`
- `component_graph.json`
- `layout_graph.json`
- `interaction_graph.json`
- `manifest.json`

## Report Sections

- Overview
- Design Philosophy
- Visual Language
- Layout Explanation
- Component Meaning
- Interaction Behavior
- Design Language Summary
- Confidence and Diagnostics

## Browser Evidence Summary

When recording browser observations, structure them by layer:

- `visual_layer`
- `dom_structure`
- `layout_geometry`
- `interaction_signals`

Each layer should contain semantic notes only, not source implementation details.
