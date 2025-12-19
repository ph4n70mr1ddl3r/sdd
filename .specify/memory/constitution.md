<!--
SYNC IMPACT REPORT
==================
Version Change: INITIAL → 1.0.0
Change Type: Initial ratification
Principles Defined:
  - I. Test-First Development (NON-NEGOTIABLE)
  - II. Specification-Driven Design
  - III. Independent Testability
  - IV. Documentation as Code
  - V. Simplicity & Clarity
Sections Added:
  - Core Principles (5 principles)
  - Quality Standards
  - Development Workflow
  - Governance
Templates Status:
  ✅ plan-template.md - Constitution Check section aligns with principles
  ✅ spec-template.md - User scenarios & testing aligns with TDD principle
  ✅ tasks-template.md - Test-first workflow aligns with TDD principle
Follow-up TODOs: None
-->

# SpecKit Constitution

## Core Principles

### I. Test-First Development (NON-NEGOTIABLE)

Test-Driven Development (TDD) is mandatory for all feature implementation:

- Tests MUST be written before implementation code
- Tests MUST fail initially, demonstrating they test new behavior
- User approval MUST be obtained on test scenarios before implementation begins
- Red-Green-Refactor cycle is strictly enforced:
  1. **Red**: Write failing tests that define desired behavior
  2. **Green**: Implement minimal code to make tests pass
  3. **Refactor**: Improve code while keeping tests green

**Rationale**: TDD ensures code correctness, prevents regression, provides living
documentation, and forces clear thinking about requirements before writing
implementation. Tests written after code tend to test what was built rather than
what was needed.

### II. Specification-Driven Design

Every feature begins with a specification that defines user scenarios and
acceptance criteria:

- Specifications MUST be written in user-centric language (user stories)
- Each user story MUST be independently testable and deliverable
- Acceptance scenarios MUST follow Given-When-Then format
- Functional requirements MUST be explicit and measurable
- Unclear requirements MUST be marked "NEEDS CLARIFICATION" rather than assumed

**Rationale**: Clear specifications prevent scope creep, enable stakeholder
alignment before development, and ensure built features match actual needs.
User-centric specifications force focus on value delivery rather than technical
implementation.

### III. Independent Testability

Every feature component must be independently verifiable:

- Each user story MUST be testable without other stories being complete
- Integration points MUST have contract tests
- Modules MUST be self-contained with clear interfaces
- Dependencies MUST be injectable to enable isolated testing

**Rationale**: Independent testability enables parallel development, incremental
delivery, easier debugging, and reduces coupling. It ensures each piece of
functionality can be verified in isolation and combined confidently.

### IV. Documentation as Code

Documentation must live alongside code and be treated as a first-class artifact:

- Implementation plans MUST define technical context before coding begins
- Data models MUST be documented before implementation
- API contracts MUST be specified before endpoint implementation
- Quickstart guides MUST be created during feature development
- Documentation MUST be version-controlled in the same repository

**Rationale**: Documentation drift is prevented when docs live with code. Teams
can onboard faster, design decisions are captured, and future maintainers
understand intent, not just implementation.

### V. Simplicity & Clarity

Favor simple, explicit solutions over clever, implicit ones:

- YAGNI (You Aren't Gonna Need It) - build only what is specified
- Prefer composition over inheritance
- Prefer explicit dependencies over hidden coupling
- Complexity MUST be justified in the Complexity Tracking section of plans
- Naming MUST be self-documenting; avoid abbreviations

**Rationale**: Simple code is maintainable code. Premature abstraction and
over-engineering create technical debt. Explicit code is easier to debug,
modify, and onboard new developers. Simplicity reduces cognitive load.

## Quality Standards

### Test Coverage Requirements

- All new features MUST have test coverage before implementation
- Contract tests MUST exist for all external integration points
- Integration tests MUST cover critical user journeys
- Unit tests are encouraged but secondary to contract/integration tests

### Code Quality Gates

- All tests MUST pass before feature is considered complete
- Linting and formatting tools MUST be configured and enforced
- Code reviews MUST verify adherence to constitution principles
- Performance requirements specified in plans MUST be verified

### Documentation Completeness

- Every feature MUST have a specification (spec.md)
- Every feature MUST have an implementation plan (plan.md)
- Every feature MUST have a task list (tasks.md)
- Complex features MUST have data model documentation
- All features MUST include quickstart guides where applicable

## Development Workflow

### Feature Development Process

1. **Specification Phase** (`/speckit.specify`):
   - Write user scenarios in plain language
   - Define acceptance criteria (Given-When-Then)
   - Identify functional requirements
   - Mark unclear requirements for clarification

2. **Planning Phase** (`/speckit.plan`):
   - Define technical context and constraints
   - Run Constitution Check - verify compliance
   - Design project structure
   - Create data models and API contracts
   - Document complexity justifications if needed

3. **Task Breakdown** (`/speckit.tasks`):
   - Break feature into independent user stories
   - Create test tasks BEFORE implementation tasks
   - Organize tasks by user story for independent delivery
   - Mark parallel-executable tasks

4. **Implementation Phase** (`/speckit.implement`):
   - Write tests first (they must fail)
   - Implement minimal code to pass tests
   - Refactor while keeping tests green
   - Validate each user story independently before moving to next

5. **Review Phase** (`/speckit.checklist`):
   - Verify all tests pass
   - Confirm constitution compliance
   - Validate documentation completeness
   - Check for unintended complexity

### Branch & Commit Strategy

- Feature branches MUST be named `###-feature-name` where ### is a unique ID
- Commits SHOULD be atomic and reference specific tasks
- Commit after each task or logical unit of work
- Test files and implementation files SHOULD be committed together

### Constitution Compliance

- Every plan MUST include a Constitution Check section
- Violations of simplicity principle MUST be documented in Complexity Tracking
- Code reviews MUST explicitly verify TDD was followed
- Features violating core principles MUST be rejected or refactored

## Governance

### Amendment Authority

This constitution supersedes all other development practices and guidelines.

Amendments require:
- Documentation of rationale for change
- Approval from project maintainers
- Migration plan for affected existing features
- Update to constitution version following semantic versioning

### Versioning Policy

Constitution versions follow semantic versioning (MAJOR.MINOR.PATCH):

- **MAJOR**: Breaking changes that remove or redefine principles
- **MINOR**: New principles or expanded guidance added
- **PATCH**: Clarifications, typo fixes, non-semantic improvements

### Compliance Review

- All pull requests MUST verify constitution compliance
- Complexity MUST be justified explicitly in implementation plans
- Test-first development MUST be verified through git history or review
- Principle violations MUST be documented and approved or rejected

### Living Document

This constitution is a living document that evolves with project needs while
preserving core values. Changes should be infrequent and deliberate.

**Version**: 1.0.0 | **Ratified**: 2025-12-19 | **Last Amended**: 2025-12-19
