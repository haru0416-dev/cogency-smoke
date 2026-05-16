# cogency-smoke

Smoke-test fixture repository for the `haru0416-dev/cogency` GitHub Action.

The workflow in `.github/workflows/cogency.yml` consumes
`haru0416-dev/cogency@v0.1.0` and runs `cogency verify` on every push.
The fixture contains only `cogency init` scaffold output, so the expected
result is "no structural diagnostics".
