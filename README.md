# Repliers OpenAPI Python Client Generator

This repository contains a GitHub Actions workflow that automatically generates a Python client library from an OpenAPI specification.

## How It Works

The workflow:
1. Fetches an OpenAPI specification from a URL
2. Generates a Python client using [openapi-python-client](https://github.com/openapi-generators/openapi-python-client)
3. Packages the generated client
4. Creates a GitHub release with the packaged client as a downloadable asset

## Usage

### Manual Trigger

You can manually trigger the workflow:

1. Go to the Actions tab in this repository
2. Select the "Generate Python Client" workflow
3. Click "Run workflow"
4. Provide:
   - URL to the OpenAPI specification
   - Tag name for the release (e.g., v1.0.0)
5. Click "Run workflow"

### Automatic Trigger

The workflow also runs automatically on pull requests to the main branch.

## Installation

Once a release is created, you can install the generated client:

```bash
pip install https://github.com/YOUR_USERNAME/YOUR_REPO/releases/download/vX.Y.Z/python-client.zip
```

Replace `YOUR_USERNAME`, `YOUR_REPO`, and `vX.Y.Z` with your actual GitHub username, repository name, and release version.

## Customization

You can customize the workflow by editing the `.github/workflows/main.yml` file. You might want to:

- Change the default OpenAPI URL
- Modify the Python version
- Adjust the release settings
- Change how the client is packaged

## License

[MIT](LICENSE)
