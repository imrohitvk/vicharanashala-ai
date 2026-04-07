# Vicharanashala Website

This repository is used to set up and manage the official Vicharanashala website codebase on GitHub.

We are migrating the existing React website into this repository and will host the live site on:

- https://vicharanashala.ai

## Project Goals

- Move the current React website into a version-controlled GitHub repository.
- Establish a clean team workflow for development, review, and deployment.
- Keep the source code in GitHub while serving production on the Vicharanashala domain.

## Migration Plan

1. Import or copy the current React app source code into this repository.
2. Organize project structure, scripts, and environment configuration.
3. Validate local build and production build.
4. Connect deployment pipeline to the hosting platform.
5. Point domain records so production resolves to vicharanashala.ai.

## Expected Repository Contents

Once migration is complete, this repository is expected to include:

- React application source code
- Static assets
- Build and deployment configuration
- Environment variable documentation
- Team contribution guidelines

## Local Development (to be finalized after migration)

Typical React workflow:

1. Clone the repository.
2. Install dependencies.
3. Start the development server.
4. Build for production.

We will update this section with exact commands after the app code is added.

## Deployment and Domain

- Code hosting: GitHub
- Production domain: vicharanashala.ai
- Deployment target: final hosting provider configuration to be documented in this repo

If needed, this repository can also include CI/CD workflows for automated deploys on merge to the main branch.

## Branching and Collaboration

Recommended flow:

- main: production-ready code
- feature branches: all ongoing development work
- pull requests: required for review before merge

## Immediate Next Steps

1. Add the current React project files to this repository.
2. Add a package manager lockfile and verify project scripts.
3. Document environment variables and deployment settings.
4. Add a CI workflow for build checks.

## License

This project is currently released under the repository license.