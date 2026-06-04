# Codex + MCP Safety Workflow

This document describes the public, sanitized version of a Codex-assisted Home Assistant MCP workflow.

The private operational setup contains local details and environment-specific configuration. This public document focuses only on the architecture, safety model, and working rules.

## Purpose

The goal is to use Codex as a safety-first assistant for Home Assistant documentation and controlled configuration support.

Codex is used for:

- reading and summarizing documentation
- preparing Home Assistant YAML or MCP payloads
- documenting decisions and setup steps
- checking configuration intent before changes
- verifying results with read-only MCP tools

Codex is not treated as an autonomous smart home controller.

## Safety Model

Every MCP-assisted change follows a strict review workflow:

1. Prepare a dry run.
2. Show the exact YAML or MCP payload.
3. Wait for explicit human approval.
4. Apply the approved change through MCP.
5. Verify the result with read-only tools.

This keeps the human in control while still making the workflow faster and easier to document.

## Default Boundary

The default mode is read-only.

Read-only checks may be used to inspect:

- Home Assistant overview information
- exposed entities
- existing configuration state
- created automation metadata after a write

Write operations require explicit approval and must be scoped to a known, reviewed payload.

## Operations Requiring Separate Approval

The following actions are outside the default workflow and require separate explicit approval:

- Home Assistant restart
- core reload
- delete or remove operations
- backup or restore operations
- direct file write or delete operations
- service calls that control devices
- camera control
- alarm control
- lock control
- door control
- gate control

## Automation Rules

Automations created through MCP should be clear, reversible, and easy to audit.

Recommended rules:

- use a clear `alias`
- include a useful `description`
- choose an explicit `mode`
- prefer verified `entity_id` values
- use placeholders only when they are intentional and obvious
- keep test automations disabled by default
- verify created automations with read-only tools

## Secret Handling

Public documentation must not include:

- tokens
- OAuth secrets
- secret paths
- private URLs containing credentials
- Wi-Fi names
- device credentials
- private identifiers
- full Home Assistant backups
- `.storage` exports

Private LAN addresses and environment-specific paths should be replaced with placeholders such as:

```text
HA_LAN_IP
HOME_ASSISTANT_URL
SECRET_PATH
```

## Why This Matters

Home Assistant can control real devices in a real home. A safe AI-assisted workflow must therefore be designed around review, approval, and rollback instead of blind automation.

This approach keeps Codex useful for documentation and configuration work while reducing the risk of accidental device control, destructive changes, or leaked secrets.
