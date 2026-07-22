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

## Stretch Goal (optional — only if you finish early)
Right now your check only reports pass/fail in the Actions tab. Add a
second job that automatically publishes a status page — but only
when your check passes.

1. Enable GitHub Pages: Settings → Pages → set source to "GitHub
   Actions"
2. Edit `public/index.html` to say something like
   "✅ [Your Company] passed its safety check"
3. Add a second job to your workflow that runs only after `check`
   succeeds and only on `main`, and deploys `public/` to Pages
4. Watch a real, live webpage go from not-existing to published,
   because your check passed

This is the difference between CI (test/verify) and CD (automatically
ship). Ask an instructor for the deploy job snippet if you want to
try this.