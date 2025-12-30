# omo-copilot-setup

Interactive configuration wizard for [oh-my-opencode](https://github.com/code-yeongyu/oh-my-opencode) using GitHub Copilot models.

## Usage

```bash
git clone https://github.com/kennyg/omo-copilot-setup
cd omo-copilot-setup
opencode
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

## Available Models

- `github-copilot/claude-sonnet-4` - Complex reasoning, coding
- `github-copilot/gpt-4o` - Multimodal, vision
- `github-copilot/gpt-4o-mini` - Fast, efficient
- `github-copilot/o1` - Deep reasoning
- `github-copilot/o1-mini` - Fast reasoning

## Notes

- All MCPs are disabled by default (suitable for work environments)
- Requires GitHub Copilot for Business license
- See `setup-copilot-models.md` for detailed model and agent descriptions
