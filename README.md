### Dmitrii Bernatskii — DevOps / DevSecOps engineer

I run Linux infrastructure for web services: monitoring, backups with tested restores, CI/CD and web perimeter protection. Stack: Linux, nginx, Docker Compose, GitLab CI, Prometheus, Grafana.

**Some of the work** (production web services, 2024–now):

- L7 flood: a 30-second nginx microcache for the home page with session bypass, cache lock and stale responses — load average went from a 69.5 peak to 1.1 in the hour after, at ~599k requests.
- PHP session lock incident: moved the session directory with the old one kept — processes waiting on it fell from 122 to 0 within a minute.
- Restore drill: production DB backup (~15 GB, 319 tables) restored on a pre-release stand in about an hour, checked by tables, rows, pages, login and the next CI deploy.
- Backups: success and freshness checks for 10 jobs, independent S3 copies for two servers after the S3 storage was suspended.
- Monitoring: Prometheus with exporters and mtail, 13 Grafana dashboards, 25 Uptime Kuma checks that verify page content, not just HTTP 200.
- Staging deploys from GitLab CI: shell runner, `flock` against parallel runs, migrations, read-only overlay on production media.

**[runsweep](https://github.com/runsweep/runsweep)** — after a supply-chain incident, tells you which GitHub Actions runs were hit and which secrets to rotate first. npm, PyPI and compromised actions; every job gets AFFECTED, POSSIBLE, UNCHECKED or CLEAN with the log line as evidence.

- Go CLI, signed releases with build provenance (`gh attestation verify`)
- `brew install runsweep/tap/runsweep`
- GitHub Action: [runsweep/action](https://github.com/runsweep/action) ([Marketplace](https://github.com/marketplace/actions/runsweep))
