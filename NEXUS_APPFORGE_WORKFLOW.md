# NEXUS AppForge — Application Development System

## What this system is
A repeatable engineering workflow and prompt kit for turning an app idea into a tested release. It is not itself an autonomous coding agent. Actual code execution, repository writes, database provisioning and deployment require connected tools, permissions and sometimes paid services.

## Delivery pipeline

| Stage | Output | Exit condition |
|---|---|---|
| 1. Discover | Problem statement, users, assumptions | User and problem are clear |
| 2. Define | PRD, MVP, user stories | Acceptance criteria are testable |
| 3. Design | User journeys, screens, architecture | Data flow and main screens agreed |
| 4. Model | Database schema, API contracts | Ownership and validation rules defined |
| 5. Build | Working frontend/backend | MVP user journey works locally |
| 6. Verify | Automated tests and manual QA | Critical tests pass or blockers documented |
| 7. Secure | Threat review and privacy checklist | High-risk issues fixed or disclosed |
| 8. Release | Deployment, docs, rollback | Public URL and commit verified |
| 9. Operate | Monitoring, backups, feedback | Recovery and maintenance plan exists |

## Recommended repository structure

```text
app/
  frontend/
  backend/
  shared/
docs/
  PRD.md
  ARCHITECTURE.md
  DATA_MODEL.md
  API.md
  TEST_PLAN.md
  SECURITY_REVIEW.md
  DEPLOYMENT.md
tests/
  unit/
  integration/
  e2e/
.env.example
.gitignore
README.md
```

Adapt this to the chosen framework; do not create empty folders just to match a template.

## Default zero-budget principles
- Start with a local development environment.
- Use a single deployable application until scale requires separation.
- Prefer established open-source libraries.
- Use managed free tiers only after checking current quotas, sleep/cold-start behavior, backups and data limits.
- Do not collect sensitive data unless necessary.
- Do not add payments until the product's paid value, refund policy, tax requirements and support process are understood.
- Never store passwords in plaintext or commit API keys.

## Definition of done
An MVP is ready for a controlled test when:
- A new user can complete the primary task.
- Data persists in the intended environment.
- Authorization prevents cross-user access where accounts exist.
- Inputs are validated and errors are understandable.
- Critical paths have executed tests.
- Mobile layout and keyboard basics have been checked.
- README setup instructions work on a clean environment.
- Environment variables are documented without exposing secrets.
- Backup/export and recovery limitations are documented.
- No fake completion, analytics, security or deployment claims remain.

## Release gate
Do not announce "production ready" merely because the UI renders. Record the exact build, test, security-review and deployment evidence. If any gate is blocked, label the release as prototype, beta or staging as appropriate.
