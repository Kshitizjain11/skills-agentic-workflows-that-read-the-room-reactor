---
name: update-github-info
description: Draft website updates for Mona's GitHub Info site from official GitHub sources.
on:
  workflow_dispatch:
  schedule:
    - cron: '17 9 * * *'
safe-outputs:
  create-pull-request:
    title-prefix: "[mona] "
    draft: true
    fallback-as-issue: false
network:
  allowed:
    - github.com
    - github.blog
tools:
  edit:
  web-fetch:
---

# Update Mona's GitHub Info website

Read notes/mona-notes.md before making changes.

Use these sources:
- notes/mona-notes.md
- GitHub Blog: https://github.blog/latest/
- GitHub Changelog: https://github.blog/changelog/

Update site/content/github-info.md with concise, practical updates for readers.
Mention the source whenever an update comes from the GitHub Blog or GitHub Changelog.

Use safe-outputs with create-pull-request so you can propose changes without writing directly to main.

Open a pull request for Mona to review. Use a pull request title that mentions Mona or GitHub Info.
