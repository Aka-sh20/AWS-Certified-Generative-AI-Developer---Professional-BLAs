# Challenges and Solutions – Agentic AI

## Challenge 1 – Normal LLM vs. AI Agent

At first, I was confused about why an AI agent is different from a normal Foundation Model.

### How I Understood It

I used a live weather example. A normal model may not have current information, but an agent can call a weather tool and then answer using the new result.

This helped me understand that an agent can use outside capabilities.

## Challenge 2 – Tool Selection

I was not sure how the agent knows which tool to use.

### How I Understood It

I learned that clear tool descriptions are very important. The model compares the request with the available tool descriptions and chooses the best match.

## Challenge 3 – Action Groups

Action Groups sounded similar to normal tools at first.

### How I Understood It

I started thinking of an Action Group as the connection between the agent's decision and the backend action, often using Lambda.

## Challenge 4 – Agentic RAG

The difference between normal RAG and Agentic RAG was confusing.

### How I Understood It

Normal RAG usually retrieves first.

Agentic RAG lets the agent decide whether it needs retrieval, another tool, both, or no tool.
