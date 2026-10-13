# Week 8 BLA – AWS Generative AI Developer

## About This Repository

This folder contains my Week 8 learning materials for AWS Generative AI.

This week I focused on **Agentic AI** and how AI agents can move beyond simple question answering. I learned how an agent can use tools, planning, memory, Knowledge Bases, multiple specialized agents, and managed AWS services to complete larger tasks.

The three presentations in this folder follow one learning path:

1. **Amazon Bedrock Agents, Tools, Action Groups, and Agentic RAG**
2. **Strands Agents, Agent Tools, and AWS Agent Squad**
3. **Deploying and Managing AI Agents**

---

## Video 1 – Amazon Bedrock Agents, Tools, Action Groups, and Agentic RAG

In the first topic, I learned the basic idea of **Agentic AI**.

A normal Foundation Model mainly receives a prompt and gives a response. An AI agent can go further by understanding a goal, planning the next steps, using outside tools, and collecting information before creating the final answer.

Main topics I studied:

- Normal LLM vs. AI Agent
- Memory and planning
- Agent tools
- Tool selection
- Tool parameters
- Amazon Bedrock Action Groups
- AWS Lambda as a backend action
- Amazon Bedrock Knowledge Bases
- Agentic RAG
- Employee support agent example
- Introduction to multi-agent systems

### Simple Agent Flow

`User Request → Understand Goal → Plan Steps → Use Tool / Knowledge Base → Combine Result → Final Response`

One important lesson for me was that an agent does not need to know everything by itself. It can recognize when it needs another capability and use the correct tool.

---

## Video 2 – Strands Agents, Agent Tools, and AWS Agent Squad

The second topic moved from one AI agent to a **multi-agent system**.

Instead of giving one agent every responsibility, a larger system can use specialized agents. Each agent can have its own instructions, tools, memory, and job.

Main topics I studied:

- Multi-agent workflows
- Routing
- Parallelization
- Prompt chaining
- Evaluator–Optimizer pattern
- Specialized agents
- Strands Agents
- Built-in tools
- Custom tools
- AWS Agent Squad
- Intelligent routing
- Supervisor Agent
- Shared context between agents

### Easy Way I Remember It

**Strands Agents** → Build capable agents and give them tools.

**AWS Agent Squad** → Route and coordinate work between multiple agents.

### Simple Multi-Agent Flow

`User → Agent Squad Router → Specialized Agent → Tools → Result → User`

This topic helped me understand that adding more agents is not the main goal. The important part is giving each agent a clear responsibility and designing how the agents work together.

---

## Video 3 – Deploying and Managing AI Agents

The third topic focused on what happens after an AI agent is already built.

A real production agent also needs a safe place to run, memory, secure access to tools, monitoring, identity, policies, and sometimes human review.

Main topics I studied:

- Amazon Bedrock AgentCore
- AgentCore Runtime
- Short-term and long-term memory
- AgentCore Memory
- AgentCore Gateway
- AgentCore Identity and policies
- Monitoring and evaluation
- Model Context Protocol (MCP)
- Human-in-the-Loop
- Amazon Quick

### Easy Way I Remember It

**Agent framework builds the agent.**

**AgentCore helps operate the agent.**

### Simple Runtime Flow

`Application → AgentCore Runtime → AI Agent → Tools / Knowledge → Response`

This topic helped me understand that building the agent is only the beginning. A complete system also needs deployment, security, monitoring, memory, and human control.

---

## Overall Learning Flow

`Foundation Model → AI Agent → Tools and Action Groups → Agentic RAG → Specialized Agents → Multi-Agent Coordination → AgentCore Deployment → Secure and Managed AI Application`

---

## Repository Structure

- **Presentations/** – My three presentation files
- **Study-Notes/** – Simple notes from each presentation
- **Workflow-Notes/** – Main workflows and service connections
- **Diagrams/** – GitHub Mermaid diagrams for each topic
- **Challenges-and-Solutions/** – Topics I found difficult and how I understood them
- **Reflections/** – My learning reflections for each video
- **Weekly-Progress/** – Weekly progress summary
- **Links/** – YouTube and LinkedIn links

---

## Main Takeaway

The biggest thing I learned is that an AI agent is more than a Foundation Model.

A useful agent may need:

- Planning
- Memory
- Tools
- Trusted information
- Security
- Monitoring
- Clear permissions
- Human review

For larger applications, multiple specialized agents can work together instead of expecting one agent to handle every task.

---

## Acknowledgment

Special thanks to **Dr. Victor Govindaswami** for his guidance and support throughout this course. These topics helped me understand how Agentic AI can move from a simple model response into a complete system that can use tools, work with other agents, and run safely in a real application.

Prepared by: **Akash Patel**  
Concordia University Chicago
