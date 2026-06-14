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
    - awesome-copilot.github.com
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
- Awesome Copilot workflows: https://awesome-copilot.github.com/workflows/

Update site/content/github-info.md with concise, practical updates for readers.
Mention the source whenever an update comes from the GitHub Blog or GitHub Changelog.

Use safe-outputs with create-pull-request to propose changes without writing directly to main.

Create a pull request with a title that mentions "Mona" or "GitHub Info" to help with review and tracking.
Open the pull request for Mona to review using the create-pull-request safe-output.
