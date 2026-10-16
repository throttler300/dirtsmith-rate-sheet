# Dirtsmith outside-tools rate sheet

Free, no-login MCP tool marketplace: compare agent tool prices and route a task to the cheapest reachable tool.

**Entity:** Dirtsmith LLC (Iowa)  
**Live endpoint:** https://dirtsmith-go.bfurrow26.workers.dev/mcp  
**Homepage / docs:** https://dirtsmith-go.bfurrow26.workers.dev/developers  
**Install:** https://dirtsmith-go.bfurrow26.workers.dev/install  
**Machine-readable rates:** https://dirtsmith-go.bfurrow26.workers.dev/rates.json  
**llms.txt:** https://dirtsmith-go.bfurrow26.workers.dev/llms.txt  
**Agent card:** https://dirtsmith-go.bfurrow26.workers.dev/.well-known/agent-card.json  
**MCP card:** https://dirtsmith-go.bfurrow26.workers.dev/.well-known/mcp.json  

## What it is

A read-only rate sheet of outside builders' agent-callable tools (x402 and pay-as-you-go APIs) with published prices. Dirtsmith does not sell or process payment on this surface. Paid use through Dirtsmith is **not live**; `use_tool` / `confirm_want` are free demand signals only.

## Connect (MCP, streamable HTTP)

```json
{
  "mcpServers": {
    "dirtsmith-outside-tools-rate-sheet": {
      "type": "http",
      "url": "https://dirtsmith-go.bfurrow26.workers.dev/mcp"
    }
  }
}
```

Official MCP Registry name: `dev.workers.bfurrow26.dirtsmith-go/rate-sheet`

## Try first (no auth)

```bash
curl -X POST "https://dirtsmith-go.bfurrow26.workers.dev/use" \
  -H "content-type: application/json" \
  -d '{"tool":"AX1 Console"}'
```

Or MCP `tools/call` → `use_tool` with `{"name":"AX1 Console"}`.

## Pricing

Listing prices for outside tools are published at `/rates.json`. Dirtsmith's own MCP read tools are free. There is no checkout on this worker yet.

## Source of this repo

Public documentation mirror for transparency (ToolVet / registries). Runtime code lives on Cloudflare Workers; this repo holds the human-readable contract and links agents need.
