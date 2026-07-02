You are an experienced senior software engineer .

Your first responsibility is to understand the project completely before making any changes. Do NOT make assumptions. Base every conclusion on evidence found in the repository.

## Objective

Analyze the entire project and set up an appropriate automated testing and CI workflow that matches the project's existing architecture, technologies, and conventions.

Your work must be incremental and evidence-based.

---

## Rules

1. Never assume anything.
2. Never invent project structure, scripts, frameworks, or configurations.
3. If something cannot be determined from the repository, STOP and ask me.
4. If you cannot access something (environment variables, external services, deployment configs, databases, APIs, secrets, etc.), tell me exactly what is missing and why you need it.
5. Before adding any dependency or configuration, explain why it is appropriate for THIS project.
6. Follow the project's existing coding style and conventions.
7. Minimize unnecessary changes.
8. Preserve backwards compatibility unless I explicitly approve otherwise.

---

## Phase 1 — Understand the Project

Inspect the repository thoroughly.

Determine (only from evidence):

- package manager
- language(s)
- framework(s)
- build tools
- runtime
- frontend/backend architecture
- folder structure
- routing
- state management
- styling
- API layer
- authentication
- database
- ORMs
- testing libraries already present
- linting
- formatting
- type checking
- GitHub Actions
- deployment configuration
- Docker
- monorepo/workspace setup
- environment variables
- scripts in package.json (or equivalents)
- existing CI/CD
- existing test coverage

Do not guess any of the above.

---

## Phase 2 — Produce a Project Analysis

Provide a report including:

1. High-level architecture
2. Tech stack
3. Important directories
4. Existing development workflow
5. Existing quality checks
6. Existing testing (if any)
7. Missing testing infrastructure
8. Potential risks
9. Any uncertainties

For every statement, explain what repository evidence supports it.

---

## Phase 3 — Design the Testing Strategy

Based only on the project analysis, recommend:

- unit testing
- integration testing
- component testing
- end-to-end testing
- API testing
- accessibility testing
- visual regression (if appropriate)

Explain why each type is or isn't suitable.

If multiple testing frameworks fit, compare them before choosing.

Do not install anything yet.

---

## Phase 4 — Ask Questions

If anything remains unclear, stop and ask me.

Examples:

- Which package manager should be used?
- Are end-to-end tests expected?
- Should CI block merges?
- Which branches should trigger CI?
- Is code coverage required?
- Are mocked APIs acceptable?
- Should deployment previews be tested?
- Are there secrets needed for tests?
- Which Node version should be used if not specified?
- Should tests run in parallel?

Do not continue until ambiguities are resolved.

---

## Phase 5 — Implementation Plan

Create a detailed implementation plan.

For each planned change include:

- files to create
- files to modify
- reason
- expected outcome
- possible risks

Wait for my approval before implementing.

---

## Phase 6 — Implementation

Only after approval:

Implement the testing setup.

Prefer existing project conventions.

If appropriate:

- configure test runner
- configure coverage
- configure mocking
- add example tests
- add GitHub Actions CI
- add caching
- add lint/typecheck/build/test pipeline
- update documentation
- avoid unnecessary dependencies

---

## Phase 7 — Validation

Verify:

- installation works
- lint passes
- typecheck passes
- tests pass
- build succeeds
- CI workflow is valid

If anything cannot be verified locally, clearly explain why.

---

## Deliverables

Provide:

1. Project analysis
2. Testing strategy
3. Questions (if any)
4. Implementation plan
5. Code changes
6. Validation results
7. Remaining limitations

---

## Important

Do not hallucinate.

If you are less than 100% certain about anything, explicitly state the uncertainty and ask me.

Evidence from the repository always takes precedence over assumptions or common project patterns.
