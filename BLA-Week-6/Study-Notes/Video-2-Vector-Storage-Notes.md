# Video 2 Study Notes – AWS Vector Storage Choices

## Topic

**AWS Vector Storage Choices: S3 Vectors, Amazon Aurora, and DynamoDB**

## Why There Are Multiple Choices

Different applications already store data in different systems. A company may keep documents in S3, structured business records in PostgreSQL, or live operational data and chat history in DynamoDB. Because of this, the vector storage choice should fit the application's existing data and access pattern.

## Amazon S3 Vectors

S3 Vectors stores embeddings inside a vector structure connected with Amazon S3.

Basic structure:

```text
S3 Vector Bucket
   ↓
Vector Index
   ↓
Vectors + Metadata
```

A vector record can contain a key, the embedding itself, and metadata. The `put_vectors` operation adds vectors to the index, while `query_vectors` searches using another vector.

S3 Vectors can integrate with Amazon Bedrock Knowledge Bases. It is useful when an application needs large-scale vector storage and cost is an important part of the design.

## Amazon RDS and Aurora

Amazon RDS is a managed relational database service. In a GenAI application, the Foundation Model may understand natural-language questions, while RDS stores trusted business facts such as customer information, order status, prices, and inventory.

Aurora PostgreSQL can use **pgvector**. This adds a vector data type to PostgreSQL so embeddings can be stored alongside normal relational columns.

Example:

```text
Product_ID | Name | Price | Category | Description_Vector
```

This allows SQL filtering and vector similarity to work together. For example, vector search can find products matching the meaning of “lightweight laptop for programming,” while SQL can enforce `Price < 1000`.

## DynamoDB and GenAI

DynamoDB is a managed NoSQL database designed for high-scale, low-latency operational access.

GenAI use cases can include:

- Current application information
- Chat history
- Saved user preferences
- AI-agent memory
- Context for later conversations

DynamoDB Vector Indexes allow embeddings to stay close to operational data. The `SearchVectors` API can perform ANN similarity searches.

The course covers cosine, Euclidean, and dot-product distance functions.

## Comparing the Options

- **S3 Vectors** – large vector collections and cost-focused storage
- **Aurora + pgvector** – relational PostgreSQL data plus vector similarity and SQL filtering
- **DynamoDB Vector Indexes** – operational data, chat history, or AI memory already stored in DynamoDB
- **OpenSearch** – richer search features including keyword, vector, and hybrid search

## My Main Takeaway

Instead of asking which vector store is always best, I should first ask where the data already lives, how often it is searched, how fast retrieval needs to be, and what type of filtering or transactions the application needs.
