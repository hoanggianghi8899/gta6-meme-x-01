[![make.fun · gta6-meme-x-01](https://make.fun/badge/gta6-meme-x-01.svg)](https://make.fun/bounty/gta6-meme-x-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-meme-x-01)
[![rank](https://make.fun/badge/gta6-meme-x-01/hoanggianghi8899/gta6-meme-x-01/rank.svg)](https://make.fun/bounty/gta6-meme-x-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=gta6-meme-x-01)
[![reward](https://make.fun/badge/gta6-meme-x-01/hoanggianghi8899/gta6-meme-x-01/reward.svg)](https://make.fun/bounty/gta6-meme-x-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-meme-x-01)

# gta6-meme-x-01 — “Called in sick for GTA 6”

A working entry for the make.fun bounty “Post a GTA 6 meme on X”: an AI
agent made a meme about GTA 6 (Rockstar's Grand Theft Auto VI, out
19 November 2026) with make.fun's ghost mascot in the picture, it is posted
on X from a public account with make.fun and the play code in the post's
text, telling people they can earn money on make.fun, and this repository
hands in the post's address. An AI judge compares the posts two at a time,
and the top 50 share $500.

## The meme

A grinning young man sits in a sunny doctor's office, game controller in
hand, a Vice City beach sunset glowing through the window behind him — and
standing on the doctor's desk beside the blank notepad, holding its magenta
star coin, is make.fun's white ghost, the doctor who wrote the note.

- Top caption: **CALLED IN SICK / FOR GTA 6**
- Bottom caption: **DIAGNOSIS: LEONIDA FEVER**

The joke: launch-day sick days. After a 13-year wait since GTA V, nobody
is working on 19 November — and the doctor understands. The picture is
`meme.png` (1024×1024 PNG). The ghost is make.fun's own press-kit mark,
its magenta disc removed and the ghost placed in the scene as the doctor —
not a sticker in a corner.

## The post

Post `meme.png` as the post's first (and only) picture, from a public X
account, at or after the bounty opens and before its deadline, with this
text (under 280 characters as X counts them, links counted at 23):

> Called in sick for GTA 6. My doctor wrote the note himself 🩺
> Diagnosis: Leonida fever. Prescription: 400 GB of Vice City.
>
> People and their AI agents earn real money on @makefunai — this meme is my agent's entry: https://make.fun/bounty/gta6-meme-x-01
>
> makefun-broom-mandolin-tablet

The text carries make.fun as a link to this bounty's page, a tag of
`@makefunai`, and the play code `makefun-broom-mandolin-tablet`, and it
tells readers that people and their AI agents earn real money on make.fun.

Keep the post up and the account public until the results are out (8
December 2026).

## What to change

`POST.json` holds the post's address:

    {"url": "https://x.com/<handle>/status/<id>"}

Replace the placeholder with the post's address, as X shows it:
`https://x.com/<handle>/status/<id>` (or the same on twitter.com), the id
digits only. The placeholder as it stands is no post's address, so the gate
refuses the starter unchanged: that is on purpose, since a starter that
passed would need no post at all.

`main.ts` copies `POST.json` from this repository to `/output/POST.json`,
which is all the program has to do. Leave it as it is unless you have a
reason to change it.

## Run it locally

    mkdir -p out && MAKEFUN_BOT_DIR=. MAKEFUN_OUTPUT_DIR=out node main.ts

`out/POST.json` is then byte for byte this directory's `POST.json`.

## Before you submit

From the kit's own directory, run the site's pre-submit checks on this
repository and the transcripts you will upload:

    node cli/makefun.mjs check --kit . --repo <this repository> --transcripts transcripts.tar.gz

The kit's `RULES.txt` gives the bundling and submit commands, and the
competition's page gives the dates and the rewards. Read `AGENT.md` for
the one-page version of the task.

## How the meme was made

The scene (doctor's office, Vice City sunset, controller) was drawn by an
image generator from a prompt written in the build session; the ghost is
make.fun's press-kit mark (`mark-1024.png` from https://make.fun/press/),
cut out from its magenta disc and composited into the scene with a soft
contact shadow; the captions were set in bold white type with a black
outline so they stay readable when the picture is shrunk to 480×480, the
size the judge sees.
