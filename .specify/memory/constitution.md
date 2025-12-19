# Speckit Constitution
<!-- Speckit Development Guidelines for OpenCode AI Plugin -->

<!-- Sync Impact Report
Version change: Initial → 1.0.0
List of modified principles: N/A (new constitution)
Added sections: Core Principles (5), Development Workflow, Quality Standards, Governance
Removed sections: N/A
Templates requiring updates: ✅ All templates reference constitution principles
Follow-up TODOs: None
-->

## Core Principles

### I. Test-Driven Development (NON-NEGOTIABLE)
All development MUST follow TDD methodology: Tests written first → User approved → Tests fail → Then implement. Red-Green-Refactor cycle strictly enforced. No production code without failing test. Rationale: Ensures reliability, prevents regressions, and maintains high code quality.

### II. Specification-First Development
Every feature MUST begin with a specification document before any implementation. Specifications include user stories, acceptance criteria, and success metrics. Rationale: Prevents scope creep and ensures user-centric development.

### III. Task-Driven Implementation
Development MUST be broken into independent, testable tasks organized by user story. Each task delivers verifiable value independently. Rationale: Enables parallel development and incremental delivery of working software.

### IV. Continuous Validation
All code changes MUST pass automated tests before integration. Contract tests required for APIs, integration tests for workflows, unit tests for functions. Rationale: Maintains system stability and prevents broken dependencies.

### V. Incremental Delivery
Features MUST be delivered in smallest valuable increments. Each increment must be independently testable and deployable. Rationale: Reduces risk, enables faster feedback, and maintains development momentum.

## Development Workflow
<!-- Speckit command sequence for feature development -->

Speckit enforces the following workflow sequence: `speckit.specify` → `speckit.plan` → `speckit.tasks` → `speckit.implement` → `speckit.checklist`. Each phase builds upon the previous and includes validation gates. Rationale: Standardized workflow ensures consistency and quality across all features.

## Quality Standards
<!-- Testing and validation requirements -->

All features MUST include: User story testing with acceptance criteria, contract testing for interfaces, integration testing for workflows, and continuous validation through automated tests. Quality gates enforced at each workflow phase. Rationale: Comprehensive testing ensures reliable, maintainable software delivery.

## Governance
All development practices MUST comply with this constitution. Amendments require documentation of changes, impact analysis, and team approval. Constitution compliance verified in all PR reviews. Rationale: Ensures consistent application of principles and continuous improvement of development practices.

**Version**: 1.0.0 | **Ratified**: 2025-12-19 | **Last Amended**: 2025-12-19