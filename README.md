# Asymmetry Architecture City

This repository hosts a static, repository-derived city view of the Asymmetry codebase: a public-safe visual map of the project's systems, surfaces, and verified repository structure. The live viewer starts with a lightweight CITY summary, then loads the full safety-filtered graph only when a visitor asks for deeper detail.

## Boundaries

- `cheffer0723/asymmetry` remains the source-of-truth product repository.
- This repository contains a committed, read-only snapshot of that repository's architecture graph.
- Its GitHub Pages deployment is independent of the product deployment and does not write back to the product repository.
- The existing Pages workflow in `.github/workflows/deploy.yml` remains unchanged.
- The public city snapshot excludes nodes and relationship metadata matching the viewer's protected-internals filter; no source-file contents are published by this viewer.

## Snapshot

`architecture-city-summary.json` is the lightweight first-load graph used for CITY mode. `architecture-map.json` was generated from `cheffer0723/asymmetry` commit `66aa5e2d69bf9cb5d9ca4e9afdcc2e362dca681f` on 2026-08-14. The viewer loads the full safety-filtered graph only when visitors choose deeper detail, preserving source-derived paths, domain grouping, evidence labels, and relationship confidence for entries that remain in scope.

Refreshing the visual is a deliberate snapshot update in this repository; it is not coupled to the near-release product repository.

## Visual reading model

District substrates establish the codebase's major domains, with footprint scaled from per-domain repository weight. Repository files resolve into towers whose footprint and height reflect source-weight signals such as lines, bytes, safe symbols, and headings; symbols resolve into circuit modules. The thin illuminated traces prioritize the graph's evidence-labelled relationships. Moving pulses are schematic relationship indicators, not claims about production traffic or users.

The city controls collapse into a compact tab on phones. Selecting a primary system tower opens that domain's expanded repository view; Reset View restores the city. Pixel-cloud blocks, district glow, and additional board illumination are intentionally schematic orientation cues, not source-derived runtime data.


## Current viewer

- `index.html` is the live GitHub Pages viewer.
- `architecture-city-summary.json` is the fast first-load CITY graph.
- `architecture-map.json` is the full safety-filtered graph.
- `source-manifest.json` records the source repository, commit, capture date, and source documents.
- `legacy/` preserves the earlier 2D explorer prototype so it does not compete with the live viewer.

## Public posture

The viewer should describe orientation, evidence boundaries, and snapshot status. It should not present source contents, private internals, production traffic, user activity, or live system guarantees.
