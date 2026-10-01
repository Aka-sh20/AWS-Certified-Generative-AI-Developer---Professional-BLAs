# Week 5 Progress

## Focus

This week I continued from the data preparation topics from the previous part of the course and moved into **Amazon OpenSearch Service**. My main goal was to understand how OpenSearch organizes and searches large amounts of data and why it is useful for Generative AI retrieval.

## What I Studied

I started with the basic OpenSearch structure, including documents, indices, shards, and replica shards. I learned why an index is divided into shards and how this allows storage and search work to be spread across multiple nodes. I also studied how replica shards improve availability and can help with read requests.

After the basic structure, I studied the managed Amazon OpenSearch Service, Zone Awareness, and the Hot, UltraWarm, and Cold storage options. This helped me understand that not all searchable data needs the same level of performance or cost.

I then moved into Index State Management, OpenSearch security, common performance problems, and OpenSearch Serverless. One thing I learned here is that OpenSearch is powerful, but it should be used for search and analytics workloads rather than treated as a replacement for every database service.

The last part of my Week 5 study focused on OpenSearch as a vector store. I reviewed semantic search, hybrid search, Approximate Nearest Neighbor search, HNSW, IVF, and how OpenSearch can retrieve relevant context for Amazon Bedrock.

## What Became Clearer

The biggest improvement for me was understanding the difference between normal keyword search and semantic vector search. Keyword search depends more on exact terms, while semantic search can retrieve information with similar meaning even when the wording is different.

I also became more comfortable with the idea that OpenSearch does not generate the final AI answer. It works as the retrieval layer that finds useful information, while the Foundation Model uses that retrieved context to create the response.

## Challenge

The most confusing part was understanding shards, replicas, and the ANN search methods at the same time. I reviewed them separately first and then connected them back to the full OpenSearch architecture. This made the flow easier to understand.

## Next Step

After OpenSearch, I planned to continue with other AWS vector storage choices such as S3 Vectors, Aurora with pgvector, and DynamoDB Vector Indexes so I could compare how different AWS services fit different GenAI data requirements.
