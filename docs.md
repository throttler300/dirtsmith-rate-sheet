# Dirtsmith rate sheet — docs

## Primary docs page
https://dirtsmith-go.bfurrow26.workers.dev/developers

## Endpoints agents use
| Path | Role |
|---|---|
| `/mcp` | MCP streamable-HTTP (tools/list, use_tool, find_tool, get_result, …) |
| `/rates.json` | Full tool catalog + prices |
| `/use` | Free quote / demand signal (POST) |
| `/a2a` | Minimal A2A JSON-RPC |
| `/llms.txt` | Agent-readable index |
| `/.well-known/agent-card.json` | A2A card |
| `/.well-known/mcp.json` | MCP discovery card |
| `/.well-known/ard.json` | ARD manifest |

## Honesty
Paid marketplace use is **not live**. Do not treat quotes as purchases.
