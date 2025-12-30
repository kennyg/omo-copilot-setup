# GitHub Copilot Models for oh-my-opencode

> Reference documentation for AGENTS.md setup wizard

## Available Models (from models.dev)

| Model | Provider | Capabilities | Best For |
|-------|----------|--------------|----------|
| `github-copilot/claude-3.5-sonnet` | Anthropic | Excellent reasoning, coding | Complex tasks, orchestration |
| `github-copilot/claude-3.7-sonnet` | Anthropic | Latest Claude | General purpose |
| `github-copilot/claude-sonnet-4` | Anthropic | Claude 4 Sonnet | Advanced coding |
| `github-copilot/gpt-4o` | OpenAI | Multimodal, vision | UI work, image analysis |
| `github-copilot/gpt-4.1` | OpenAI | Latest GPT | General purpose |
| `github-copilot/o3-mini` | OpenAI | Fast reasoning | Quick analysis |
| `github-copilot/o3` | OpenAI | Deep reasoning | Strategic decisions, planning |
| `github-copilot/o4-mini` | OpenAI | Faster reasoning | Quick tasks |
| `github-copilot/gemini-2.5-pro` | Google | Long context | Large codebases |

## Agent Descriptions

### Sisyphus (Primary Orchestrator)
The main agent that coordinates work, delegates to other agents, and handles complex multi-step tasks.
- **Recommended**: `claude-3.7-sonnet` or `gpt-4o`
- Needs strong reasoning and task planning

### oracle (Strategic Advisor)
Provides architectural guidance, code review, and strategic decisions.
- **Recommended**: `o3-mini` (reasoning model)
- Benefits from deep thinking capabilities

### librarian (Multi-Repo Analysis)
Searches across repositories, finds documentation, and retrieves OSS examples.
- **Recommended**: `claude-3.7-sonnet`
- Needs good comprehension and synthesis

### explore (Fast Exploration)
Quickly navigates codebases, finds files, and answers structural questions.
- **Recommended**: `gpt-4o`
- Speed is more important than depth

### frontend-ui-ux-engineer (UI/UX Generation)
Creates and modifies frontend code, handles styling and visual components.
- **Recommended**: `gpt-4o` (multimodal)
- Benefits from vision capabilities

### document-writer (Documentation)
Generates technical documentation, READMEs, and explanations.
- **Recommended**: `gpt-4o`
- Fast generation, good quality

### multimodal-looker (Vision/PDF Analysis)
Analyzes images, PDFs, diagrams, and visual content.
- **Recommended**: `gpt-4o` (required for vision)
- Must have multimodal capabilities

## Model Selection Tips

- **For speed**: Use `gpt-4o` or `o4-mini`
- **For reasoning**: Use `o3` or `o3-mini` - thinking models
- **For coding**: Use `claude-3.7-sonnet` - excellent code generation
- **For vision**: Use `gpt-4o` - required for image/PDF analysis

## Example Configurations

### Balanced (Recommended)
Best mix of capabilities across different model strengths.

### GPT-Heavy
Use when you prefer OpenAI models or have better experience with them.

### Claude-Heavy
Use when you prefer Claude's coding style and reasoning approach.

### Custom
Select each agent individually based on your specific needs.
