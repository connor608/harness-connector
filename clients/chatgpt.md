# Connect Harness to ChatGPT

Harness is a remote MCP server. ChatGPT adds it as a custom MCP server. There is no config file to edit: you give ChatGPT a name and the URL.

Values:

| Field | Value |
|---|---|
| Name | Harness |
| Description | Harness by Heoka: the business brain for unpaid invoices, quiet quotes and mail waiting on a reply |
| Connection | MCP server URL, including the `/mcp` path: `https://mcp.heoka.co.uk/mcp` |
| Authentication | OAuth, sign in with your Harness account |

Steps, from the OpenAI Developers page "Connect and test your plugin" (https://developers.openai.com/plugins/deploy/connect-chatgpt), current at 3 Nov 2026:

1. Go to ChatGPT Plugins (https://chatgpt.com/plugins).
2. Select the plus button, then **Add custom MCP server**.
3. Enter a user-facing name and description (values above).
4. Under **Connection**, for a public endpoint, enter the MCP server URL, including the `/mcp` path.
5. Configure authentication, review the risk warning, and select **I understand and want to continue**.
6. Select **Create as a plugin**.
7. Review the tools and metadata discovered from the server.

Account and workspace policies apply to adding and using custom MCP servers, so a workspace admin may need to allow it.

After the server changes its tools, open the connection at ChatGPT Plugins and select **Refresh**.

An anonymous request to the URL returns 401. That is expected until you sign in.
