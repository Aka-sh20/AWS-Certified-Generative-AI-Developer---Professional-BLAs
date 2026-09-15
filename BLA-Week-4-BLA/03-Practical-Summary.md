# Practical Summary

## Video 1 – Improving RAG

A simple improved RAG flow can look like this:

```text
Source Documents
      ↓
Prepare and Split Data
      ↓
Create Embeddings
      ↓
Store in Vector Store
      ↓
User Question
      ↓
Search Relevant Chunks
      ↓
Rank / Filter Results
      ↓
Foundation Model
      ↓
Final Response
```

I also learned that retrieval can be divided into three parts:

- **Pre-Retrieval:** prepare data, create chunks, make embeddings, and build the search index.
- **Retrieval:** search for useful information.
- **Post-Retrieval:** filter or rank the retrieved information before sending it to the model.

## Video 2 – Safety and Control

A simple protection flow can look like this:

```text
User Input
    ↓
Sensitive Data / Guardrail Check
    ↓
Foundation Model
    ↓
Output Check
    ↓
Final Response
```

Bedrock Flows can also connect different application steps such as:

```text
Input
  ↓
Prompt
  ↓
Condition
  ↓
Knowledge Base or Model
  ↓
Output
```

## Video 3 – Data Preparation

One example data-preparation flow from the presentation is:

```text
Raw Files in Amazon S3
      ↓
Bedrock Data Automation
      ↓
AWS Lambda + Amazon Comprehend
      ↓
AWS Glue
      ↓
Amazon Bedrock / Knowledge Base / ML Application
      ↓
Amazon CloudWatch
```

I will add real screenshots in the Screenshots folder when I capture the AWS work.
