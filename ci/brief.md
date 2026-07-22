# Section 1: CI (Continuous Integration)
Led by the CI Lead

Harborlight Cloud engineers run maintenance commands that remove
servers from a subsystem. Look at `maintenance-command.md` — this one
is about to remove far more than it should.

**Real parallel:** the actual 2017 incident happened because a
routine command had no safeguard checking what it was about to
remove — a typo turned a small, intended change into a much bigger
one, taking down a large portion of the internet for hours.

## Your task
Build a workflow that fails if the command would remove more than 10%
of the total servers in the subsystem. (Hint: this is a percentage
calculation — a short Python step works better than grep.)

## Success looks like
Fails on the current numbers (6000 of 8000 = 75%). Lower "Servers to
remove" to 800 or fewer, push again, it passes.

## If you get stuck
Screenshot the failing run and error log — still useful to bring to
the Presenter.

## What to hand the Presenter
2-3 bullets on what you built and why, plus a screenshot of the
Actions tab (red, then green — or red, with your diagnosis). This
becomes Slide 2.