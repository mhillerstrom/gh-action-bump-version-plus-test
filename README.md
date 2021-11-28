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
pre-alpha
## Starting Version
23.0.0
## Expectation
- **Version:** 23.0.1-alpha.0