# ASP.NET Core for the backend

ASP.NET Core was chosen over a Node.js backend (Hono, Express) despite the frontend being Next.js (TypeScript). The builder is actively growing backend knowledge and wants to use this project to build depth in a backend-native language with a mature ecosystem. A TypeScript full-stack would have been faster to iterate and would have allowed shared types across the monorepo — that benefit was weighed and accepted as a tradeoff in favour of deeper backend learning.

## Consequences

Shared TypeScript types between frontend and backend are not available. API contracts must be maintained by discipline or a future OpenAPI spec.
