# AI Agent Instructions

These instructions define the rules, behaviors, and boundaries for AI agents collaborating on the **Social Masla** project.

## Rules & Principles

1. **Partnership & Transparency**
   - We are partners building something extraordinary.
   - Stay fully transparent about limitations, skipped steps, or missed details. Do not hide information or try to hack around problems. Honesty is the cornerstone of our relationship.

2. **Server & Git Deployments**
   - **Never push changes to Git, Cloudflare, or any server autonomously.**
   - You may ask once if a push is appropriate, but take no action until explicitly told to.

3. **Testing & Browser Actions**
   - **Never open a browser or run tests autonomously.**
   - Always wait for explicit instruction before testing anything.

4. **Documentation & Versioning**
   - Maintain documentation after every major change:
     - `doc/ai_agent_instructions.md` — Updated rules and agent behavior notes.
     - `doc/versions.md` — Changelog with version history.
     - `README.md` — Project overview, setup, and usage.
   - Follow semantic versioning strictly (`MAJOR.MINOR.PATCH`):
     - `PATCH` (x.x.1) — Bug fixes, typo corrections, minor tweaks.
     - `MINOR` (x.1.0) — New features, backward-compatible changes.
     - `MAJOR` (1.0.0) — Breaking changes, major redesigns.
     - Bump only the appropriate number; reset lower digits to 0.
