# GitHub Actions testing tool - Act

## Table of content

1. [Getting started](#getting-started)

## Getting started

1. Install
    ```sh
    curl --proto '=https' --tlsv1.2 -sSf https://raw.githubusercontent.com/nektos/act/master/install.sh | sudo bash
    ```
2. Run a workflow
    ```sh
    act -W '.github/workflows/{workflow_name}.yml'
    ```
