# Diagram 3 – AgentCore Deployment Architecture

```mermaid
flowchart TD
    A[User / Application] --> B[AgentCore Runtime]
    B --> C[AI Agent]
    C --> D[AgentCore Memory]
    C --> E[AgentCore Gateway]
    E --> F[API / Lambda / Business Service]
    C --> G[Identity and Policies]
    C --> H[MCP Tools / External Systems]
    C --> I[Monitoring and Evaluation]
    C --> J{Confidence / Risk Check}
    J -->|Normal case| K[Automatic Response]
    J -->|High risk / uncertain| L[Human Review]
    L --> K
    K --> M[Final Response]
```

This diagram shows the main parts needed to run an AI agent safely in a real application, including memory, tools, security, monitoring, MCP, and human review.
