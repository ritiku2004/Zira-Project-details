Diagrams
========

This folder contains source files for diagrams referenced in the project README. Two formats are provided:

- PlantUML sources (`*.puml`) — can be rendered to PNG/SVG using PlantUML (jar or Docker).
- Mermaid sources (`*.mmd`) — can be rendered by GitHub when embedded in Markdown or by Mermaid tools.

Files
- component.puml / component.mmd — component / integration diagram
- class-data-model.puml / class-data-model.mmd — data model / class diagram
- sequence-signin.puml / sequence-signin.mmd — signin sequence diagram
- deployment.puml / deployment.mmd — deployment topology

Generating images (PowerShell)

If you have `plantuml.jar` and Java:

```powershell
java -jar .\tools\plantuml\plantuml.jar -tpng .\diagrams\*.puml
```

Or using Docker (if Docker is available):

```powershell
docker run --rm -v ${PWD}:/work plantuml/plantuml -tpng /work/diagrams/*.puml
```

Mermaid

The `.mmd` files are plain Mermaid sources and can be embedded directly in Markdown files or rendered by local Mermaid tools.
