# M365 Cookbook

A companion to the [Entra Admin Flow Cookbook](https://github.com/MSPFE2019/entra-admin-flow-cookbook), focused on read-only reporting recipes for Microsoft 365 workloads, Power Platform, and Microsoft 365 Copilot.

## Current status

This repository begins with an interactive cookbook prototype in [`index.html`](index.html). It demonstrates workload filters, recipe details, full request URLs, permission guidance, and Power Automate outlines. The initial collection covers Teams, SharePoint, OneDrive, Exchange, Power Platform inventory, and Copilot usage reporting.

The recipes link to Microsoft API documentation and are intended as learning examples. Before using a recipe, verify its current endpoint, permission, licensing, cloud availability, response format, and your organization's privacy and retention requirements. Usage reports can contain identifiable user data.

## API notes

- Microsoft Graph usage reports use `Reports.Read.All` and return CSV data; some report APIs redirect to a short-lived download URL. They are not JSON collection endpoints.
- Power Platform inventory uses the separate Power Platform API, not Microsoft Graph. Its inventory API requires delegated user authentication and does not support service-principal or managed-identity app-only authentication.
- The cookbook is read-only. It does not modify tenant configuration or resources.

## Preview locally

Open `index.html` in a browser, or serve this directory with any static web server. No build step or external runtime dependencies are required.

## References

- [Microsoft Graph permissions](https://learn.microsoft.com/graph/permissions-reference)
- [Microsoft Graph national cloud deployments](https://learn.microsoft.com/graph/deployments)
- [Power Platform inventory API](https://learn.microsoft.com/power-platform/admin/inventory-api)
