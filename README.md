# Onlyx for OnlyFans

An OnlyFans agency assistant provided by Onlyx. Connect your existing Onlyx workspace through OAuth to read creators, inbox activity, fans and statistics, and use the workspace operations permitted by your connection.

Onlyx is independently developed and is not affiliated with or endorsed by OnlyFans.

## Install in Claude Code

Run this command inside Claude Code:

```text
/plugin install onlyx --marketplace x-project-coding/onlyx-plugins
```

Or register the marketplace and install from your terminal:

```sh
claude plugin marketplace add x-project-coding/onlyx-plugins
claude plugin install onlyx@onlyx
```

Open `/mcp` in Claude Code to complete the Onlyx OAuth connection. An Onlyx workspace owner or admin signs in and reviews the permissions and creator restrictions. Choose read-only access and specific creators for reporting. Installation alone does not grant workspace access.

## Install in Codex

Add the public marketplace:

```sh
codex plugin marketplace add x-project-coding/onlyx-plugins
```

Open the Onlyx marketplace in Codex, install **Onlyx for OnlyFans**, and complete the Onlyx OAuth connection when prompted.

## Connect in Claude or ChatGPT

You can also add `https://mcp.onlyx.ai/mcp` as a custom remote MCP connector using OAuth. See the [Claude setup guide](https://help.onlyx.ai/developers/mcp/claude) or the [ChatGPT setup guide](https://help.onlyx.ai/developers/mcp/chatgpt).

This GitHub-hosted marketplace is provided by Onlyx. Listings in Anthropic's directory and OpenAI's public directory are separate publication processes.

## What the connection can do

Read workspace details, creators, inbox counts, fans, statistics and Help Center documentation. When granted the required permissions, the service also exposes message sending, vault media, paid-message actions, AI persona and content settings, and tracking links. Review an action before sending a message or changing a live creator account. Available operations depend on your workspace access, granted scopes and creator restrictions.

Your assistant sends MCP tool inputs to `https://mcp.onlyx.ai/mcp` and receives the results from your authorized Onlyx workspace. OAuth authorization is handled by `https://api.onlyx.ai`. Onlyx uses the workspace's authorized account connections for the requested operations. The package contains remote connection configuration and the approved Onlyx icon; it has no local executable, hooks or embedded credentials.

The `search_docs` tool can send its search query to Mintlify when the documentation search service is configured. Keep credentials and private workspace information out of documentation search queries. Write operations, such as updating fan notes or settings, save the requested changes in your Onlyx workspace.

To revoke access, open **Onlyx Settings → API & MCP → Connected apps** and disconnect the app.

Example requests:

- Which Onlyx workspace am I connected to, and what access does this connection have?
- List the creators visible to my Onlyx connection and their connection status.
- Summarize today's statistics and inbox counts without changing anything.

## Help

- [Onlyx MCP documentation](https://help.onlyx.ai/developers/mcp)
- [Tool catalog and scopes](https://help.onlyx.ai/developers/mcp/tools)
- [Support](https://onlyx.ai/support): support@onlyx.ai
- [Privacy policy](https://onlyx.ai/privacy)

## License

The plugin configuration and documentation use the [MIT license](plugins/onlyx/LICENSE). Onlyx logo and trademark rights are reserved; the hosted Onlyx service is outside this license. See the license file for its scope.
