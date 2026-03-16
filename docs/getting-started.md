# Getting Started with Muninn

This document tests the `list_docs` and `get_doc` MCP tools.

## Overview

Muninn is an MCP server that provides on-demand access to documentation stored in GitHub repositories.

## Installation

```bash
npm install @onurkerem/muninn
```

## Usage

Configure your MCP client to use muninn with your repositories:

```json
{
  "mcpServers": {
    "muninn": {
      "command": "npx",
      "args": ["-y", "@onurkerem/muninn@latest", "--repos", "owner/repo"]
    }
  }
}
```

## Sync Test Section

Testing modification sync: E2E-MODIFICATION-TEST-$(date +%s)

## Next Steps

- Read the [API Reference](./api-reference.md) for available tools
- Check out the main repository for more examples
