# Video 3 Study Notes – Vector Maintenance and Amazon S3

## Topic

**Keeping GenAI Data Reliable: Vector Maintenance and Amazon S3 Storage & Security**

## Keeping Vector Data Current

A vector store needs to stay synchronized with the source data. If a source document changes but the embeddings do not, the AI system may retrieve outdated information.

Ways to manage updates include:

- Incremental updates
- Real-time change detection
- Automated synchronization
- Scheduled refresh pipelines
- EventBridge-triggered workflows

A simple update flow can look like this:

```text
New or Changed Source File
   ↓
Event Detected
   ↓
Process Updated Content
   ↓
Create New Embeddings
   ↓
Update Vector Store
```

## Vector Index Maintenance

Over time, continuously adding, changing, or removing data can make an index less efficient. A maintenance process may rebuild and validate a new index before switching from the old one.

```text
EventBridge Trigger
   ↓
AWS Batch Job
   ↓
Create New Embeddings
   ↓
Build New Vector Database
   ↓
Validate New Index
   ↓
Replace Old Index
```

## Reranking

A vector search may return several relevant chunks, but the first result is not always the best one. A reranker evaluates the retrieved results again and places the most relevant chunks first.

```text
Query
   ↓
Vector Search
   ↓
Several Relevant Chunks
   ↓
Reranker
   ↓
Best Chunks First
   ↓
Foundation Model
```

## Amazon S3 Storage Classes

S3 storage classes are designed around different access patterns and cost requirements.

- S3 Standard
- Standard-Infrequent Access
- One Zone-Infrequent Access
- Glacier Instant Retrieval
- Glacier Flexible Retrieval
- Glacier Deep Archive
- Intelligent-Tiering

**Durability** means whether the object remains preserved over time. **Availability** means whether the object can be accessed when requested.

## Lifecycle and Replication

S3 Lifecycle Rules can move objects to cheaper storage or delete them after a defined period. Replication can create copies in the same Region or another Region.

- CRR – Cross-Region Replication
- SRR – Same-Region Replication

## S3 Encryption

The course covers four main approaches:

- SSE-S3
- SSE-KMS
- SSE-C
- Client-Side Encryption

SSE-KMS adds AWS KMS API calls into the request path, so KMS service quotas can become part of high-volume architecture planning.

Encryption in transit normally uses HTTPS with SSL/TLS.

## Access Logs and Access Points

S3 Access Logging records requests to a bucket and writes the logs to another bucket. The logging bucket should not be the same bucket being monitored because that can create a logging loop.

S3 Access Points create separate access paths and policies for different teams or applications. Access Points can also use VPC Origin for private access from inside a VPC.

## My Main Takeaway

A reliable GenAI system needs more than a model and vector database. The data must stay current, relevant, cost-efficient, protected, and accessible to the correct users.
