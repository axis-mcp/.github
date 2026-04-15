# Axis MCP

**Managed MCP infrastructure for AI agents.**

We build the tooling layer between AI agents and the data they need — from open-source server management to a curated marketplace of production-ready MCP servers.

---

### Open Source

**[axis-mcp-cli](https://github.com/axis-mcp/axis-mcp-cli)** — A free, open-source CLI framework for managing MCP servers across Claude Desktop, Cursor, and Windsurf.

axis keeps a single local registry at `~/.axis/registry.json` as the source of truth. Client config files for Claude Desktop, Cursor, and Windsurf are treated as write targets — add a server once, sync it everywhere with one command. No more manual JSON editing, no more config drift between machines.

```bash
# Install
npm install -g axis-mcp-cli

# Set up your local registry
axis init

# Register a server
axis add npm:@modelcontextprotocol/server-sse --name axis-stocks \
  --command npx \
  --args "-y @modelcontextprotocol/server-sse https://mcp.axis-mcp.live/stocks"

# Sync to every client at once
axis enable axis-stocks --target all

# Check what is synced where
axis status
```

Built with TypeScript, MIT licensed, Node 18+. Contributions welcome.

---

### Platform

**[axis-mcp.live](https://axis-mcp.live)** — A marketplace of managed MCP servers. One API key gives your AI agent access to stock data, company intelligence, web scraping, and more. Zero infrastructure to maintain.

---

### Links

- Website: [axis-mcp.live](https://axis-mcp.live)
- Docs: [axis-mcp.live/docs](https://axis-mcp.live/docs)
- CLI: [axis-mcp.live/axis](https://axis-mcp.live/axis)
- Contact: [axis.mcp.support@gmail.com](mailto:axis.mcp.support@gmail.com)
