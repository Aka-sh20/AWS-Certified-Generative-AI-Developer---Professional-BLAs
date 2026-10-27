# Challenges and Solutions – Video 1

## Challenge 1: Thinking that shorter prompts are always better
**What was confusing:** It may seem that removing as much context as possible is always the best optimization.

**Solution:** Keep the information that is useful for the current task and remove information that does not help. The goal is useful context, not minimum context.

## Challenge 2: Understanding when to use a smaller model
**What was confusing:** It is easy to assume that the largest model should handle every request.

**Solution:** Match model capability with task complexity. Classification, extraction, formatting, and simple summarization may not require the strongest model.

## Challenge 3: Managing long conversation history
**What was confusing:** Resending the entire history preserves context but increases token usage.

**Solution:** Keep recent relevant messages and summarize older information that still matters.

## Challenge 4: Prompt compression
**What was confusing:** Compressing context can remove important details.

**Solution:** Use compression only when important facts and instructions are preserved, and evaluate the final task quality.

## Challenge 5: Choosing a model objectively
**What was confusing:** Model popularity or size can look like an easy decision rule.

**Solution:** Test real workload prompts and compare quality, cost, latency, token usage, and use-case requirements.
