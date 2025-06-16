# Rooroo Project Memory

This document provides a shared understanding of the Rooroo project for all AI agents.

## 1. Project Overview
- **Goal:** A minimalist AI orchestration framework for VS Code using specialized agents.
- **Core Dependency:** The project relies on the "Roo Code VS Code extension".
- **Primary Workflow:** The user interacts with the **🧭 Rooroo Navigator**, which manages tasks by creating briefings and dispatching them to other agents.

## 2. Key Conventions & Project Structure
- **Operational Directory:** All operational files are stored in the `.rooroo/` directory.
- **Task Management:** Tasks are managed via `.rooroo/queue.jsonl`. Each task has a dedicated directory (`.rooroo/tasks/TASK_ID/`).
- **Task Briefings (`context.md`):** Task details are provided in a `context.md` file. **Crucially, these briefings should link to necessary files rather than embedding their content.**
- **Logging:** All significant events are logged in `.rooroo/logs/activity.jsonl`.
- **Custom Rules:** Workspace-specific agent instructions can be defined in the `.roo/rules/` directory to ensure consistent behavior.

## 3. Coding & Style Conventions
- **Communication:** Agents report back to the Navigator using a structured JSON "Output Envelope".
- **File Paths:** Always use workspace-relative paths.
- **Task IDs:** Use the `ROO#` prefix for all task identifiers for easy tracking.
- **Principle of Least Assumption:** If a task is ambiguous, agents must ask for clarification rather than making assumptions.