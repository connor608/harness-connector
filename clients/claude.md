# Connect Harness to Claude

Harness is a remote MCP server. Claude adds it as a custom connector. There is no config file to edit: you give Claude a name and the URL.

Values:

| Field | Value |
|---|---|
| Name | Harness |
| Remote MCP server URL | `https://mcp.heoka.co.uk/mcp` |
| Authentication | Sign in (OAuth) with your Harness account |

Steps, from the Claude help article "Get started with custom connectors using remote MCP" (https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp), current at 3 Nov 2026:

1. Open the Customize section and go to the Connectors tab.
2. Choose the add option, then select the option to add a custom connector.
3. Give the connector a name (Harness).
4. Enter the remote MCP server URL, `https://mcp.heoka.co.uk/mcp`, then continue.
5. Check the authentication settings Claude detected and change them if needed. Then continue.
6. Under Authentication, pick "Sign in now". You will be taken to Harness to sign in.
7. Under OAuth client, "Use Claude's published identity (Recommended)" is the default choice. Leave it.
8. Leave Request headers empty. Harness uses OAuth, not a fixed key.
9. Finish by adding the connector.

Team and Enterprise plans: an Owner adds the connector under Organization settings > Connectors (Add, hover over Custom, select Web). Each member then connects individually from Customize > Connectors.

To use it in a chat, click "+" at the lower left of the chat, choose Connectors, and toggle Harness on.

An anonymous request to the URL returns 401. That is expected until you sign in.
