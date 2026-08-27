# nephi-bingo

The **published copy** of NEPHI Bingo — one self-contained `index.html`,
served by GitHub Pages at https://ryanxbutcher.github.io/nephi-bingo/.
Public so Pages can serve it; `noindex` keeps it out of search.

## Do not develop here

**The source lives in the-butchery `projects/nephi-bingo/`.** This repo is a
mirror. A fix made here and not made there is a fix that the next publish
silently reverts — so change the source, rebuild, and republish the page.
If you are here to change how the game works, you are in the wrong repo; say
so and move.

## An iOS version is intended (2026-08-27)

Ryan intends to make NEPHI Bingo a **native iOS game**, not just a web page.
That is a stated intention, not a schedule — nothing is built and nothing is
sequenced yet. It is written down here because this repo is the first place
anyone looks when they think about this game, and an intention nobody
recorded is an intention the next session re-invents from scratch.

Three things follow from it, and they matter more than the plan:

- **The iOS app does not get built here, or in the-butchery.** Apps and
  games people install belong in **butcher-shop**
  (`~/repos/butcher-shop`, https://github.com/ryanxbutcher/butcher-shop),
  which is the estate's storefront repo. Its notes on this game live at
  `apps/nephi-bingo/INTENT.md`. Butcher's Hot Tip goes through the iOS
  pipeline first, on purpose — signing, provisioning and review are the
  expensive unknowns, and they should be paid for once on the smaller app.
- **The web version is not a prototype to be replaced.** It works, it is
  live, and it is the version that runs in a chapel basement on somebody
  else's Android phone with no App Store account. It keeps being maintained
  after an iOS app exists. Two front ends, one game.
- **`nephi-bingo.html` is the specification.** The rules, the two content
  tiers, the N·E·P·H·I columns, the win patterns, and — the load-bearing
  part — the **seeded-derivation multiplayer**, where the game code alone
  determines every card and the whole draw order so devices agree with no
  network between them. An iOS port that reimplements the game but not that
  derivation is a different game. Read the source before designing the app.

## Leaving `main` good

Ryan is the sole contributor. There is no reviewer and no PR queue.
**`main` is where work lives; a branch is a temporary container, never a
destination** — and here `main` is literally the live site, so a branch is a
change nobody can see.

- Commit and push as each piece of work lands, not once at the finish. A
  session can be closed mid-sentence, and unpushed work dies with it.
- **If the harness put you on a branch, you own the merge.** Web, iOS,
  Remote Control and cloud sessions open on `claude/<slug>`. Finishing
  means: merge `origin/main` in, push the branch, merge the branch into
  `main`, push `main`, then delete the branch on both ends
  (`git push origin --delete <branch>`). A merged branch left on GitHub is
  litter the next session cannot tell from unfinished work.
- **Never hand Ryan a merge.** A close-out that says "ready to merge" is an
  unfinished session.
- **Prove it; do not claim it.** `git status --porcelain` empty and
  `git log --oneline origin/main..HEAD` empty before you say it is done.
  Report what they printed.

## Where this sits

pi-brain's roster (`agents/the-overseer/config/repositories.json`) lists this
repo as a read-only mirror. The estate map lives in pi-brain's `CLAUDE.md`.
