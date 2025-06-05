# SkyOps CLI

A high-performance GPU monitoring and job management agent for the SkyOps network.

## Features

- **Cross-platform**: Native binaries for Linux, macOS, and Windows
- **GPU Monitoring**: Real-time NVIDIA GPU monitoring via NVML
- **System Monitoring**: CPU, memory, disk, and network statistics
- **Job Management**: Automatic job offer handling and execution
- **Lightweight**: Single binary with no dependencies
- **Logging**: Structured logging with configurable levels

## Installation

### Download Pre-built Binaries

Download the appropriate binary for your platform from the [latest release](https://github.com/skyopslabs/skyops-cli/releases/):

- **Linux (x64)**: `skyops-linux-amd64.tar.gz`
- **Linux (ARM64)**: `skyops-linux-arm64.tar.gz`  
- **macOS (Intel)**: `skyops-darwin-amd64.tar.gz`
- **macOS (Apple Silicon)**: `skyops-darwin-arm64.tar.gz`
- **Windows (x64)**: `skyops-windows-amd64.zip`

### Linux Installation (.deb package)

```bash
# Download the .deb package from releases
wget https://github.com/skyopslabs/skyops-cli/releases/latest/download/skyops_1.0.0-1_amd64.deb

# Install the package
sudo dpkg -i skyops_1.0.0-1_amd64.deb

# If there are dependency issues, fix them with:
sudo apt-get install -f
```

### Windows Installation (.msi package)

1. Download the `.msi` installer from the [releases page](https://github.com/skyopslabs/skyops-cli/releases/)
2. Double-click the installer and follow the setup wizard
3. The CLI will be available in your PATH as `skyops`

### Manual Installation

1. Download and extract the appropriate archive for your platform
2. Move the binary to your skyops directory:

```bash
# Linux/macOS
mkdir -p ~/skyops
mv skyops ~/skyops/

# Add to your PATH (add this to your ~/.bashrc, ~/.zshrc, or ~/.profile)
export PATH="$HOME/skyops:$PATH"

# Or use the system-wide installation
sudo mv skyops /usr/local/bin/
```

## Configuration

Create a configuration file at `~/skyops/config.json`:

```json
{
  "agent_id": "skyops_node_${hostname}",
  "backend_url": "https://app.skyopslabs.ai", 
  "heartbeat_interval": 30,
  "max_price_per_hour": 1.50,
  "auto_accept_jobs": false,
  "gpu_whitelist": [],
  "logging_level": "info",
  "logging_file": "gpu-agent.log"
}
```

## Usage

### Start the Agent

```bash
# Start with default configuration
skyops start

# Start with custom config file
skyops start --config /path/to/config.json

# Start in daemon mode (background)
skyops daemon start

# Check status
skyops status

# Stop the daemon
skyops daemon stop
```

### Monitor GPU Status

```bash
# Show current GPU status
skyops gpu status

# Monitor GPU usage in real-time
skyops gpu monitor

# Show system information
skyops system info
```

### Version Information

```bash
# Show version
skyops version

# Show detailed build information
skyops version --verbose
```

## Command Reference

- `skyops start` - Start the agent
- `skyops daemon start|stop|status` - Manage daemon process
- `skyops gpu status|monitor` - GPU monitoring commands
- `skyops system info` - System information
- `skyops version` - Version information
- `skyops help` - Show help

## Troubleshooting

### Common Issues

1. **GPU not detected**: Ensure NVIDIA drivers are installed and `nvidia-smi` works
2. **Permission denied**: Run with appropriate permissions or use `sudo` for system-wide installation
3. **Config file not found**: Create the config directory: `mkdir -p ~/skyops`

### Logs

Check logs for troubleshooting:
- Linux/macOS: `~/skyops/logs/gpu-agent.log`
- Windows: `%USERPROFILE%\skyops\logs\gpu-agent.log`

### Support

- Documentation: [docs.skyopslabs.ai](https://docs.skyopslabs.ai)
- Issues: [GitHub Issues](https://github.com/skyopslabs/skyops-cli/issues)
- Community: [Discord](https://discord.gg/skyops)

## License

Copyright © 2025 SkyOps Labs. All rights reserved.
