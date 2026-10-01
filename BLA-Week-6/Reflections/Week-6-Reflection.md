# Week 6 Reflection

During Week 5 and Week 6, I moved from learning individual AWS data services to thinking more about how they connect inside a Generative AI application.

The first topic that became clearer for me was Amazon OpenSearch. At the beginning, terms such as shards, replicas, semantic search, hybrid search, HNSW, and IVF felt like separate concepts. After studying the flow from documents and indices to vector retrieval, I understood why those pieces exist and how OpenSearch can work as the retrieval layer for an AI application.

The second challenge was comparing vector storage choices. OpenSearch, S3 Vectors, Aurora with pgvector, and DynamoDB Vector Indexes can all be used around vector data, so I initially found it difficult to understand why AWS provides several options. What helped me was comparing them based on the application's existing data. If the application already depends on PostgreSQL, Aurora with pgvector can keep structured data and embeddings together. If operational data or chat history is already in DynamoDB, vector indexes can keep semantic search close to that data. OpenSearch provides richer search features, while S3 Vectors focuses more on large-scale and cost-conscious vector storage.

The third thing I learned is that the work does not stop when vectors are stored. Business data changes, so embeddings and indexes need maintenance. Reranking can also improve retrieval after the first vector search.

The S3 section helped me connect AI architecture with normal cloud design decisions. Storage classes, Lifecycle Rules, replication, encryption, logs, and Access Points are not AI models, but they still affect whether a GenAI system is affordable, secure, and reliable.

My biggest takeaway from this BLA is that a good Generative AI application is built from several layers. The Foundation Model is important, but the application also needs correct source data, appropriate storage, reliable retrieval, regular updates, and security around the data.
