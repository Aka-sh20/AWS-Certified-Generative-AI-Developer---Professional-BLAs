# Workflow Notes – Multi-Agent System

## Basic Multi-Agent Workflow

1. User sends a request.
2. A router or coordinator checks the request.
3. The request is sent to the correct specialized agent.
4. The specialized agent uses its tools.
5. If more than one agent is needed, a Supervisor Agent can coordinate them.
6. Results are combined.
7. One final response is returned to the user.

## Simple Flow

`User → Agent Squad Router → Specialized Agent → Tools → Result → User`

## Example

User asks about a business trip.

- Travel Agent checks flights.
- Hotel Agent checks lodging.
- Budget Agent checks the total cost.
- Supervisor Agent combines the plan.
