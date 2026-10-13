# Workflow Notes – AgentCore Deployment

## Basic Production Agent Flow

1. The application sends a request to AgentCore Runtime.
2. Runtime runs the AI agent.
3. AgentCore Memory can provide useful short-term or long-term context.
4. The agent can use AgentCore Gateway to access tools and external services.
5. Identity and policies control what the agent is allowed to do.
6. Monitoring helps developers observe the agent.
7. High-risk or uncertain actions can be sent for human review.
8. The final result is returned to the application.

## Simple Flow

`Application → AgentCore Runtime → Agent → Memory / Gateway / Tools → Policy Check → Response`

## Human Review Path

`Agent → Confidence / Risk Check → Automatic Action OR Human Review`
