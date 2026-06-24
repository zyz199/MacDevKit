<p align="center">
  <h1 align="center">🚀 MacDevKit</h1>
</p>

<p align="center">
  <img src="docs/brand.webp" alt="MacDevKit Logo" width="200">
</p>

<p align="center">
  <strong>一键配置 macOS 开发环境的终极脚本</strong>
</p>

<p align="center">
  <a href="#-特性">✨ 特性</a> •
  <a href="#-快速开始">🚀 快速开始</a> •
  <a href="#-安装方式">🔧 安装方式</a> •
  <a href="#-使用方法">📖 使用方法</a> •
  <a href="#-包含工具">🛠️ 包含工具</a> •
  <a href="#-自定义">⚙️ 自定义</a> •
  <a href="#-本地构建">🛠 本地构建</a> •
  <a href="#-贡献">👥 贡献</a> •
  <a href="#-许可证">📄 许可证</a>
</p>

<p align="center">
  <a href="https://github.com/zyz199/MacDevKit/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/zyz199/MacDevKit" alt="License">
  </a>
  <img src="https://img.shields.io/badge/platform-macOS-lightgrey" alt="Platform">
  <img src="https://img.shields.io/badge/shell-bash-4EAA25" alt="Shell">
  <img src="https://img.shields.io/badge/macOS-Monterey%20|%20Ventura%20|%20Sonoma-blue" alt="macOS">
</p>

_中文 | [English](README.en.md)_

---

## ✨ 特性

MacDevKit 是一个全面的 macOS 开发环境配置工具包，专为开发者设计，可以在几分钟内完成新 Mac 的开发环境设置。

- 🚀 **一键安装** - 一个命令设置所有开发工具和配置
- 🎨 **美观的界面** - 彩色输出和清晰的进度指示
- 🔄 **幂等操作** - 可以安全地多次运行，不会重复安装
- 🔧 **全面的工具集** - 包含前端、后端、移动和云开发所需的所有工具
- 🎛️ **交互式选项** - 可以选择安装哪些应用程序和配置
- 💻 **支持 Intel 和 Apple Silicon** - 自动检测并适配不同的 Mac 芯片
- 🔒 **安全可靠** - 使用官方源和安全的安装方法
- ⚙️ **开发者友好的系统设置** - 自动配置 macOS 系统，优化开发体验，包括：
  - 显示 Finder 中的隐藏文件
  - 在 Finder 窗口显示路径栏和状态栏
  - 启用按键重复（禁用长按弹出特殊字符）
  - 增加键盘重复速率
  - 禁用自动更正
  - 增强安全设置
  - 自定义截图设置（位置和格式）
- 🦀 **现代化 CLI** - 提供 Rust 编写的现代命令行界面（可选）

<p align="center">
  <img src="https://user-images.githubusercontent.com/12573233/236685568-5b4c9ae5-f222-4fdb-b1bf-b536d2cc0c0d.gif" alt="MacDevKit Demo" width="600">
</p>

## � 快速开始

### 方式一：使用 Bash 脚本（最快）

```bash
# 下载脚本到本地
curl -fsSL https://raw.githubusercontent.com/zyz199/MacDevKit/main/init.sh -o init.sh

# 给脚本赋予执行权限
chmod +x init.sh

# 直接执行脚本
./init.sh
```

### 方式二：使用现代化 Rust CLI

```bash
# 克隆项目
git clone https://github.com/zyz199/MacDevKit.git
cd MacDevKit/macdevkit-cli

# 构建项目
cargo build --release

# 运行 CLI
./target/release/macdevkit-cli
```

**提示**：两种方式功能相同，选择你喜欢的即可。Bash 脚本无需构建，Rust CLI 提供现代化的用户界面。

## 📖 使用方法

运行脚本后，您将看到一个交互式界面，引导您完成整个设置过程：

1. 脚本将首先安装基本工具，如 Homebrew、Git 和 Xcode Command Line Tools
2. 然后，它会设置您的 Git 配置并生成 SSH 密钥
3. 接下来，它会安装开发工具，如 VS Code、Node.js、Docker 等
4. 您可以选择安装额外的应用程序，如 Chrome、Slack、Postman 等
5. 最后，您可以选择配置 macOS 系统设置，优化开发体验

脚本执行过程中会显示彩色输出，清晰指示当前进度和成功/失败状态。

## 🛠️ 包含工具

MacDevKit 包含以下开发工具和应用程序：

### 基础工具

- **Homebrew** - macOS 包管理器
- **Git** - 版本控制系统
- **Xcode Command Line Tools** - 基本开发工具

### 开发环境

- **Visual Studio Code** - 代码编辑器，包含常用扩展
- **iTerm2** - 终端模拟器
- **Oh My Zsh** - Zsh 配置框架，包含 Powerlevel10k 主题和插件
- **Docker** - 容器化平台

### 编程语言和运行时

- **Node.js** (通过 NVM) - JavaScript 运行时
- **Python** - 编程语言
- **Go** - 编程语言
- **Rust** - 编程语言

### 数据库工具

- **PostgreSQL** - 关系型数据库
- **MySQL** - 关系型数据库
- **SQLite** - 轻量级数据库

### 云工具

- **AWS CLI** - Amazon Web Services 命令行工具
- **Terraform** - 基础设施即代码工具

### 命令行工具

