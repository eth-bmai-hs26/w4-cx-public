# CLAUDE.md : w4-cx-public, the PUBLIC weekend-4 notebooks (CAS BMAI HS26)

`https://github.com/eth-bmai-hs26/w4-cx-public` (PUBLIC, `main`). Everything committed here, this file
included, is world-readable: keep internal notes, history and decisions OUT of it. They live in the PRIVATE
`w4-cx-private/CLAUDE.md` (clone: `git_bmai/2026hs/w4-cx-private`), which also holds the masters.

## What it holds

github.com/eth-bmai-hs26/w4-cx-public, PUBLIC, what the room opens for weekend 4: the manifold games and, since 2026-10-21, a byte-for-byte copy of the pufferfish notebook; since 2026-10-22 also of the apples-and-oranges notebook and of the happy-and-sad diffusion exercise and the two sunrise CNN notebooks, and, on Carlos's word of the same day, of every weekend-4 SOLUTION, listed in its SOLUTIONS.md; since 2026-10-23 also the adversarial cats-and-dogs exercise and solution, the exercise linked on the site, and Kangsheng Qi's CIFAR-10 exercise without its solution

## Rules

- Every notebook here is a byte-for-byte copy of its master in `w4-cx-private`; after changing a master,
  recopy it here. The room opens the exercises in Colab from this repository.
- Standing rule of Carlos (2026-10-22): every exercise AND its solution go here, as soon as they exist.
  `SOLUTIONS.md` lists every notebook with its solution as Colab addresses: whoever adds a notebook or a
  solution adds it to that list. The public `README.md` describes the exercises.
- The course site (BMAI-PAGE) links exercises and their worked examples, never a solution.
- Two teaching assistants' exercises (Stable Diffusion, adversarial attacks on CIFAR-10) are public
  WITHOUT their solutions. Ask Carlos before publishing any teaching assistant's solution.

## Maintenance contract

- This file is the working memory for this repository. After any major change here, meaning a new or
  changed exercise, deck, page or script, a renamed or moved directory, a changed build or run procedure,
  a changed data format, or a change in who owns the work, UPDATE THIS FILE IN THE SAME COMMIT. A
  CLAUDE.md that describes a layout the repository no longer has is worse than none.
- History, decisions, gotchas and publication records (commits, sha256 sums, "on Carlos's word")
  stay in THIS file. The root `git_bmai/CLAUDE.md` is an index of about 8 KB: it gets at most one
  line per change, and only when the map of repositories changes.
- Every subdirectory that holds work of its own carries its own CLAUDE.md, and that file must itself
  carry this same maintenance contract, including this propagation rule. When you create a
  subdirectory, create its CLAUDE.md at the same time.
- Keep it concrete: real file names, real identifiers, real commands. Record the gotchas that cost
  someone an hour. Do not restate what the code already says plainly.
