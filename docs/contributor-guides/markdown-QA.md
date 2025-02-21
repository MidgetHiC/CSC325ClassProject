# Markdown Quality Assurance Guide

## Introduction
To maintain high-quality documentation in this repository, contributors must use **Vale** and **markdownlint-cli** to lint, spell check, and grammar check all Markdown files before pushing to the default branch.

## Setting Up the DevContainer
Before running the quality checks, ensure you are working in the DevContainer environment:

1. Open the repository in **GitHub Codespaces** or **VS Code**.
2. If using VS Code, click the blue button in the bottom-left corner and select **Reopen in Container**.
3. This will load the configured Ubuntu-based DevContainer with the required tools pre-installed.

## Running Markdown Quality Checks
Once inside the DevContainer terminal, use the following commands to check your Markdown files:

### Spell Checking and Grammar Checking with Vale
Vale ensures that Markdown files adhere to grammar, style, and readability standards.

Run the following command in the repository's root directory:
```sh
vale .
```
This command will scan all Markdown files and provide suggestions based on the **Google Developer Documentation Style Guide** and **write-good** rules.

### Linting with markdownlint-cli
markdownlint helps enforce proper Markdown syntax and style.

Run the following command:
```sh
markdownlint .
```
This will scan all Markdown files and provide warnings or errors if any formatting issues are detected.

## Configuration Files
Two configuration files control how these tools function:

- **`.vale.ini`** (located in the repository root) defines Vale’s style and rules.
- **`.markdownlint.yaml`** (located in the repository root) configures markdownlint, with the following setting:
  ```yaml
  "MD013": false
  ```
  This disables the rule enforcing line length limits.

## Contributor Guidelines
- **Always run `vale .` and `markdownlint .`** before committing any Markdown files.
- Fix any reported issues before pushing to the repository.
- If uncertain about a flagged issue, consult the [Vale documentation](https://vale.sh/docs) and [markdownlint documentation](https://github.com/DavidAnson/markdownlint) for clarification.
- Follow the Google Developer Documentation Style Guide for writing clear and consistent documentation.

By adhering to these guidelines, we ensure high-quality and readable documentation for all contributors. Thank you for your cooperation!

