# Agent Instructions

## Startup Procedure
1. Read `agents/REQUIREMENTS.md` to understand the goal.
2. Read `agents/SUMMARY.md` for the current task status.
3. Check `agents/TECH_STACK.md` for architectural constraints.

## Operational Rules
- **Progress Tracking:** Before finishing a session or when I say 'checkpoint', you must generate a new version of SUMMARY.md. Use the Handover Notes section to speak directly to the next AI agent, warning them of any 'gotchas' or rabbit holes you encountered.
- **Anti-divergence:** Update `agents/TECH_STACK.md` when adding or changing libraries, to prevent, for example, different agents using three different HTTP clients.
- **PRD Currency:** Update `agents/REQUIREMENTS.md` when we add new features conversationally.
- **Git Workflow:** One feature per commit. Use conventional commit messages (e.g., `feat:`, `fix:`, `test:`).
    - Remember to maintain files like .gitignore
- **Git Protocol:** This repository uses a pre-commit hook. Before every commit, you must update the agents/SUMMARY.md to reflect the changes you just made and what the next agent should focus on. If the commit fails due to the hook, update the summary and try again.
- **Test-Driven Development:** Write the test first, or immediately after. Commit tests separately from feature code.
- **State Management:** If you are nearing a context limit (or ending a session), summarize the "Next Steps" explicitly in `SUMMARY.md`.

## Quality Guardrails
- Avoid "placeholder" comments. Write full implementations.
- If a task is ambiguous, ASK for clarification rather than guessing.
- If asked how to do something, explain first, don't just do it.

## Code Particulars
- Comments: Add code comments sparingly. Focus on why something is done, especially for complex logic, rather than what is done.

