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
