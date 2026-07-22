# Team: CI/CD & Automation

Harborlight Cloud's 8 subsystems should all be marked PROTECTED,
meaning destructive commands can't run against them without an
explicit override. One isn't — check `configs/subsystem-1.md` through
`configs/subsystem-8.md`.

**Real parallel:** the actual 2017 incident happened because a
routine command had no safeguard checking what it was about to remove
— a typo turned a small, intended change into a much bigger one.

## Your task
Build a GitHub Actions workflow (`.github/workflows/`) that fails the
build if any subsystem's config isn't marked PROTECTED.

## Success looks like
Your workflow fails on the current repo state (subsystem-8 is the
outlier). Fix it, push again, it passes.

## If you get stuck
Screenshot the failing run and the error log. That's still a real
slide — explain what you tried and what you think is wrong.

## Your slides (aim for 3)
1. What the real 2017 incident got wrong, in this category
2. Your workflow — screenshot of the Actions tab (red, then green — or red, with your diagnosis)
3. One question for the class: why didn't a human catch this instead?