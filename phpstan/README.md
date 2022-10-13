# Magento PHPStan Testing

## Inputs

All inputs and their descriptions are as included in the [action.yml](./action.yml)

## Usage

The example below skips a number of attributes. The omitted attributes adopt the default values
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
      - uses: actions/checkout@v2
      - uses: ./.github/actions/phpstan
        with:
          composer_repository: https://repo.magento.com/
          magento_version: 2.4.5
          composer_auth: ${{ secrets.COMPOSER_AUTH }}
          extensions_path: app/code

```