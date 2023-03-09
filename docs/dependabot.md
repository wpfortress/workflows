# dependabot

The `dependabot` workflow is located
at [`.github/workflows/dependabot.yml`](https://github.com/wpfortress/workflows/tree/main/.github/workflows/dependabot.yml).

This workflow auto-merges [Dependabot](https://github.com/dependabot) PRs for minor and patch updates.

This reusable action depends on the following actions:

- [checkout](https://github.com/marketplace/actions/checkout)
- [fetch-metadata](https://github.com/marketplace/actions/fetch-metadata-from-dependabot-prs)

## Usage

### With defaults

```yml
name: dependabot

on:
    pull_request:
        branches:
            - main

jobs:
    dependabot:
        uses: wpfortress/workflows/.github/workflows/dependabot.yml@main
```
