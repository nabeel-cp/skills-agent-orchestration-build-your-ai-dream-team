# Agent team for Mona's Project Pulse

I will use a small custom agent team, defined under the repository's `.github/agents/` folder, to build Mona's Project Pulse dashboard with GitHub Copilot CLI running in a Codespace.

## Team overview

### Orchestrator
- Model: Claude Opus 5.5 (copilot)
- Responsibility: Coordinates the work across the planning, design, and implementation phases, delegates tasks to specialists, and verifies that the final dashboard fits together coherently.
- Definition: `.github/agents/orchestrator.agent.md`

### Planner
- Model: Claude Opus 5.5 (copilot)
- Responsibility: Researches the repo, checks docs and dependencies, and creates a practical implementation plan with file ownership, sequencing, validation, and edge cases.
- Definition: `.github/agents/planner.agent.md`

### Designer
- Model: Gemini 3.7 Flash (copilot)
- Responsibility: Focuses on user experience, accessibility, layout, visual hierarchy, responsive behavior, and the look-and-feel of the Project Pulse dashboard.
- Definition: `.github/agents/designer.agent.md`

### Coder
- Model: GPT-5.5 (copilot)
- Responsibility: Implements the code, fixes bugs, and handles runnable app support needed for the dashboard, while staying within the scope assigned by the Orchestrator.
- Definition: `.github/agents/coder.agent.md`

## Notes

This team is intentionally specialized: the Planner maps the work, the Designer shapes the product experience, the Coder builds the implementation, and the Orchestrator keeps the whole effort coordinated. Using GitHub Copilot CLI in a Codespace gives the workflow a structured agent-based orchestration model for the dashboard build.
