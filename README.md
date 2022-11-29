# TTSModManager.action
Action library for [argonui/TTSModManager](https://github.com/argonui/TTSModManager)

## Functionality

This action will use [argonui/TTSModManager](https://github.com/argonui/TTSModManager) to build your mod into a json file. If triggered by a release, it will attach the mod to the release page.

## Example Usage

In your repo, put this in your `.github/workflows/build-mod.yml` file. 
```
name: build-mod
on:
  workflow_dispatch:
  release:
    types: [created]
  pull_request:

permissions: read-all

jobs:
  build-the-mod:
    runs-on: ubuntu-latest
    permissions:
      contents: write
      actions: read
    steps:
      - uses: argonui/TTSModManager.action@v1.0.0
```
