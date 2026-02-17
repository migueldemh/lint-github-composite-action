# lint-github-actions-workflows

A composite action for linting GitHub Actions workflow configuration.

## Usage

```yaml
name: Lint

on: pull_request

permissions:
  contents: read

jobs:
  actionlint:
    name: GitHub Actions
    runs-on: ubuntu-24.04
    steps:
      - name: Checkout
        uses: actions/checkout@v6

      - name: Lint Workflow Files
        uses: craigsloggett/lint-github-actions-workflows@v1
```

### Inputs

| Input            | Required? | Default  | Description                                          |
| ---------------- | --------- | -------- | ---------------------------------------------------- |
| `go-version`     | `false`   | `1.25.5` | The version of Go to use when running `actionslint`. |
