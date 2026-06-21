# Browser Reading Workflow

## Goal

Use browser automation to read a live URL as a normal user would, then turn what is observed into semantic evidence.

Structure browser evidence into four layers:

1. Visual Layer - visual prominence, tone, hierarchy, color and density cues.
2. DOM Structure - semantic regions, repeated groups, landmarks, and role-level meaning.
3. Layout Geometry - composition, grouping, spacing rhythm, and spatial relationships expressed semantically.
4. Interaction Signals - safe affordances, triggers, state changes, and intent cues.

## Runtime Order

1. Host browser tool or in-app browser.
2. Project-local Playwright if already installed.
3. Diagnostic helper if browser access is unclear.
4. User-approved installation only if absolutely needed.

## Observation Steps

1. Navigate to the URL and record the final URL and title.
2. Stabilize the page with bounded waits.
3. Observe desktop and mobile first-meaningful views when practical.
4. Capture the four layers in order: visual, structure, layout, interaction.
5. Explore only safe, non-destructive interactions.
6. Normalize observations into semantic evidence.

## Safe Interactions

- scroll
- hover
- focus
- open menu
- expand disclosure
- switch tab
- toggle non-destructive view

## Layer Notes

### Visual Layer

Record what the page feels like and what visually dominates, but do not report raw CSS or pixel values.

### DOM Structure

Record semantic groupings, roles, repeated blocks, and region boundaries, but do not expose selectors or element IDs.

### Layout Geometry

Record layout grammar and composition patterns, not coordinates or exact measurements.

### Interaction Signals

Record trigger, target summary, visible change, and semantic effect.

## Never Do

- submit forms
- login
- purchase
- publish
- delete
- upload
- grant permissions
- send sensitive data
