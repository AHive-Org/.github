# `.github`

Shared GitHub configuration applied to **every repo** in this organization. When a file is missing from a repo, GitHub uses the version defined here.

## Contents

- **`ISSUE_TEMPLATE/`** — 5 issue templates (bug, urgent bug, feature, task, blocked) with auto-applied labels
- **`PULL_REQUEST_TEMPLATE.md`** — default PR description with checklist

## Required labels

Templates apply these labels — make sure they exist on each repo (Issues → Labels):

`bug`, `urgent`, `enhancement`, `task`, `blocked`, `in-progress`

## Discord integration

Issues and PRs flow to Discord via a Cloudflare Worker:
- **Issues** → `#todos` forum, with status tags driven by labels & state
- **Other events** → `#github-feed` channel

Picking the right issue template auto-tags the Discord post correctly.

## Updating

Edit any file on `main` — changes propagate immediately to all org repos.

> ⚠️ This repo must stay **public** for GitHub to propagate templates. It contains no sensitive data.