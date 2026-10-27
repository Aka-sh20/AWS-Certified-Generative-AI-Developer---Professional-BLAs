# Video 1 Study Notes – Token Efficiency, Context Optimization, and Smart Model Selection

## 1. Why Optimization Matters
A GenAI application should balance answer quality with cost, speed, token usage, and model performance. Making a prompt shorter is not automatically an improvement if useful context is removed.

## 2. Tokens
Foundation Models process text as tokens rather than only complete words.

**Input tokens** may include:
- User prompt
- System instructions
- Conversation history
- Retrieved RAG context
- Examples and supporting text

**Output tokens** are generated in the model response.

Token usage affects context limits, model cost, and sometimes latency.

## 3. Amazon Bedrock CountTokens
CountTokens can estimate token usage before inference.

```text
Prompt → CountTokens → Token Count → Send or Optimize → Model
```

Different models can tokenize the same text differently, so counting should be done for the model actually being used.

## 4. Monitoring with CloudWatch
Useful measurements include:
- Input token count
- Output token count
- Request count
- Latency
- Throttles
- Client errors
- Server errors
- Streaming performance

**Lesson:** Measure first, then optimize.

## 5. Context-Window Optimization
The goal is not to provide the most information. The goal is to provide the most useful information for the current task.

## 6. Context Pruning in RAG
Instead of sending every retrieved chunk:
- Limit the number of chunks
- Rank results by relevance
- Use metadata filters
- Remove unrelated or weakly related content

## 7. Conversation History
Long conversations can be optimized by:
- Keeping recent and relevant messages
- Removing old information that no longer matters
- Summarizing older messages

## 8. Output Control
Output token usage can be controlled with:
- `maxTokens`
- Clear requested length
- Few-shot examples
- Structured formats such as JSON

## 9. Prompt Compression
A smaller model can summarize a large context before a stronger model performs the complex task.

```text
Large Context → Smaller Model → Compressed Context → Larger Model
```

The summary still needs to preserve important facts and instructions.

## 10. Smart Model Selection
Smaller models can handle tasks such as:
- Classification
- Formatting
- Extraction
- Summarization
- Preprocessing

More capable models can be saved for:
- Complex troubleshooting
- Difficult business analysis
- Deeper reasoning

## 11. Intelligent Prompt Routing
```text
User Request
   ↓
Analyze Complexity
   ↓
Simple → Smaller Model
Complex → More Capable Model
   ↓
Response
```

## 12. Model Evaluation
A model should be tested using prompts that represent the real application.

Compare:
- Quality
- Cost
- Latency
- Token usage
- Use-case requirements

## Main Takeaway
Efficient GenAI is about using the right amount of context and the right model for the task while maintaining the quality the application needs.
