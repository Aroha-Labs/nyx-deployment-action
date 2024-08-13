# Nyx Deployment GitHub Action

This action deploys services using the Nyx deployment API and checks their status.

## Inputs

- `environment`: Deployment environment (default `stg`)
- `name`: Name of the service (defaults to the current repository name)
- `path`: Deployment path (default `/`)
- `port`: Service port (default `80`)
- `repo`: Git repository URL (defaults to the current repository URL)

## Example Usage

```yaml
steps:
  - name: Checkout
    uses: actions/checkout@v2

  - name: Deploy and Check Service
    uses: Aroha-Labs/nyx-deployment-action/action@main
    with:
      environment: "prod"
      name: "custom-name"
      port: "8080"
```
