# Agent Operating Contract

## Mission

Convert a real website URL into semantic design-language artifacts using browser evidence plus LLM reasoning.

## Inputs

- Required: one URL
- Optional: output language, depth, target surfaces, output directory

## Required Pipeline

1. Confirm scope.
2. Collect browser evidence.
3. Normalize evidence.
4. Split evidence into Visual Layer, DOM Structure, Layout Geometry, and Interaction Signals.
5. Synthesize with the LLM.
6. Write artifacts.
7. Validate outputs.

## Evidence Requirements

Capture at minimum:

- desktop first meaningful state
- mobile first meaningful state when feasible
- one safe interaction state when useful

## Quality Gates

- browser evidence source recorded
- JSON artifacts parse
- report and JSON agree
- forbidden leakage checked
- diagnostics recorded
