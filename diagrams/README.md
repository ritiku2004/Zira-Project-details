# UML Diagrams for Gojira Project

This folder contains source files for UML diagrams used in the project documentation:

## Diagram Types

### 1. Component Diagrams
- `component.puml` / `component.mmd` - System component interactions
Purpose: Shows high-level system components and their relationships

### 2. Class Diagrams
- `class-data-model.puml` / `class-data-model.mmd` - Domain model classes
Purpose: Shows data structure and relationships between entities

### 3. Sequence Diagrams
- `sequence-signin.puml` / `sequence-signin.mmd` - Authentication flow
Purpose: Shows the login process interaction between components

### 4. Use Case Diagrams
- `use-case.puml` / `use-case.mmd` - System functionality
Purpose: Shows what users can do with the system

### 5. Activity Diagrams
- `activity.puml` / `activity.mmd` - Task lifecycle
Purpose: Shows the flow of task creation and updates

### 6. Object Diagrams
- `object.puml` / `object.mmd` - Instance examples
Purpose: Shows concrete examples of system objects

### 7. Deployment Diagrams
- `deployment.puml` / `deployment.mmd` - Runtime topology
Purpose: Shows how components are deployed

## Generating Images

### Using PlantUML (PowerShell)

With Java and PlantUML jar:
```powershell
java -jar .\tools\plantuml\plantuml.jar -tpng .\diagrams\*.puml
```

Using Docker:
```powershell
docker run --rm -v ${PWD}:/work plantuml/plantuml -tpng /work/diagrams/*.puml
```

### Mermaid
The `.mmd` files are embedded directly in the project README and rendered by GitHub.
