# Workflow Notes – Amazon Bedrock Agent

## Basic Agent Workflow

1. User sends a request.
2. The agent understands the goal.
3. The agent plans what needs to happen.
4. The agent decides whether it needs a tool or Knowledge Base.
5. If an action is needed, an Action Group can connect the agent to a Lambda function.
6. Lambda performs the backend action.
7. The result returns to the agent.
8. The agent combines the information and gives the final response.

## Simple Flow

`User → Bedrock Agent → Plan → Tool / Knowledge Base → Result → Foundation Model → Final Response`

## Example

User asks about an order status.

`User → Bedrock Agent → Check Order Action Group → Lambda → Order System → Result → Agent → User`
