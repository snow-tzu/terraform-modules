# Contributing

This repository's settings, branch protection, and team access are managed
in Terraform, not in the GitHub UI. See the org's `github-user-teams-terraform`
repository, specifically `data/repos/<team>.yaml` for this repo's entry.

- To change who has access to this repo, edit the `access:` map for this
  repo, don't add collaborators via Settings.
- To change branch protection, merge policy, or security settings, edit
  this repo's `overrides:` block (loosening a control also requires an
  `exception:` block with an owner, approver, and expiry).
- Open a PR against the Terraform repo; changes apply automatically once
  merged to `main`.

Everyday code contributions (branches, PRs, reviews) work exactly as normal
in this repo - only repo/team *configuration* goes through Terraform.
