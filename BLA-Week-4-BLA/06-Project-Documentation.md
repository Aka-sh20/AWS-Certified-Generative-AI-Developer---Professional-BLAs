# Project Documentation

## Project Topic

Improving, protecting, and preparing a Generative AI application on AWS.

## Purpose

The purpose of this work was to understand how a Generative AI system can be improved after the basic model or RAG setup is already working.

The three main areas were:

1. Improve retrieval quality.
2. Add safety and control.
3. Prepare and manage data correctly.

## Stage 1 – Improve RAG

The RAG system needs good chunks, useful embeddings, metadata, fresh data, and good retrieval.

A simple flow is:

```text
Documents
   ↓
Chunking
   ↓
Embeddings
   ↓
Vector Store
   ↓
Retrieval
   ↓
Relevant Context
```

## Stage 2 – Add Safety and Control

After retrieval, the application also needs controls.

Important topics included:
- Bedrock Guardrails
- Contextual Grounding
- Automated Reasoning
- Token-level redaction
- Prompt Management
- Bedrock Flows
- Prompt injection protection

## Stage 3 – Prepare Data

Real-world data may come from many sources and may need processing before it can be used.

The AWS services covered include:
- Bedrock Data Automation
- SageMaker Data Wrangler
- AWS Glue
- CloudWatch
- Amazon Transcribe
- Amazon Comprehend

## Final Architecture

```text
Raw Data
   ↓
Prepare / Extract / Clean
   ↓
Chunk Data
   ↓
Create Embeddings
   ↓
Knowledge Base / Vector Store
   ↓
Retrieve Useful Context
   ↓
Guardrails + Prompt Controls
   ↓
Foundation Model
   ↓
Final Response
   ↓
Evaluate and Monitor
```

## Main Point

A real Generative AI application is more than a model connected to a prompt. Good data, retrieval, safety, monitoring, and evaluation are all important parts of the complete system.
