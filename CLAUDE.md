
# FlowPilot - Project Instructions

## Project Overview
FlowPilot is an event-driven workflow automation engine.

This project demonstrates agentic software development,
backend engineering, and human-led code verification.

The coding agent should implement most of the code.
The human developer is responsible for planning,
architectural decisions, code review, verification,
and final approval.

## Tech Stack
- Frontend: React, TypeScript
- Backend: Node.js, NestJS
- Database: PostgreSQL
- ORM: Prisma
- Testing:
  - Backend: Jest for unit and integration tests
  - HTTP API: Jest + Supertest
  - Frontend: Vitest + React Testing Library
  - Browser E2E: Playwright

Do not introduce additional technologies without
explaining the tradeoffs and receiving approval.

## Development Workflow
1. Read the relevant project documentation.
2. Inspect existing code before proposing changes.
3. Propose a small implementation plan.
4. Wait for my approval before writing code.
5. Implement only the approved task.
6. Write or update relevant tests.
7. Run tests and report actual results.
8. Stop for my code review.
9. Apply requested changes after approval.
10. Wait for final approval before proceeding.

Do not automatically move to the next task.

## Coding Standards
- Use TypeScript strict mode.
- Prefer clear, maintainable code.
- Keep functions focused and reasonably small.
- Use descriptive variable and function names.
- Avoid unnecessary dependencies and abstractions.
- Validate external inputs.
- Handle errors explicitly.
- Do not use `any` without justification; prefer explicit types or `unknown`.
- Never evaluate untrusted workflow expressions as executable code (e.g., `eval()` or `new Function()`). Use validated, allowlisted operators instead.

## Database Guidelines
- Use PostgreSQL with Prisma ORM.
- Do not introduce another ORM without approval.
- Propose database models and relationships before implementing them.
- Explain primary keys, foreign keys, and constraints.
- Review database migrations before executing them.
- Use transactions when multiple related writes must remain consistent.
- Explain important database queries and their performance implications.
- Raw SQL may be used when justified and approved.

## Code Review
After each implementation task, provide:
- Files created or modified
- Important functions and their locations
- Explanation of critical logic
- Edge cases and error handling
- Tests written and executed
- Actual test results
- Known limitations
- Steps for manual verification
- Highlight any changes affecting security, data integrity, or concurrency.
- Show the actual code changes and test evidence, not just a summary.
- Do not proceed to the next implementation task until I have reviewed and approved the current changes.

Do not edit files while I am reviewing them.

## Testing
- Use Jest for backend unit and integration tests.
- Use Jest + Supertest for HTTP API tests.
- Use Vitest + React Testing Library for frontend component tests.
- Use Playwright for critical browser end-to-end tests.
- Use a dedicated test database for PostgreSQL integration tests.
- Use supported and compatible versions of the testing tools.
- Explain the test configuration before implementation.
- Do not change testing frameworks without approval.
- Test normal behavior, edge cases, and failure scenarios.
- Add regression tests for confirmed bugs.
- Do not mock the core logic being tested.
- Do not weaken tests merely to make them pass.
- Do not claim tests passed unless they were executed.
- Report tests that could not be run.
- Ask before destructive database operations.
- Stop for human review after each testable task.

## Security
- Never hardcode credentials or API keys.
- Never commit `.env` files.
- Treat webhook payloads as untrusted input.
- Do not expose sensitive information in logs.
- Do not execute untrusted code.
- Ask before running destructive commands.

## Git Rules
- Never commit or push without my approval.
- Never force-push.
- Do not modify unrelated files.
- Summarize changes before requesting approval.
- Do not include private session logs or secrets.

## Documentation
Refer to approved documentation when available:
- docs/requirements.md
- docs/architecture.md
- docs/test-plan.md
- docs/decisions.md

Do not invent missing project decisions.

Suggest documentation updates when behavior changes.

## Communication
- Explain unfamiliar concepts clearly.
- Explicitly identify assumptions and explain the tradeoffs of important technical decisions.
- Do not treat unapproved assumptions as confirmed requirements.
- Ask questions when important decisions are unclear.
- Distinguish completed work from proposed work.

## Task Completion
End each implementation task with:
1. Summary
2. Files Changed
3. Critical Code to Review
4. Tests and Results
5. Risks and Limitations
6. Manual Verification Steps
7. Awaiting Approval
