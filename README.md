# COMP3104 Group 28 Assignment

Collaborative Git and GitHub assignment demonstrating individual branches,
meaningful commits, pull requests, and continuous integration.

## Group Members

| Member | Student ID | Role | GitHub |
|---|---|---|---|
| Jocelyn Brown | 101597391 | Group Lead | [jocelynbrown96](https://github.com/jocelynbrown96) |
| John | 101577733 | Member and repository owner | [jkenny264](https://github.com/jkenny264) |
| Mackenzie | 101597352 | Member | [mcknz-dev](https://github.com/mcknz-dev) |
| Derek Page | 101590623 | Member | [derekpage](https://github.com/derekpage) |

## Project Overview

This repository contains our COMP3104 DevOps group assignment.
Each member contributes three text files covering George Brown,
the DevOps course, and the role of DevOps in the software development
lifecycle.

The project demonstrates how contributors develop changes locally,
maintain individual branches, review proposed changes through pull
requests, and integrate their work into a shared main branch.

## Repository Contents

Each member's files are stored directly in the repository root:

| Filename pattern | Content |
|---|---|
| `STUDENTID_gb.txt` | George Brown and academic context |
| `STUDENTID_devops.txt` | COMP3104 DevOps concepts and practices |
| `STUDENTID_sdlc.txt` | DevOps in the software development lifecycle |

Shared project files:

- `README.md` — team information and collaboration instructions.
- `.github/workflows/ci.yml` — GitHub Actions workflow.
- `.github/PULL_REQUEST_TEMPLATE.md` — pull request description and checklist.

## Local Setup

Requirements: Git and access to the shared GitHub repository.
No application dependencies are required for this documentation project.

```bash
git clone https://github.com/jkenny264/COMP3104_Group28_Assignment.git
cd COMP3104_Group28_Assignment
git fetch origin
```

To create a new individual branch:

```bash
git switch -c STUDENTID-Name
git push -u origin STUDENTID-Name
```

If your branch already exists remotely, switch to that existing branch:

```bash
git switch --track origin/STUDENTID-Name
```

Replace `STUDENTID-Name` with your assigned branch name.

## Branching Strategy

| Member | Individual branch |
|---|---|
| Jocelyn | `101597391-Jocelyn` |
| John | `101577733-John` |
| Mackenzie | `101597352-Mackenzie` |
| Derek | `101590623-Derek` |

Each contributor makes changes and commits on their local machine.
Changes are pushed to the contributor's branch and proposed for
integration into `main` through a pull request.

Before merging, contributors review the changes and workflow results.
Any merge conflicts must be resolved by reviewing the affected content
and preserving the intended contributions.

## Keeping Local Work Updated

With local work committed and the working tree clean, update your
individual branch from the shared main branch:

```bash
git fetch origin
git merge origin/main
git push
```

After your pull request is merged, update your local main branch:

```bash
git switch main
git pull --ff-only origin main
```

Use `git status` to check the current branch and working tree.
Commit messages should describe the purpose of each change.

## Continuous Integration

[View GitHub Actions runs](https://github.com/jkenny264/COMP3104_Group28_Assignment/actions)

The workflow is defined in `.github/workflows/ci.yml`.

- Workflow name: `CI`
- Trigger: pushes to the repository
- Runner: `ubuntu-latest`
- Checkout action: `actions/checkout@v4`
- Steps: print execution details and check out the repository

This workflow demonstrates automated execution and records its outcome
in GitHub Actions. It does not currently run application tests,
build an application, or deploy a service.

## Pull Requests

Use the provided pull request template to explain the changes and
record the checks performed. Mark checklist items only when applicable
and completed; explain items that do not apply to documentation changes.

Pull requests provide a place to review contributions and resolve
integration issues before merging into `main`.

## Submission Evidence

Each member supplies a separate PDF or DOCX containing the public
repository link and screenshots showing:

- Local repository setup.
- Git commit history.
- Branch structure.
- CI pipeline status.

The group lead assembles the individual documents and submits them
through D2L.