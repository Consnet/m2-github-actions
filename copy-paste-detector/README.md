# Magento PHPCPD Analysis

This action is used for detecting copied and pasted code, which can be a symptom of code duplication.

## Inputs

All inputs and their descriptions are as included in the [action.yml](./action.yml)

## Usage

The example below skips a number of attributes. The omitted attributes adopt the default values

```yml
name: PHPCPD Static Analysis
on:
  push:
    branches:
      - master
  pull_request:
    branches:
      - master
jobs:
  copy-paste-detector:
    name: PHPCPD Static Analysis
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: ./.github/actions/copy-paste-detector
        with:
          extensions_path: app/code
```