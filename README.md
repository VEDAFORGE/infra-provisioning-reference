# infra-provisioning-reference

Public reference implementation for the landing-zone infrastructure that
platform CI/CD (Databricks, Fabric, ...) gets deployed onto: network,
workspace, and identity, provisioned as code and fully destroyable.

This repository is scaffolded and not yet populated with a working example.
Content is added once an example has actually been built, tested locally, and
run for real, and once the CI/CD article that depends on it has published —
see the parent playbook's publishing order for why the build order and the
publish order differ here.

## Repository structure

- `modules/` — reusable Terraform modules, shared across platform examples
  (network, identity, and one module per platform's workspace resource)
- `examples/` — one composed stack per published article
- `diagrams/` — Mermaid diagram sources
- `images/` — screenshots per article
- `docs/articles/` — article notes
- `docs/releases/` — release notes
- `release-assets/` — Gist-ready bundles

## License

MIT. See [LICENSE](LICENSE).
