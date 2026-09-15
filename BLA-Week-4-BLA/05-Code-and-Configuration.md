# Code and Configuration Examples

I kept this file simple and only included examples that were covered in the presentations.

## Video 1 – RAG Related Example

Knowledge Base update flow:

```text
Amazon S3
→ AWS Lambda
→ Bedrock Ingestion Job
→ Updated Knowledge Base
```

## Video 2 – Prompt and Structured Output Examples

### Prompt Variables

```text
{{genre}}
{{number}}
```

Example:

```text
Create a playlist for {{genre}} music with {{number}} songs.
```

### Structured JSON Output

```json
{
  "sentiment": "positive",
  "rating": 5,
  "topic": "customer service"
}
```

### Example Policy Logic

```text
Full-Time Employee + At Least 1 Year of Service
→ Eligible for Parental Leave
```

### Better Prompt Example

```text
Explain Amazon S3 to a beginner in five simple bullet points and include one practical example.
```

## Video 3 – Data Preparation Example

### Divider String

```text
<SECTION_BREAK:Executive Summary>
```

### Example Data Pipeline

```text
Amazon S3
→ Bedrock Data Automation
→ Amazon Comprehend
→ AWS Glue
→ Amazon Bedrock
→ CloudWatch
```

## AWS CLI Commands

I will add AWS CLI commands here only if I actually use them during hands-on work.
