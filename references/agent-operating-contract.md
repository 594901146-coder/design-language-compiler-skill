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
4. Synthesize with the LLM.
5. Write artifacts.
6. Validate outputs.

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

