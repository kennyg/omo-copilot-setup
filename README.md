# omo-copilot-setup

Interactive configuration wizard for [oh-my-opencode](https://github.com/code-yeongyu/oh-my-opencode) using GitHub Copilot models.

## Prerequisites

Install oh-my-opencode first:

```bash
bunx oh-my-opencode install
```

Or for non-interactive setup (useful for CI/scripts):

```bash
bunx oh-my-opencode install --no-tui --claude=no --chatgpt=no --gemini=no
```

Verify installation:

```bash
opencode --version  # Should be 1.0.150 or higher
```

## Usage

**Option 1: Paste into opencode**

Paste this into a fresh opencode session:
```
Configure GitHub Copilot models by following the instructions here https://raw.githubusercontent.com/kennyg/omo-copilot-setup/main/AGENTS.md
```

**Option 2: Clone and run locally**

```bash
git clone https://github.com/kennyg/omo-copilot-setup
cd omo-copilot-setup
opencode
# then type "set up my config"
```

OpenCode will read `AGENTS.md` and guide you through:

1. Selecting a configuration preset (Balanced, GPT-Heavy, Claude-Heavy) or custom
2. Writing config to `~/.config/opencode/oh-my-opencode.json`

## Presets

| Preset | Description |
|--------|-------------|
| **Balanced** | Mix of Claude and GPT models (recommended) |
| **GPT-Heavy** | All OpenAI models via GitHub Copilot |
| **Claude-Heavy** | Prefer Claude models where available |
| **Custom** | Select each agent individually |

## Available Models (from models.dev)

- `github-copilot/claude-3.7-sonnet` - Latest Claude, excellent coding
- `github-copilot/claude-sonnet-4` - Claude 4 Sonnet
- `github-copilot/gpt-4o` - Multimodal, vision
- `github-copilot/o3-mini` - Fast reasoning
- `github-copilot/o3` - Deep reasoning
- `github-copilot/gemini-2.5-pro` - Long context

## Notes

- All MCPs are disabled by default (suitable for work environments)
- Requires GitHub Copilot for Business license
- See `setup-copilot-models.md` for detailed model and agent descriptions
