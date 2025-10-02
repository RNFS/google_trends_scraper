```markdown
# Contributing to apify-google-trends-scraper

First off, thank you for your interest in improving this project! We welcome contributions of all kinds: bug reports, feature requests, documentation updates, examples, and code.

## Table of Contents

- [How to Submit Changes](#how-to-submit-changes)  
- [Code Style and Quality](#code-style-and-quality)  
- [Testing](#testing)  
- [Reporting Bugs](#reporting-bugs)  
- [Feature Requests](#feature-requests)  
- [Pull Request Process](#pull-request-process)  
- [Code of Conduct](#code-of-conduct)  

## How to Submit Changes

1. Fork this repository on GitHub.  
2. Clone your fork locally:
   ```
   git clone https://github.com/your-username/google_trends_scraper.git
   cd google_trends_scraper
   ```  
3. Create a new branch for your work:
   ```
   git checkout -b feature/my-feature
   ```  
4. Make your changes in that branch.  
5. Commit your changes with a descriptive message:
   ```
   git add .
   git commit -m "Add support for custom timezones"
   ```  
6. Push your branch to your fork:
   ```
   git push origin feature/my-feature
   ```  
7. Open a Pull Request against the `main` branch of this repository.

## Code Style and Quality

- **Python**  
  - Follow [PEP 8](https://www.python.org/dev/peps/pep-0008/) for formatting.  
  - Use type hints for all public functions and classes.  
  - Include Google or Sphinx–style docstrings on all modules, classes, and functions.  
- **JavaScript/Node.js**  
  - Follow the [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript).  
  - Use semicolons and single quotes.  
  - Include JSDoc comments on public functions and classes.  
- Always run linters and formatters before committing:
  ```
  npm run lint
  npm run format
  ```

## Testing

- Unit tests should cover new features and bug fixes.  
- For Python examples, use `pytest`.  
- For Node.js examples, use `jest` or `mocha`.  
- To run all tests:
  ```
  npm test
  pytest
  ```

## Reporting Bugs

If you find a bug, please open an issue and include:

- A clear and descriptive title.  
- Steps to reproduce the problem.  
- Expected versus actual behavior.  
- Environment details:  
  - Node.js version or Python version  
  - Operating system and version  

Before opening an issue, search existing issues to avoid duplicates.

## Feature Requests

To propose a new feature, open an issue and provide:

- A clear description of the use case.  
- Desired API changes or input schema additions.  
- Any relevant examples or pseudo-code.

Label your issue with `enhancement`.

## Pull Request Process

1. Ensure any install or build dependencies are removed before the end of the layer when doing a build.  
2. Update documentation in `README.md` or `docs/` as needed.  
3. Make sure your code passes linting and tests.  
4. Commit early and often, with clear messages.  
5. Fill out the pull request template in `.github/PULL_REQUEST_TEMPLATE.md`.

## Code of Conduct

This project follows the [Contributor Covenant Code of Conduct](https://www.contributor-covenant.org/). By participating, you agree to abide by its terms. Please read `CODE_OF_CONDUCT.md` for more details.
```