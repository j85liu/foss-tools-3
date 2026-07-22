# Team: CI/CD & Automation

Harborlight Cloud engineers run maintenance commands that remove
servers from a subsystem. Look at `maintenance-command.md` — this
one is about to remove far more than it should.

**Real parallel:** the actual 2017 incident happened because a
routine command had no safeguard checking what it was about to
remove — a typo turned a small, intended change into a much bigger
one, taking down a huge portion of the internet for hours.

## Your task
Build a GitHub Actions workflow (`.github/workflows/`) that fails the
build if the command would remove more than 10% of the total servers
in the subsystem. (Hint: this is a percentage calculation, not a text
match — a short Python step inside your workflow works better than
grep.)

## Success looks like
Your workflow fails on the current numbers (6000 of 8000 = 75%, way
over the 10% limit). Lower "Servers to remove" to a safe number (800
or fewer), push again, and it passes.

## If you get stuck
Screenshot the failing run and the error log. That's still a real
slide — explain what you tried and what you think is wrong.

## Your slides (aim for 3)
1. What the real 2017 incident got wrong, in this category
2. Your workflow — screenshot of the Actions tab (red, then green — or red, with your diagnosis)
3. One question for the class: why is checking a blast-radius percentage different from checking a placeholder string?