# Contributing Guide

Thank you for your interest in contributing! This guide will help you get started.

---

## Code of Conduct

By participating in this project, you agree to maintain a respectful and professional environment for everyone.

---

## How to Contribute

### 1. Fork and Clone

```bash
# Fork the repo on GitHub, then clone your fork
git clone https://github.com/YOUR_USERNAME/REPO_NAME.git
cd REPO_NAME
```

### 2. Create a Branch

Always create a new branch for your changes. Never commit directly to `main`.

```bash
# For a new feature
git checkout -b feature/your-feature-name

# For a bug fix
git checkout -b fix/bug-description

# For documentation
git checkout -b docs/what-you-are-documenting
```

### 3. Branch Naming Convention

| Type | Pattern | Example |
|------|---------|---------|
| Feature | `feature/description` | `feature/add-jwt-auth` |
| Bug Fix | `fix/description` | `fix/null-reference-error` |
| Documentation | `docs/description` | `docs/update-api-endpoints` |
| Refactor | `refactor/description` | `refactor/clean-service-layer` |
| Chore | `chore/description` | `chore/upgrade-efcore-8` |

---

## Commit Message Standards

This project follows **Conventional Commits**:

```
<type>(<scope>): <short description>

[optional body]
[optional footer]
```

### Types

| Type | When to Use |
|------|------------|
| `feat` | New feature |
| `fix` | Bug fix |
| `docs` | Documentation only |
| `refactor` | Code refactoring (no feature/fix) |
| `test` | Adding or updating tests |
| `chore` | Maintenance tasks (deps, config) |
| `perf` | Performance improvements |
| `style` | Code formatting (no logic change) |

### Examples

```bash
# Good commits
git commit -m "feat(auth): add JWT refresh token support"
git commit -m "fix(api): handle null reference in patient lookup"
git commit -m "docs(readme): add API endpoints table"
git commit -m "chore(deps): upgrade EF Core to 8.0.1"
git commit -m "refactor(services): extract appointment validation logic"
git commit -m "test(unit): add xUnit tests for booking service"

# Bad commits - avoid these
git commit -m "update"
git commit -m "fix bug"
git commit -m "changes"
git commit -m "wip"
```

---

## Development Setup

### Prerequisites
- .NET 8 SDK
- SQL Server 2019+
- Visual Studio 2022 or VS Code

### Local Setup

```bash
# 1. Install dependencies
dotnet restore

# 2. Create local config (excluded from git)
cp appsettings.json appsettings.Development.json
# Edit appsettings.Development.json with your local DB connection

# 3. Apply migrations
dotnet ef database update

# 4. Run the project
dotnet run
```

---

## Pull Request Process

### Before Submitting

- [ ] Code builds without errors (`dotnet build`)
- [ ] All existing tests pass (`dotnet test`)
- [ ] New functionality has unit tests
- [ ] No sensitive data (passwords, connection strings) in the code
- [ ] README updated if needed

### PR Template

When opening a Pull Request, please include:

```markdown
## Description
Brief description of what this PR does.

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Refactoring
- [ ] Documentation

## How to Test
Steps to test the changes locally.

## Related Issues
Closes #(issue number)
```

### PR Review Guidelines

- PRs require at least **1 review** before merging
- All CI checks must pass
- Keep PRs focused â€” one feature/fix per PR
- Respond to review comments within reasonable time

---

## Reporting Bugs

Use GitHub Issues and include:

1. **Description** â€” Clear description of the bug
2. **Steps to reproduce** â€” Exact steps that cause the issue
3. **Expected behavior** â€” What should happen
4. **Actual behavior** â€” What actually happens
5. **Environment** â€” OS, .NET version, SQL Server version

```markdown
## Bug Report

**Description:**
[Clear description]

**Steps to Reproduce:**
1. Go to '...'
2. Call endpoint '...'
3. See error

**Expected:**
[What you expected]

**Actual:**
[What happened]

**Environment:**
- OS: Windows 11
- .NET: 8.0.x
- SQL Server: 2022
```

---

## Suggesting Features

Open a GitHub Issue with:
- Clear title: `[Feature Request] Add appointment reminder emails`
- Detailed description of the feature
- Why it would be useful
- Possible implementation approach (optional)

---

## Code Style

This project uses `.editorconfig` for consistent formatting:
- **Indentation**: 4 spaces
- **Line endings**: CRLF (Windows)
- **Encoding**: UTF-8
- **Naming**: PascalCase for classes/methods, camelCase for variables

---

## Questions?

Feel free to open a GitHub Issue with the label `question` or reach out via:
- **LinkedIn**: [linkedin.com/in/mohamed-ashraf-dot-netdevelper](https://www.linkedin.com/in/mohamed-ashraf-dot-netdevelper)
- **GitHub**: [@mohamed68909](https://github.com/mohamed68909)

---

**Thank you for contributing!**