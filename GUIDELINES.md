# IEEE CS Project Guidelines

This repository serves as the official IEEE Computer Society project template.

All IEEE CS repositories should be created using this template to ensure:
- Consistent documentation
- Standardized contribution workflow
- Structured issue tracking
- Governance and branch discipline

---

## Purpose

This template provides:
- README structure
- Contribution guidelines
- Issue templates
- Pull request template
- Environment variable policy
- Basic CI placeholder

Teams must customize this template according to their project stack.

---

## How To Use This Template

When creating a new project from this repository:

1. Replace the contents of this README with the project-specific README template provided below.
2. Fill in all placeholder sections.
3. Define the project’s tech stack and architecture.
4. Update `.env.example` with required variables.
5. Modify CI workflow based on the project stack.

---

## Environment Policy

- `.env` files must never be committed.
- `.env.example` should define required variables without values.
- Production secrets must be stored in deployment platform dashboards.
- Access to production credentials should be restricted to maintainers.

---

## Containerization Policy

All IEEE CS projects must provide a Docker setup.

Each project repository should include:

- A valid `Dockerfile`
- A `docker-compose.yml` (if multiple services are involved)
- Clear instructions for building and running containers

Example build command:

docker build -t <project-name> .

Example run command:

docker run -p <port>:<port> <project-name>

Projects are responsible for customizing Docker configuration according to their stack.

---

## Branch Strategy

All repositories created from this template must follow the branching strategy below:

Recommended Workflow:

feature/* → dev → main

All changes should first be merged into `dev`, and then into `main` after review.

- `main` → Protected branch
- `feature/<feature-name>` → New features
- `fix/<issue-name>` → Bug fixes
- `chore/<task>` → Maintenance

Direct commits to `main` are not allowed.

---

## Contribution Rules

- All changes must go through Pull Requests.
- At least one reviewer approval required before merge.
- Clear PR descriptions are mandatory.
- Follow structured issue templates.

---