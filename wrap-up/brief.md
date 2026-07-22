# Wrap-Up: Docs, Licensing & Dependency Hygiene

These three didn't get their own build task, but they're still real
gaps at Harborlight Cloud — cover them as a short group discussion,
not a build.

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
subsystem could silently run different tooling code. This is a
smaller version of the same root problem as the CI/CD gap: nothing
confirms what's actually protected before a command runs. One
sentence: why does this matter even if it's not today's build task?

## Your slide (just 1)
One slide, 3 bullets — one per section above. No artifact required.
This is a discussion slide, not a demo.