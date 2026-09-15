# Weekly Progress

This week I worked on three connected Generative AI topics.

I started with improving RAG systems. I already understood the basic idea of RAG, but this presentation helped me understand that retrieval quality depends on more than just connecting a Knowledge Base. I learned about pre-retrieval, retrieval, and post-retrieval. I also spent time understanding chunking because the size and type of chunks can change what information is retrieved.

The difference between standard, hierarchical, and semantic chunking took me some time to understand. Standard chunking is simple and based mainly on size. Hierarchical chunking uses smaller child chunks and larger parent chunks. Semantic chunking tries to keep information together based on meaning.

After that, I studied embeddings, metadata, and RAG evaluation. I learned that metadata can help filter or rank results, and that a RAG system should be tested for things like correctness, completeness, helpfulness, faithfulness, and citation quality.

The second video was about making Generative AI applications safer and more controlled. I learned about Bedrock Guardrails, contextual grounding, Automated Reasoning, and token-level redaction. This helped me understand that a production AI application should not depend only on the model to control sensitive or unsafe information.

I also studied Prompt Management and Bedrock Flows. Prompt Management can save and reuse prompts, while Bedrock Flows can connect prompts, models, Knowledge Bases, conditions, and other steps into a workflow.

The third video focused on data preparation. I learned that real business data may come from PDFs, images, audio, video, emails, databases, and other sources. Before using this information in Generative AI, it may need to be extracted, cleaned, organized, transformed, or validated.

I studied Bedrock Data Automation, SageMaker Data Wrangler, AWS Glue, CloudWatch, Amazon Transcribe, and Amazon Comprehend. The biggest thing I learned from this part is that each service solves a different problem, and they can be connected together when the application needs several data-preparation steps.

Overall, this week helped me understand that a useful Generative AI system needs good data, good retrieval, safety, monitoring, and testing in addition to a strong Foundation Model.
