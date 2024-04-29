# CI/CD Workflow

The CI/CD workflow of this project is based on GitHub Actions, a automation platform of GitHub that 
allowing to automate software development workflows for software stored in a GitHub repository.
It allows you to create custom workflows, called "Actions", 
that are triggered by certain events on GitHub, 
such as when a new pull request is opened or when code is pushed to a branch.

![workflow](diagrams/out/workflow.svg#darkable)

Commits made to the main branch, typically through a Pull Request, will trigger a testing, linting & build pipeline to identify bugs early. If these pipelines are successful and a version bump is detected, a version bump commit will be created on the main branch, updating the version strings in the repository. Publishing a new release will trigger the documentation pipeline, updating the documentation hosted on GitHub Pages, and trigger the build & push pipeline to build a new docker image and upload it to the GitHub container registry.

Badges: The workflows test.yml, lint.yml & build.yml are required for the badges to work. Even though they are triggered by the orchestrator, they must run on their own. As a consequence, a pipeline (test, lint, build) runs twice for every commit to the default branch main 

# Test workflow

# Documentation workflow

## Repository files

## Project documentation
It is based on mkdocs library and follows the best practices for project documentation as described by Daniele Procida in the [Diataxis documentation framework](https://archive.is/o/rnO97/https://diataxis.fr/)

### Build documentation locally
`> mkdocs build`
or
`> make docs-build`

### CI/CD 
A GitHub actions helps to keep documentation updated and deploys the documentation.

### Docstrings
Used to generate documentation

### Badge
A badge has been added to README.md that proudly showcases the awesome documentation to the world!
