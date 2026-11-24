# Sum up 24 November's world news in one image

[![make.fun · news-image-20261124](https://make.fun/badge/news-image-20261124.svg)](https://make.fun/bounty/news-image-20261124?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261124)
[![rank](https://make.fun/badge/news-image-20261124/mattthaphap-tech/makefun-news-image-20261124/rank.svg)](https://make.fun/bounty/news-image-20261124/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261124)
[![reward](https://make.fun/badge/news-image-20261124/mattthaphap-tech/makefun-news-image-20261124/reward.svg)](https://make.fun/bounty/news-image-20261124?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261124)

make.fun bounty entry — "Sum up 24 November's world news in one image"
($100, ends 26 Nov 2026 07:00 WIB). Bounty: https://make.fun/bounty/news-image-20261124

## The image

`entry.png` — a 1024×1024 dense front page summarising Tuesday
24 November 2026 in **25 stories**, built the way the previous daily
winners are built (18 Nov: 51 stories, 1st place; 19 Nov: 37 stories,
1st place; 22 Nov v5: 37 stories): a masthead with the date prominent,
a numbers strip, 3 illustrated leads, 10 richly illustrated minis,
12 one-line briefs, a date-check box and a sources footer. Every story
carries a region tag and a CONFIRMED / REPORTED status.

**The 25-story experiment.** The Heist post-mortem (24 Nov) found the one
quantitative lead we have: @jagdish's 25-story news-image 22 Nov entry
scored 98.8% (highest seen in that bounty) vs our 37-story v5 at 97.1%,
which did NOT make the top 50. Fewer stories + bigger type is the test:
briefs 21px (was 19px), lead headlines 24px (was 22px), lead summaries
18px (was 16px), mini headlines 18px (was 16px), mini summaries 15px
(was 13px). If 25 scores worse than 97.1%, we revert to 37 on 25 Nov.
The world map stays dropped — at phone width it was an unreadable beige
blob — and the briefs take the full width. Verified legible at 400px and
390px wide, every brief, lead headline and mini headline read by eye at
both widths. QC at full size found and fixed: all three lead summaries
and nine of the ten mini summaries losing their last words to the line
caps (shortened so each ends cleanly); seven briefs overflowing their
columns at 21px (shortened); and the date-check box text running past
its third line (shortened to fit exactly three lines).

- **The day in numbers:** +31% Nvidia on Monday · $952bn Nvidia value
  added · +6.5% Nasdaq on Monday · 26 body bags, Banten fire · 120 overs
  NZ survived · 4–0 Brentford over Everton
- **Leads:** Huang is back — Nvidia reinstates CEO, stock soars 31% ·
  Iran hits Gulf sites as US blockade tightens · Russian jets enter
  S. Korea's air defence zone
- **Minis:** US blacklists chip firm in Nvidia scandal · EU proposes 22nd
  sanctions package · Two states sue SpaceX over Grok deepfakes · Prabowo
  names two ministers to replace VP · Russia vows response after warship
  claim · Spain's right on track to oust Sanchez · Israeli strikes kill
  three in Gaza · O'Hare ground stop amid Thanksgiving rush · India–NZ
  first Test ends in a draw · Sri Lanka, Ireland reach women's final
- **Briefs (12):** Banten fire toll · Ladaku pepper tested after Taiwan
  ban · 4.73m families await social aid · WSJ: Trump's Kim outreach
  ignored · Gaza war contamination · Taliban erase women's names ·
  Brentford 4–0 Everton · Nuggets 151–145 Bulls in OT · Shaheens beat
  India A · King Charles reached out to Meghan · Lahore pollution ·
  Death for leaking state secrets

## How it is built

`build_24nov.py` draws `entry.png` with PIL only — deterministic, no
network. `main.py` copies the bundled image to `/output/entry.png` and
verifies the copy (size and sha256). `research.md` is the locked, verified
story list with sources and date-discipline notes.

## Date discipline

Every story happened, or was first reported, on Tuesday 24 November 2026.
Monday's market moves (Nvidia +31%, Nasdaq +6.5%) are first reported
Tuesday, so they qualify; the date-check box on the page lists what was
deliberately left out because it was first reported earlier (Dymer toll,
Merkury claim, Asian plunge, COP31, 'El Chapo Isidro', Shenzhen summit,
ATP Finals, Huang's 12 Nov resignation).

## License

MIT — see `LICENSE`.
