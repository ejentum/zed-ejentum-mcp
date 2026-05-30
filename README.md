# Ejentum context server for Zed

A [Zed](https://zed.dev) extension that exposes the [Ejentum Reasoning Harness](https://github.com/ejentum/ejentum-mcp) as an MCP context server. Ejentum is a library of 679 cognitive operations engineered in natural language, organized across four harnesses. Each harness call retrieves a task-matched scaffold rather than serving a fixed template: a named failure pattern, an executable procedure, suppression vectors that block the obvious shortcut, and a falsification test for self-verification. The assistant ingests the scaffold and writes from it, addressing attention decay, sycophantic collapse, hallucination drift, and reasoning decay.

Four tools are exposed:

- `reasoning` for analytical, diagnostic, planning, multi-step questions
- `code` for codegen, refactor, review, debugging, architecture choices
- `anti-deception` when the prompt pressures the assistant to validate, certify, or soften an honest assessment
- `memory` for sharpening an observation already formed about cross-turn drift

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

Free tier (30-day trial, no card) at [ejentum.com/pricing](https://ejentum.com/pricing).

## Hosted alternative

This extension bundles the `ejentum-mcp` npm package and runs it as a stdio subprocess inside Zed. If you'd rather avoid the local subprocess (no npx install, no Node version pinning), the same four harness tools are also hosted at `https://api.ejentum.com/mcp` with Bearer auth via your `EJENTUM_API_KEY`. Most Zed users will prefer this extension (tighter integration, no extra MCP-client configuration needed); the hosted endpoint is documented here for users who want to route through Zed's HTTP-capable MCP support, or who run Zed alongside other clients (n8n, custom HTTP-MCP agents) sharing one key.

## License

MIT.
