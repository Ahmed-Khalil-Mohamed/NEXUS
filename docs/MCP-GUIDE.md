# MCP connections in NEXUS

## Add and inspect a server

1. Open **Store → MCP connections** to explore entries, or **Settings → MCP connections** to configure a server.
2. Choose HTTP or stdio and enter the server's documented configuration. A stdio server needs a command and a valid JSON array of arguments. HTTP uses its URL and supported bearer authentication.
3. Save the server. New servers start disabled. Saving an edited record preserves its ID.
4. Discover its tools, inspect descriptions and choose individual permissions before enabling use.
5. Select a supported connection for chat. Use the **@** picker to mention available tools, skills or MCP entries, or allow enabled tools through conversation preferences.

## Manage connections

Search saved servers and discovered tools. Saved server count, enabled server count and tool count are separate. Configuration and server management have distinct panels, so you can review an existing server without confusing it with a new connection.

JSON errors are shown before saving. Switching to HTTP ignores inactive stdio arguments. Discovery is not proof that every tool will succeed: credentials, environment and model tool support still matter.

## Data and execution

MCP tools execute through the selected server and may read files or contact external services according to their permissions. Review the server, arguments and each allowlisted tool. Never paste secrets into chat instructions. MCP OAuth is not supported in this build; use a supported transport/authentication method. NEXUS's project Apply workflow does not govern every action an external MCP server may perform.

[API connections](API-GUIDE.md) · [Privacy](PRIVACY.md) · [Back to NEXUS](../README.md)
