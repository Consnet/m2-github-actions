# Magento PHPStan Testing

## Inputs

All inputs and their descriptions are as included in the [action.yml](./action.yml)

## Usage

The example below may skip some attributes. As all attributes have default values, it's possible to use the action without specifying values

```yml
name: PHPStan Static Analysis
on:
  push:
    branches:
      - master
  pull_request:
    branches:
      - master
jobs:
  phpstan_static_analysis:
    name: PHPStan Static Analysis
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: Consnet/m2-github-actions/phpstan@main
        with:
          php_version: 8.1
          composer_version: 2
          composer_repository: https://repo.magento.com/
          magento_edition: magento/project-community-edition
          magento_version: 2.4.5
          composer_auth: ${{ secrets.COMPOSER_AUTH }}
          extensions_path: app/code
          phpstan_level: 1
```