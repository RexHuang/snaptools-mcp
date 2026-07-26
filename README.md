# SnapTool MCP Server ⚡

[![MCP](https://img.shields.io/badge/MCP-Compatible-purple)](https://modelcontextprotocol.io)
[![OpenAPI](https://img.shields.io/badge/OpenAPI-3.1-blue)](https://www.snaptools.uk/openapi.json)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![Website](https://img.shields.io/badge/Website-snaptools.uk-6c5ce7)](https://www.snaptools.uk)

> **Give your AI agent 32+ developer tools via a single REST API endpoint.**

SnapTool MCP Server connects AI agents (Claude, Cursor, Codex, etc.) to 32+ instant developer utilities — JSON formatting, Base64 encoding, hashing, UUID generation, regex testing, and more — all through the Model Context Protocol.

## 🛠️ Available Tools (15 via MCP, 32+ total)

| Tool | Description |
|------|-------------|
| `json_format` | Format and beautify JSON |
| `json_minify` | Minify JSON to one line |
| `base64_encode` | Encode text to Base64 |
| `base64_decode` | Decode Base64 to text |
| `hash_sha256` | Generate SHA-256 hash |
| `hash_sha512` | Generate SHA-512 hash |
| `uuid_generate` | Generate UUIDs (1-100) |
| `slug_generate` | Convert text to URL slug |
| `url_encode` | URL-encode text |
| `url_decode` | URL-decode text |
| `case_upper` | Convert to UPPERCASE |
| `case_lower` | Convert to lowercase |
| `reverse` | Reverse a string |
| `word_count` | Count words, characters, lines |

> 💡 **32+ browser tools** also available at [snaptools.uk](https://www.snaptools.uk) including: regex tester, JWT decoder, CSS/HTML/SQL/XML formatters, color converter, markdown preview, text diff, password generator, IP/DNS lookup, and more.

## 🚀 Quick Start

### Claude Desktop / Claude Code

Add to your `claude_desktop_config.json` or `~/.claude/claude.json`:

```json
{
  "mcpServers": {
    "snaptool": {
      "url": "https://www.snaptools.uk/mcp.json"
    }
  }
}
```

### Cursor / VS Code

Add to your MCP configuration:

```json
{
  "mcpServers": {
    "snaptool": {
      "url": "https://www.snaptools.uk/mcp.json"
    }
  }
}
```

### Any MCP Client

Point your client to:
```
https://www.snaptools.uk/mcp.json
```

## 📡 REST API

For direct API access (requires [API key](https://www.snaptools.uk/pricing)):

```bash
curl "https://www.snaptools.uk/api/tools" \
  -H "x-api-key: sk-YOUR_KEY" \
  -H "Content-Type: application/json" \
  -d '{"tool":"json-format","input":"{\"hello\":\"world\"}"}'
```

```json
{
  "tool": "json-format",
  "input": "{\"hello\":\"world\"}",
  "result": "{\n  \"hello\": \"world\"\n}"
}
```

**49 API endpoints** available. Full docs: [snaptools.uk/docs/api](https://www.snaptools.uk/docs/api)

## 📋 Specifications

| Resource | URL |
|----------|-----|
| MCP Server | [snaptools.uk/mcp.json](https://www.snaptools.uk/mcp.json) |
| OpenAPI 3.1 | [snaptools.uk/openapi.json](https://www.snaptools.uk/openapi.json) |
| llms.txt | [snaptools.uk/llms.txt](https://www.snaptools.uk/llms.txt) |
| AI Plugin | [snaptools.uk/.well-known/ai-plugin.json](https://www.snaptools.uk/.well-known/ai-plugin.json) |

## 💰 Pricing

| Plan | Price | Features |
|------|-------|----------|
| **Free** | $0 | All 32 browser tools, single processing |
| **Pro** | $5/mo | Batch up to 100, 30-day history, ad-free |
| **API** | $9/mo | REST API access, 10K calls/mo, MCP + OpenAPI |

[View pricing →](https://www.snaptools.uk/pricing)

## 🔒 Privacy

All browser-based tools run **100% client-side**. Your data never leaves your browser.

## 📄 License

MIT © SnapTool

---

**Built for agents, by agents.** 🤖
