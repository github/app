# GitHub Copilot app

The GitHub Copilot app is an agent-native desktop experience for finding, running, steering, and landing software work across your GitHub repositories.

<p align="center">
  <a href="https://github.com/github/app#install">
    <img alt="Download the GitHub Copilot app" src="https://img.shields.io/badge/Download-GitHub%20Copilot%20app-0969DA?style=for-the-badge&logo=github&logoColor=white">
  </a>
</p>


https://github.com/user-attachments/assets/50f215b5-f708-444e-83f7-3303bfa97963

## The GitHub Copilot app

The GitHub Copilot app is an agent-native desktop experience for managing software work from idea to pull request. It gives you a single control center for finding the right work to pick up, starting and steering agents, reviewing progress, and landing changes across repositories without constantly switching between terminals, editors, browser tabs, and GitHub pages.

The app is built for parallel agent-driven development. Each local session runs in its own isolated git worktree, and cloud sessions let agents keep working in isolated GitHub-hosted environments that you can pick up from anywhere. That means you can have Copilot investigate bugs, implement issues, address review feedback, or explore changes side by side without branches or files colliding.

Canvases turn agent work into shared, inspectable surfaces. Instead of burying plans, terminals, browser previews, diffs, and workflow state in a chat thread, canvases give you a place to see what an agent is doing, edit or redirect the work, and verify progress in context.

But we also know as developers, much our time has always been devoted to tasks that aren't 'just' writing code. My Work brings together sessions, issues, pull requests, and repository context so you can decide what needs attention next. Automations turn repeatable prompts and workflows into scheduled or background tasks. Agent Merge helps carry pull requests through review, checks, and merge conditions so you stay focused on judgment, quality, and delivery.

## Getting started

### Prerequisites

- [Git](https://github.com/git-guides/install-git)
- A [GitHub Copilot](https://github.com/features/copilot/plans) plan — any plan works, including Copilot Free and [GitHub Copilot Student](https://github.com/education/students). No Copilot plan? You can still use the app by bringing your own key (BYOK) with your own model provider.

### Install

Download the app for your platform:

- [Windows (x64)](../../releases/latest/download/GitHub-Copilot-windows-x64-setup.exe)
- [Windows (ARM)](../../releases/latest/download/GitHub-Copilot-windows-arm64-setup.exe)
- [Mac (Apple Silicon)](../../releases/latest/download/GitHub-Copilot-darwin-arm64.dmg)
- [Mac (Intel)](../../releases/latest/download/GitHub-Copilot-darwin-x64.dmg)
- [Linux](../../releases/latest/download/GitHub-Copilot-linux-x64.AppImage)

You can also browse all builds on the [Releases](../../releases) page.

For setup and a walkthrough of your first session, see the [documentation](https://gh.io/github-app-docs).

## This repository

This repo is the public home for the GitHub Copilot app. Use it to:

- Download releases from the [Releases](../../releases) page
- File bugs and feature requests
- Join discussions
- Read release notes in [`changelog.md`](./changelog.md)

## Feedback

Report problems or feature requests for the GitHub Copilot app team in the [Issues](https://github.com/github/app/issues) tab. When filing an issue, please include:

- The app version
- Your operating system and version
- Steps to reproduce
- Expected vs. actual behavior
- Screenshots or videos
- Logs from the `/collect-debug-logs` command. Note: These logs may contain sensitive information.

For open-ended questions, please visit the [Discussions](https://github.com/github/app/discussions) tab.

### Stale issues

Open issues with no activity for 30 days receive a warning and the `stale`
label. They are automatically closed if there is no new activity for another
7 days. New activity removes that label on a subsequent daily run and resets
the inactivity timer. Issues labeled `never-stale`, `help wanted`, `on-roadmap`,
`pinned`, or `security` are exempt. Pull requests are left unchanged.
The [stale issue workflow](./.github/workflows/stale-issues.yml) runs daily at
01:30 UTC and can also be run manually. GitHub Actions must be enabled for
this automation to run.

## License

© GitHub, Inc. All rights reserved.

## Data & Telemetry

If you use the GitHub Copilot App with your GitHub Copilot account, we may collect usage data (such as code acceptance or rejections), associated conversation data, and user feedback submitted via the feedback dialog. See our [GitHub Copilot Trust Center](https://copilot.github.trust.page) for more information.
