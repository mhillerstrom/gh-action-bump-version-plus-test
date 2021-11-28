# Test Details
## .github/workflows/push.yml
```YAML
name: Bump Version
'on':
  push: null
jobs:
  bump-version:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - run: echo "Bump Version"
      - run: env
      - id: version-bump
        uses: ./action
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

```
## Message
pre-rc
## Starting Version
10.0.0
## Expectation
- **Version:** 10.0.1-rc.0