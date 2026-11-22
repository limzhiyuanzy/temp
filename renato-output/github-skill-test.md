# Renato GitHub Integration Workflow

Renato uses the existing restricted GitHub client and bridge to publish explicitly approved changes to `limzhiyuanzy/temp`.

1. Confirm the requested repository, task and approved file content.
2. Inspect the relevant source and choose a descriptive `renato/` feature branch.
3. Validate each file: UTF-8 text, no more than 64 KB, and a remote path below `renato-output/`. Check for secrets and unapproved private data.
4. Create and register the branch through the existing client, then independently verify it.
5. Commit only the approved file through the client and verify its remote contents and commit.
6. Open a draft pull request targeting `main`, then independently verify its head, base, draft status and changed files.
7. Return the verified PR URL and a concise summary. Report any uncertainty or verification blocker honestly.

All GitHub writes use `/workspace/projects/renato-github-client.py`. Public GitHub API GET requests provide independent read-only verification without accessing credentials.

The workflow does not push directly to `main` or `master`, merge pull requests, delete branches, modify other repositories, change infrastructure or bypass bridge restrictions. Unsupported operations stop with an explanation.

This document is the single approved file for the live `renato-github` skill verification.
