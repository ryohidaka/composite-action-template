# composite-action-template

[![GitHub Release](https://img.shields.io/github/v/release/ryohidaka/composite-action-template)](https://github.com/ryohidaka/composite-action-template/releases/)
[![Test Action](https://github.com/ryohidaka/composite-action-template/actions/workflows/test.yml/badge.svg)](https://github.com/ryohidaka/composite-action-template/actions/workflows/test.yml)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/B0B6TVH92)

Template to create composite-action for GitHub Actions.

## Usage

```yml
- uses: ryohidaka/composite-action-template@v0.3.1
  with:
    who-to-greet: "Mona the Octocat"
- run: echo random-number "$RANDOM_NUMBER"
  shell: bash
  env:
    RANDOM_NUMBER: ${{ steps.foo.outputs.random-number }}
```

## Inputs

| Input          | Required | Description  | Default | Example |
| -------------- | -------- | ------------ | ------- | ------- |
| `who-to-greet` | ✔        | Who to greet | `World` | `World` |
| ``             | ❌       |              | ``      | ``      |

## Outputs

| Output          | Description   | Example |
| --------------- | ------------- | ------- |
| `random-number` | Random number | `9999`  |
