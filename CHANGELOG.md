# Changelog

All notable changes to SkyOps CLI will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- Planning future features and improvements

## [1.0.0] - 2025-06-05

### Added
- Cross-platform GPU monitoring and job management agent
- Real-time NVIDIA GPU monitoring via NVML
- Comprehensive system monitoring (CPU, memory, disk, network)
- Single binary distribution with no external dependencies
- Structured logging with configurable levels
- Daemon mode for background operation
- Professional packaging for Windows MSI and Linux DEB
- Automatic PATH integration on installation

### Commands
- **Authentication**: `login` - Authenticate with SkyOps network
- **Registration**: `register` - Register node with SkyOps network  
- **Agent Control**: `start`, `stop`, `status` - Manage agent lifecycle
- **Monitoring**: `stats`, `ping` - Monitor agent performance and connectivity
- **Information**: `version`, `help` - Get version and usage information

### Features
- **Platforms**: Linux (x64, ARM64), macOS (Intel, Apple Silicon), Windows (x64)
- **GPU Support**: NVIDIA GPU monitoring with temperature, utilization, memory tracking
- **System Metrics**: Real-time CPU, memory, disk, and network monitoring
- **Job Management**: Automatic job acceptance and execution capabilities
- **Configuration**: JSON-based configuration with intelligent defaults
- **Logging**: Structured logging with file output and configurable levels

### Installation
- **Linux**: DEB package with automatic PATH setup and system integration
- **Windows**: MSI installer with Start Menu shortcuts and PATH configuration
- **macOS/Manual**: Binary distributions for flexible installation

### Security
- Secure HTTPS communication with SkyOps backend
- Local configuration management with proper file permissions
- No sensitive data exposure in logs or command output
- Authenticated API communication

[Unreleased]: https://github.com/skyopslabs/skyops-cli/compare/v1.0.0...HEAD
[1.0.0]: https://github.com/skyopslabs/skyops-cli/releases/tag/v1.0.0

