# ⚡ HELIX CLI

<p align="center">
  <strong>A blazing fast, autonomous AI coding assistant and agent harness built in Rust.</strong><br>
  <em>Created by Vinay</em>
</p>

---

**HELIX CLI** is an advanced, production-ready AI agent framework designed to seamlessly integrate into your development workflow. Built natively in Rust, it delivers unparalleled speed, safety, and deep system-level integration. 

HELIX is specifically optimized for Windows environments and engineered to operate autonomously with local Large Language Models (LLMs), ensuring ultimate privacy, zero API costs, and uncensored agentic capabilities.

## ✨ Core Features

*   **🤖 Autonomous Agentic Workflow:** Powered by a production-hardened system prompt, HELIX operates as a deterministic, highly capable task-executing agent. It analyzes, plans, and executes code generation, file manipulation, and system commands with extreme precision.
*   **💻 Windows Native & WSL Resilient:** Custom-engineered execution harnesses provide bulletproof `cmd.exe` command execution on Windows, completely bypassing broken or misconfigured WSL wrappers that crash standard Unix-ported CLIs.
*   **🧠 Local LLM First:** Fully configured to leverage local models like `gemma4:e4b` via OpenAI-compatible endpoints (e.g., Ollama), allowing for massive context windows without the overhead of expensive cloud provider APIs.
*   **🛡️ Dynamic Tooling & Permissions:** Features a robust internal toolchain (file reading/writing, regex searching, shell execution) guarded by configurable permission modes ranging from `read-only` to `danger-full-access`.
*   **🦀 Rust Foundation:** Memory-safe, incredibly fast, and compiled natively.

## 🚀 Quick Start

### Prerequisites
1. **Rust Toolchain:** Install from [rustup.rs](https://rustup.rs/).
2. **Local Model Provider:** Ensure your local OpenAI-compatible endpoint (like Ollama) is running and configured for your desired model.

### 1. Clone & Build
```bash
git clone https://github.com/V1N4Y007/claw-code.git
cd claw-code/rust
cargo build --release
```

### 2. Run the REPL
Launch the interactive HELIX REPL:
```powershell
# Windows (PowerShell)
.\target\release\claw.exe
```

## 📖 Usage

### Interactive Mode
Starting the CLI drops you into an interactive session where you can chat, pair-program, and assign complex, multi-step tasks to the agent.
```text
> push the changes to github
✔ ✨ Done
```

### One-Shot Prompts
Execute single tasks directly from your terminal without entering the REPL:
```powershell
.\target\release\claw.exe prompt "Refactor the authentication flow in src/auth.rs"
```

### Useful Commands (In-REPL)
*   `/help` - View all available slash commands.
*   `/status` - View current context, active model, workspace state, and token usage.
*   `/diff` - Show git diff of current changes.
*   `/commit` - Package current changes into a git commit.
*   `/resume latest` - Jump back into your most recent session context.

## ⚙️ Configuration

HELIX discovers context and instructions dynamically:
*   **System Instructions:** Project-specific agent behavior is defined in `CLAUDE.md` and `.claw/instructions.md`.
*   **Permission Modes:** Control agent autonomy via the `--permission-mode` flag. For fully autonomous local development, `danger-full-access` allows the agent to execute shell commands and modify files without constant prompting.

---
*Built for the future of agentic development.*
