---
name: design-language-compiler
description: Analyze a real website URL with browser automation plus LLM reasoning to produce semantic design-language artifacts and Chinese or English reports. Use when the user provides a URL and asks for design language analysis, visual language, layout grammar, component semantics, interaction semantics, scene/component/layout/interaction graphs, or report.zh.md.
---

# Design Language Compiler

Use this skill to turn a live URL into semantic design-language outputs.

## Workflow

1. Confirm the URL, output language, depth, and target surfaces.
2. Open the page with the best available browser runtime in the current environment.
3. Collect desktop and mobile first-meaningful states when feasible.
4. Probe only safe non-destructive interactions when they improve understanding.
5. Normalize browser observations into semantic evidence.
6. Use the LLM to synthesize the site's design philosophy, visual language, layout grammar, component semantics, interaction semantics, diagnostics, and confidence.
7. Write the required artifacts.
8. Validate outputs and check for forbidden leakage.

## Reading Order

Read these references when needed:

- `references/agent-operating-contract.md`
- `references/browser-reading-workflow.md`
- `references/semantic-vocabulary.md`
- `references/schemas.md`
- `references/leakage-rules.md`

## Runtime Preference

Use browser runtimes in this order:

1. Host browser tool or in-app browser.
2. Project-local Playwright if already installed.
3. Browser diagnostic helper in this skill folder.
4. User-approved installation only if needed.

## Required Outputs

- `report.md`
- `report.zh.md` when Chinese output is useful or requested
- `design_language.json`
- `scene_graph.json`
- `component_graph.json`
- `layout_graph.json`
- `interaction_graph.json`
- `manifest.json`

## Guardrails

- Keep outputs semantic only.
- Do not expose selectors, DOM trees, raw CSS, source IDs, exact nesting, or pixel values.
- If evidence is thin, inspect a safe secondary state before compiling.
- If a risky action is required, stop and record diagnostics instead.