- **jq** - JSON 处理器
- **ripgrep** - 快速搜索工具
- **fd** - 快速查找工具
- **bat** - 增强的 cat 命令
- **exa** - 增强的 ls 命令
- **htop** - 进程查看器
- **tmux** - 终端复用器
- **fzf** - 模糊查找器
- 以及更多...

### 可选应用程序

- **Google Chrome** - 网络浏览器
- **Firefox** - 网络浏览器
- **Slack** - 团队协作工具
- **Postman** - API 测试工具
- **Rectangle** - 窗口管理工具
- **Alfred** - 生产力工具
- **Notion** - 笔记和协作工具
- **Obsidian** - 知识管理工具
- **Figma** - 设计工具

## ⚙️ 自定义

您可以通过编辑 `init.sh` 文件来自定义安装过程：

- 添加或删除要安装的工具和应用程序
- 修改 Git 配置和 SSH 密钥生成
- 调整 VS Code 扩展
- 更改 macOS 系统设置

未来版本将支持通过配置文件进行更灵活的自定义。

## 🛠 本地构建

如果您想从源代码构建 MacDevKit CLI 或对项目进行开发，请按照以下步骤操作：

### 前提条件

- **Rust 工具链** - 需要安装 Rust 1.70 或更高版本
  ```bash
  # 使用 rustup 安装 Rust（如果还没有安装）
  curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
  
  # 更新到最新版本
  rustup update
  ```

- **Git** - 用于克隆仓库
  ```bash
  # macOS 上通常已预装，或通过 Homebrew 安装
  brew install git
  ```

### 构建步骤

#### 方式一：使用 Cargo（推荐）

```bash
# 1. 克隆仓库
git clone https://github.com/zyz199/MacDevKit.git
cd MacDevKit/macdevkit-cli

# 2. 构建 Release 版本
cargo build --release

# 3. 运行构建的二进制文件
./target/release/macdevkit-cli

# 4. （可选）安装到系统路径
cargo install --path .
# 二进制文件将安装到 ~/.cargo/bin/macdevkit-cli
```

#### 方式二：使用 Makefile

项目包含 Makefile 以简化常见操作：

```bash
# 构建项目
make build

# 构建并安装到 ~/.local/bin
make install

# 运行项目（开发模式）
make run

# 运行测试
make test

# 清理构建产物
make clean
```

安装后，确保将安装目录添加到 PATH：

```bash
# 对于 make install（安装到 ~/.local/bin）
export PATH="$HOME/.local/bin:$PATH"

# 对于 cargo install（安装到 ~/.cargo/bin）
export PATH="$HOME/.cargo/bin:$PATH"

# 将上述行添加到 ~/.zshrc 或 ~/.bashrc 以持久化设置
```

### 开发构建

如果您正在开发或调试，可以使用开发模式构建：

```bash
# 开发构建（更快，但未优化）
cargo build

# 运行开发版本
cargo run

# 运行时传递参数
cargo run -- --help

# 启用日志输出进行调试
RUST_LOG=debug cargo run

# 运行测试
cargo test

# 运行测试并显示输出
cargo test -- --nocapture

# 检查代码风格
cargo clippy

# 格式化代码
cargo fmt
```

### 构建产物

- Release 二进制文件位于：`target/release/macdevkit-cli`
- Debug 二进制文件位于：`target/debug/macdevkit-cli`
- 大小对比：Release 版本经过优化，体积更小，运行速度更快

### 项目结构

```
macdevkit-cli/
├── Cargo.toml          # 项目配置和依赖
├── Cargo.lock          # 依赖锁定文件
├── Makefile            # 构建自动化
├── build.rs            # 构建脚本
├── init_wrapper.sh     # Shell 包装脚本
└── src/
    ├── main.rs         # 主程序入口
    └── script_handler.rs  # 脚本处理逻辑
```

### 依赖说明

项目使用以下主要依赖：

- **clap** (4.4) - 命令行参数解析
- **colored** (2.0) - 彩色终端输出
- **dialoguer** (0.11) - 交互式命令行界面
- **indicatif** (0.17) - 进度条和加载指示器
- **which** (5.0) - 查找系统可执行文件

### 常见问题

**Q: 构建失败，提示找不到 Rust 工具链**
```bash
# 安装或更新 Rust
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env
```

**Q: 链接错误或依赖问题**
```bash
# 清理并重新构建
cargo clean
cargo build --release
```

**Q: 如何交叉编译到其他平台？**
```bash
# 添加目标平台（例如：Intel Mac）
rustup target add x86_64-apple-darwin

# 为特定平台构建
cargo build --release --target x86_64-apple-darwin
```

**Q: 构建时间太长**
```bash
# 使用增量编译（默认启用）和并行构建
cargo build --release -j 4

# 或使用 sccache 缓存编译结果
cargo install sccache
export RUSTC_WRAPPER=sccache
cargo build --release
```

## 👥 贡献

欢迎贡献！如果您有改进建议或发现了问题，请：

1. Fork 这个仓库
2. 创建您的特性分支 (`git checkout -b feature/amazing-feature`)
3. 提交您的更改 (`git commit -m 'Add some amazing feature'`)
4. 推送到分支 (`git push origin feature/amazing-feature`)
5. 创建一个 Pull Request

## 📄 许可证

该项目采用 MIT 许可证 - 详情请参阅 [LICENSE](LICENSE) 文件。

---

<p align="center">
  <sub>Made with ❤️ by <a href="https://github.com/zyz199">zyz199</a></sub>
</p>
