# Recording code coverage

**Tracking code coverage in Continuous Integration (CI) workflow is essential for maintaining and improving the quality of your codebase.**

Here's why it's important and how you can incorporate it into your CI workflow:

- Detecting Untested Code: As you mentioned, even though existing tests may pass, new code additions without corresponding tests can lead to decreased code coverage. By tracking code coverage in your CI workflow, you can quickly identify areas of the codebase that lack sufficient test coverage.

- Ensuring Quality: Higher code coverage doesn't guarantee bug-free code, but it does indicate a higher likelihood of thorough testing. By monitoring code coverage, you can ensure that critical parts of your codebase are adequately tested, reducing the risk of undiscovered bugs.

- Encouraging Best Practices: Integrating code coverage tracking into your CI workflow promotes a culture of writing tests alongside code changes. Developers are more likely to prioritize writing tests if they know that code coverage metrics are monitored and valued by the team.

- Preventing Regression: As the codebase evolves, new features and changes can inadvertently introduce regressions in existing functionality. Comprehensive test coverage, coupled with code coverage tracking in CI, helps catch regressions early by ensuring that existing functionality remains covered by tests.

Steps:

- Choose a Code Coverage Tool: There are several code coverage tools available for various programming languages, such as JaCoCo for Java, coverage.py for Python, Istanbul for JavaScript, and PHPUnit for PHP. Choose a tool that's compatible with your project's tech stack.

- Configure Your CI Pipeline: Integrate code coverage measurement into your CI pipeline by adding a step to run tests with coverage instrumentation enabled. This typically involves modifying your CI configuration file (e.g., .gitlab-ci.yml, .travis.yml, or azure-pipelines.yml) to include commands for running tests with coverage.

- Generate Code Coverage Reports: After running tests with coverage instrumentation, generate code coverage reports using the chosen coverage tool. These reports provide insights into which parts of your codebase are covered by tests and to what extent.

- **Publish Code Coverage Reports: Publish code coverage reports as artifacts or integrate them into your CI platform's reporting feature. This allows team members to access and review code coverage metrics alongside other CI results.**

- Set Thresholds and Notifications: Define minimum acceptable code coverage thresholds for your project and configure notifications to alert the team if coverage drops below these thresholds. This encourages proactive action to improve coverage when necessary.


| Tool | Reference|
|:-----|:--------:|
| **[Codecov](https://codecov.io/)** service| [Recording code coverage](https://py-pkgs.org/08-ci-cd#recording-code-coverage), [Codecov action](https://github.com/marketplace/actions/codecov)|


# PyPi distribution and TestPyPi

**Testing the distribution uploads to TestPyPI before uploading to PyPI**

| Tool | Reference|
|:-----|:--------:|
| **[pypa/gh-action-pypi-publish@release/v1](https://github.com/pypa/gh-action-pypi-publish)** service| [Uploading to TestPyPI and PyPI, and creating a release on GitHub](https://py-pkgs.org/08-ci-cd#uploading-to-testpypi-and-pypi-and-creating-a-release-on-github)|


# Hosting documentation online

It’s common to host Python package documentation on the free online hosting service Read the Docs, which can automate the building, deployment, and hosting of your documentation. Read the Docs works by connecting to an online repository hosting your package documentation, such as a GitHub repository.

| Tool | Reference|
|:-----|:--------:|
| **[Read the Docs](https://readthedocs.org/)** service| [Hosting documentation online](https://py-pkgs.org/06-documentation#hosting-documentation-online)|