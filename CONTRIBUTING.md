# Contributing to the Q-Pathformer organisation profile

This guide applies to **qpathformer/.github**, which hosts the organisation
profile and its maintenance tooling. It does not set contribution terms or
merge requirements for every Q-Pathformer project.

GitHub may display this file as default guidance for another organisation
repository. For project changes, follow that repository's own contribution
guide, checks and applicable licence notices:

- [Dataset Lifecycle contribution guide](https://github.com/qpathformer/qpath-dataset-lifecycle/blob/main/CONTRIBUTING.md)
- [Enterprise v1.0 contribution guide](https://github.com/qpathformer/qpathformer-enterprise-v1.0-release/blob/main/CONTRIBUTING.md)
- [Enterprise v2.0 Standards Edition contribution guide](https://github.com/qpathformer/qpathformer-enterprise-v2.0-standards-release/blob/main/CONTRIBUTING.md)

## Profile change workflow

1. **Create a focused branch from current `main`.** Contributors without write
   access can propose changes from a fork, subject to the applicable terms.
2. **Prepare a narrow change.** Check factual claims, project names, versions
   and attribution. Link to project material instead of copying papers,
   datasets, execution artifacts or licence text into the profile repository.
3. **Review links and push the branch.** Follow the
   [profile repository checks](https://github.com/qpathformer/.github/blob/main/.github/CHECKS.md).
   Open external links manually; the automated check is offline.
4. **Open a draft pull request to `main`.** Explain the change, its sources and
   validation. Identify any third-party or AI-assisted material so its
   provenance and accuracy can be reviewed.
5. **Complete review.** Mark the pull request ready, inspect the full diff and
   resolve conversations. Update the branch if `main` advances, then wait for
   **README links** to pass again.
6. **Merge deliberately.** A maintainer merges the reviewed change. Squash
   merging is suitable for a focused update. Remove the finished working branch
   if no longer needed and update local `main`.

## Merge rules and scope

Changes to this repository's `main` require a pull request, the exact GitHub
Actions check **README links**, an up-to-date branch and resolved review
conversations. No bypass actors are configured; force pushes and deletion of
`main` are blocked.

The single-maintainer workflow requires **zero approving reviews**, allowing
the maintainer to merge their own pull request once the other conditions are
met. This preserves a visible proposal and review record without representing
independent approval. Human review remains part of the workflow.

There is no required JSON check or project-release workflow in this profile
repository. Updating the organisation profile does not alter a project's
published tags, release assets, evidence, licence or operational permissions.

## Attribution and licences

Submit only material you have permission to contribute. Preserve attribution,
identify sources and respect project-specific and third-party notices. This
guide introduces no repository-wide licence or additional contribution grant.

The helpers under `.github/ci/` carry a scoped
[MIT notice](https://github.com/qpathformer/.github/blob/main/.github/ci/LICENSE)
retained from the Access PoD maintenance helpers from which they were adapted.
It applies to those helpers, not to the organisation profile or linked projects.
Do not infer a project's reuse or production rights from its appearance here.
