# Contributing to SkyOps CLI

Thank you for your interest in contributing to SkyOps CLI! This document provides guidelines for contributing to the project.

## Development Setup

SkyOps CLI is developed in Go. To set up your development environment:

1. Install Go 1.21 or later
2. Clone the development repository (private)
3. Install dependencies: `go mod download`
4. Build the project: `go build -o skyops .`

## How to Contribute

### Reporting Issues

Before creating an issue, please:

1. Check if the issue already exists
2. Use the issue templates when available
3. Provide clear steps to reproduce the problem
4. Include system information (OS, GPU type, etc.)

### Feature Requests

We welcome feature requests! Please:

1. Check if a similar request exists
2. Describe the use case and expected behavior
3. Explain why this feature would be valuable
4. Consider the impact on existing functionality

### Pull Requests

Currently, this is a release-only repository. Development happens in our private repository. However, we welcome:

- Documentation improvements
- Bug reports with detailed reproduction steps
- Feature suggestions
- Community feedback

## Code Style

- Follow Go conventions and `gofmt` formatting
- Write clear, self-documenting code
- Include tests for new functionality
- Update documentation as needed

## Testing

Before submitting changes:

1. Run the test suite: `go test ./...`
2. Test on multiple platforms when possible
3. Verify GPU monitoring functionality works
4. Check that configuration changes are backward compatible

## Documentation

- Update README.md for user-facing changes
- Update CHANGELOG.md following the format
- Include code comments for complex logic
- Update help text and command descriptions

## Release Process

Releases are managed by the SkyOps team:

1. Development occurs in the private repository
2. Releases are tagged and published here
3. Binary assets are built and attached to releases
4. Package managers are updated (DEB, MSI)

## Community Guidelines

- Be respectful and constructive
- Focus on the technical aspects of issues
- Help other users when possible
- Follow the code of conduct

## Getting Help

- Check the documentation first
- Search existing issues
- Join our Discord community
- Contact support at support@skyopslabs.ai

## License

By contributing, you agree that your contributions will be licensed under the same license as the project (MIT License).

Thank you for contributing to SkyOps CLI!
