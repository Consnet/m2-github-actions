# Magento PHPCS Analysis

## Inputs

All inputs and their descriptions are as included in the [action.yml](./action.yml)

## Usage

The example below skips a number of attributes. The omitted attributes adopt the default values
```yml
name: PHPCS Static Analysis
on:
  push:
    branches:
      - master
  pull_request:
    branches:
      - master
jobs:
  code-sniffer-test:
    name: PHPCS Static Analysis
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: ./.github/actions/code-sniffer
        with:
          extensions_path: app/code

```