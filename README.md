# Test Details
## .github/workflows/push.yml
```YAML
name: Bump Version (Target Branch)
'on':
  push: null
jobs:
  bump-version:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - run: echo "Bump Version (Target Branch)"
      - run: env
      - run: git branch other-branch
      - id: version-bump
        uses: ./action
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        with:
          target-branch: other-branch

```
## Message
no keywords
## Starting Version
28.0.0
## Expectation
- **Version:** 28.0.1
- **Branch:** other-branch