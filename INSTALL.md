# Installation Guide

This guide provides detailed installation instructions for SkyOps CLI on different platforms.

## Quick Installation

### Linux (Debian/Ubuntu) - DEB Package

```bash
# Download the latest DEB package
wget https://github.com/skyopslabs/skyops-cli/releases/skyops_1.0.0-1_amd64.deb

# Install the package
sudo dpkg -i skyops_1.0.0-1_amd64.deb

# Fix any dependency issues (if needed)
sudo apt-get install -f

# Verify installation
skyops version
```

### Windows - MSI Installer

1. Download the latest MSI installer from [releases](https://github.com/skyopslabs/skyops-cli/releases/latest)
2. Run the installer as Administrator  
3. Follow the installation wizard
4. **Restart your command prompt** after installation
5. Verify installation: `skyops version`

📋 **For detailed Windows installation instructions, including PATH setup and troubleshooting, see [WINDOWS_INSTALL.md](WINDOWS_INSTALL.md)**

### macOS/Linux - Binary Installation

```bash
# Download for your platform
# Linux x64
wget https://github.com/skyopslabs/skyops-cli/releases/latest/download/skyops-linux-amd64.tar.gz

# macOS Intel
wget https://github.com/skyopslabs/skyops-cli/releases/latest/download/skyops-darwin-amd64.tar.gz

# macOS Apple Silicon
wget https://github.com/skyopslabs/skyops-cli/releases/latest/download/skyops-darwin-arm64.tar.gz

# Extract the archive
tar -xzf skyops-*.tar.gz

# Move to PATH
sudo mv skyops /usr/local/bin/

# Or install to user directory
mkdir -p ~/.local/bin
mv skyops ~/.local/bin/
export PATH="$HOME/.local/bin:$PATH"

# Verify installation
skyops version
```

## System Requirements

### Minimum Requirements
- **OS**: Linux (Ubuntu 18.04+), macOS (10.14+), Windows (10+)
- **CPU**: x64 or ARM64 architecture
- **Memory**: 64MB RAM
- **Disk**: 50MB free space

### GPU Requirements (for GPU monitoring)
- **NVIDIA GPU** with CUDA support
- **NVIDIA Drivers** (latest recommended)
- **CUDA Toolkit** (optional, for advanced features)

### Verify GPU Setup

```bash
# Check NVIDIA drivers
nvidia-smi

# Test GPU detection with SkyOps CLI
skyops gpu status
```


## Troubleshooting

### Common Issues

**Command not found**
```bash
# Check if binary is in PATH
which skyops

# Add to PATH (Linux/macOS)
export PATH="$HOME/.local/bin:$PATH"
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc
```

**Permission denied**
```bash
# Make binary executable
chmod +x skyops

# Or install with proper permissions
sudo install -m 755 skyops /usr/local/bin/
```

**GPU not detected**
```bash
# Check NVIDIA drivers
nvidia-smi

# Check CUDA installation
nvcc --version

# Test GPU access
skyops gpu status
```

### Log Files

Check logs for detailed error information:

- **Linux/macOS**: `~/.skyops/logs/gpu-agent.log`
- **Windows**: `%USERPROFILE%\.skyops\logs\gpu-agent.log`

### Getting Help

- Check the [troubleshooting guide](https://docs.skyopslabs.ai/troubleshooting)
- Join our [Discord community](https://discord.gg/skyops)
- Create an issue on [GitHub](https://github.com/skyopslabs/skyops-cli/issues)

## Uninstallation

### DEB Package (Linux)
```bash
sudo apt remove skyops
```

### MSI Installer (Windows)
Use "Add or Remove Programs" in Windows Settings

### Manual Installation
```bash
# Remove binary
sudo rm /usr/local/bin/skyops

# Remove configuration (optional)
rm -rf ~/.skyops
```
