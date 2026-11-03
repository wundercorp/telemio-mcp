# Security

Telemio handles observability data that may contain operationally sensitive information.

## Reporting a security issue

Do not report suspected vulnerabilities in a public GitHub issue when the report contains sensitive technical details, credentials, telemetry, or customer information.

Use Telemio's published security contact or private support channel when available.

## Credentials

Never commit any of the following to this repository:

- Telemio access tokens
- ingest keys
- browser/RUM keys intended to remain private
- OAuth client secrets
- customer telemetry
- production environment secrets

## Repository scope

This repository contains public integration documentation and metadata only. The production MCP server implementation is operated as part of the hosted Telemio service.
