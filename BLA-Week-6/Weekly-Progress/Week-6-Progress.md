# Week 6 Progress

## Focus

This week I continued from OpenSearch and studied other AWS storage choices for Generative AI. I also focused on what happens after vectors and source data are stored: how the data stays current, how retrieval can be improved, and how Amazon S3 can control cost and security over time.

## What I Studied

I first studied **Amazon S3 Vectors** and learned about vector buckets, vector indexes, metadata, `put_vectors`, and `query_vectors`. I also reviewed how S3 Vectors can work with Amazon Bedrock Knowledge Bases.

Next, I studied **Amazon RDS and Aurora PostgreSQL with pgvector**. This helped me understand how normal relational business data and vector embeddings can stay in the same database. The example of combining semantic product search with an exact SQL price filter made this easier for me to understand.

I then moved into **Amazon DynamoDB** and its GenAI use cases. I reviewed how DynamoDB can store operational data, chat history, and information that can act as long-term memory for an AI assistant. I also studied DynamoDB Vector Indexes and the `SearchVectors` API.

The next part focused on **vector-store maintenance and reranking**. I learned that embeddings can become outdated when source documents change, so the vector store needs a process for synchronization. I also learned how reranking can reorder retrieved chunks so the Foundation Model receives the most useful context first.

Finally, I studied **Amazon S3 storage and security**. I compared the major storage classes, durability and availability, Intelligent-Tiering, Lifecycle Rules, Cross-Region and Same-Region Replication, S3 encryption methods, encryption in transit, access logs, and S3 Access Points.

## What Became Clearer

This week helped me understand that Generative AI architecture is not only about the model. The data architecture also matters. The system needs the correct storage service, the vectors need to stay synchronized, older data should move to the correct storage class, and sensitive information must have the correct access and encryption controls.

## Challenge

The most difficult part was comparing OpenSearch, S3 Vectors, Aurora, and DynamoDB because they can all be involved in vector-based applications. I started comparing them by where the original data lives and what the application needs instead of trying to memorize one service as the best option.

## Next Step

My next course section will move into Agentic AI and how models can use tools, knowledge, memory, and multi-step workflows to complete tasks.
