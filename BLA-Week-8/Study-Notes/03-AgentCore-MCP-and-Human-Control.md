# Study Notes – AgentCore, MCP, and Human Control

## From Building an Agent to Running It

Building the agent logic is only one part of the application.

A production agent also needs:

- Hosting
- Memory
- Secure tool access
- Identity
- Policies
- Monitoring
- Evaluation
- Human control

## Amazon Bedrock AgentCore

AgentCore helps developers deploy and operate AI agents.

Easy way to remember:

Agent framework builds the agent.  
AgentCore helps operate the agent.

## AgentCore Runtime

Runtime gives the agent a managed serverless place to run.

`Application → AgentCore Runtime → Agent → Tools / Knowledge → Response`

## AgentCore Memory

Short-term memory keeps information from the current session.

Long-term memory can store useful information from earlier sessions such as preferences, facts, or summaries.

Memory should store useful context, not everything forever.

## AgentCore Gateway

Gateway gives agents a controlled way to access external APIs, Lambda functions, and business services.

`Agent → AgentCore Gateway → API / Lambda / Business Service`

## Identity and Policies

An agent should receive only the permissions it needs.

Example:

A support agent may read an order status but may not be allowed to approve a large refund.

## Monitoring and Evaluation

Production agents should be monitored for:

- High latency
- Failed tool calls
- Unexpected behavior
- Poor response quality

## Model Context Protocol (MCP)

MCP provides a more standardized way for AI applications to connect to external tools and information sources.

Examples can include GitHub, Slack, PostgreSQL, and other external systems.

## Human-in-the-Loop

Some decisions should still involve a person.

`AI Agent → Confidence / Risk Check → Automatic Path OR Human Review`

Human review is useful when the case is uncertain, risky, or sensitive.

## Amazon Quick

Amazon Quick brings Agentic AI capabilities closer to business users through chat, knowledge, research, automation, and connected actions.

## Main Lesson

A useful AI agent needs more than a model. It also needs memory, tools, security, monitoring, and human control.
