## Example Usage

```
name: Release workflow

on:
  push:
    branches:
      - master
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@master
      with:
        fetch-depth: '0'
    - name: Bump version and push tag
      id: tag_release
      uses: anothrNick/github-tag-action@1.17.2
      env:
        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        WITH_V: true
        DEFAULT_BUMP: patch
    - name: Upload release notes
      if: steps.tag_release.outputs.tag
      uses: Roang-zero1/github-create-release-action@master
      with:
        created_tag: ${{ steps.tag_release.outputs.tag }}
      env:
        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```
