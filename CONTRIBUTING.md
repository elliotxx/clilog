# Contribution Guide

Thank you for considering contributing to clilog (Command Line Interface Log)!

## Development Process

1. Fork the project
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Commit Convention

We use [Conventional Commits](https://www.conventionalcommits.org/) specification:

- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation changes
- `style`: Code style changes
- `refactor`: Code refactoring
- `perf`: Performance improvements
- `test`: Test related changes
- `chore`: Build process or tooling changes

Examples:
feat: Add weekly report generation
fix: Fix authentication expiration issue
docs: Update installation instructions

## Code Style

- Use `gofmt` to format code
- Follow [Effective Go](https://golang.org/doc/effective_go.html) guidelines
- Add necessary comments and documentation
- Ensure test coverage

## Development Setup

1. Clone the project
```bash
git clone https://github.com/elliotxx/clilog.git

2. Install dependencies
```bash
go mod tidy

3. Run tests
```bash
go test ./...


## PR Checklist

- [ ] All tests pass
- [ ] Relevant documentation is updated
- [ ] Necessary test cases are added
- [ ] Code follows style guidelines
- [ ] Commit messages follow convention

## Reporting Issues

When reporting issues, please include:

1. Problem description
2. Steps to reproduce
3. Expected behavior
4. Actual behavior
5. Environment information
   - clilog version
   - Go version
   - Operating system
   - Other relevant information

## Feature Requests

We welcome feature requests! When suggesting new features:

1. Check existing issues to avoid duplicates
2. Describe the feature in detail
3. Explain use cases
4. Consider implementation approach

## Code of Conduct

Please refer to our [Code of Conduct](CODE_OF_CONDUCT.md).

## License

By contributing code, you agree to license your contribution under the [MIT License](LICENSE).
