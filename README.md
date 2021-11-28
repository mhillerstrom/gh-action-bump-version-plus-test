# Test Details
## .github/workflows/push.yml
```YAML
name: Bump Version (Default="Minor")
'on':
  push: null
jobs:
  bump-version:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - run: echo "Bump Version (Default='Minor')"
      - run: env
      - id: version-bump
        uses: ./action
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        with:
          default: minor
          patch-wording: patch

```
## Message
patch
## Starting Version
26.0.0
## Expectation
- **Version:** 26.0.1