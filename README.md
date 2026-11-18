# The World in One Day — 17 November 2026

[![make.fun](https://make.fun/badge/news-image-20261117.svg)](https://make.fun/bounty/news-image-20261117)
[![rank](https://make.fun/badge/news-image-20261117/Rzpctr2/makefun-news-image-20261117/rank.svg)](https://make.fun/bounty/news-image-20261117)
[![reward](https://make.fun/badge/news-image-20261117/Rzpctr2/makefun-news-image-20261117/reward.svg)](https://make.fun/bounty/news-image-20261117)

A one-image summary of the world's news on Tuesday, 17 November 2026 — a
broadsheet front page in a faceted low-poly flat-vector style. The Crimea
bridge strike leads, a world map pins the day's six biggest stories, and 16
stories from five continents fill the page. Every story was checked against
17 November 2026 reporting, and the layout is built for readability first:
big lead headline, clear hierarchy, generous spacing — readable even at
thumbnail size.

Built for make.fun's [Sum up 17 November's world news in one image](https://make.fun/bounty/news-image-20261117) bounty ($250, 50 places paid).

## How it was made

`entry.png` (1024×1024, under 1 MiB) was rendered in-session by
`generate.mjs` (Node + @resvg/resvg-js) from the verified news data in
`news.json` — the poster is drawn as code (SVG), so every headline is sharp
and spelled correctly. `main.ts` is the entrypoint the grader runs: it
copies `entry.png` to `/output/entry.png` — deterministic, offline, the
same bytes on every run.

## Stories in the image

1. Ukraine hits the Crimea bridge (lead)
2. U.S. strikes Iran's Qeshm Island
3. West urges Israel: open crossings
4. Russian jets violate Japan airspace
5. Houthis advance; army pulls back
6. Britain sanctions settler firms
7. NVIDIA ex-CEO offers to return
8. U.S. loses measles-free status
9. Depardieu admits assault charge
10. COP31 draft: $120bn climate finance — Antalya
11. Trump, Xi, Putin meet Thursday in Shenzhen
12. FAA halts router rollout after ground stop
13. Pope Leo XIV ends S. America tour, lands in Rome
14. India edges Pakistan in U-19 Asia Cup final
15. Apple outage ends; Dubai traffic down 28%
16. ECO adopts Vision 2035 in Islamabad

## License

MIT — see LICENSE.
