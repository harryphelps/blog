---
title: "What a Postmaster File Is"
date: 2021-09-22T11:58:16+01:00
draft: false
---
My laptop restarted over night. Logged in this morning and was faced with this message when I tried to run a test: `Stale postmaster.pid file`

Turns out the postmaster.pid file is a lock file that stops two instances of Postgres running at the same time. It becomes stale if the server crashes or is killed and has to be removed before the server will start up again.

**Solution:** remove the postmaster.pid file from `/Users/<username>/Library/Application\ Support/Postgres/var-13` and restart the Postgres server.
