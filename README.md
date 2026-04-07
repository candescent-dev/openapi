# Candescent DI OpenAPI Specification

Public distribution of the **Candescent Digital Insight API** OpenAPI specification.

## Quick Links

| Resource | Description |
|----------|-------------|
| [`candescent-di-api.yaml`](candescent-di-api.yaml) | Latest OpenAPI 3.0 specification |
| [`CHANGELOG.md`](CHANGELOG.md) | Release-by-release change summary |

## About

The Candescent Digital Insight API enables financial institutions, Marketplace Partners, and developers to build digital banking experiences. This repository contains the public OpenAPI specification that documents the available API endpoints, request/response schemas, and authentication requirements.

## Usage

### Download the latest spec

```bash
curl -LO https://raw.githubusercontent.com/candescent-dev/openapi/main/candescent-di-api.yaml
```

### Use a specific version

Previous versions are available via git tags. Each release is tagged as `v{VERSION}`:

```bash
# View available versions
git tag -l

# Download a specific version
curl -LO https://raw.githubusercontent.com/candescent-dev/openapi/v1.3.1/candescent-di-api.yaml
```

### Import into tools

The spec is compatible with any OpenAPI 3.0 tooling:

- **Swagger UI / Swagger Editor** — paste the URL or upload the file
- **Postman** — import via URL or file upload
- **Code generators** — use with `openapi-generator-cli`, `swagger-codegen`, or similar

## Versioning

This specification follows [Semantic Versioning](https://semver.org/):

- **Major** — breaking changes (removed endpoints, incompatible schema changes)
- **Minor** — new endpoints or backward-compatible additions
- **Patch** — documentation fixes, description updates, non-breaking corrections

## Contributing

This repository is a **read-only mirror** published from an internal source. We do not accept pull requests directly. For questions or feedback, please reach out through your existing Candescent support channels.

## License

Proprietary — see your Candescent agreement for usage terms.
