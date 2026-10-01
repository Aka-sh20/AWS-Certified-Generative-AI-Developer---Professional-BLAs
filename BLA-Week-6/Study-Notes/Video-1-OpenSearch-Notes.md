# Video 1 Study Notes – Amazon OpenSearch

## Topic

**Amazon OpenSearch: From Search Engine to GenAI Vector Store**

## OpenSearch Basics

Amazon OpenSearch is a search and analytics platform. It can support full-text search, log analytics, application monitoring, security analytics, and other workloads where large amounts of information need to be searched or analyzed.

A **document** is one searchable item. An **index** is a searchable collection of related documents. An index can become too large for one machine, so OpenSearch divides it into **shards**. Each shard can live on a different node, which distributes storage and search work.

A **primary shard** is the main copy of part of an index. A **replica shard** is an additional copy. Replicas help with availability and can also handle read requests.

## Managed OpenSearch

Amazon OpenSearch Service manages much of the underlying infrastructure, but the user still chooses important settings such as capacity, storage, networking, and domain configuration.

OpenSearch can use different storage levels:

- **Hot** – active data that needs fast performance
- **UltraWarm** – searchable data with fewer writes and lower storage cost
- **Cold** – older information that is accessed only occasionally

**Index State Management (ISM)** can automatically move an index between stages, change it to read-only, adjust replicas, create snapshots, or delete old indices.

## Security and Serverless

OpenSearch security can use resource-based policies, IAM identity policies, IP restrictions, request signing, VPC networking, and Amazon Cognito for dashboard access.

OpenSearch Serverless reduces the amount of capacity planning needed. It uses collections and OpenSearch Compute Units instead of a traditional provisioned domain model.

## OpenSearch for Generative AI

OpenSearch can store vector embeddings and search by meaning. A typical retrieval flow is:

```text
User Question
   ↓
Create Query Embedding
   ↓
Search OpenSearch
   ↓
Retrieve Relevant Information
   ↓
Send Context to Bedrock
   ↓
Generate Answer
```

**Semantic search** uses vector similarity to search by meaning. **Hybrid search** combines vector similarity with traditional keyword search.

Large vector collections often use Approximate Nearest Neighbor methods. HNSW uses a graph structure, while IVF groups vectors before searching. These methods improve speed by avoiding a full comparison with every stored vector.

## My Main Takeaway

OpenSearch can work as the retrieval engine between business data and a Foundation Model. It does not normally generate the final answer; it helps find the information that should support the answer.
