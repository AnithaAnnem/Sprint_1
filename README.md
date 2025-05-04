
![image](https://github.com/user-attachments/assets/6efb9fbf-d728-4445-9dab-8e157f4257e8)

| Author        | Date       | Version | Review Level   | Reviewer Name        | 
|---------------|------------|---------|----------------|----------------------|
| Anitha Annem  | April 27   | v1.0   | Pre-Reviewer   | Priyanshu            |
| Anitha Annem  |    |     | L0             | Khushi Malhothra      |
| Anitha Annem  |            |         | L1             | Rishabh Sharma       |
| Anitha Annem  |            |         | L2             | piyush Upadhyay      |

# Table of Contents

1. [Recommended Commit Hooks](#recommended-commit-hooks)
2. [Implementation Tools](#implementation-tools)
3. [Pre-commit Hook](#pre-commit-hook)
4. [Commit-msg Hook](#commit-msg-hook)
5. [Pre-push Hook](#pre-push-hook)
6. [Contact Information](#contact-information)
7. [References](#references)

 For commit hooks understanding refer this link [Understanding commit Hooks](https://github.com/Cloud-NInja-snaatak/Documentation/blob/aniruddh_SCRUM-102/vcs_design/commithooks/understanding/README.md) 

# Recommended Commit Hooks

Below is a comprehensive list of hooks that we recommend implementing, categorized by type and purpose:

| **Hook Name**         | **Trigger Point**             | **Purpose**                                      | **Mandatory** |
|-----------------------|-------------------------------|--------------------------------------------------|---------------|
| **pre-commit**         | Before commit                 | Run linters, formatters, security scans          | ✅ Yes        |
| **commit-msg**         | On commit message             | Enforce commit message standards                 | ✅ Yes        |
| **pre-push**           | Before push                   | Run test suites, type-checks, build validation   | ✅ Yes        |
| **post-merge**         | After merge                   | Auto-install dependencies if needed              | ⚪ Optional    |
| **pre-merge-commit**   | Before merge commit           | Prevent merge of broken branches                 | ⚪ Optional    |
| **prepare-commit-msg** | Before commit message editor  | Auto-generate commit prefixes/tags               | ⚪ Optional    |
| **pre-rebase**         | Before rebase                 | Block unsafe rebases                             | ⚪ Optional    |

# Implementation Tools

We recommend using the following tools to manage and implement Git hooks efficiently:

| **Tool**             | **Use Case**                                 |
|----------------------|----------------------------------------------|
| **Husky**            | Manage Git hooks via scripts                 |
| **Lint-Staged**      | Run linters only on staged files             |
| **Commitlint**       | Enforce commit message format                |
| **Prettier**         | Code formatting                              |
| **ESLint**           | JavaScript/TypeScript linting                |
| **detect-secrets**   | Prevent committing secrets                   |
| **Jest / PyTest**    | Run test suites in `pre-push` hook only      |

# Pre-commit Hook

### Purpose:
Ensure that only clean, linted, and secure code is committed.

### Checks:
- **Linting**: Use tools like **ESLint** (for JavaScript/TypeScript), **Flake8** (for Python), etc., to catch syntax and style issues.
- **Formatting**: Automatically format code with tools like **Prettier** (for JavaScript) or **Black** (for Python) to enforce consistent code style.
- **Secrets Detection**: Tools like **GitLeaks** or **detect-secrets** help prevent sensitive data such as API keys or passwords from being committed to the repository.
- **Large File Prevention**: Ensure that large files are not accidentally committed by implementing a custom script that checks for file size limits.

### Example Configuration:

You can use **husky** and **lint-staged** to run these checks in your `pre-commit` hook:

```bash
# Install dependencies
npm install --save-dev husky lint-staged eslint prettier detect-secrets

# Initialize husky (if not done already)
npx husky install

# Create a pre-commit hook
npx husky add .husky/pre-commit "npx lint-staged"
```

Then configure lint-staged to run the checks:

```json
// .lintstagedrc.json
{
  "src/**/*.{js,ts}": ["eslint --fix", "prettier --write"],
  "src/**/*.{py}": ["flake8", "black"],
  "src/**/*": ["detect-secrets --scan"]
}
```

This configuration will run ESLint and Prettier on JavaScript/TypeScript files, Flake8 and Black on Python files, and detect-secrets on all files before they are committed.

# Commit-msg Hook

### Purpose:
Enforce a consistent and conventional commit message format.

### Checks:
- **Match Conventional Commits**: Ensure commit messages follow a standard format, such as `feat:` for new features, `fix:` for bug fixes, and so on.
- **Block Generic or Non-descriptive Messages**: Prevent commit messages like "update" or "fix issues" that don’t clearly explain the change.

### Example Configuration:

You can use **Commitlint** to enforce the commit message format:

1. Install **Commitlint** and the necessary configuration:

```bash
npm install --save-dev @commitlint/{config-conventional,cli}

```
2. Add a commitlint configuration file (e.g., commitlint.config.js):

```javascript
// commitlint.config.js
module.exports = { extends: ['@commitlint/config-conventional'] };
```
3. Add a commit-msg hook with Husky:


```bash
npx husky add .husky/commit-msg "npx --no-install commitlint --edit $1"
```

#  Pre-push Hook

### Purpose:
Ensure that only tested, valid code is pushed to remote repositories.

### Checks:
- **Unit and Integration Tests**: Run tests to verify the functionality of your code before pushing.
- **Build Verification**: Ensure that the code builds successfully and does not break the build process.
- **Type-checking**: For TypeScript or Python projects, ensure type correctness by running type-checking tools like **TypeScript** or **MyPy**.

### Example Configuration:

1. Install **Jest** for testing and **TypeScript** type checking (if using TypeScript):

```bash
npm install --save-dev jest typescript ts-jest
```
2. Set up a pre-push hook using Husky:

```bash
npx husky add .husky/pre-push "npm test && tsc --noEmit"
```
This configuration runs your tests with Jest and checks TypeScript types with the TypeScript compiler.

For Python, you can set up PyTest and MyPy:
```bash
pip install pytest mypy
```

Add the following to the pre-push hook:
```bash
npx husky add .husky/pre-push "pytest && mypy src/"
```

This ensures that all code passes tests and type checks before it is pushed.

# Contact Information

| Name       | Email Address                |
|------------|------------------------------|
| Anitha     |anitha.annem.snaatak@mygurukulam.co|

# References

| **Link** | **Description** |
|----------|-----------------|
| [githooks](https://git-scm.com/docs/githooks) | The documentation for this section is followed from this link. |






