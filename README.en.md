<p align="center">
  <h1 align="center">🚀 MacDevKit</h1>
</p>

<p align="center">
  <img src="docs/brand.webp" alt="MacDevKit Logo" width="200">
</p>

<p align="center">
  <strong>The Ultimate Toolkit for Setting Up macOS Development Environment in One Click</strong>
</p>

<p align="center">
  <a href="#-features">✨ Features</a> •
  <a href="#-quick-start">🚀 Quick Start</a> •
  <a href="#-usage">📖 Usage</a> •
  <a href="#-included-tools">🛠️ Included Tools</a> •
  <a href="#-customization">⚙️ Customization</a> •
  <a href="#-local-build">🛠 Local Build</a> •
  <a href="#-contributing">👥 Contributing</a> •
  <a href="#-license">📄 License</a>
</p>

<p align="center">
  <a href="https://github.com/zyz199/MacDevKit/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/zyz199/MacDevKit" alt="License">
  </a>
  <img src="https://img.shields.io/badge/platform-macOS-lightgrey" alt="Platform">
  <img src="https://img.shields.io/badge/shell-bash-4EAA25" alt="Shell">
  <img src="https://img.shields.io/badge/macOS-Monterey%20|%20Ventura%20|%20Sonoma-blue" alt="macOS">
</p>

_[中文文档](README.md) | English_

---

## ✨ Features

MacDevKit is a comprehensive macOS development environment setup toolkit designed for developers, capable of setting up a new Mac development environment in minutes.

- 🚀 **One-Click Installation** - Set up all development tools and configurations with a single command
- 🎨 **Beautiful Interface** - Colorful output and clear progress indicators
- 🔄 **Idempotent Operations** - Can be safely run multiple times without duplicate installations
- 🔧 **Comprehensive Toolset** - Includes all tools needed for frontend, backend, mobile, and cloud development
- 🎛️ **Interactive Options** - Choose which applications and configurations to install
- 💻 **Support for Intel and Apple Silicon** - Automatically detects and adapts to different Mac chips
- 🔒 **Secure and Reliable** - Uses official sources and secure installation methods
- ⚙️ **Developer-Friendly System Settings** - Automatically configures macOS to enhance development experience, including:
  - Show hidden files in Finder
  - Display path bar and status bar in Finder windows
  - Enable key repeat (disable press-and-hold for special characters)
  - Increase keyboard repeat rate
  - Disable auto-correct
  - Enhance security settings
  - Configure screenshot settings (location and format)

<p align="center">
  <img src="https://user-images.githubusercontent.com/12573233/236685568-5b4c9ae5-f222-4fdb-b1bf-b536d2cc0c0d.gif" alt="MacDevKit Demo" width="600">
</p>

## 🚀 Quick Start

### Method 1: Using Bash Script (Fastest)

```bash
# Download the script
curl -fsSL https://raw.githubusercontent.com/zyz199/MacDevKit/main/init.sh -o init.sh

# Make the script executable
chmod +x init.sh

# Run the script directly to ensure interactive commands work properly
./init.sh
```

### Method 2: Using Modern Rust CLI

```bash
# Clone the repository
git clone https://github.com/zyz199/MacDevKit.git
cd MacDevKit/macdevkit-cli

# Build the project
cargo build --release

# Run the CLI
./target/release/macdevkit-cli
```

**Tip**: Both methods provide the same functionality. Choose the one you prefer. The Bash script requires no build, while the Rust CLI provides a modern user interface.

## 📖 Usage

After running the script, you'll see an interactive interface guiding you through the entire setup process:

1. The script will first install basic tools like Homebrew, Git, and Xcode Command Line Tools
2. Then, it will set up your Git configuration and generate SSH keys
3. Next, it will install development tools like VS Code, Node.js, Docker, etc.
4. You can choose to install additional applications like Chrome, Slack, Postman, etc.
5. Finally, you can choose to configure macOS system settings to optimize your development experience

The script displays colorful output, clearly indicating current progress and success/failure status.

## 🛠️ Included Tools

MacDevKit includes the following development tools and applications:

### Basic Tools

- **Homebrew** - macOS package manager
- **Git** - Version control system
- **Xcode Command Line Tools** - Basic development tools

### Development Environment

- **Visual Studio Code** - Code editor with common extensions
- **iTerm2** - Terminal emulator
- **Oh My Zsh** - Zsh configuration framework with Powerlevel10k theme and plugins
- **Docker** - Containerization platform

### Programming Languages and Runtimes

- **Node.js** (via NVM) - JavaScript runtime
- **Python** - Programming language
- **Go** - Programming language
- **Rust** - Programming language

### Database Tools

- **PostgreSQL** - Relational database
- **MySQL** - Relational database
- **SQLite** - Lightweight database

### Cloud Tools

