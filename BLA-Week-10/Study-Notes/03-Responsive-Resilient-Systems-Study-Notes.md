# Video 3 Study Notes – Building Responsive and Resilient GenAI Systems

## 1. Responsive and Resilient

**Responsive:** Gives useful output quickly and avoids unnecessary waiting.

**Resilient:** Handles temporary failures, throttling, capacity issues, or service interruptions without immediately breaking the application.

A production application needs both.

## 2. Parallel Execution
Independent tasks do not always need to run sequentially.

Example travel assistant:
- Find flights
- Find hotels
- Check local transportation

These tasks may be able to run in parallel.

AWS Step Functions can coordinate sequential and parallel workflow steps.

## 3. Streaming and TTFT
Without streaming:
```text
Request → Wait → Wait → Complete Answer
```

With streaming:
```text
Request → First Tokens → More Tokens → Complete Answer
```

**TTFT (Time to First Token)** measures the wait until the first generated token reaches the user.

## 4. Focused Prompts
Responsiveness can improve by:
- Summarizing old conversation history
- Removing irrelevant context
- Pruning weak RAG results
- Breaking very complex tasks into smaller requests

## 5. RAG Retrieval Speed
A RAG request may include:
```text
User Question
   ↓
Query Embedding
   ↓
Search / Retrieval
   ↓
Filtering
   ↓
Relevant Context
   ↓
Foundation Model
   ↓
Answer
```

A slow retrieval pipeline can make the whole application slow even if the model is fast.

## 6. Improving Retrieval Quality
Techniques include:
- Hybrid search
- Query preprocessing
- Splitting multi-part questions
- Clarifying ambiguous wording
- Metadata filtering

## 7. Inference Parameters
### Temperature
Lower values can produce more consistent output. Higher values can allow more variation.

### top_p and top_k
These influence which token possibilities the model considers during generation.

Settings should match the use case.

## 8. Test Instead of Guessing
Compare configurations using representative prompts and evaluate:
- Quality
- Latency
- Consistency
- Usefulness

## 9. Temporary Failures
Temporary problems may include:
- Busy service
- Rate limit
- Network issue

Retrying immediately and repeatedly can make overload worse.

## 10. Exponential Backoff
```text
First failure  → short wait
Second failure → longer wait
Third failure  → even longer wait
```

## 11. Jitter
Jitter adds small timing differences so many clients do not retry at exactly the same moment.

## 12. Connection Pooling
Without pooling:
```text
Request → New Connection → Response → Close
```

With pooling:
```text
Create Connection → Reuse for Multiple Requests
```

This reduces repeated network setup work.

## 13. Amazon Bedrock Cross-Region Inference
```text
Application
    ↓
Inference Profile
    ↓
Available Supported Region
    ↓
Foundation Model
    ↓
Response
```

This can improve resilience and available inference capacity.

## 14. Geographic and Global Inference Profiles
- Geographic profile: routes within supported Regions associated with a geographic area.
- Global profile: can use a broader set of supported AWS Regions.

Organization controls such as SCPs must allow the Regions required by the profile.

## Main Takeaway
A responsive and resilient GenAI system comes from improving the complete workflow, not only the Foundation Model.
