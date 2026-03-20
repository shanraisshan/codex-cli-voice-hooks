# Installation - macOS

[< Back to Main README](../README.md)

## Prerequisites

- **Python 3**: Required for running the hook script
  - Verify: `python3 --version`
  - Install: `brew install python3` (requires [Homebrew](https://brew.sh/))
- **Audio Player**: `afplay` (built-in, no installation needed)

All details are mentioned in [HOOKS-README.md](../.codex/hooks/HOOKS-README.md)

---

## Installation

### Step 1: Copy hooks folder

Open terminal in your project directory and run the following commands:

```bash
mkdir -p .codex/hooks
git clone https://github.com/shanraisshan/codex-cli-hooks.git temp-hooks
cp -r temp-hooks/.codex/hooks/* .codex/hooks/
cp temp-hooks/install/hooks-mac.json .codex/hooks.json
rm -rf temp-hooks
```

