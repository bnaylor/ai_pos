# Project State & Session Summary

## Meta-Comment for Bootstrap
- This is currently a template for SUMMARY.md as we have not yet started the project.  If you are reading this, you should
update this to be in an initial state.  And delete this line/section, since it won't be true anymore.

## 📍 Current Status
- **Last Updated:** [Date/Time]
- **Active Branch:** `main` / `feature-xyz`
- **Current Milestone:** [e.g., Auth Implementation]
- **Build Status:** ✅ Passing / ❌ Broken

## 🛠 Recent Changes (Last Session)
*Summarize what was actually accomplished in the last 10-20 turns.*
- [feat] Added JWT middleware to `/api/v1`
- [refactor] Moved database config to `internal/db`
- [fix] Resolved race condition in user signup flow

## 🧠 Working Memory & Context
*Crucial for the "Vibe Coding" transition—what's in the AI's head right now?*
- **Known Technical Debt:** The `user_test.go` is currently mocked; needs real DB integration.
- **Assumptions Made:** Assuming the frontend will handle the 401 redirect logic.
- **Blockers:** Waiting for API key confirmation for Stripe integration.

## 🤝 Handover Notes (Gemini ↔ Claude)
*Specifically for when you switch models or start a fresh session.*
> **STOP! Read this before starting:**
> 1. We just finished the backend logic for [Feature X], but the **tests are failing** because of a type mismatch in the schema.
> 2. **Don't** try to refactor the whole schema; just patch the `User` struct in `types.ts`.
> 3. The next logical step is to verify the connection in the `/dashboard` route.

## 📋 Next Steps (Priority Order)
1. [ ] Fix the failing type check in `types.ts`.
2. [ ] Implement the `useAuth` hook in the React frontend.
3. [ ] Run `npm run test:unit` to verify core logic.
