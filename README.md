# PMD Source Code Analyzer Action

This action integrates PMD with github workflows
Also writes output to pull request comments
_This repo was forked from sfdx-actions/setup-pmd and modified to suit_

## Example usage

```yaml
name: PMD Source Code Analyzer on Push

on: [push]

jobs:
  pmd:
    runs-on: ubuntu-latest

    steps:
      - uses: sfdx-actions/setup-pmd@v1
      - name: run-pmd
        run: pmd -d ./force-app/main/default/classes -R category/apex/design.xml -f text
```
