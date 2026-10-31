# Organisation profile repository checks

This document applies only to **qpathformer/.github**. Project repositories
retain their own checks, contribution guides and licence notices.

The required GitHub Actions job **README links** runs on every pull request to
`main`, every push to `main`, and manual workflow runs, without path filters.
It checks local Markdown links and images in tracked Markdown files whose
names contain `README`, ignoring letter case.

The checker verifies tracked targets, exact filename case, repository
boundaries, and Markdown heading or explicit HTML anchors. It handles inline
and reference Markdown links, images, angle-bracket paths containing spaces
and HTML links. It reads files without rewriting them.

## Coverage limits

The check is offline. External websites, bare URLs, paths shown as code and
links in documents other than README files are excluded. Each job reports
the current local and parsed external link counts. Review external
destinations separately; a green check does not establish that those
websites or references work.

There is no JSON job because this profile repository has no JSON artifacts to
validate. The checker does not execute any Q-Pathformer tooling, evaluate
research claims or modify project releases.

## Run locally

From this repository's root, using Python 3.12:

```sh
python -m pip install --require-hashes -r .github/ci/requirements.txt
python -B -m unittest discover -s .github/ci/tests -v
python -B .github/ci/check_readme_links.py --root .
```

Only Git-tracked paths are checked. Stage intended new files before checking
their links locally so the inventory matches CI. Pass `--root .` explicitly
when invoking the checker from the repository root. The required check must
still pass on the pull request.

## Merge requirements and workflow permissions

The `main` rules require **README links** from GitHub Actions and an up-to-date
pull-request branch. Resolve review conversations and inspect the full diff
before merging. See the [profile contribution guide](../CONTRIBUTING.md).
If the job is renamed or removed, coordinate its workflow and ruleset changes
so pull requests are not left waiting for a check that no longer runs.

The workflow uses pinned actions, hash-pinned parser dependencies, a read-only
token, no persisted checkout credentials and no repository secrets. It uses
`pull_request`, not `pull_request_target`. GitHub may require maintainer approval
before a first-time external contributor's workflow runs.

Passing this bounded navigation check does not establish factual accuracy,
rights clearance, independent review or approval of any linked project.
