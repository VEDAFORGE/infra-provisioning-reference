# Contributing

This repository is a public reference implementation for landing-zone
infrastructure provisioning: the network, workspace, and identity baseline
that platform-specific CI/CD (Fabric, Databricks, ...) is deployed onto.

## What to Contribute

- Reusable Terraform modules, kept platform-agnostic where the resource
  itself is platform-agnostic (network, identity/RBAC)
- Public-safe example stacks that compose modules for one platform
- Sanitized diagrams
- Documentation that helps another engineer reproduce the pattern

## What Not to Contribute

- Secrets, `.tfvars` with real values, `.tfstate` files
- Tenant IDs, subscription IDs, workspace IDs, account IDs
- Service principal client IDs or secrets
- Local file paths
- Private planning notes
- Customer names

## Expectations

- Keep `modules/` free of anything specific to one example stack — a module
  used by only one example probably belongs inside that example instead.
- Keep examples aligned with the article flow.
- State module boundaries and singleton/external dependencies (e.g. an
  account-level resource that already exists and this repo does not manage)
  plainly in the module's README.
