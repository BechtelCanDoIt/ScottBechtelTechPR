# Identity Server: AI Agent Delegated Authorization Flow
**Date:** Tuesday, August 18, 2026  **Product:** [Identity Server](https://wso2.com/identity-and-access-management/)

## Business Problem
Enterprises rolling out AI agents to act on behalf of employees or customers face an attribution gap: 

- Service account - Who initiated is lost and that account might have more privilege then the user.
- User account - User might not have enough privilege to accomplish the requested action. And if they do well we'll talk about that next.
- And the two approaches break the best practice rule of least privilege and zero trust. 

Today **Agents typically borrow a human's static credentials or a shared service account**. That makes it impossible to scope what the agent can do, for how long, or to revoke its access without breaking the human's own session. 

When an **agent overreaches**, auditors can't tell whether it was the human or the agent behind the action.

## How WSO2 Solves This
WSO2 Identity Server treats **AI agents as first-class identities**[1] instead of hidden service accounts, issuing each agent its **own auditable credential distinct from the human it acts for**. 

Using OAuth 2.0 token exchange, a user grants an agent a narrow, time-bound scope for a single task, and that grant automatically expires once the task or window ends. Every agent action is logged separately from human actions in the same platform used for workforce and customer identity, giving security teams one control plane **instead of a sprawl of API keys and shared logins**.

## Patterns Used

- OAuth 2.0 Token Exchange
- Time-Bound Delegated Authorization
- Rich Authorization Requests (RAR)
- Zero Trust Security

## Architecture
![Flow Diagram](images/wso2_flow_animated.gif)


[1] Learn more here >> https://is.docs.wso2.com/en/next/guides/agentic-ai/ai-agents/
---
WSO2 Identity Server · wso2.com/identity-and-access-management ·  by, Scott Bechtel
