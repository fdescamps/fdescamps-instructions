---
applyTo: '**'
---

# Coding Style & Sonar Rules

These rules must be followed by all developers and automatically checked by SonarQube/SonarCloud.

---

## 1. Naming

- **Use explicit and consistent names for variables, functions, and classes.**
- **Follow the naming convention of the language (camelCase, PascalCase, snake_case, etc.).**
- **Avoid non-standard abbreviations and single-letter names (except for loop indices).**

## 2. Complexity

- **Limit the cyclomatic complexity of functions/methods.**
- **Split long or complex functions into smaller sub-functions.**
- **Avoid excessive nesting of blocks (if/else, switch, loops).**

## 3. Comments & Documentation

- **Comment on complex or non-trivial parts of the code.**
- **Add documentation for each public function and class.**
- **Remove obsolete or unnecessary comments.**

## 4. Security

- **Never leave passwords, keys, or secrets in plain text in the code.**
- **Always validate user inputs.**
- **Use secure APIs provided by the language/framework.**

## 5. Exception Handling

- **Explicitly handle exceptions and errors.**
- **Do not use empty or generic catch blocks without processing.**
- **Log critical errors.**

## 6. Dead & Redundant Code

- **Remove dead code, unused variables, and unused imports.**
- **Avoid code duplication (factor out common functions).**

## 7. Tests

- **Write unit tests for every critical feature.**
- **Cover error cases and edge cases.**
- **Keep tests up to date as the code evolves.**

## 8. Formatting

- **Respect code indentation and formatting.**
- **Use a linter appropriate for the language.**
- **Avoid lines longer than 120 characters.**

## 9. Specific Best Practices

- **Always close opened resources (files, connections, etc.).**
- **Prefer explicit control structures over ambiguous shortcuts.**
- **Use appropriate types and avoid unnecessary conversions.**
- **Do not modify objects or arrays passed as parameters without reason.**
- **Use constants for magic values.**
- **Avoid side effects in pure functions.**
- **Use promises or async/await for asynchronous handling.**
- **Do not mix business logic with presentation logic.**
- **Use modules or namespaces to organize code.**
- **Follow the project's code style conventions (e.g., Prettier, ESLint).**
- **Use static analysis tools to detect code issues.**
- **Update code documentation with every change.**
- **Use semantic versioning for libraries and APIs.**
- **Avoid using deprecated or obsolete APIs.**
- **Use feature flags for experimental features.**
- **Use environment variables for configuration.**
- **Use a consistent error handling strategy (try/catch, error codes, etc.).**
- **Use a consistent logging strategy (log levels, formats, etc.).**
- **Use a consistent strategy for managing dependencies (e.g., package.json, requirements.txt).**
- **Use a consistent strategy for managing configuration files (e.g., .env, config.json).**
- **Use a consistent strategy for managing build and deployment (e.g., Docker, CI/CD).**
- **Use a consistent strategy for managing version control (e.g., Git).**
- **Use a consistent strategy for managing code reviews (e.g., pull requests, code reviews).**
- **Use a consistent strategy for managing documentation (e.g., Markdown).**
- **Use a consistent strategy for managing issues and tasks (e.g., Jira, Ajir).**