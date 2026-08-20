# AGENTS.md

This file provides guidance to Claude Code, Codex, GitHub Copilot, and other AI coding agents
working in this repository.

## About This Project

`gamesystems-model` was a Swift shared-model library for game systems (ruleset/edition, name,
publisher reference, metadata). Its Swift package contents were retired when `gamesystems-api`
was rebuilt as a Go service that owns its own models directly rather than sharing a library - see
`sweetrpg/platform`'s `openspec/changes/game-systems-service`.

## Committing Code

Use [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <description>
```

## Branches and Workflow

* `develop` - integration branch, default branch, target for all PRs.
* `master` - latest released state, nothing committed directly.
* `feature/*`, `fix/*` branched from `develop`; `hotfix/*` branched from `master`.

See `CONTRIBUTING.md` for the full workflow.

## Running Checks Locally

```bash
go build -v ./...
go vet ./...
go test -v -coverprofile coverage.out ./...
```
