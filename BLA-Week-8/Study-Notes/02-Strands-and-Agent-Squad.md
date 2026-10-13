# Study Notes – Strands Agents and AWS Agent Squad

## Why Use Multiple Agents?

One AI agent can use many tools, but too many responsibilities can make the system difficult to manage.

A multi-agent system divides work between specialized agents.

Example:

- Research Agent
- Budget Agent
- Schedule Agent
- Supervisor Agent

## Common Multi-Agent Patterns

### Routing

A router sends the request to the best agent.

### Parallelization

Several agents work on different parts at the same time.

### Prompt Chaining

The output from one step becomes the input for the next step.

### Evaluator–Optimizer

One agent creates a result and another agent checks it and suggests improvements.

## Why Specialized Agents Help

A specialized agent can have:

- Focused instructions
- Fewer tools
- Clear responsibility
- Easier management

## Strands Agents

Strands Agents is an open-source SDK for building AI agents and multi-agent applications.

A Strands agent can receive:

- A model
- Instructions
- Built-in tools
- Custom tools

## Built-In vs. Custom Tools

Built-in tools are common capabilities already available.

Examples:

- Calculator
- Current time
- File operations
- Python execution
- AWS access

Custom tools are created for a specific application.

Examples:

- `check_inventory(product_id)`
- `create_support_ticket(issue)`

## AWS Agent Squad

Agent Squad focuses on intelligent routing and coordination between agents.

It can examine a user request and choose the correct specialized agent.

## Supervisor Agent

A Supervisor Agent can coordinate several agents when one request needs multiple areas of work.

Example:

Travel Agent → finds flights  
Hotel Agent → finds lodging  
Budget Agent → checks total cost  
Supervisor Agent → combines the final plan

## Easy Way to Remember

Strands → Build capable agents and tool usage.

Agent Squad → Route and coordinate work between agents.

## Main Lesson

A strong multi-agent system needs clear responsibilities and good coordination. More agents do not automatically mean a better system.
