# API Reference

This document tests the `search_docs` MCP tool.

## Available Tools

### list_repos

List all configured repositories.

**Returns:** Array of repository identifiers in `owner/repo` format.

### get_repo_info

Get metadata and README preview for a repository.

**Parameters:**
- `repo` (string): Repository in `owner/repo` format

**Returns:** Repository metadata including description, stars, and README preview.

### list_docs

List all markdown and text files in a repository.

**Parameters:**
- `repo` (string): Repository in `owner/repo` format
- `path` (optional): Path to list from (defaults to root)

**Returns:** List of files with path, size, and last commit date.

### get_doc

Fetch the content of a specific file.

**Parameters:**
- `repo` (string): Repository in `owner/repo` format
- `path` (string): File path within the repository

**Returns:** File content with TOON frontmatter containing metadata.

### search_docs

Full-text search across configured repositories.

**Parameters:**
- `query` (string): Search query
- `repo` (optional): Limit search to specific repository

**Returns:** Matching files with snippets highlighting the search terms.

## Error Handling

All tools return structured error responses when issues occur:

- `repository_not_found`: Repository doesn't exist or isn't accessible
- `file_not_found`: Requested file doesn't exist
- `rate_limited`: GitHub API rate limit exceeded
