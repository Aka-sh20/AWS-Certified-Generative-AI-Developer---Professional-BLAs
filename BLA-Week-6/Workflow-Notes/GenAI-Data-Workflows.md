# GenAI Data Workflows

These are the main workflows I understood while preparing the Week 6 BLA. They are written as study diagrams so I can see how the AWS services connect together.

## 1. OpenSearch Retrieval Workflow

```mermaid
flowchart LR
    A[User Question] --> B[Create Query Embedding]
    B --> C[Amazon OpenSearch]
    C --> D[Retrieve Relevant Information]
    D --> E[Amazon Bedrock]
    E --> F[Generated Answer]
```

The Foundation Model generates the answer. OpenSearch helps decide which source information should be sent to the model as context.

## 2. S3 Vectors Retrieval Workflow

```mermaid
flowchart LR
    A[User Question] --> B[Create Embedding]
    B --> C[query_vectors]
    C --> D[S3 Vector Index]
    D --> E[Relevant Vector Records]
    E --> F[Knowledge Base / AI Application]
```

S3 Vectors provides another storage layer for embeddings. The vector search retrieves information, while the AI application uses that information afterward.

## 3. Updating a Vector Store

```mermaid
flowchart LR
    A[Updated Source File] --> B[Change Detected]
    B --> C[EventBridge / Processing Workflow]
    C --> D[Create New Embeddings]
    D --> E[Update Vector Store]
```

The purpose of this workflow is to reduce the chance that an AI application keeps retrieving an older version of business information.

## 4. Reranking Workflow

```mermaid
flowchart LR
    A[Query] --> B[Vector Search]
    B --> C[Relevant Chunks]
    C --> D[Reranker]
    D --> E[Best Chunks First]
    E --> F[Foundation Model]
```

Reranking happens after retrieval. It improves the order of the retrieved chunks instead of replacing the vector store.

## 5. S3 Data Lifecycle for GenAI Source Files

```mermaid
flowchart LR
    A[Active Source Data] --> B[S3 Standard]
    B --> C[Standard-IA]
    C --> D[Glacier]
    D --> E[Expiration if Policy Allows]
```

This shows how older GenAI source data can move into lower-cost storage instead of staying forever in the most active class.

## 6. Complete GenAI Data Management View

```mermaid
flowchart TD
    A[Source Documents in S3] --> B[Process / Prepare Data]
    B --> C[Create Embeddings]
    C --> D[Vector Store]
    D --> E[Retrieve Relevant Chunks]
    E --> F[Rerank Results]
    F --> G[Amazon Bedrock]
    G --> H[Generated Answer]
    A --> I[Lifecycle / Replication / Encryption]
    I --> J[Cost and Security Management]
```

This final view helped me understand that retrieval quality, storage cost, security, and data freshness are all part of the same GenAI data architecture.
