<div align="center">
    <img src="https://raw.githubusercontent.com/agentuity/setup-action/main/.github/Agentuity.png" alt="Agentuity" width="100"/> <br/>
    <strong>Build Agents, Not Infrastructure</strong> <br/>
<br />

<a href="https://github.com/agentuity/sdk-js/blob/main/README.md"><img alt="License" src="https://badgen.now.sh/badge/license/Apache-2.0"></a>
<a href="https://discord.gg/vtn3hgUfuc"><img alt="Join the community on Discord" src="https://img.shields.io/discord/1332974865371758646.svg?style=flat"></a>
</div>
</div>


# Setup Agentuity Action

This GitHub Action sets up the Agentuity CLI in your GitHub Actions workflow.

## Example Workflow

```yaml
name: Example Workflow
on: [push]

jobs:
  example:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Setup Agentuity CLI
        uses: agentuity/setup-agentuity-action@v1
        with:
          api_key: ${{ secrets.AGENTUITY_API_KEY }}
      - name: Use Agentuity CLI
        run: agentuity version
```

## How it works

This action:
1. Downloads the latest version of the Agentuity CLI for Linux x86_64
2. Adds it to the PATH
3. Makes it available for subsequent steps in your workflow
