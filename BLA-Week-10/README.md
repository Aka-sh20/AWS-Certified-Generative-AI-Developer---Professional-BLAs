# AWS Generative AI Learning Series – BLA Week 10

**Student:** Akash Patel  
**University:** Concordia University Chicago  
**Focus:** Building efficient, scalable, responsive, and resilient Generative AI applications on AWS

## Overview

This week I focused on three connected areas of Generative AI application design:

1. **Token Efficiency, Context Optimization, and Smart Model Selection**
2. **Resource Utilization, Throughput, and Intelligent Caching**
3. **Building Responsive and Resilient Generative AI Systems**

The main goal was to understand that a production GenAI application is not optimized by changing only one setting. Good design requires decisions about token usage, context size, model choice, throughput, batch processing, caching, retrieval performance, streaming, retries, network connections, and inference capacity.

---

## Video 1 – Token Efficiency, Context Optimization, and Smart Model Selection

### Main topics
- Input and output tokens
- Amazon Bedrock CountTokens API
- Monitoring token usage with Amazon CloudWatch
- Context-window optimization
- Context pruning in RAG
- Conversation-history optimization
- Output-size control
- Prompt compression
- Small model vs. large model task selection
- Cost vs. capability tradeoff
- Intelligent Prompt Routing
- Model evaluation based on quality, cost, latency, and token usage

### Main learning
The most powerful model is not automatically the best model for every request. The goal is to give the model enough useful context and enough capability for the task without automatically using more tokens or model capacity than necessary.

---

## Video 2 – Resource Utilization, Throughput, and Intelligent Caching

### Main topics
- Resource utilization
- Requests per minute and tokens per minute
- AWS Service Quotas
- Batch processing
- Amazon Bedrock Batch Inference
- On-Demand vs. Provisioned Throughput
- Monitoring with CloudWatch and cost information
- Traditional caching
- Semantic caching with embeddings
- Similarity thresholds
- Edge caching with Amazon CloudFront
- Time to Live (TTL)

### Main learning
Different workloads should not all be processed in the same way. Real-time inference, batch processing, capacity planning, and caching should be selected according to how the application is actually used.

---

## Video 3 – Building Responsive and Resilient Generative AI Systems

### Main topics
- Responsive vs. resilient application design
- Parallel execution for independent tasks
- Streaming and Time to First Token (TTFT)
- Focused prompts
- RAG retrieval speed
- Hybrid search and query preprocessing
- Model parameters such as temperature, top_p, and top_k
- Testing changes with real prompts
- Temporary failure handling
- Exponential backoff and jitter
- Connection pooling
- Amazon Bedrock Cross-Region Inference
- Geographic and global inference profiles

### Main learning
Responsiveness and resilience come from improving the complete workflow. Prompt design, retrieval, model inference, streaming, retries, connections, and regional capacity all affect the final user experience.

---

## Repository Structure

```text
BLA-Week-10/
├── Challenges-and-Solutions/
│   ├── 01-Token-Efficiency-Challenges-and-Solutions.md
│   ├── 02-Resource-Utilization-Challenges-and-Solutions.md
│   └── 03-Responsive-Resilient-Systems-Challenges-and-Solutions.md
├── Diagrams/
│   ├── 01-Token-Optimization-Workflow.md
│   ├── 02-Resource-and-Caching-Workflow.md
│   └── 03-Responsive-Resilient-Architecture.md
├── Links/
│   └── Video-and-Social-Links.md
├── Presentations/
│   ├── 01-Token-Efficiency-Context-Optimization-Smart-Model-Selection.pptx
│   ├── 02-Resource-Utilization-Throughput-Intelligent-Caching.pptx
│   └── 03-Building-Responsive-Resilient-GenAI-Systems.pptx
├── Reflections/
│   ├── 01-Token-Efficiency-Reflection.md
│   ├── 02-Resource-Utilization-Reflection.md
│   └── 03-Responsive-Resilient-Systems-Reflection.md
├── Study-Notes/
│   ├── 01-Token-Efficiency-Study-Notes.md
│   ├── 02-Resource-Utilization-Study-Notes.md
│   └── 03-Responsive-Resilient-Systems-Study-Notes.md
├── Weekly-Progress/
│   └── Week-10-Progress.md
├── Workflow-Notes/
│   ├── 01-Token-Efficiency-Workflow.md
│   ├── 02-Resource-Utilization-Workflow.md
│   └── 03-Responsive-Resilient-Workflow.md
└── README.md
```

---

## How the Three Topics Connect

A simple way I connected the three presentations is:

```text
Use the right context and model
        ↓
Use the right capacity and processing method
        ↓
Reduce repeated work with caching
        ↓
Improve retrieval and perceived response time
        ↓
Handle temporary failures safely
        ↓
Use available inference capacity across supported Regions
        ↓
Build a more efficient and reliable GenAI application
```

---

## Key AWS Services and Concepts

- Amazon Bedrock
- CountTokens API
- Amazon CloudWatch
- Amazon Bedrock Batch Inference
- Provisioned Throughput
- AWS Service Quotas
- Amazon CloudFront
- AWS Step Functions
- Amazon Bedrock Cross-Region Inference
- RAG
- Embeddings
- Semantic caching
- Prompt compression
- Intelligent Prompt Routing
- Exponential backoff and jitter
- Connection pooling

---

## Challenges and Solutions

The `Challenges-and-Solutions` folder documents the main concepts that initially required more attention, including:

- Understanding why fewer tokens do not always mean a better prompt
- Deciding when a smaller model is enough
- Understanding throughput beyond request count
- Choosing real-time vs. batch processing
- Understanding safe semantic-cache matching
- Separating model latency from RAG retrieval latency
- Understanding exponential backoff and jitter
- Understanding how Cross-Region Inference improves available capacity

---

## Diagrams

The `Diagrams` folder contains GitHub-renderable Mermaid diagrams created from the workflows studied in the presentations. They show:

- Token optimization and model routing
- Resource utilization, batch processing, and caching
- Responsive and resilient GenAI architecture

---

## YouTube and LinkedIn

YouTube and LinkedIn links will be added in:

`Links/Video-and-Social-Links.md`

This keeps the GitHub repository connected with the explanation videos and social learning posts.

---

## Final Reflection

This week helped me understand that Generative AI optimization is much broader than only reducing cost. A strong application needs the right context, the right model, the right amount of capacity, an efficient retrieval pipeline, safe caching, responsive output, and reliable failure handling.

The most useful lesson for me was that optimization decisions should be based on the real workload. Different tasks may need different models, different processing methods, and different infrastructure choices.

Special thanks to **Professor Dr. Victor Govindaswamy** for his continued guidance and support throughout my AWS Generative AI learning journey.
