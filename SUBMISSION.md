# Publishing and directory submission

## 1. Create the public GitHub repository

Recommended repository name:

```text
telemio-mcp
```

Recommended description:

```text
Official public integration metadata and documentation for the hosted Telemio MCP server.
```

Upload the contents of this repository to your chosen public GitHub repository.

## 2. MCP.directory

Use the public GitHub repository URL in the MCP.directory submission form.

Recommended form values:

### GitHub Repository URL

Use the final public repository URL, for example:

```text
https://github.com/WunderCorp/telemio-mcp
```

### npm Package

Leave blank.

### PyPI Package

Leave blank.

### Short Description

```text
Investigate logs, traces, metrics and production issues in Telemio via MCP.
```

### Email

Use the email address where you want directory publication notifications delivered.

## 3. Official MCP Registry

The repository includes a remote-only `server.json`.

Install the publisher on macOS with Homebrew:

```bash
brew install mcp-publisher
```

Validate locally:

```bash
mcp-publisher validate
```

Authenticate using a method that proves control of the `telemio.sh` namespace, then publish:

```bash
mcp-publisher publish
```

The current registry name is:

```text
sh.telemio/observability
```

The hosted remote is:

```text
https://mcp.telemio.sh/mcp
```

Before publishing, verify the endpoint is publicly reachable and supports Streamable HTTP.

## 4. What remains private

Do not add the proprietary Telemio MCP implementation merely to satisfy a directory scanner.

This repository is intentionally limited to public integration documentation and metadata. The actual hosted server remains part of Telemio's private production infrastructure.
