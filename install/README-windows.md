# Installation - Windows

[< Back to Main README](../README.md)

## Prerequisites

- **Python 3**: Required for running the hook script
  - Verify: `python --version`
  - Install: Download from [python.org](https://www.python.org/downloads/) or install via `winget install Python.Python.3`
- **Audio Player**: Built-in `winsound` module (included with Python)

All details are mentioned in [HOOKS-README.md](../.codex/hooks/HOOKS-README.md)

---

## Installation

### Step 1: Copy hooks folder

Open terminal in your project directory and run the following commands:

**PowerShell:**
```powershell
New-Item -ItemType Directory -Force -Path .codex\hooks
git clone https://github.com/shanraisshan/codex-cli-voice-hooks.git temp-hooks
Copy-Item -Recurse -Force temp-hooks\.codex\hooks\* .codex\hooks\
Remove-Item -Recurse -Force temp-hooks
```

**Command Prompt:**
```cmd
if not exist .codex\hooks mkdir .codex\hooks
git clone https://github.com/shanraisshan/codex-cli-voice-hooks.git temp-hooks
xcopy /E /I /Y temp-hooks\.codex\hooks\* .codex\hooks\
rmdir /S /Q temp-hooks
```

### Step 2: Copy config.toml into your project

1. If you don't have a `.codex/config.toml` file in your project, create one: `New-Item -Force .codex/config.toml`
2. Open [`install/config-windows.toml`](config-windows.toml) and copy the `notify` line into your `.codex/config.toml`

### Step 3: Copy hooks.json for SessionStart and Stop hooks (v0.114.0+)

1. Copy [`install/hooks-windows.json`](hooks-windows.json) to `.codex/hooks.json` in your project
2. Run Codex with the hooks feature flag: `codex -c features.codex_hooks=true`

> **Why separate config files per platform?**
> - Python command: `python3` (macOS/Linux) vs `python` (Windows)
