<!--
Sync Impact Report:
- Version change: 1.0.0 → 1.1.0 (MINOR bump for expanded TDD guidance)
- Modified principles: 
  * Made Test-Driven Development the primary principle (PRINCIPLE_1_NAME)
  * Enhanced TDD description with comprehensive requirements
  * Renumbered other principles to accommodate TDD prominence
- Added sections: Development Workflow, Quality Gates
- Removed sections: Template placeholders (all filled with concrete content)
- Templates updated: ✅ .specify/templates/plan-template.md (Constitution Check section updated with TDD gates)
- Templates requiring updates: ✅ spec-template.md already aligned, ✅ tasks-template.md already TDD-compliant
- Follow-up TODOs: None - all placeholders filled with concrete values
--->

# Speckit Constitution
<!-- Specification System Constitution -->

## Core Principles

### I. Test-Driven Development (NON-NEGOTIABLE)
All development MUST follow TDD practices: Write failing tests first → Implement minimum code to pass → Refactor while maintaining green tests. Red-Green-Refactor cycle strictly enforced for every feature. Tests serve as living documentation and design specifications. No production code without corresponding failing tests.

### II. User Story Independence
Every feature MUST be decomposed into independently testable user stories. Each story delivers value independently without dependencies on other stories. Stories prioritized as P1 (MVP), P2, P3 for incremental delivery. Independent testability ensures parallel development and validation at each increment.

### III. Specification-First Development
All features MUST start with formal specification documents. User stories with Given-When-Then acceptance criteria required before implementation. Technical requirements and success criteria defined upfront. Specifications serve as contracts between stakeholders and implementation teams.

### IV. Contract Testing & Integration
Integration tests REQUIRED for: Library contracts, API endpoints, Inter-service communication, Shared data schemas. Contract tests verify compatibility between components and prevent breaking changes. All external integrations must have contract tests.

### V. Incremental Architecture
Build MVPs through incremental delivery. Each user story adds value without breaking existing functionality. Architecture evolves through patterns discovered during implementation. Keep complexity minimal until justified by actual requirements (YAGNI principle).

## Development Workflow

**Phase 1: Setup** - Project initialization and structure per implementation plan  
**Phase 2: Foundational** - Core infrastructure that blocks all user stories  
**Phase 3: User Stories** - Independent implementation in priority order (P1 → P2 → P3)  
**Phase 4: Polish** - Cross-cutting concerns and improvements

All user stories MUST have independent tests. Tests written first, verified to fail, then implementation proceeds until tests pass.

## Quality Gates

**Constitution Compliance Check**: All plans must verify principle adherence before Phase 0 research  
**Test Coverage**: 100% test coverage for critical paths, contract tests for all integrations  
**Independent Validation**: Each user story testable and demonstrable independently  
**Documentation**: Specifications, contracts, and quickstart guides required

**Version**: 1.1.0 | **Ratified**: 2025-12-19 | **Last Amended**: 2025-12-19