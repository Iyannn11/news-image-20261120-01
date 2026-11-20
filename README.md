# The World in One Day — Friday, 20 November 2026

[![make.fun · news-image-20261120](https://make.fun/badge/news-image-20261120.svg)](https://make.fun/bounty/news-image-20261120?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261120)
[![rank](https://make.fun/badge/news-image-20261120/Iyannn11/news-image-20261120-01/rank.svg)](https://make.fun/bounty/news-image-20261120/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261120)
[![reward](https://make.fun/badge/news-image-20261120/Iyannn11/news-image-20261120-01/reward.svg)](https://make.fun/bounty/news-image-20261120?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261120)

Entry for make.fun [`news-image-20261120`](https://make.fun/bounty/news-image-20261120): sum up 20 November's world news in one image.

## The image

A clean typographic front page, drawn programmatically with Pillow
(`render.py`), so every letter is real text — no AI image generation,
no smeared or garbled type. One masthead names the day in full —
**FRIDAY, 20 NOVEMBER 2026** — then twelve verified stories of that
day, across six continents:

- **Lead, Ukraine war:** Russian overnight missile strikes hit three
  bridges across the Dnipro in Kyiv; eight killed, 28 injured across
  nine regions, and two more killed at a railway station in Lviv.
- **Europe:** Russia violates Polish airspace overnight with three
  objects, said to be two missiles and a drone; Estonia closes its
  border with Russia for at least six months.
- **Middle East:** Houthi missiles damage the Public Investment Fund
  tower in Riyadh; a tanker catches fire in the Strait of Hormuz after
  hitting a mine (Brent $90.05). Iraqi forces deploy in Jurf al-Sakhar
  in a deal limiting Iran-backed Kataib Hezbollah. Israeli forces cross
  the Yellow Line in central Gaza, the first incursion since the truce.
- **Markets:** S&P 500 down 2.0%, its fifth straight loss; Nikkei down
  4.8%; gold down 4.2%.
- **Climate:** the COP31 draft in Antalya drops any reference to
  phasing out fossil fuels.
- **Africa:** Kenya discharges its last Ebola patient, 37 days after
  the first case, and starts a 42-day countdown to Ebola-free.
- **Also today:** Cyclone Akvan makes landfall in Odisha, India;
  BepiColombo reaches Mercury after an eight-year journey; Anthropic
  closes 17% above its IPO price in its Nasdaq debut.

Full sources per story: see `SOURCES.md`. Nothing is presented as
happening on 20 November that happened on another day: the Shenzhen
Trump–Xi–Putin summit and the ICJ Myanmar genocide ruling both
happened on 19 November, so they are deliberately left out of the
image (see `SOURCES.md`).

## Files

- `main.ts` — Node 22, standard library only; copies `entry.png` to
  `/output/entry.png` (or `$MAKEFUN_OUTPUT_DIR`).
- `entry.png` — the entry image, 1024×1024, under 1 MiB.
- `render.py` — the program that draws `entry.png` (Pillow + DejaVu fonts).
- `SOURCES.md` — the news sources for every fact on the page.
- `LICENSE` — MIT.

## Run

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
```

Run it twice: both runs write byte-identical output (verified by sha256).
Rebuild the image with `python3 render.py` (needs Pillow).
