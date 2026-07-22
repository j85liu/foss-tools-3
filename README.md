# foss-tools-3: Harborlight Cloud

In February 2017, an engineer at a real cloud storage provider ran a
routine maintenance command intended to remove a small number of
servers. A typo caused it to remove far more than intended, taking
down a large portion of the internet for several hours. (Source: the
company's own public post-incident summary.)

Harborlight Cloud (fictional) just had the same thing happen. Look at
`ci/maintenance-command.md` — this command is about to remove far
more servers than is safe.

Your team has 5 roles: a CI Lead, a Version Control Lead, a CD Lead,
a Wrap-Up Lead, and a Presenter. Work through the four sections
together, in order — CI, then Version Control, then CD, then Wrap-Up
— each led by its own lead. The Presenter compiles everyone's
contributions into a 3-4 slide deck.

By the end, Harborlight will have gone from "one typo takes down
everything" to "destructive changes can't happen without a check —
and a safe state is confirmed automatically, in public."