- **AWS CLI** - Amazon Web Services command-line tool
- **Terraform** - Infrastructure as code tool

### Command Line Tools

- **jq** - JSON processor
- **ripgrep** - Fast search tool
- **fd** - Fast find tool
- **bat** - Enhanced cat command
- **exa** - Enhanced ls command
- **htop** - Process viewer
- **tmux** - Terminal multiplexer
- **fzf** - Fuzzy finder
- And more...

### Optional Applications

- **Google Chrome** - Web browser
- **Firefox** - Web browser
- **Slack** - Team collaboration tool
- **Postman** - API testing tool
- **Rectangle** - Window manager
- **Alfred** - Productivity tool
- **Notion** - Note-taking and collaboration tool
- **Obsidian** - Knowledge management tool
- **Figma** - Design tool

## ⚙️ Customization

You can customize the installation process by editing the `init.sh` file:

- Add or remove tools and applications to install
- Modify Git configuration and SSH key generation
- Adjust VS Code extensions
- Change macOS system settings

Future versions will support more flexible customization through configuration files.

## 🛠 Local Build

If you want to build MacDevKit CLI from source or develop the project, follow these steps:

### Prerequisites

- **Rust Toolchain** - Requires Rust 1.70 or higher
  ```bash
  # Install Rust using rustup (if not already installed)
  curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
  
  # Update to the latest version
  rustup update
  ```

- **Git** - For cloning the repository
  ```bash
  # Usually pre-installed on macOS, or install via Homebrew
  brew install git
  ```

### Build Steps

#### Method 1: Using Cargo (Recommended)

```bash
# 1. Clone the repository
git clone https://github.com/zyz199/MacDevKit.git
cd MacDevKit/macdevkit-cli

# 2. Build release version
cargo build --release

# 3. Run the built binary
./target/release/macdevkit-cli

# 4. (Optional) Install to system path
cargo install --path .
# Binary will be installed to ~/.cargo/bin/macdevkit-cli
```

#### Method 2: Using Makefile

The project includes a Makefile to simplify common operations:

```bash
# Build the project
make build

# Build and install to ~/.local/bin
make install

# Run the project (development mode)
make run

# Run tests
make test

# Clean build artifacts
make clean
```

After installation, make sure to add the installation directory to your PATH:

```bash
# For make install (installs to ~/.local/bin)
export PATH="$HOME/.local/bin:$PATH"

# For cargo install (installs to ~/.cargo/bin)
export PATH="$HOME/.cargo/bin:$PATH"

# Add the above line to ~/.zshrc or ~/.bashrc to persist the setting
```

### Development Build

If you're developing or debugging, you can use development mode builds:

```bash
# Development build (faster, but not optimized)
cargo build

# Run development version
cargo run

# Run with arguments
cargo run -- --help

# Enable logging for debugging
RUST_LOG=debug cargo run

# Run tests
cargo test

# Run tests with output
cargo test -- --nocapture

# Check code style
cargo clippy

# Format code
cargo fmt
```

### Build Artifacts

- Release binary located at: `target/release/macdevkit-cli`
- Debug binary located at: `target/debug/macdevkit-cli`
- Size comparison: Release version is optimized, smaller in size, and runs faster

### Project Structure

```
macdevkit-cli/
├── Cargo.toml          # Project configuration and dependencies
├── Cargo.lock          # Dependency lock file
├── Makefile            # Build automation
├── build.rs            # Build script
├── init_wrapper.sh     # Shell wrapper script
└── src/
    ├── main.rs         # Main program entry
    └── script_handler.rs  # Script handling logic
```

### Dependencies

The project uses the following main dependencies:

- **clap** (4.4) - Command-line argument parsing
- **colored** (2.0) - Colored terminal output
- **dialoguer** (0.11) - Interactive command-line interface
- **indicatif** (0.17) - Progress bars and loading indicators
- **which** (5.0) - Find system executables

### Troubleshooting

**Q: Build fails with Rust toolchain not found**
```bash
# Install or update Rust
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env
```

**Q: Linker errors or dependency issues**
```bash
# Clean and rebuild
cargo clean
cargo build --release
```

**Q: How to cross-compile to other platforms?**
```bash
# Add target platform (e.g., Intel Mac)
rustup target add x86_64-apple-darwin

# Build for specific platform
cargo build --release --target x86_64-apple-darwin
```

**Q: Build takes too long**
```bash
# Use incremental compilation (enabled by default) and parallel builds
cargo build --release -j 4

# Or use sccache to cache compilation results
cargo install sccache
export RUSTC_WRAPPER=sccache
cargo build --release
```

## 👥 Contributing

Contributions are welcome! If you have suggestions for improvements or have found issues, please:

1. Fork this repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Create a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<p align="center">
  <sub>Made with ❤️ by <a href="https://github.com/zyz199">zyz199</a></sub>
</p>
