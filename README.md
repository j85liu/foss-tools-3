# foss-tools-3: Harborlight Cloud

In February 2017, an engineer at a real cloud storage provider ran a
routine maintenance command intended to remove a small number of
servers from one subsystem. A typo in the command's input caused it
to remove far more servers than intended — including ones that
several core services depended on. There was no safeguard checking
the size or safety of the command before it ran. The result: a large
portion of the internet's storage-dependent services went down for
several hours. (Source: the company's own public post-incident
summary.)

Harborlight Cloud (fictional) just had the same thing happen. Look
at `ci-cd/maintenance-command.md` — this command is about to remove
far more servers than is safe, just like the real incident.
Everything else in this repo is Harborlight's tooling as it existed
that day: no CI, no required review, no license, no documented
process.

Two teams will build real fixes. A third piece — docs, licensing, and
dependency hygiene — gets covered as a group discussion, not a build.
By the end, Harborlight will have gone from "one typo takes down
everything" to "destructive changes can't happen without a check."