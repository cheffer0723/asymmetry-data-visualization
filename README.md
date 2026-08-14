# Asymmetry Architecture City

This repository hosts a static, repository-derived city view of the Asymmetry codebase.

## Boundaries

- `cheffer0723/asymmetry` remains the source-of-truth product repository.
- This repository contains a committed, read-only snapshot of that repository's architecture graph.
- Its GitHub Pages deployment is independent of the product deployment and does not write back to the product repository.
- The existing Pages workflow in `.github/workflows/deploy.yml` remains unchanged.

## Snapshot

`architecture-map.json` was generated from `cheffer0723/asymmetry` commit `66aa5e2d69bf9cb5d9ca4e9afdcc2e362dca681f` on 2026-08-14. The city viewer loads that graph directly and preserves source-derived paths, domain grouping, evidence labels, and relationship confidence.

Refreshing the visual is a deliberate snapshot update in this repository; it is not coupled to the near-release product repository.

## Visual reading model

District substrates establish the codebase's major domains. Repository files resolve into towers, symbols resolve into circuit modules, and the thin illuminated traces prioritize the graph's evidence-labelled relationships. Moving pulses are schematic relationship indicators, not claims about production traffic or users.
