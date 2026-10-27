# Workflow Notes – Token Efficiency and Smart Model Selection

## Optimization Flow
```text
User Request
    ↓
Prepare Prompt + Context
    ↓
CountTokens
    ↓
Is Context Too Large?
    ├── Yes → Prune / Summarize / Compress
    └── No  → Continue
    ↓
Analyze Task Complexity
    ├── Simple → Smaller Model
    └── Complex → More Capable Model
    ↓
Control Output Size
    ↓
Return Response
    ↓
Monitor Token Usage / Latency / Errors in CloudWatch
    ↓
Evaluate and Improve
```

## RAG Optimization
```text
User Question
    ↓
Retrieve Candidate Chunks
    ↓
Rank + Metadata Filter
    ↓
Keep Most Relevant Context
    ↓
Foundation Model
    ↓
Answer
```
