# Magento PHPMD Analysis

## Inputs

All inputs and their descriptions are as included in the [action.yml](./action.yml)

## Usage

The example below may skip some attributes. As all attributes have default values, it's possible to use the action without specifying values

```yml
name: PHPMD Static Analysis
on:
  push:
    branches:
      - master
  pull_request:
    branches:
      - master
jobs:
  mess-detector-test:
    name: PHPMD Static Analysis
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: Consnet/m2-github-actions/mess-detector@main
        with:
          php_version: 8.1
          extensions_path: app/code
          exclusions: "*/tests/*"
```