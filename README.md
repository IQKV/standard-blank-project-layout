> ## 🤔 What is this template all about?
>
> - This template can be used as a base layer for a GitHub profile page.
> - Make the project easy to maintain with **7 issue templates**.
> - Quick-start documentation with an extraordinary README structure.
> - Manage issues with **20 issue labels**.
> - Make _community healthier_ with all the guides like code of conduct, contributing, support, security...
> - Learn more with the [official GitHub guide on creating repositories from a template](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-from-a-template).
> - To start using it, click **[Use this template](https://github.com/dimdnk/standard-dotgithub-profile-layout/generate)** to create your new repository.

---

<!-- CUT HERE -->

# ✨ Blank Project Template

No Code repo for the future project.

---

<a name="changelog"></a>

## 📆 Changelog

Conventional changelog located [here](CHANGELOG.md).

<a name="acknowledgments"></a>

## 👍 Acknowledgments

...

<a name="contributing"></a>

## 🙏 Community & Contributions

Please, follow [Contributing](.github/CONTRIBUTING.md) page.

<a name="codeofconduct"></a>

## 📙 Code of Conduct

Please, follow [Code of Conduct](.github/CODE_OF_CONDUCT.md) page.

<a name="troubleshooting"></a>

## 💥 Troubleshooting

...

## 📑 License

This project is licensed under the Apache License. See the [LICENSE](LICENSE) file for more details.

## <!-- CUT HERE -->

## _GitHub Project Tooling Overview_

### 📦 Package Management

- **pnpm** - Package manager for Node.js
- **Node.js** - Version 22.13.0+ required

### 🛠️ Development Tools

- **Husky** - Git hooks management (v9.1.7)
- **lint-staged** - Pre-commit linting (v16.1.0)
- **Prettier** - Code formatting (v3.5.3)
- **Stylelint** - CSS linting (v16.21.0)

### 📋 Scripts (package.json)

```shell script
# Linting
pnpm lint                  # Run stylelint
pnpm lint:stylelint        # Lint CSS files with cache

# Code Formatting
pnpm prettier:check        # Check code formatting
pnpm prettier:write        # Auto-format code

# Maintenance
pnpm node_modules:clear    # Clean node_modules
pnpm prepare               # Setup husky hooks

# Release
pnpm release               # Create release with release-it
```

### 🔄 Workflow Automation (GitHub Actions)

- **build-nodejs-project.yml** - CI/CD for Node.js project
- **check-commit-message.yml** - Validate commit message format
- **check-pr-title.yml** - Validate pull request titles
- **use-template.yml** - Template usage workflow

### 🎯 Quality Checks

- **CommitLint** - Conventional commit message validation
- **Commitizen** - Interactive commit message creation
- **Pre-commit hooks** - Automated code quality checks via Husky
- **lint-staged** - Run linters only on staged files

### 📄 Release Management

- **release-it** - Automated versioning and publishing (v19.0.2)
- **Conventional Changelog** - Automatic changelog generation
- **pnpm integration** - Release with pnpm support

### 🏗️ Configuration Files

- `.prettierrc` / `.prettierignore` - Code formatting rules
- `.stylelintignore` - CSS linting exclusions
- `.release-it.json` - Release configuration
- `commitlint.config.js` - Commit message rules
- `.editorconfig` - Editor consistency settings

### 🤖 GitHub Features

- **Issue templates** - Standardized issue creation (7 templates)
- **PR template** - Pull request template
- **Labels** - Issue management (20+ labels via issue_label_bot.yaml)
- **Community files** - CODE_OF_CONDUCT.md, CONTRIBUTING.md, SECURITY.md, SUPPORT.md
