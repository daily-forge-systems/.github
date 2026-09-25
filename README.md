# .github

The organisation repository of `daily-forge-systems`. It holds the public profile page of the
organisation and the defaults for issues and pull requests that GitHub applies across its
repositories. It is the only public repository here, and it has to stay public for both to work.
Every product and package repository stays private.

## What lives here

| Path | Purpose | Reach |
| --- | --- | --- |
| `profile/README.md` | The page shown on [github.com/daily-forge-systems](https://github.com/daily-forge-systems). It introduces Quorvyn, its applications and the ways to get in touch. | Organisation profile |
| `.github/ISSUE_TEMPLATE/` | The four issue forms Fehler, Feature / User Story, Technische Aufgabe and Spike / Untersuchung. `config.yml` disables blank issues and sends security reports and usage questions to e-mail instead. | Organisation default |
| `.github/pull_request_template.md` | The default pull request description. | Organisation default |
| `.github/CODEOWNERS` | Code owner for this repository. | This repository |
| `.github/dependabot.yml` | Monthly update pull requests for the GitHub Actions used here, which are pinned by commit SHA. | This repository |
| `.github/workflows/security-scan.yml` | gitleaks for committed secrets and semgrep for static analysis, weekly on Mondays, on every pull request and on demand. | This repository |

The issue forms and the pull request template are written in German.

## How the defaults reach other repositories

GitHub uses a community health file from this repository for any repository in the organisation
that has no copy of that file of its own, whether that repository is public or private. Every
other repository carries its own issue forms and pull request template today, so the defaults
here are a fallback for a new repository rather than the forms in daily use.

`CODEOWNERS`, `dependabot.yml` and workflows are not among the files GitHub inherits, so they
apply to this repository alone. Every other repository has its own copies of all three, including
the same security scan. There is no `SECURITY.md` here. Every other repository ships its own, and
the public policy lives at [quorvyn.de/sicherheit](https://quorvyn.de/sicherheit/).

## How a change goes live

Work happens on `develop`, which is also the default branch of this repository. GitHub renders the
profile page and reads the defaults from the default branch, so a push to `develop` is visible at
once and needs the same explicit approval as any other push. `main` receives releases through a
pull request from `develop`, following `docs/workflows/release.md` in the workspace repository.
Commits follow Conventional Commits.

Outside contributions are not expected, because there is nothing here to build or run. Questions
about Quorvyn go to [contact@quorvyn.de](mailto:contact@quorvyn.de), and security reports go
confidentially to [security@quorvyn.de](mailto:security@quorvyn.de) rather than into an issue.
