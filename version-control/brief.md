# Team: Version Control & Enforcement

Right now, anyone can push straight to Harborlight's main branch — no
review, no required checks. Detection isn't the same as enforcement:
even if the CI/CD team's check exists, nothing forces it to actually
block a change that removes a protected subsystem.

**Real parallel:** the real 2017 command was run directly by one
engineer, with no second person or automated check confirming the
scope of what it would remove before it ran.

## Your task
Turn on branch protection on this repo (Settings → Branches) so the
CI/CD team's check is *required* before merging to main. Then draft a
PR template (`.github/PULL_REQUEST_TEMPLATE.md`) that makes a
reviewer explicitly confirm no protected subsystem is being removed
or downgraded.

## Success looks like
Try opening a test PR with a change that fails the CI/CD check —
GitHub should block the merge button. Screenshot that blocked state.

## If you get stuck
A written description of the exact settings you'd enable, even if you
couldn't apply them, is still a real slide.

## Your slides (aim for 3)
1. What "no safeguard on a destructive command" means, concretely
2. Screenshot: a bad PR blocked from merging
3. One question for the class: what's the tradeoff of requiring review — speed vs. safety, especially for routine maintenance work?