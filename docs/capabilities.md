# Telemio MCP capabilities

Telemio MCP gives authorized users an AI-friendly interface to observability data stored in Telemio.

## Investigation workflows

Typical workflows include:

- searching and narrowing application logs
- locating traces associated with requests, services, or incidents
- inspecting trace context and related failures
- identifying and summarizing application errors
- examining service health within a selected environment and time range
- comparing telemetry before and after a deployment or change
- correlating logs, traces, metrics, errors, and deployment context
- producing concise incident summaries backed by telemetry evidence

## Tool design

Telemio favors explicit, bounded observability operations rather than generic shell, SQL, or arbitrary command execution.

The exact exposed MCP tool set may evolve as the service develops. Clients should discover the current tool definitions from the MCP server rather than relying on names documented in this repository.

## Read-oriented default

The primary MCP experience is investigation and analysis. Read-oriented operations are preferred for production observability workflows.

Any future state-changing operations should be separately exposed, clearly described, appropriately authorized, and require explicit user intent where applicable.

## Data boundaries

MCP requests operate within the permissions of the authenticated Telemio user. The integration must not make data from unrelated workspaces available to a caller.
