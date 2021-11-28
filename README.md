# Test Details
## .github/workflows/push.yml
```YAML
name: Bump Version (Skip If Commit Contains)
'on':
  push: null
jobs:
  bump-version:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - run: echo "Bump Version (Skip If Commit Contains)"
      - run: env
      - id: version-bump
        uses: ./action
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        with:
          skip-if-commit-contains: dependabot

```
## Message
major
## Starting Version
20.0.0
## Expectation
- **Version:** 21.0.0