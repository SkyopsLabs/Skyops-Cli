# SkyOps CLI

A high-performance GPU monitoring and job management agent for the SkyOps network.

## Features

- **Cross-platform**: Native binaries for Linux, macOS, and Windows
- **GPU Monitoring**: Real-time NVIDIA GPU monitoring via NVML
- **System Monitoring**: CPU, memory, disk, and network statistics

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
wget https://github.com/SkyopsLabs/Skyops-Cli/releases/download/v1.0.0/skyops_1.0.0-1_amd64.deb 

# Install the package
sudo dpkg -i skyops_1.0.0-1_amd64.deb

# If there are dependency issues, fix them with:
sudo apt-get install -f
```

### Windows Installation (.msi package)

1. Download the `.msi` installer from the [releases page](https://github.com/skyopslabs/skyops-cli/releases/)
2. Double-click the installer to install
3. The Skyops binary will be installed to `C:\Program Files\SkyOps` or `C:\Program Files (x86)\SkyOps`
4. Add the installation directory to your PATH environment variable if not already added:
   - Open System Properties → Advanced → Environment Variables
   - Under System Variables, select "Path" and click "Edit"
   - Click "New" and add the installation path
   - Click "OK" to save changes
5. The CLI will be available in your PATH as `skyops`

### Manual Installation

1. Download and extract the appropriate archive for your platform
2. Move the binary to your skyops directory:

```bash
# Linux/macOS
mkdir -p ~/.skyops
mv skyops ~/.skyops/

# Add to your PATH (add this to your ~/.bashrc, ~/.zshrc, or ~/.profile)
export PATH="$HOME/.skyops:$PATH"


```

## Usage

### Start the Agent

```bash
# Authenticate with your wallet
skyops login

# Register your node with the network
skyops register

# Test connectivity to the network (add -v flag for more detailed output)
skyops ping

# Start your node to wait and process jobs if available
skyops start

# Start in daemon mode (background)
skyops start --daemon

# Check status (if node is running or not)
skyops status

# Check statistics of your node on the network
skyops stats

# Stop the daemon / node from running
skyops stop
```

### Version Information

```bash
# Show version
skyops version

# Show help
skyops help
```


## Troubleshooting

### Common Issues

1. **GPU not found**: Ensure NVIDIA drivers are installed and `nvidia-smi` works

### Logs

Check logs for troubleshooting:

- Linux/macOS: `~/.skyops/logs/gpu-agent.log`
- Windows: `%USERPROFILE%\.skyops\logs\gpu-agent.log`

### Support

- Documentation: [docs.skyopslabs.ai](https://docs.skyopslabs.ai/documentation/join-as-provider)
- Issues: [GitHub Issues](https://github.com/skyopslabs/skyops-cli/issues)
- Community: [Discord](https://discord.gg/skyops)

## License

Copyright © 2025 SkyOps Labs. All rights reserved.
