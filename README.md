### Dmitrii Bernatskii — DevOps / DevSecOps engineer

I run Linux infrastructure for web services: monitoring, backups with tested restores, CI/CD and web perimeter protection. Stack: Linux, nginx, Docker Compose, GitLab CI, Prometheus, Grafana.

**[runsweep](https://github.com/runsweep/runsweep)** — after a supply-chain incident, tells you which GitHub Actions runs were hit and which secrets to rotate first. npm, PyPI and compromised actions; every job gets AFFECTED, POSSIBLE, UNCHECKED or CLEAN with the log line as evidence.

- Go CLI, signed releases with build provenance (`gh attestation verify`)
- `brew install runsweep/tap/runsweep`
- GitHub Action: [runsweep/action](https://github.com/runsweep/action) ([Marketplace](https://github.com/marketplace/actions/runsweep))
