# Post Merge PR Label Getter

GitHub action to get label names from PR on merge

## Usage

```yml
name: Your Super Sweet Action Name

on:
  push:
    branches:
      - "main"

jobs:
  my-job:
    runs-on: ubuntu-latest

    steps:
      name: Get Labels
      id: get-labels
      uses: revrenlove/post-merge-pr-label-getter@v1.0.5
      with:
        github-token: ${{ secrets.GITHUB_TOKEN }}
```

These labels can be accessed via: `${{ steps.get-labels.outputs.label-names }}`
