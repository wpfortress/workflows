# phpunit

The `phpunit` workflow is located
at [`.github/workflows/phpunit.yml`](https://github.com/wpfortress/workflows/tree/main/.github/workflows/phpunit.yml).

This workflow will use [`phpunit`](https://phpunit.de) script that tests your PHP code.

This reusable action depends on the following actions:

- [checkout](https://github.com/marketplace/actions/checkout)
- [setup-php](https://github.com/marketplace/actions/setup-php-action)
- [composer-install](https://github.com/marketplace/actions/install-php-dependencies-with-composer)

## Inputs

The action has the following inputs:

### Optional inputs

#### php-versions

The PHP versions to setup and use.

- This `input` is optional, with a default of '8.1'.

#### composer-dependency-versions

The Composer dependency version constraints.

- This `input` is optional, with a default of 'locked'.

## Usage

### With defaults

```yml
name: phpunit

on:
    pull_request:
        branches:
            - main

jobs:
    phpunit:
        uses: wpfortress/workflows/.github/workflows/phpunit.yml@main
```

### Overriding some defaults

```yml
name: phpunit

on:
    pull_request:
        branches:
            - main

jobs:
    phpunit:
        uses: wpfortress/workflows/.github/workflows/phpunit.yml@main
        with:
            php-versions: '["8.0", "8.1", "8.2"]'
            composer-dependency-versions: '["lowest", "highest"]'
```
