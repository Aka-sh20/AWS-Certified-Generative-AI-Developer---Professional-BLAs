# Study Notes – Agentic AI and Amazon Bedrock Agents

## What Is Agentic AI?

Agentic AI means the Foundation Model can be part of a larger system that can use memory, planning, instructions, and tools.

A chatbot mainly responds to a prompt. An agent can decide that it needs another step before giving the final answer.

## Normal LLM vs. AI Agent

A normal LLM answers using the information available in the prompt and model.

An AI agent can also use outside information or actions.

Example:

- User asks for current weather.
- A normal model may not have live information.
- An agent can call a weather tool and then explain the result.

## Main Parts of an Agent

- Memory – keeps useful context
- Planning – breaks a bigger task into smaller steps
- Tools – connect the agent to APIs, databases, Lambda, calculators, or other services
- Instructions – guide how the agent should behave

## Tools

A tool is something outside the Foundation Model that the agent can use.

Examples:

- `get_weather(city)`
- `check_order_status(order_id)`
- `calculate_tax(amount)`
- `search_company_policy(topic)`

Clear tool descriptions are important because they help the model choose the correct tool.

## Action Groups

Amazon Bedrock Action Groups organize actions that an agent is allowed to perform.

Example flow:

`User → Bedrock Agent → Action Group → Lambda → Business System → Result → Agent → User`

## Tool Parameters

A tool may require values such as:

- flight number
- travel date
- order ID
- amount

If required information is missing, the agent should ask the user instead of guessing.

## Knowledge Bases as Tools

A Bedrock Knowledge Base can provide trusted company information.

Example:

A user asks about parental leave. The agent can search the HR Knowledge Base and answer using the retrieved policy information.

## Agentic RAG

Traditional RAG usually retrieves information before generating the answer.

Agentic RAG allows the agent to decide whether retrieval is needed.

`Question → Agent Evaluates Task → Tool / Knowledge Base → Result → Final Answer`

## Main Lesson

The power of an AI agent is not that it knows everything. The power comes from recognizing what it needs and using the correct capability.
