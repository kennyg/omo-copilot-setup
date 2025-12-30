# GitHub Copilot Models for oh-my-opencode

> Reference documentation for AGENTS.md setup wizard

## Available Models

| Model | Provider | Capabilities | Best For |
|-------|----------|--------------|----------|
| `github-copilot/claude-sonnet-4` | Anthropic | Excellent reasoning, coding | Complex tasks, orchestration |
| `github-copilot/claude-3.5-sonnet` | Anthropic | Good balance | General purpose |
| `github-copilot/gpt-4o` | OpenAI | Multimodal, vision | UI work, image analysis |
| `github-copilot/gpt-4o-mini` | OpenAI | Fast, efficient | Quick tasks, exploration |
| `github-copilot/o1` | OpenAI | Deep reasoning | Strategic decisions, planning |
| `github-copilot/o1-mini` | OpenAI | Fast reasoning | Quick analysis |
| `github-copilot/o1-preview` | OpenAI | Preview features | Experimental |

## Agent Descriptions

### Sisyphus (Primary Orchestrator)
The main agent that coordinates work, delegates to other agents, and handles complex multi-step tasks.
- **Recommended**: `claude-sonnet-4` or `gpt-4o`
- Needs strong reasoning and task planning

### oracle (Strategic Advisor)
Provides architectural guidance, code review, and strategic decisions.
- **Recommended**: `o1` (reasoning model)
- Benefits from deep thinking capabilities

### librarian (Multi-Repo Analysis)
Searches across repositories, finds documentation, and retrieves OSS examples.
- **Recommended**: `claude-sonnet-4`
- Needs good comprehension and synthesis

### explore (Fast Exploration)
Quickly navigates codebases, finds files, and answers structural questions.
- **Recommended**: `gpt-4o-mini`
- Speed is more important than depth

### frontend-ui-ux-engineer (UI/UX Generation)
Creates and modifies frontend code, handles styling and visual components.
- **Recommended**: `gpt-4o` (multimodal)
- Benefits from vision capabilities

### document-writer (Documentation)
Generates technical documentation, READMEs, and explanations.
- **Recommended**: `gpt-4o-mini`
- Fast generation, good quality

### multimodal-looker (Vision/PDF Analysis)
Analyzes images, PDFs, diagrams, and visual content.
- **Recommended**: `gpt-4o` (required for vision)
- Must have multimodal capabilities

## Model Selection Tips

- **For speed**: Use `gpt-4o-mini` - fastest response times
- **For reasoning**: Use `o1` or `o1-mini` - thinking models
- **For coding**: Use `claude-sonnet-4` - excellent code generation
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
