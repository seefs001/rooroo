# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [v0.0.2] - 2025-04-25

### Changed
- **Agent Directive Overhaul (v2/v3/v4):** Updated agent instructions in `.roomodes` to enhance coordination and robustness.
    - **Centralized State:** Mandated `project_state.json` for all workflow state, task tracking, and status updates.
    - **Standardized Protocols:** Clarified task handoff (Architect defines, Orchestrator delegates based on state), status reporting (agents update `project_state.json`), logging (within `project_state.json`), and `new_task` payload structure.
    - **Refined Error Handling:** Restricted Orchestrator's direct fixes and improved the interactive debugging protocol using `Blocked-Debug` status.
    - **Increased Clarity:** Improved consistency and definitions across agent roles.

## [v0.0.1] - Initial Release
- Initial project setup and definition of core agent roles.