# Home Assistant Multi-Site Homelab

A documented Home Assistant setup across two locations: Poland and Mettmann (Germany).

## Overview
This repository documents my Home Assistant homelab with a focus on:
- energy monitoring
- automations
- dashboard design
- helper/template sensor logic
- Codex-assisted MCP safety workflow
- practical smart home use cases

## Locations
- Poland
- Mettmann, Germany

## Main Features
- real-time power monitoring
- daily, weekly, and monthly energy tracking
- cost calculation based on actual electricity price
- custom Lovelace dashboards
- helper-based and template-based sensors
- motion and tablet automations
- device-level energy visibility
- safety-first Codex + MCP workflow for controlled documentation and configuration support

## Repository Structure
- `docs/` architecture and setup notes
- `config-examples/` selected YAML examples
- `screenshots/` dashboard and system screenshots

## Highlights
- custom energy monitoring based on Home Assistant helpers
- comparison of current vs previous day/week/month
- multi-site organization
- practical automations for daily living
- documented dry-run and approval workflow for AI-assisted Home Assistant changes

## Codex + MCP Safety Workflow
This setup also documents a controlled Codex-assisted workflow for Home Assistant MCP work.

The goal is not to let an AI agent freely control the smart home, but to use it as a safety-first assistant for documentation, dry runs, payload review, and read-only verification.

See [docs/codex-mcp-safety-workflow.md](docs/codex-mcp-safety-workflow.md).

## Notes
Sensitive data such as IP addresses, tokens, secrets, Wi-Fi names, and private identifiers have been removed.
