# Section 4: Wrap-Up — Docs, Licensing & Dependency Hygiene
Led by the Wrap-Up Lead

## Docs & Community
Harborlight has no CONTRIBUTING.md and no runbook for maintenance
commands. The real 2017 incident happened during otherwise routine
work — there was no written checklist confirming the scope of the
command before it ran. What would a one-page runbook need to say to
prevent that?

## Licensing
If Harborlight wanted to open-source its safeguard tooling so other
cloud providers could adopt the same protection, it has no LICENSE
file today. Pick one license (check choosealicense.com) and explain
in one sentence why it fits a company that still sells a commercial
product on top of this code.

## Dependency Hygiene
Harborlight's dependencies aren't pinned to specific versions — every
subsystem could silently run different tooling code. One sentence:
why does this matter even if it's not today's build task?

## What to hand the Presenter
One bullet per topic above (3 total). This becomes Slide 4, if
included — otherwise fold one line into Slide 1.