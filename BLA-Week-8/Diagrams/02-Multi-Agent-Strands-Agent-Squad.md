# Diagram 2 – Multi-Agent Workflow with Strands and Agent Squad

```mermaid
flowchart TD
    A[User Request] --> B[AWS Agent Squad Router]
    B --> C{Intent Classification}
    C --> D[Research Agent]
    C --> E[Technical Agent]
    C --> F[Order / Billing Agent]
    D --> G[Strands Tools]
    E --> H[Strands Tools]
    F --> I[Strands Tools]
    G --> J[Supervisor / Coordinator]
    H --> J
    I --> J
    J --> K[Combined Response]
    K --> L[User]
```

This diagram shows how Agent Squad can route work to specialized agents and how a supervisor can combine results when several agents are needed.
