# Challenges and Solutions – Video 3

## Challenge 1: Treating every task as sequential
**Problem:** Independent work waits unnecessarily.

**Solution:** Run independent retrieval, calculations, searches, or other steps in parallel when the workflow allows it.

## Challenge 2: Optimizing only model latency
**Problem:** A slow RAG retrieval pipeline can dominate total response time.

**Solution:** Optimize query preparation, vector search, filtering, and context preparation as well as inference.

## Challenge 3: Guessing model settings
**Problem:** Changing temperature, top_p, or top_k without testing can hurt quality or consistency.

**Solution:** Compare settings with representative application prompts and evaluate quality, latency, consistency, and usefulness.

## Challenge 4: Aggressive retries after temporary failures
**Problem:** Immediate repeated retries can add more pressure to an overloaded service.

**Solution:** Use exponential backoff and jitter.

## Challenge 5: Creating a new connection for every service request
**Problem:** Repeated connection setup adds unnecessary overhead.

**Solution:** Reuse connections with connection pooling where appropriate.

## Challenge 6: Depending on capacity from one AWS Region
**Problem:** High demand or regional capacity pressure can reduce available inference capacity.

**Solution:** Use Amazon Bedrock Cross-Region Inference where appropriate and ensure organization policies allow required Regions.
