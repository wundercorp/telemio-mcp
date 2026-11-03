# Telemio MCP

Official public integration repository for the hosted Telemio Model Context Protocol server.

Telemio is an OpenTelemetry-native observability platform for investigating logs, traces, metrics, errors, deployments, service health, and production incidents with AI-assisted workflows.

## Hosted MCP endpoint

```text
https://mcp.telemio.sh/mcp
```

The production MCP server is hosted and operated by Telemio. The server implementation is not distributed from this repository.

## What Telemio MCP enables

Connected AI clients can help authorized Telemio users investigate their own telemetry and answer questions such as:

- Why did checkout latency increase after the latest deployment?
- Which errors are affecting the payments service in production?
- Find traces related to a request or correlation ID.
- Summarize the highest-impact errors in a recent time window.
- Compare service health before and after a deployment.
- Correlate logs, traces, metrics, and deployment context during an incident.

## Authentication and authorization

Telemio MCP is an authenticated hosted service. Access is limited to the Telemio workspaces and telemetry the signed-in user is authorized to access.

See [Authentication](docs/authentication.md) for the public integration model.

## Capabilities

The integration is designed around explicit observability operations rather than arbitrary command execution. Public capability categories include:

- log investigation
- trace discovery and inspection
- error analysis
- service health analysis
- telemetry comparison across time windows
- deployment and regression investigation
- incident-oriented correlation of telemetry signals

See [Capabilities](docs/capabilities.md).

## MCP transport

Telemio exposes a remote MCP endpoint over Streamable HTTP:

```text
https://mcp.telemio.sh/mcp
```

## Official MCP Registry

This repository includes [`server.json`](server.json) for publishing Telemio as a remote-only MCP server in the official MCP Registry.

The intended registry identity is:

```text
sh.telemio/observability
```

Publishing requires control of the `telemio.sh` namespace and is intentionally not automated from this public repository.

## MCP.directory

This repository can also be used as the public GitHub repository when submitting Telemio to MCP.directory.

Suggested short description:

> Investigate logs, traces, metrics and production issues in Telemio via MCP.

## Security

Do not open public issues containing telemetry, access tokens, API keys, customer data, or other sensitive information.

See [SECURITY.md](SECURITY.md).

## Source availability

This repository contains public integration metadata and documentation for Telemio MCP. It does not contain the proprietary production server implementation or Telemio backend source code.

## Links

- Website: https://telemio.sh
- MCP endpoint: https://mcp.telemio.sh/mcp
