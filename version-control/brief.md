# Section 2: Version Control & Enforcement
Led by the Version Control Lead

Right now, anyone can push straight to Harborlight's main branch — no
review, no required checks. Detection isn't the same as enforcement:
even if the CI Lead's check exists, nothing forces it to actually
block a change that removes a protected subsystem.

**Real parallel:** the real 2017 command was run directly by one
engineer, with no second person or automated check confirming the
scope of what it would remove before it ran.

## Your task
Turn on branch protection on this repo (Settings → Branches) so the
CI check is *required* before merging to main. Then draft a PR
template (`.github/PULL_REQUEST_TEMPLATE.md`) that makes a reviewer
explicitly confirm no command exceeds the 10% removal threshold.

## Success looks like
Open a test PR that raises the removal count back above the
threshold — GitHub should block the merge button. Fix it, confirm the
merge button unblocks.

## If you get stuck
A written description of the settings you'd enable is still useful to
bring to the Presenter.

## What to hand the Presenter
A screenshot of the blocked PR and, ideally, the unblocked one after
the fix. This becomes half of Slide 3 (shared with CD).