# Installation - Linux

[< Back to Main README](../README.md)

## Prerequisites

- **Python 3**: Required for running the hook script
  - Verify: `python3 --version`
  - Install: `sudo apt install python3` (Ubuntu/Debian) or `sudo yum install python3` (RHEL/CentOS)
- **Audio Player**: `paplay` from `pulseaudio-utils`
  - Install: `sudo apt install pulseaudio-utils`

All details are mentioned in [HOOKS-README.md](../.codex/hooks/HOOKS-README.md)

---

## Installation

### Step 1: Copy hooks folder

Open terminal in your project directory and run the following commands:

```bash
mkdir -p .codex/hooks
git clone https://github.com/shanraisshan/codex-cli-hooks.git temp-hooks
cp -r temp-hooks/.codex/hooks/* .codex/hooks/
cp temp-hooks/install/hooks-linux.json .codex/hooks.json
rm -rf temp-hooks
```

