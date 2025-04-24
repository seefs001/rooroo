# 🚀 rooroo (如如) - Your AI Agent Orchestration Crew! 🚀

**Version: v0.0.1**

Welcome to `rooroo`, an AI-powered system designed to streamline complex software development by orchestrating a team of specialized AI agents right within your VS Code environment using the [Roo Code extension](https://github.com/RooVetGit/Roo-Code). Think of it as having a virtual, expert software team at your command, managed by a central coordinator.

## 🤔 What's in a Name? The Meaning of "rooroo (如如)"

The name "rooroo" comes from the term **"如如" (rú rú)** found in Buddhist philosophy. It relates to the concept of **Tathātā**, often translated as "Thusness" or "Suchness."

*   **Thusness/Suchness (真如):** Refers to the fundamental, unchanging, true nature of all phenomena – reality as it is.
*   **Equality & Non-Duality (不二平等):** Implies that, at the ultimate level, all things share this same essential nature.
*   **Emphasis:** The repetition "如如" emphasizes that this inherent "thusness" is pervasive across *all* things.

In the context of this project, the name evokes the idea of an underlying, consistent nature or principle guiding the orchestration process, aiming for a true and effective realization of the development goal through the coordinated action of its parts.

## 🤔 Initial Design Philosophy

The `rooroo` project was conceived with several core principles in mind:

*   **Simplicity & Minimalism:** Avoid unnecessary complexity. The agent team is kept to a focused minimum, with clear, distinct roles.
*   **Specialized Components:** Each agent is designed like a "swiss army knife" component, highly capable within its specific domain, allowing each part to perform its task optimally.
*   **Document & Test-Based Approach:** Emphasize clarity and reliability through a workflow that encourages documentation-driven development (DDD) via specifications and a strong focus on testing (TDD) for validation.

## ✨ Why Use rooroo? ✨

`rooroo` offers a structured and efficient approach to AI-assisted development:

*   **🧠 Specialized Expertise:** Delegate tasks to the right AI expert. Instead of one generalist AI, `rooroo` uses agents specifically designed for architecture, UX, coding, validation, and documentation, leading to potentially higher quality results in each domain.
*   **⚙️ Simplified Orchestration:** You interact primarily with the **🧠 Master Orchestrator**. It handles the complexity of breaking down your goals, delegating tasks, and managing the workflow, keeping your interaction focused and straightforward.
*   **🏗️ Structured Workflow:** `rooroo` follows a defined process for feature development, breaking down complex goals into manageable phases (Design, Implement, Validate). This brings clarity and predictability to the development lifecycle.
*   **💾 Clear Artifacts:** Key outputs are organized into dedicated directories (`.specs/` for technical specifications, `.design/` for UX/UI designs, `.docs/` for documentation), creating a traceable project history.
*   **🎯 Focused Execution:** Each agent works on specific, delegated tasks based on clear inputs (like specifications), reducing ambiguity and improving the reliability of outcomes.

## 🔑 Core Concepts

Understanding these ideas is key to leveraging `rooroo`:

1.  **Multi-Agent System (The "Crew"):** `rooroo` operates with a team of distinct AI agents (modes), each optimized for a specific role in the software development lifecycle.
2.  **Orchestration (The "Conductor"):** The **🧠 Master Orchestrator** mode is central. It interprets your high-level goals, plans the execution strategy, delegates tasks to the appropriate specialist agents using `new_task`, monitors progress, and synthesizes results. It does *not* perform the specialized tasks itself.
3.  **Specialized Roles:** Each agent (Architect, UX Specialist, Implementer, Validator, DocuCrafter) has a clearly defined responsibility and operates within that scope, using inputs like specifications or code to perform its function.
4.  **Structured Artifacts:** The system relies on generating and using artifacts stored in conventional locations (`.specs/`, `.design/`, `.docs/`) to maintain context and provide clear inputs/outputs between phases and agents.

## 🔄 The Core Development Workflow

`rooroo` guides feature development through a structured lifecycle managed by the Orchestrator:

1.  **🎯 Goal Setting:** You provide your high-level goal to the **🧠 Master Orchestrator**.
2.  **✍️ Planning & Design:** The Orchestrator plans the phases and delegates detailed design tasks:
    *   **📐 Solution Architect:** Creates technical specifications (`.specs/`).
    *   **🎨 UX Specialist:** Defines user experience and UI design (`.design/`).
3.  **💻 Implementation:** Once designs are ready, the Orchestrator assigns precise coding tasks to the **⚡ Apex Implementer**, referencing the specs.
4.  **✅ Validation:** The **🛡️ Guardian Validator** independently verifies the implemented features against the specifications.
5.  **🔄 Iteration:** Based on validation results, the Orchestrator manages feedback loops, assigning refinements or fixes back to the appropriate agents.

*(Note: Documentation tasks are handled separately by the DocuCrafter, see below).*

## 🤖 Meet the Crew 🤖

*   **🧠 Master Orchestrator (Conductor):** The project lead and central coordinator. Manages the overall workflow, delegates tasks, and communicates with you.
*   **📐 Solution Architect (Blueprint Creator):** The technical designer. Creates detailed architectural blueprints and specifications (`.specs/`).
*   **🎨 UX Specialist (User Advocate):** The user experience expert. Designs user flows and UI structures (`.design/`).
*   **⚡ Apex Implementer (Precision Builder):** The coding specialist. Writes high-quality code based strictly on specifications.
*   **🛡️ Guardian Validator (Independent Verifier):** The quality assurance agent. Independently validates implementation against requirements.
*   **✍️ DocuCrafter (Markdown Documentation Generator):** The documentation specialist. **Operates primarily on the `.docs/` directory.** Handles specific documentation tasks delegated by the Orchestrator or triggered by commands like:
    *   `init`: Creates the standard documentation set (`README.md`, `architecture.md`, etc.) in `.docs/`.
    *   `update`: Refreshes documentation in `.docs/` based on analyzing the codebase (e.g., `src/`).

## 🚀 Get Started! 🚀

To use this specific `rooroo` agent team, you need the [Roo Code VS Code extension](https://marketplace.visualstudio.com/items?itemName=RooVeterinaryInc.roo-cline) installed.

Once Roo Code is installed:

1.  **Override Local Modes:** Copy the `.roomodes` file from this repository into the root directory of your VS Code workspace. This file contains the definitions for the `rooroo` agent team and will override any global or default modes.
2.  **Reload Roo Code:** Reload the VS Code window (`Ctrl+Shift+P` or `Cmd+Shift+P` -> "Developer: Reload Window") to ensure Roo Code recognizes the new mode configurations.
3.  **Activate the Orchestrator:** Open a Roo Code chat and select the **🧠 Master Orchestrator** mode.
4.  **State Your Goal:** Clearly describe the project or task you want to accomplish (e.g., "Implement feature X", "Refactor module Y").
5.  **Collaborate:** Follow the Orchestrator's lead. It will manage the delegation to specialist agents for design, implementation, and validation.
6.  **Manage Documentation:** To initialize or update project documentation, explicitly ask the Orchestrator to delegate the `init` or `update` task to the **✍️ DocuCrafter**, or invoke DocuCrafter directly with the command.
7.  **Review Artifacts:** Monitor progress by reviewing the specifications, designs, code, and documentation generated by the crew in their respective directories (`.specs/`, `.design/`, `.docs/`).

Let `rooroo` orchestrate your AI development team!