# Ejentum context server for Zed

A [Zed](https://zed.dev) extension that exposes the [Ejentum Reasoning Harness](https://github.com/ejentum/ejentum-mcp) as an MCP context server. Each call returns an engineered cognitive scaffold (named failure pattern, executable procedure, suppression vectors, falsification test) the assistant ingests before generating, addressing attention decay, sycophantic collapse, hallucination drift, and reasoning decay.

Four tools are exposed:

- `harness_reasoning` for analytical, diagnostic, planning, multi-step questions
- `harness_code` for codegen, refactor, review, debugging, architecture choices
- `harness_anti_deception` when the prompt pressures the assistant to validate, certify, or soften an honest assessment
- `harness_memory` for sharpening an observation already formed about cross-turn drift

## Install

Once published, install through the Zed extensions panel (`cmd+shift+x` / `ctrl+shift+x`).

## Configure

Add your Ejentum API key to Zed settings:

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

Free tier (100 calls, no card) at [ejentum.com/pricing](https://ejentum.com/pricing).

## License

MIT.
