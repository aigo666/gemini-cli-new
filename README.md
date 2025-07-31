# Gemini CLI New

[![Gemini CLI CI](https://github.com/aigo666/gemini-cli-new/actions/workflows/ci.yml/badge.svg)](https://github.com/aigo666/gemini-cli-new/actions/workflows/ci.yml)

> 🔗 **Forked from Official Google Gemini CLI**: [https://github.com/google-gemini/gemini-cli](https://github.com/google-gemini/gemini-cli)
> 
> ⭐ **致敬原作者**: 本项目基于 Google 官方开源的 [Gemini CLI](https://github.com/google-gemini/gemini-cli) 进行二次开发
> 
> 📋 **声明**: 本项目为非官方增强版本，保持与上游项目的完全兼容性
## 🌐 Language / 语言选择

| Language | Link |
|----------|------|
| English | [English Version](#english-version) |
| 中文 | [中文版本](#中文版本) |

---

# English Version

> 🚀 **Enhanced Fork Version** 🚀
> 
> **🔗 Based on**: [Official Google Gemini CLI](https://github.com/google-gemini/gemini-cli) (Star ⭐ 65.9k)
> 
> This project is a **fork** of Google's official Gemini CLI with secondary development, **fully retaining all original features** while adding the following enhancements:
> 
> ✨ **New Features**:
> - 🌍 **Native Proxy API Support** - Custom API endpoints via `GEMINI_API_BASE_URL` environment variable
> - 🔀 **Enhanced Proxy Functionality** - Complete HTTP/HTTPS proxy support, including sandbox environment proxy
> - 📦 **Direct GitHub Installation** - Install directly from GitHub repository without npm publishing
> - 🛡️ **Network Security** - Complete proxy script examples and network filtering functionality
> - 🔧 **Flexible Configuration** - Support for various network environments and proxy configurations
> 
> 🎯 **Use Cases**: Especially suitable for users who need to access Gemini API through proxy or relay services

![Gemini CLI Screenshot](./docs/assets/gemini-screenshot.png)

This repository contains the Gemini CLI, a command-line AI workflow tool that connects to your
tools, understands your code and accelerates your workflows.

With the Gemini CLI you can:

- Query and edit large codebases in and beyond Gemini's 1M token context window.
- Generate new apps from PDFs or sketches, using Gemini's multimodal capabilities.
- Automate operational tasks, like querying pull requests or handling complex rebases.
- Use tools and MCP servers to connect new capabilities, including [media generation with Imagen,
  Veo or Lyria](https://github.com/GoogleCloudPlatform/vertex-ai-creative-studio/tree/main/experiments/mcp-genmedia)
- Ground your queries with the [Google Search](https://ai.google.dev/gemini-api/docs/grounding)
  tool, built into Gemini.

## Quickstart

You have two options to install Gemini CLI.

### With Node

1. **Prerequisites:** Ensure you have [Node.js version 20](https://nodejs.org/en/download) or higher installed.
2. **Run the CLI:** Execute the following command in your terminal:

   ```bash
   npx https://github.com/aigo666/gemini-cli-new
   ```

   Then, run the CLI from anywhere:

   ```bash
   gemini
   ```

### Common Configuration steps

3. **Pick a color theme**
4. **Authenticate:** When prompted, sign in with your personal Google account. This will grant you up to 60 model requests per minute and 1,000 model requests per day using Gemini.

You are now ready to use the Gemini CLI!

### 🔑 Configure Gemini API Key (with Proxy Support)

🌟 **This enhanced version supports proxy API access through custom endpoints**

💡 **Recommended Proxy Service**: [极速API](https://api.jisuai.top) - Reliable Gemini API proxy service sponsor

The Gemini API provides a free tier with [100 requests per day](https://ai.google.dev/gemini-api/docs/rate-limits#free-tier) using Gemini 2.5 Pro, control over which model you use, and access to higher rate limits (with a paid plan):

1. Generate a key from [Google AI Studio](https://aistudio.google.com/apikey).
2. Set it as an environment variable in your terminal. Replace `YOUR_API_KEY` with your generated key.

   **✨ Standard Configuration (Direct):**
   ```bash
   export GEMINI_API_KEY="YOUR_API_KEY"
   ```

   **🌍 Proxy API Configuration (Recommended):**
   ```bash
   export GEMINI_API_KEY="YOUR_API_KEY"
   export GEMINI_API_BASE_URL="https://your-proxy-server.com"
   # Example with 极速API: export GEMINI_API_BASE_URL="https://api.jisuai.top"
   # Other examples: export GEMINI_API_BASE_URL="https://api.example.com/v1"
   ```

   **🔀 Advanced Proxy Configuration:**
   ```bash
   export GEMINI_API_KEY="YOUR_API_KEY"
   export GEMINI_API_BASE_URL="https://api.jisuai.top"  # Using 极速API
   export HTTPS_PROXY="http://proxy.example.com:8080"
   export HTTP_PROXY="http://proxy.example.com:8080"
   ```

3. (Optionally) Upgrade your Gemini API project to a paid plan on the API key page (will automatically unlock [Tier 1 rate limits](https://ai.google.dev/gemini-api/docs/rate-limits#tier-1))

## Examples

Once the CLI is running, you can start interacting with Gemini from your shell.

You can start a project from a new directory:

```sh
cd new-project/
gemini
> Write me a Gemini Discord bot that answers questions using a FAQ.md file I will provide
```

Or work with an existing project:

```sh
git clone https://github.com/aigo666/gemini-cli-new
cd gemini-cli-new
gemini
> Give me a summary of all of the changes that went in yesterday
```

### Next steps

- Learn how to [contribute to or build from the source](./CONTRIBUTING.md).
- Explore the available **[CLI Commands](./docs/cli/commands.md)**.
- If you encounter any issues, review the **[troubleshooting guide](./docs/troubleshooting.md)**.
- For more comprehensive documentation, see the [full documentation](./docs/index.md).
- Take a look at some [popular tasks](#popular-tasks) for more inspiration.
- Check out our **[Official Roadmap](./ROADMAP.md)**

### Troubleshooting

Head over to the [troubleshooting guide](docs/troubleshooting.md) if you're
having issues.

## Popular tasks

### Explore a new codebase

Start by `cd`ing into an existing or newly-cloned repository and running `gemini`.

```text
> Describe the main pieces of this system's architecture.
```

```text
> What security mechanisms are in place?
```

```text
> Provide a step-by-step dev onboarding doc for developers new to the codebase.
```

```text
> Summarize this codebase and highlight the most interesting patterns or techniques I could learn from.
```

```text
> Identify potential areas for improvement or refactoring in this codebase, highlighting parts that appear fragile, complex, or hard to maintain.
```

```text
> Which parts of this codebase might be challenging to scale or debug?
```

```text
> Generate a README section for the [module name] module explaining what it does and how to use it.
```

```text
> What kind of error handling and logging strategies does the project use?
```

```text
> Which tools, libraries, and dependencies are used in this project?
```

### Work with your existing code

```text
> Implement a first draft for GitHub issue #123.
```

```text
> Help me migrate this codebase to the latest version of Java. Start with a plan.
```

### Automate your workflows

Use MCP servers to integrate your local system tools with your enterprise collaboration suite.

```text
> Make me a slide deck showing the git history from the last 7 days, grouped by feature and team member.
```

```text
> Make a full-screen web app for a wall display to show our most interacted-with GitHub issues.
```

### Interact with your system

```text
> Convert all the images in this directory to png, and rename them to use dates from the exif data.
```

```text
> Organize my PDF invoices by month of expenditure.
```

### Uninstall

Head over to the [Uninstall](docs/Uninstall.md) guide for uninstallation instructions.

## 🔧 Enhanced Version Features

### Proxy API Configuration Details

The core feature of this enhanced version is proxy API support, implemented through:

1. **`GEMINI_API_BASE_URL` Environment Variable**: Set custom API endpoints (recommended: [极速API](https://api.jisuai.top))
2. **Proxy Support**: Support for HTTP/HTTPS proxy servers
3. **Sandbox Proxy**: Custom sandbox network proxy via `GEMINI_SANDBOX_PROXY_COMMAND`
4. **Network Filtering**: Domain whitelist and security filtering features

### Configuration Examples

For detailed proxy configuration examples, refer to:
- [Proxy Script Examples](./docs/examples/proxy-script.md)
- [CLI Configuration Documentation](./docs/cli/configuration.md)
- [Authentication Configuration](./docs/cli/authentication.md)

### Technical Support

- 🐛 **Issue Reports**: [Submit Issue](https://github.com/aigo666/gemini-cli-new/issues)
- 📚 **Complete Documentation**: [View Docs](./docs/index.md)
- 🚀 **Contribute Code**: [Contribution Guide](./CONTRIBUTING.md)

### Compatibility with Official Version

✅ **Fully Compatible**: This version is fully compatible with the official Gemini CLI, all original features work normally
✅ **Configuration Migration**: Existing configuration files and settings can be used without modification
✅ **Command Line Interface**: All command line arguments and interaction methods remain consistent

## Terms of Service and Privacy Notice

For details on the terms of service and privacy notice applicable to your use of Gemini CLI, see the [Terms of Service and Privacy Notice](./docs/tos-privacy.md).

---

# 中文版本

> 🚀 **二开增强版本** 🚀
> 
> **🔗 基于项目**: [Google 官方 Gemini CLI](https://github.com/google-gemini/gemini-cli) (⭐ 65.9k Stars)
> 
> 本项目是 Google 官方 Gemini CLI 的 **Fork 版本**，进行二次开发，**完全保留原版所有功能**的同时，新增以下特性：
> 
> ✨ **新增特性**：
> - 🌍 **原生中转API支持** - 通过 `GEMINI_API_BASE_URL` 环境变量支持自定义API端点
> - 🔀 **增强代理功能** - 完整的HTTP/HTTPS代理支持，包括沙盒环境代理
> - 📦 **GitHub直装** - 支持直接从GitHub仓库安装，无需发布到npm
> - 🛡️ **网络安全** - 提供完整的代理脚本示例和网络过滤功能
> - 🔧 **灵活配置** - 支持多种网络环境和代理配置方案
> 
> 🎯 **适用场景**：特别适合需要通过代理或中转服务访问Gemini API的用户

![Gemini CLI Screenshot](./docs/assets/gemini-screenshot.png)

本仓库包含 Gemini CLI，这是一个命令行AI工作流工具，能够连接到您的工具，理解您的代码并加速您的工作流程。

使用 Gemini CLI，您可以：

- 在 Gemini 的 1M token 上下文窗口内外查询和编辑大型代码库
- 使用 Gemini 的多模态功能从 PDF 或草图生成新应用
- 自动化操作任务，如查询拉取请求或处理复杂的变基操作
- 使用工具和 MCP 服务器连接新功能，包括[使用 Imagen、Veo 或 Lyria 进行媒体生成](https://github.com/GoogleCloudPlatform/vertex-ai-creative-studio/tree/main/experiments/mcp-genmedia)
- 使用内置于 Gemini 的 [Google 搜索](https://ai.google.dev/gemini-api/docs/grounding)工具来完善您的查询

## 快速开始

您有两种安装 Gemini CLI 的选择。

### 使用 Node

1. **前提条件：** 确保您已安装 [Node.js 版本 20](https://nodejs.org/en/download) 或更高版本。
2. **运行 CLI：** 在终端中执行以下命令：

   ```bash
   npx https://github.com/aigo666/gemini-cli-new
   ```

   然后，您可以从任何地方运行 CLI：

   ```bash
   gemini
   ```

### 通用配置步骤

3. **选择颜色主题**
4. **身份验证：** 出现提示时，使用您的个人 Google 账户登录。这将为您提供每分钟最多 60 个模型请求和每天 1,000 个模型请求的使用量。

现在您已准备好使用 Gemini CLI！

### 🔑 配置 Gemini API 密钥（支持中转API）

🌟 **本增强版本支持通过自定义端点进行中转API访问**

💡 **推荐中转服务商**: [极速API](https://api.jisuai.top) - 可靠的Gemini API中转服务赞助商

Gemini API 提供免费套餐，使用 Gemini 2.5 Pro 可享受[每天 100 个请求](https://ai.google.dev/gemini-api/docs/rate-limits#free-tier)，控制使用的模型，并可访问更高的速率限制（通过付费计划）：

1. 从 [Google AI Studio](https://aistudio.google.com/apikey) 生成密钥。
2. 在终端中将其设置为环境变量。将 `YOUR_API_KEY` 替换为您生成的密钥。

   **✨ 标准配置（直连）：**
   ```bash
   export GEMINI_API_KEY="YOUR_API_KEY"
   ```

   **🌍 中转API配置（推荐）：**
   ```bash
   export GEMINI_API_KEY="YOUR_API_KEY"
   export GEMINI_API_BASE_URL="https://your-proxy-server.com"
   # 推荐使用极速API：export GEMINI_API_BASE_URL="https://api.jisuai.top"
   # 其他示例：export GEMINI_API_BASE_URL="https://api.example.com/v1"
   ```

   **🔀 高级代理配置：**
   ```bash
   export GEMINI_API_KEY="YOUR_API_KEY"
   export GEMINI_API_BASE_URL="https://api.jisuai.top"  # 使用极速API
   export HTTPS_PROXY="http://proxy.example.com:8080"
   export HTTP_PROXY="http://proxy.example.com:8080"
   ```

3. （可选）在 API 密钥页面将您的 Gemini API 项目升级到付费计划（将自动解锁[第1层速率限制](https://ai.google.dev/gemini-api/docs/rate-limits#tier-1)）

## 示例

CLI 运行后，您可以开始从shell与 Gemini 交互。

您可以从新目录开始项目：

```sh
cd new-project/
gemini
> 为我编写一个 Gemini Discord 机器人，使用我将提供的 FAQ.md 文件回答问题
```

或者与现有项目一起工作：

```sh
git clone https://github.com/aigo666/gemini-cli-new
cd gemini-cli-new
gemini
> 给我一个昨天所有更改的摘要
```

### 下一步

- 了解如何[贡献或从源代码构建](./CONTRIBUTING.md)。
- 探索可用的 **[CLI 命令](./docs/cli/commands.md)**。
- 如果遇到任何问题，请查看 **[故障排除指南](./docs/troubleshooting.md)**。
- 要获取更全面的文档，请参阅[完整文档](./docs/index.md)。
- 查看一些[热门任务](#热门任务)以获得更多灵感。
- 查看我们的 **[官方路线图](./ROADMAP.md)**

### 故障排除

如果您遇到问题，请前往[故障排除指南](docs/troubleshooting.md)。

## 热门任务

### 探索新代码库

首先 `cd` 到现有或新克隆的仓库，然后运行 `gemini`。

```text
> 描述此系统架构的主要组成部分。
```

```text
> 有哪些安全机制？
```

```text
> 为新加入此代码库的开发者提供逐步的开发入门文档。
```

```text
> 总结此代码库并突出显示我可以学到的最有趣的模式或技术。
```

```text
> 识别此代码库中潜在的改进或重构领域，突出显示看起来脆弱、复杂或难以维护的部分。
```

```text
> 此代码库的哪些部分可能在扩展或调试时具有挑战性？
```

```text
> 为 [模块名称] 模块生成 README 部分，解释它的作用和使用方法。
```

```text
> 项目使用什么样的错误处理和日志记录策略？
```

```text
> 此项目中使用了哪些工具、库和依赖项？
```

### 处理现有代码

```text
> 为 GitHub issue #123 实现初稿。
```

```text
> 帮我将此代码库迁移到最新版本的 Java。先制定计划。
```

### 自动化工作流程

使用 MCP 服务器将您的本地系统工具与企业协作套件集成。

```text
> 为我制作一个幻灯片演示，显示过去7天的git历史，按功能和团队成员分组。
```

```text
> 制作一个全屏网络应用用于墙面显示，显示我们交互最多的 GitHub issues。
```

### 与系统交互

```text
> 将此目录中的所有图像转换为 png，并使用 exif 数据中的日期重命名它们。
```

```text
> 按支出月份整理我的PDF发票。
```

### 卸载

前往[卸载](docs/Uninstall.md)指南获取卸载说明。

## 🔧 二开版本特性说明

### 中转API配置详解

本增强版本的核心特性是支持中转API，通过以下方式实现：

1. **`GEMINI_API_BASE_URL` 环境变量**：设置自定义API端点（推荐：[极速API](https://api.jisuai.top)）
2. **代理支持**：支持HTTP/HTTPS代理服务器
3. **沙盒代理**：通过 `GEMINI_SANDBOX_PROXY_COMMAND` 自定义沙盒网络代理
4. **网络过滤**：提供域名白名单和安全过滤功能

### 配置示例

详细的代理配置示例请参考：
- [代理脚本示例](./docs/examples/proxy-script.md)
- [CLI配置文档](./docs/cli/configuration.md)
- [认证配置](./docs/cli/authentication.md)

### 技术支持

- 🐛 **问题反馈**：[提交Issue](https://github.com/aigo666/gemini-cli-new/issues)
- 📚 **完整文档**：[查看文档](./docs/index.md)
- 🚀 **贡献代码**：[贡献指南](./CONTRIBUTING.md)

### 与官方版本的兼容性

✅ **完全兼容**：本版本与官方Gemini CLI完全兼容，所有原有功能均可正常使用
✅ **配置迁移**：现有的配置文件和设置无需修改即可使用
✅ **命令行接口**：所有命令行参数和交互方式保持一致

## 服务条款和隐私声明

有关适用于您使用 Gemini CLI 的服务条款和隐私声明的详细信息，请参阅[服务条款和隐私声明](./docs/tos-privacy.md)。

---

## 🙏 致谢与声明 / Acknowledgments

### 原项目致谢 / Original Project Credits

本项目基于 Google 官方开源的 [Gemini CLI](https://github.com/google-gemini/gemini-cli) 进行二次开发：

**Original Project**: [https://github.com/google-gemini/gemini-cli](https://github.com/google-gemini/gemini-cli)  
**License**: Apache-2.0  
**Authors**: Google & Contributors  

### 项目关系说明 / Project Relationship

- ✅ **完全开源**: 遵循原项目 Apache-2.0 开源协议
- ✅ **非官方版本**: 本项目为社区维护的增强版本，非 Google 官方发布
- ✅ **上游兼容**: 保持与官方版本的完全兼容性，可随时迁移回官方版本
- ✅ **功能增强**: 在原有功能基础上新增中转API、代理支持等特性

### 贡献 / Contributing

欢迎向本项目贡献代码，同时也鼓励向[官方项目](https://github.com/google-gemini/gemini-cli)贡献！

---

**⚡ 快速链接 / Quick Links**  
- 🏠 [官方项目](https://github.com/google-gemini/gemini-cli) | [本增强版](https://github.com/aigo666/gemini-cli-new)
- 📖 [官方文档](https://github.com/google-gemini/gemini-cli/tree/main/docs) | [增强版文档](./docs/index.md)
- 🐛 [官方Issues](https://github.com/google-gemini/gemini-cli/issues) | [增强版Issues](https://github.com/aigo666/gemini-cli-new/issues)
