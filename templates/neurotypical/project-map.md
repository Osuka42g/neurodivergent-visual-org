---
mode: neurotypical
template: project-map
---
# Neurotypical Project Map Templates

## Project Phase Map

```mermaid
flowchart LR
    subgraph Phase1[Phase 1: Discovery]
        A1[Requirements] --> A2[Research]
        A2 --> A3[Feasibility]
    end

    subgraph Phase2[Phase 2: Design]
        B1[Architecture] --> B2[UI/UX]
        B2 --> B3[Database Schema]
    end

    subgraph Phase3[Phase 3: Implementation]
        C1[Backend] --> C2[Frontend]
        C2 --> C3[Integration]
    end

    subgraph Phase4[Phase 4: Launch]
        D1[Testing] --> D2[Deployment]
        D2 --> D3[Monitoring]
    end

    Phase1 --> Phase2 --> Phase3 --> Phase4
```

## Dependency Diagram

```mermaid
graph TB
    A[Component A] --> C[Component C]
    B[Component B] --> C
    C --> D[Component D]
    C --> E[Component E]
    D --> F[Final Product]
    E --> F

    style A fill:#e8f4f8
    style B fill:#e8f4f8
    style F fill:#d4edda
```

**Characteristics:**
- Clear phase separation
- Dependency relationships explicit
- Standard project management format
- Assumes sequential execution capability
