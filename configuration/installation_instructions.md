# Ejentum context server

[Ejentum](https://ejentum.com) is a Reasoning Harness for agentic AI: a library of 679 cognitive operations engineered in natural language, organized across four harnesses (`harness_reasoning`, `harness_code`, `harness_anti_deception`, `harness_memory`). Each harness call retrieves a task-matched scaffold rather than serving a fixed template: a failure pattern, an executable procedure, suppression vectors that block the obvious shortcut, and a falsification test for self-verification. The model ingests the scaffold and writes from it.

## Setup

1. Get a free Ejentum API key at [ejentum.com/pricing](https://ejentum.com/pricing). Free tier: 100 calls, no card required.
2. Open Zed settings (`cmd+,` / `ctrl+,`) and add:

```jsonc
{
  "context_servers": {
    "ejentum-mcp": {
      "settings": {
        "ejentum_api_key": "YOUR_KEY_HERE"
      }
    }
  }
}
```

The four harness tools become available in the assistant's tool palette.

## Source

- MCP server: <https://github.com/ejentum/ejentum-mcp> (MIT)
- Documentation: <https://ejentum.com/docs/claude_code_guide>
- "Under Pressure" research paper: <https://doi.org/10.5281/zenodo.19392715>
