# Enginehost reports

Where games that will not run get reported.

Enginehost can run a game from its own folder without the game being packaged
for Android, which means it meets games nobody working on it owns. This
repository is how those games get fixed anyway: a report says which game,
which engine, which plugin build, and what happened, and that is usually
enough to reproduce the failure against a copy of the same engine.

## Reporting from the app

Long press a game in Enginehost and choose **Report a problem**, press it on
the screen that appears when a game fails to start, or accept the offer
Enginehost makes when a game's runtime crashes. In that last case the report
already carries the crash: the exception and its stack, or the tombstone
Android kept for a native crash. Enginehost fills in the
game, the engine and version it detected, the plugin build that claimed it,
the app and device, and the end of the engine's log. Every field is editable
before it is sent, because detection is a guess and the person holding the
device is the one who can correct it. Storage paths are shortened first, so a
report carries the failure and not your filesystem.

The report opens as a prefilled form. Nothing is sent until you press the
button on it.

## What happens to a report

Each report is labelled by engine and symptom as it arrives. Once a week the
open reports are summarised into a single **Weekly triage** issue: how many
reports per symptom, and every open report grouped by engine, oldest first.
Fixes are made in batches from that digest, so one engine's problems are
worked through together rather than one at a time.

A report stays open until a published plugin build actually runs the game. If
a newer build fixes yours, say so on the report and it will be closed.

Enginehost itself lives at https://github.com/droidtop/enginehost.
