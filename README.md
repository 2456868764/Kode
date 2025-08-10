# Kode With Agent

You can see this as open-cc for everyone, agent-system design is in [./system-design.md](./system-design.md)

## Features

- 🛠️ **Code Analysis & Fixes** - Analyzes and improves your codebase
- 📖 **Code Explanation** - Explains complex functions and logic
- 🧪 **Test Execution** - Runs tests and shell commands
- 🔧 **Workflow Automation** - Handles entire development workflows
- 🤖 **Multi-Model Support** - Works with any OpenAI-compatible API
- 🎯 **Many Built-in Tools** - File operations, shell execution, notebooks, and more
- 💾 **Smart Checkpoints** - Intelligent project state management and recovery
- 🌿 **Worktree Workflows** - Isolated development environments for features

## Installation

```bash
# not relased, i am on the plane with very poor network, if the plane can not land, anyone see this help me make this agent-system more strong.
```

## Quick Start

1. **Model Setup**: Use the onboarding flow or `/model` command to configure your AI provider
2. **Custom Models**: If your model isn't listed, manually configure it via `/config`
3. **OpenAI-Compatible**: Works with any OpenAI-style endpoint (Ollama, OpenRouter, etc.)

## MCP Server Integration

Use Agent Kode as a Model Context Protocol server with Claude Desktop:

1. Find the full path: `which kode`
2. Add to Claude Desktop config:
```json
{
  "mcpServers": {
    "agent-kode": {
      "command": "/path/to/kode",
      "args": ["mcp", "serve"]
    }
  }
}
```

## Development

```bash
# Install dependencies
pnpm install

# Run in development mode
pnpm run dev

# Build for production
pnpm run build

# Debug with verbose logging
NODE_ENV=development pnpm run dev --verbose --debug
```

## Architecture

- **React/Ink** - Terminal UI framework
- **18 Core Tools** - File operations, shell execution, AI workflows, checkpoints
- **Multi-Provider** - Anthropic Claude, OpenAI, custom endpoints
- **TypeScript** - Full type safety throughout
- **MCP Compatible** - Model Context Protocol integration
- **Smart Workflows** - Checkpoint system and worktree management

## Advanced Workflows

Agent Kode provides sophisticated development workflow management:

### 🎯 Checkpoint System
Intelligent project state management with automatic analysis and recovery:
- **`/checkpoint-save`** - Smart analysis and state preservation
- **`/checkpoint-restore`** - Natural language version recovery

### 🌿 Worktree Development
Isolated development environments for feature work:
- **`/worktree-create`** - Task-driven environment creation
- **`/worktree-review`** - Comprehensive code quality assessment
- **`/worktree-merge`** - Safe integration with quality gates

📚 **[Complete Workflow Documentation](docs/commands/README.md)**

## Bug Reports

Submit bugs directly from the app using `/bug` - it will open GitHub with pre-filled information.

## Privacy & Data

- **No telemetry** - No backend servers except your chosen AI providers
- **Local processing** - All data stays on your machine
- **Open source** - Full transparency in code and data handling

## Repository

- **Homepage**: [https://github.com/shareAI-lab/agent-kode](https://github.com/shareAI-lab/agent-kode)
- **Issues**: [https://github.com/shareAI-lab/agent-kode/issues](https://github.com/shareAI-lab/agent-kode/issues)

## License

See [LICENSE.md](LICENSE.md) for details.

---

**⚠️ Use at your own risk** - This tool executes code and commands on your system.

## Thanks
- some code from @dnakov 's anonkode
- some ui learn from gemini-cli
- some system design learn from claude code