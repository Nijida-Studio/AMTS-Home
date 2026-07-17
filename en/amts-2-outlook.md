---
layout: nijida-topic
title: Outlook for AMTS 2
kicker: 2.0.0 Beta · Team collaboration
excerpt: AMTS 2 aims to coordinate teams, protect core data, and assign tasks and feedback to individual members.
lang: en
nav_id: projects
local_nav_id: outlook
permalink: /en/amts-2-outlook/
translations:
  de: /de/ausblick-amts-2/
  en: /en/amts-2-outlook/
  ja: /ja/amts-2-outlook/
---

AMTS 2.0.0 is in early beta design. The stable AMTS 1.x specification remains
unchanged until the new model has been described and tested sufficiently.

## Why built-in teamwork?

When many people and assistant systems continuously update the same Space,
changes to central project and Space data can overlap. AMTS 2 therefore aims to
distinguish protected, consolidated core data from distributed contributions
made by individual members.

Space and project maintainers curate the canonical core data. Members write
task progress, results, and requested opinions in their assigned contribution
areas. Maintainers can read and review those contributions and deliberately
integrate them into the core data.

## Identity and responsibility

AMTS 2 should identify members locally and map them to a stable member ID in
the shared Space. Shared and local information remain strictly separated:

- **Shared and synchronized:** member ID, display name, voluntarily published
  official name, GitHub username, roles, and Space or project membership.
- **Local only:** computer account name, local repository paths,
  device-specific identities, and references to non-public Spaces.

A Space names its maintainers. Every project also names its maintainers and
members. Only authorized people may change the protected core data in their
respective scope.

## Proposed contribution model

The exact file structure is part of the beta work. One possible model is:

```text
members/<member-id>/profile.md
governance.md
contributions/<member-id>/
projects/<Project>/governance.md
projects/<Project>/contributions/<member-id>/
```

A member's public directory contains only synchronized identity and
contributions. Tasks, progress, results, and responses to feedback requests are
stored there so several people do not need to overwrite the same working file.

`governance.md` is currently a design candidate for maintainers, memberships,
protected core data, and integration rules. Its name and exact format are not
yet normative.

## Tasks and GitHub Issues

A task belongs to one responsible member or has one explicitly designated lead.
It states its scope and the core data into which a result may later be
integrated.

GitHub Issues are planned as the first external task source. Repository, issue
number, and assignee are mapped to an AMTS member ID. The issue remains the
source of truth for its current status; the Space keeps only the AMTS-specific
assignment, results, and integration information. This avoids creating a
second, quickly outdated copy of the full issue.

## Requesting opinions and feedback

An initiator can explicitly ask selected members or roles for their opinion.
Each requested person writes a response in their own contribution area. The
initiator synthesizes the results and decides what enters the initiating work.
Feedback does not replace the initiator's responsibility or authorization to
change protected core data.

When entering a project, AMTS should therefore check whether the locally
identified member has open tasks, expected contributions, or feedback requests.

## Initialization questions

Initialization or reinitialization should ask step by step for:

1. preferred form of address and a stable member ID,
2. voluntarily public name and GitHub username,
3. local computer identity and repository paths for each device,
4. optional cross-references to other public Spaces,
5. Space maintainers and members,
6. and maintainers and members of existing or newly created projects.

Before writing, AMTS identifies the current member, reads their tasks and
requests, and checks whether the intended files belong to the member's
contribution area or to protected core data.

## Rules and technical enforcement

AMTS can define responsibility and writing rules, but a Markdown Space alone
cannot technically prevent local file access. Git-based implementations may
reinforce the rules with protected branches, required reviews, and
`CODEOWNERS`. Other storage systems may use their own access controls.

The 2.0.0 beta still needs to define which files count as protected core data,
how member IDs remain stable across Spaces, and how conflicting or abandoned
tasks can be reassigned.
