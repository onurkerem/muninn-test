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

Testing modification sync: UNIQUE-MOD-STRING-98765

## Next Steps

- Read the [API Reference](./api-reference.md) for available tools
- Check out the main repository for more examples

## E2E Modification Test

Modified at: 1773697220
Unique mod string: MOD-UNIQUE-1773697220
