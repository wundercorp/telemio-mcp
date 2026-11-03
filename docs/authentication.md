# Authentication and authorization

Telemio MCP is a hosted authenticated service.

## Account access

Users connect through Telemio and may access only the workspaces and telemetry their Telemio account is authorized to access.

The public MCP endpoint is:

```text
https://mcp.telemio.sh/mcp
```

A publicly reachable endpoint does not imply anonymous access to private telemetry.

## Least privilege

Telemio's MCP integration is intended to follow least-privilege principles:

- access is associated with an authenticated Telemio identity
- authorization is enforced at the workspace and resource level
- production telemetry is not exposed merely because the MCP endpoint is discoverable
- credentials must not be committed to this repository

## Client setup

Authentication details may vary by supported MCP client and by the current Telemio account-linking flow.

Do not place long-lived Telemio credentials directly in public configuration files or Git repositories.
