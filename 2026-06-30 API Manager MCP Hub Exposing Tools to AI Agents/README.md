# API Manager: MCP Hub — Exposing Tools to AI Agents
**Date:** Monday, June 30, 2026  **Product:** [WSO2 API Manager](https://wso2.com/api-platform/api-manager/)

![Flow Diagram](images/wso2_flow_animated.gif)

## Flow Overview
How WSO2 API Manager acts as an MCP Hub — publishing backend services as Model Context Protocol tools that AI agents can discover and invoke with full policy enforcement.


## 🔴 Business Problem
AI agents need to call real backend services — but most backends weren't built with agent-friendly interfaces. Teams end up writing bespoke integration glue for every LLM integration, with no governance, no rate limiting, and no visibility into how agents are consuming APIs. As agent proliferation accelerates, this becomes an ungoverned surface area.

## ✅ How WSO2 Solves This
WSO2 API Manager acts as an MCP Hub — a single gateway that wraps any REST, SOAP, or GraphQL backend and exposes it as a Model Context Protocol tool. Developers publish their service once; AI agents discover it via tools/list and call it via tools/call. Every invocation passes through APIM's full policy engine: OAuth validation, rate limiting, quota enforcement, and audit logging — with zero changes to the backend.

## 📐 Patterns Used
MCP Tool Registration Pattern · API Gateway Facade · OAuth 2.0 Token Introspection · Tool Schema Discovery · Agentic Request Routing
