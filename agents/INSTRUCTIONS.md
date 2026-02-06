# Agent Instructions

## Repository Setup (Once Per Clone)
Run this after cloning to enable the pre-commit hook:
```bash
git config core.hooksPath .githooks
```

## Startup Procedure
1. Read `agents/REQUIREMENTS.md` to understand the goal.
2. Read `agents/SUMMARY.md` for the current task status.
3. Check `agents/TECH_STACK.md` for architectural constraints.
4. Consult `agents/DECISIONS.md` if you need context on past architectural choices.

## Operational Rules
- **Progress Tracking:** Before finishing a session or when I say 'checkpoint', you must generate a new version of SUMMARY.md. Use the Handover Notes section to speak directly to the next AI agent, warning them of any 'gotchas' or rabbit holes you encountered.
- **Anti-divergence:** Update `agents/TECH_STACK.md` when adding or changing libraries, to prevent, for example, different agents using three different HTTP clients.
- **PRD Currency:** Update `agents/REQUIREMENTS.md` when we add new features conversationally.
- **Decision Tracking:** When making significant architectural or library choices, add an entry to `agents/DECISIONS.md` explaining the rationale.
- **Scratchpad:** Use `agents/scratchpad/` for work-in-progress notes during a session. This directory is gitignored.
- **Git Workflow:** One feature per commit. Use conventional commit messages (e.g., `feat:`, `fix:`, `test:`).
    - Remember to maintain files like .gitignore
- **Git Protocol:** This repository uses a pre-commit hook. Before every commit, you must update the agents/SUMMARY.md to reflect the changes you just made and what the next agent should focus on. If the commit fails due to the hook, update the summary and try again.
- **Test-Driven Development:** Write the test first, or immediately after. Commit tests separately from feature code.
- **State Management:** If you are nearing a context limit (or ending a session), summarize the "Next Steps" explicitly in `SUMMARY.md`.

## Quality Guardrails
- Avoid "placeholder" comments. Write full implementations.
- If a task is ambiguous, ASK for clarification rather than guessing.
- If asked how to do something, explain first, don't just do it.
- **Conflict Resolution:** If agents disagree on approach or the build is broken at session start, escalate to the human.

## Code Particulars
- Comments: Add code comments sparingly. Focus on why something is done, especially for complex logic, rather than what is done.

