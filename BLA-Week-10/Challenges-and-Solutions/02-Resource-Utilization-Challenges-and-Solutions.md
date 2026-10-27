# Challenges and Solutions – Video 2

## Challenge 1: Measuring throughput only by request count
**Problem:** A few large prompts can consume significant capacity even when request count is low.

**Solution:** Consider both requests per minute and tokens per minute.

## Challenge 2: Choosing real-time processing for every workload
**Problem:** Large offline jobs do not always need interactive inference.

**Solution:** Use batch processing when users do not need immediate individual responses.

## Challenge 3: Choosing Provisioned Throughput too early
**Problem:** Reserved capacity may be underused for applications with occasional traffic.

**Solution:** Base the choice on actual traffic volume, consistency, performance needs, cost, and usage pattern.

## Challenge 4: Reusing cached answers safely
**Problem:** A previously correct response may become outdated or may depend on a specific user.

**Solution:** Cache only when the result is still accurate, appropriate, and safe to reuse.

## Challenge 5: Setting the semantic similarity threshold
**Problem:** A strict threshold misses useful matches, while a loose threshold may return the wrong old answer.

**Solution:** Test threshold behavior with representative user questions and validate answer correctness.
