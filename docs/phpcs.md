# phpcs

The `phpcs` workflow is located
at [`.github/workflows/phpcs.yml`](https://github.com/wpfortress/workflows/tree/main/.github/workflows/phpcs.yml).

This workflow will use [`phpcs`](https://github.com/squizlabs/PHP_CodeSniffer) script that tokenizes PHP to detect
possible violations of a defined set of coding standards.

> NOTE: This workflow can only be performed with a specific PHP version and not in a PHP matrix, as it should always be
> tested with the highest PHP version in use.

This reusable action depends on the following actions:

- [checkout](https://github.com/marketplace/actions/checkout)
- [setup-php](https://github.com/marketplace/actions/setup-php-action)
- [composer-install](https://github.com/marketplace/actions/install-php-dependencies-with-composer)

## Inputs

The action has the following inputs:

### Optional inputs

#### php-version

The PHP version to setup and use.

- This `input` is optional, with a default of 8.1.

## Usage

### With defaults

```yml
name: phpcs

on:
    pull_request:
        branches:
            - main

jobs:
    phpcs:
        uses: wpfortress/workflows/.github/workflows/phpcs.yml@main
```

### Overriding some defaults

```yml
name: phpcs

on:
    pull_request:
        branches:
            - main

jobs:
    phpcs:
        uses: wpfortress/workflows/.github/workflows/phpcs.yml@main
        with:
            php-version: 8.2
```
