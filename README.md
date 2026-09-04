# NEPHI Bingo

A Book of Mormon study game in a single HTML file. Play it here:

**https://ryanxbutcher.github.io/nephi-bingo/**

No server, no internet, no install. Open the page — or the file — in any
browser and play. Built for Primary classes, Sunday school, and family study.

## Playing across several devices

The start page asks who the device is: **caller**, **player**, or **all in
one**. The caller runs the tumbler and shows a game code; players join with
that code and see only their own card.

There is no network between them, and none is needed. Both the cards and the
draw order are pure functions of the game code, so every device in the room
derives the identical game from the same four digits. A player picks a card
number to make their card differ from everyone else's. This is why it works
in a chapel basement with no signal.

## Unlisted, not secret

This repo is public so GitHub Pages can serve it, and the page carries a
`noindex` tag to keep it out of search results. Nothing links to it. But the
URL is not a secret — treat it as unlisted rather than private.

## Where it is edited

The canonical copy lives in the private `the-butchery` repo at
`projects/nephi-bingo/nephi-bingo.html`. This repo is the published copy:
`index.html` here is that file plus the one `noindex` meta tag. Edit it
there, republish here — a deliberate step, so a work-in-progress never goes
live by accident.

(That path was `butcher-block/nephi-bingo/` until the 2026-08-22
re-architecture split that repo; corrected 2026-08-27.)

## A native iOS version is planned

Ryan intends to build NEPHI Bingo as an iOS game as well. It will live in
the `butcher-shop` repo (notes at `apps/nephi-bingo/INTENT.md`), not this
one, and it will not replace this page — the web version is what works on
any device in a room with no signal and no App Store account. Two front
ends, one game.

**The source file is the specification.** The rules, the two content tiers,
the N·E·P·H·I columns, the win patterns, and — the load-bearing part — the
seeded derivation, where the game code alone determines every card and the
whole draw order so devices agree with no network between them. A port that
reimplements the game but not that derivation is a different game. Read the
source before designing anything.

## Working on this repo

`main` is literally the live site, so a branch here is a change nobody can
see. Commit and push as each piece lands, merge any branch back into `main`
yourself, and delete it on both ends when you do. Never rewrite history that
is already on GitHub — no `--force`, no rebase or amend of pushed commits.
pi-brain pulls this repo on a timer, and a rewrite on 2026-09-03 left that
clone with no common ancestor and a finding in the morning report.
