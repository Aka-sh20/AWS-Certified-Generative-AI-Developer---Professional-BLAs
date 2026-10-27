# Video 2 Study Notes – Resource Utilization, Throughput, and Intelligent Caching

## 1. Resource Utilization
A GenAI application uses more than tokens. It may also use:
- Model capacity
- Network connections
- Compute resources
- Supporting AWS services

Too much reserved capacity can be wasteful. Too little capacity can cause throttling, delays, or failures.

## 2. Throughput
Throughput describes how much work a system processes during a period of time.

Important measures include:
- Requests per minute
- Tokens per minute

A small number of very large requests can create a heavy workload even if request count looks low.

## 3. AWS Service Quotas
Service Quotas define resource and capacity limits.

If traffic exceeds available capacity, requests may be throttled.

Capacity planning should happen before production traffic reaches those limits.

## 4. Batch Processing
Batch processing is useful when each individual request does not need an immediate answer.

Examples:
- Summarizing thousands of support tickets
- Classifying many customer comments
- Overnight dataset processing
- Generating product descriptions

**Rule:** Real-time when the user is waiting; batch when the work can happen later.

## 5. Amazon Bedrock Batch Inference
```text
Input Dataset
    ↓
Batch Job
    ↓
Foundation Model
    ↓
Process Many Requests
    ↓
Output Results
```

This separates offline workloads from interactive application traffic.

## 6. On-Demand vs. Provisioned Throughput

### On-Demand
Useful for flexible or unpredictable traffic.

### Provisioned Throughput
Reserves model capacity for more predictable or consistent workloads.

Decision factors:
- Traffic volume
- Traffic consistency
- Performance requirements
- Cost
- Model usage pattern

## 7. Monitoring Resource Utilization
CloudWatch can monitor:
- Model requests
- Latency
- Throttling
- Errors
- Token usage

Cost information can help connect technical usage with actual spending.

## 8. Caching
Caching stores a result so it can be reused when doing the same work again is unnecessary.

Caching should only be used when the result is still accurate and safe.

## 9. Semantic Caching
Exact-match caching compares exact request text.

Semantic caching compares meaning.

A common flow:
```text
Prompt → Embedding → Compare With Cached Embeddings
                     ↓
             Similar Enough?
              ↙           ↘
          Reuse Cache   Call Model
```

## 10. Similarity Threshold
If the threshold is:
- Too strict → useful cache matches may be missed
- Too loose → incorrect old responses may be reused

## 11. Edge Caching with CloudFront
CloudFront can cache reusable content closer to users.

Suitable content may include:
- Static files
- API responses
- Supporting content
- Some deterministic or repeatable requests

TTL determines how long content remains reusable before refresh.

## Main Takeaway
Efficient GenAI systems choose capacity, processing method, and caching strategy according to real workload behavior.
