# Mini Apps Builder

A small meta-workspace for designing and generating polished, single-file vanilla HTML mini apps.

The goal is simple: describe a useful local tool, generate one complete `.html` file, open it in a browser, and use it without a backend, build step, or server. This repo is meant for temporary-but-serious utilities: calculators, dashboards, cheatsheets, local data viewers, parsers, learning tools, planners, small workbenches, and client-side reports.

## What This Is

This is not a framework. It is a working system of prompts, standards, visual themes, and starter templates for producing self-contained browser apps.

Each generated app should feel like a real tool, not a demo:

- one complete `.html` output;
- vanilla HTML, CSS, and JavaScript;
- no required server;
- no required build pipeline;
- local persistence when useful;
- import/export when useful;
- modern UI, but restrained and purposeful;
- readable code that can be edited later.

## Repository Layout

```txt
mini-apps-builder/
  AGENTS.md
  meta-system-prompt.md
  README.md
  apps/
    README.md
  data/
    README.md
  examples/
    json-dashboard.html
    recipe-scaler.html
  prompts/
    app-request-template.md
  standards/
    app-checklist.md
    aesthetic-packs.md
    data-patterns.md
    design-system.md
    output-contract.md
    themes/
      tokyo-mono.css
  templates/
    single-file-app.html
```

## Core Files

- `AGENTS.md` tells Codex how to behave inside this repo.
- `meta-system-prompt.md` is the main generation contract.
- `templates/single-file-app.html` is the reusable baseline.
- `standards/` contains product, data, UI, output, and theme rules.
- `examples/` contains sanitized reference apps.
- `prompts/app-request-template.md` is a structured request template.

## Local Outputs

Generated apps and imported data are local by default:

- `apps/` is for generated user-specific HTML apps.
- `data/` is for local CSV/JSON imports, exports, and analysis artifacts.

Both directories are ignored by git except for their README and `.gitkeep` files. This is intentional: generated apps often contain private logic, embedded datasets, screenshots, or one-off work.

If a generated app becomes a clean public example, move a sanitized copy to `examples/`.

## Using With Codex

Clone the repo:

```bash
git clone <repo-url> mini-apps-builder
cd mini-apps-builder
```

Then ask Codex for a concrete tool:

```txt
Read AGENTS.md and meta-system-prompt.md.
Build a single-file mini app in apps/ for analyzing a local CSV.
Use Tokyo Mono. Include filters, import/export JSON, and a clean mobile layout.
```

Codex should:

- read `AGENTS.md`;
- use `meta-system-prompt.md` as the main contract;
- follow `standards/`;
- create the app inside `apps/`;
- keep local datasets and exports inside `data/`;
- avoid committing local/private outputs.

## Manual Prompt Flow

Use `meta-system-prompt.md` as the base instruction, then add a specific request:

```txt
I want a single-file mini app for planning weekly meals.
It should scale recipes, generate a shopping list, persist locally, and export JSON.
Use Notebook Warm.
```

The expected output is one complete `.html` file.

## Visual Themes

Themes live in `standards/aesthetic-packs.md`. Tokenized CSS can live in `standards/themes/`.

Current packs:

- `Workbench Calm`: practical, light, quiet, general-purpose.
- `Studio Glass`: more visual and expressive for creative tools.
- `Ledger Sharp`: compact and tabular for dashboards and calculators.
- `Notebook Warm`: editorial and comfortable for recipes, learning, and writing.
- `Tokyo Mono`: monochrome, serious, sleek, ideal for runbooks and technical tools.
- `Graphite Hacker`: darker graphite/charcoal, monospace-heavy, warmer technical feel.

## Design Bias

Generated apps should open directly into the useful workspace.

Prefer:

- dense but readable layouts;
- clear controls;
- compact toolbars;
- useful empty states;
- careful mobile behavior;
- code blocks and tables only where they help;
- restrained visual language;
- export/import flows for portability.

Avoid:

- marketing landing pages;
- decorative dashboards with no workflow;
- oversized hero sections;
- noisy color palettes;
- fake feature text;
- private data in tracked files.

## Data Patterns

Use the lightest storage that fits:

- `localStorage` for small state and preferences;
- `IndexedDB` for larger local datasets;
- JSON import/export for backups;
- CSV/Markdown/PDF/image exports when useful;
- SQLite/WASM only when the app really benefits from queries.

Remote scraping is limited by browser CORS. Prefer pasted HTML, uploaded files, local CSV/JSON, or CORS-friendly public endpoints.

## Publishing

This repo is meant to publish the builder, not local outputs.

Before pushing:

```bash
git status --short --ignored
```

Make sure private files under `apps/` and `data/` are still ignored.

Then:

```bash
git add .
git commit -m "Update mini apps builder workspace"
git remote add origin <repo-url>
git push -u origin main
```
