# Test Details
## .github/workflows/push.yml
```YAML
name: Bump Version (Custom Checkout Token)
'on':
  push: null
jobs:
  bump-version:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
        with:
          token: ${{ secrets.TEST_TOKEN }}
      - run: echo "Bump Version (Custom Checkout Token)"
      - run: env
      - id: version-bump
        uses: ./action
        env:
          GITHUB_TOKEN: ${{ secrets.TEST_TOKEN }}

```
## Message
no keywords
## Starting Version
29.0.0
## Expectation
- **Version:** 29.0.1