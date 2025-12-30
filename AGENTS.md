# GitHub Copilot Model Setup for oh-my-opencode

When the user opens this project, guide them through configuring oh-my-opencode to use GitHub Copilot models.

## Your Task

1. **Greet the user** and explain this wizard will configure oh-my-opencode agents to use GitHub Copilot models available through Copilot for Business.

2. **Read `setup-copilot-models.md`** to understand available models and agent roles.

3. **Ask the user to select a configuration preset OR custom selection:**
   - **Balanced (Recommended)**: Mix of Claude and GPT models
   - **GPT-Heavy**: All OpenAI models via Copilot
   - **Claude-Heavy**: Prefer Claude models where available
   - **Custom**: Select each agent individually

4. **If Custom, prompt for each agent** using AskUserQuestion with these options:
   - Sisyphus: claude-sonnet-4 (recommended), gpt-4o, o1
   - oracle: o1 (recommended), o1-mini, claude-sonnet-4
   - librarian: claude-sonnet-4 (recommended), gpt-4o
   - explore: gpt-4o-mini (recommended), gpt-4o
   - frontend-ui-ux-engineer: gpt-4o (recommended), claude-sonnet-4
   - document-writer: gpt-4o-mini (recommended), claude-sonnet-4
   - multimodal-looker: gpt-4o (recommended - has vision)

5. **Generate and write the config file** to `~/.config/opencode/oh-my-opencode.json`
   - Include `disabled_mcps` to disable all MCPs by default

6. **Confirm success** and explain how to verify (run opencode, trigger an agent)

## Preset Configurations

### Balanced (Recommended)
```json
{
  "disabled_mcps": ["websearch_exa", "context7", "grep_app"],
  "agents": {
    "Sisyphus": { "model": "github-copilot/claude-sonnet-4" },
    "oracle": { "model": "github-copilot/o1" },
    "librarian": { "model": "github-copilot/claude-sonnet-4" },
    "explore": { "model": "github-copilot/gpt-4o-mini" },
    "frontend-ui-ux-engineer": { "model": "github-copilot/gpt-4o" },
    "document-writer": { "model": "github-copilot/gpt-4o-mini" },
    "multimodal-looker": { "model": "github-copilot/gpt-4o" }
  }
}
```

### GPT-Heavy
```json
{
  "disabled_mcps": ["websearch_exa", "context7", "grep_app"],
  "agents": {
    "Sisyphus": { "model": "github-copilot/gpt-4o" },
    "oracle": { "model": "github-copilot/o1" },
    "librarian": { "model": "github-copilot/gpt-4o" },
    "explore": { "model": "github-copilot/gpt-4o-mini" },
    "frontend-ui-ux-engineer": { "model": "github-copilot/gpt-4o" },
    "document-writer": { "model": "github-copilot/gpt-4o-mini" },
    "multimodal-looker": { "model": "github-copilot/gpt-4o" }
  }
}
```

### Claude-Heavy
```json
{
  "disabled_mcps": ["websearch_exa", "context7", "grep_app"],
  "agents": {
    "Sisyphus": { "model": "github-copilot/claude-sonnet-4" },
    "oracle": { "model": "github-copilot/claude-sonnet-4" },
    "librarian": { "model": "github-copilot/claude-sonnet-4" },
    "explore": { "model": "github-copilot/gpt-4o-mini" },
    "frontend-ui-ux-engineer": { "model": "github-copilot/claude-sonnet-4" },
    "document-writer": { "model": "github-copilot/gpt-4o-mini" },
    "multimodal-looker": { "model": "github-copilot/gpt-4o" }
  }
}
```

## Notes

- All MCPs (websearch_exa, context7, grep_app) are disabled by default for work environments
- User can remove items from `disabled_mcps` array to re-enable specific MCPs if needed
