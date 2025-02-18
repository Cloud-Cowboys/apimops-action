# Install API Management Operations CLI

This GitHub Action installs the API Management Operations CLI from GitHub Packages.

## Inputs

### `token`

**Required** The token to use for acquiring the NPM package.

### `version`

The version of the API Management Operations CLI to install. Default is `latest`.
## Example usage
To install the latest version:
```yaml
uses: cloud-cowboys/setup-apimops@v1
with:
  token: ${{ secrets.NPM_TOKEN }}
```

To install a specific version:
```yaml
uses: cloud-cowboys/setup-apimops@v1
with:
  token: ${{ secrets.NPM_TOKEN }}
  version: '1.5.0'
```

## Steps

1. **Setup Node.js**: Uses the `actions/setup-node@v4` action to set up Node.js version 20.x.
2. **Authenticate to GitHub Packages**: Authenticates to GitHub Packages using the provided token.
3. **Install NPM package**: Installs the `@cloud-cowboys/apimops` package globally.
4. **Run NPM package**: Runs the `apimops` command to verify the installation.