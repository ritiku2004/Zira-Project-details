# UML Diagrams for Gojira Project

This folder contains source files for UML diagrams used in the project documentation:

## Diagram Types (slide-friendly sources)

The `*-slide.mmd` files are horizontal, compact Mermaid sources optimized for slides. Files:

- `component-slide.mmd` — system component overview (LR)
- `class-data-model-slide.mmd` — class/data model (LR)
- `sequence-signin-slide.mmd` — login sequence (compact)
- `use-case-slide.mmd` — use-case overview (LR)
- `activity-slide.mmd` — activity/task flow (LR)
- `deployment-slide.mmd` — deployment topology (LR)
- `erd-slide.mmd` — compact ERD for slides
- `dfd-level-0-slide.mmd`, `dfd-level-1-slide.mmd`, `dfd-level-2-slide.mmd` — DFD levels (LR)
- `object-slide.mmd` — sample object instances (LR)

## Generating images from Mermaid sources

Recommended: use `@mermaid-js/mermaid-cli` (`mmdc`) to export PNG/SVG sized for slides.

Install (project root):
```powershell
npm install -D @mermaid-js/mermaid-cli
```

Example exports (PowerShell):
```powershell
# Architecture (wide banner)
npx mmdc -i diagrams/component-slide.mmd -o diagrams/component-1920x540.png -w 1920 -H 540

# ERD for slide (16:9)
npx mmdc -i diagrams/erd-slide.mmd -o diagrams/erd-1600x900.png -w 1600 -H 900

# DFD / Activity examples
npx mmdc -i diagrams/dfd-level-1-slide.mmd -o diagrams/dfd-level-1-1600x600.png -w 1600 -H 600
```

Notes:
- The `*-slide.mmd` files are already LR/horizontal and compact vertically to suit PPT slides.
- If you want different image sizes (taller or shorter), change `-w` and `-H`.
