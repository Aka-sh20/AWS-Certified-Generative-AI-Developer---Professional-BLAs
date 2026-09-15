# AWS Study Notes

## RAG Retrieval Stages

### Pre-Retrieval
This is where the source data is prepared. Documents can be cleaned, divided into chunks, converted into embeddings, and added to a search index.

### Retrieval
The system searches for information related to the user's question.

### Post-Retrieval
The retrieved information can be filtered or ranked before it is sent to the Foundation Model.

## Chunking

Chunking means splitting a large document into smaller pieces.

### Standard Chunking
- Uses a selected token size
- Can use overlap between chunks
- Simple and predictable
- Good for documents with a consistent structure

### Hierarchical Chunking
- Uses small child chunks and larger parent chunks
- Child chunks help with precise matching
- Parent chunks give more surrounding context

### Semantic Chunking
- Groups information based on meaning
- Can keep related sentences together
- Can cost more because a model may be used during chunking

### Easy Way I Remember It
- Standard = split by size
- Hierarchical = small + large chunks together
- Semantic = split by meaning

## Embeddings

Embeddings are numerical representations of information.

Larger vectors can represent more detail, but they also need more storage and processing.

Dense embeddings are commonly used in semantic search.

## Metadata

Metadata can include:
- Document ID
- Topic
- Department
- Category
- Date
- Author
- Section
- Access permission

Metadata can help improve filtering and ranking.

## Keeping a Knowledge Base Current

One possible flow is:

```text
Amazon S3
   ↓
AWS Lambda
   ↓
Bedrock Ingestion Job
   ↓
Updated Knowledge Base
```

## RAG Evaluation

Important evaluation areas include:
- Correctness
- Completeness
- Helpfulness
- Logical coherence
- Faithfulness
- Citation quality

## LLM as a Judge

A separate Foundation Model can evaluate another model's response using instructions, expected answers, or reference context.

## Multimodal Retrieval

Multimodal models can work with:
- Text
- Images
- Audio
- Video
- PDFs and other documents

## Amazon Bedrock Guardrails

Guardrails can help control:
- Unwanted topics
- Profanity
- Sensitive information
- PII
- Grounding
- Relevance

## Contextual Grounding

This checks whether the model's answer is actually supported by the context it received.

## Automated Reasoning

This can be useful for applications that need to follow logical business rules.

Example:

```text
Full-Time Employee + At Least 1 Year of Service
→ Eligible for Parental Leave
```

## Token-Level Redaction

Sensitive information can be checked before the prompt reaches the model and again after the model creates its response.

## Prompt Management

Prompt Management helps store, version, reuse, and test prompts.

Variables can look like:

```text
{{genre}}
{{number}}
```

## Bedrock Flows

Flows can connect:
- Input
- Prompts
- Models
- Knowledge Bases
- Conditions
- Output

## Prompt Engineering

A good prompt can include:
- Instructions
- Context
- Input data
- Output format

## Zero-Shot Prompting

The task is given without examples.

## Few-Shot Prompting

The model is given a few examples before the actual task.

## Chain-of-Thought

The course explains this as asking the model to work through a task step by step.

## Prompt Injection

Prompt injection is when a user tries to change the intended behavior of the application using malicious instructions.

## Prompt Leaking

Prompt leaking is an attempt to reveal system prompts, internal instructions, or sensitive information.

## Bias

Bias can come from:
- Training data
- Prompt design
- Model output

The model output should be evaluated instead of assuming it is always balanced.

## Bedrock Data Automation

BDA can process:
- Documents
- Images
- Audio
- Video

It can extract structured information from different media types.

## BDA Blueprints

Blueprints can define what information should be extracted.

Main uses:
- Classification
- Extraction
- Normalization
- Transformation
- Validation

## SageMaker Data Wrangler

Data Wrangler provides a visual environment for:
- Importing data
- Previewing data
- Visualizing data
- Transforming data
- Testing data
- Exporting data

## AWS Glue

AWS Glue is a serverless data integration service.

A Glue Crawler can scan data, identify structure, and create a schema in the Glue Data Catalog.

## Glue Data Quality

Glue Data Quality can check data using rules.

Failed checks can stop a job or be reported through CloudWatch.

## Amazon CloudWatch

CloudWatch is used to monitor AWS services, metrics, and system health.

## Amazon Transcribe

Amazon Transcribe converts speech to text.

It can support:
- Language identification
- PII redaction
- Custom vocabulary
- Custom language models
- Toxicity detection

## Amazon Comprehend

Amazon Comprehend can:
- Detect language
- Find key phrases
- Recognize entities
- Detect sentiment
- Perform custom classification
- Perform custom entity recognition
