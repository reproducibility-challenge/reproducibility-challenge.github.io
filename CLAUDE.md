# CLAUDE.md

## Project Overview

This is the website for the **Machine Learning Reproducibility Challenge (MLRC)** at [reproducibility-challenge.github.io](https://reproducibility-challenge.github.io), built with [Hugo](https://gohugo.io/) using the Wowchemy Documentation theme. It is deployed via Netlify.

## About MLRC

The **Machine Learning Reproducibility Challenge** is an annual community-driven initiative promoting reproducibility in ML research. Founded in 2018 by Joelle Pineau (McGill / Mila), it invites researchers and students to independently reproduce empirical results from papers accepted at top ML conferences.

- **Publication venue:** [Transactions on Machine Learning Research (TMLR)](https://jmlr.org/tmlr/) (since 2023; previously ReScience C)
- **Permanent home:** [reproml.org](https://reproml.org)
- **Social:** [@repro_challenge](https://x.com/repro_challenge) on Twitter/X, [@reproml.org](https://bsky.app/profile/reproml.org) on BlueSky

### Edition History

| Edition | Year | Venue / Notes |
|---------|------|---------------|
| 1st | 2018 | ICLR submissions |
| 2nd | 2019 | ICLR submissions |
| 3rd | 2019 | NeurIPS accepted papers |
| 4th | 2020 | 7 major venues (NeurIPS, ICML, ICLR, CVPR, ECCV, ACL, EMNLP) via Papers with Code |
| 5th | 2021 | 9 conferences |
| 6th | 2022 | 12 conferences + 3 journals |
| 7th | 2023 | Transitioned to TMLR; launched reproml.org |
| 8th | 2025 | First in-person conference at Princeton University (Aug 21, 2025) |
| 9th | 2026 | Official track at NeurIPS 2026, Sydney |

### MLRC 2025 (Most Recent Edition)

- **Date:** August 21, 2025
- **Venue:** Friend Center 101, Princeton University, NJ, USA
- **Format:** Single-track in-person conference (keynotes, orals, posters)
- **Sponsors:** Meta AI, OpenAI
- **General Chair:** Koustuv Sinha (Meta)
- **Program Chairs:** Jessica Forde, Adina Williams, Angela Fan, Mike Rabbat, Naila Murray
- **Senior Program Chair:** Joelle Pineau (Cohere / Mila / McGill)

### MLRC 2026 (Upcoming)

- MLRC 2026 is an **official track at NeurIPS 2026** — the first time MLRC is embedded in a major ML conference as a dedicated track.
- **Conference dates:** December 6–13, 2026, Sydney (venue only Sydney for MLRC track)
- **Submission eligibility:** Papers accepted to TMLR submitted between June 21, 2025 and June 4, 2026
- **Intent to submit deadline:** June 4, 2026 (23:59 AOE)
- **TMLR decision deadline:** September 30, 2026 (AOE)
- Papers are accepted via three paths: expression of interest, self-nomination, or Area Chair nomination

## Repo Structure

```
content/          # Hugo content pages (Markdown)
  _index.md       # Homepage
  blog/           # Announcement blog posts
  board/          # Organizer/board info
  call_for_papers/ # CFP pages
  challenge_resources/
  code_of_conduct/
  code_of_ethics/
  faq/
  proceedings/    # Accepted papers listings
config/_default/  # Hugo configuration (YAML)
assets/           # CSS, JS, images
static/           # Static files served as-is
netlify.toml      # Netlify deploy config
go.mod            # Hugo module dependencies
```

## Development

- Build: `hugo server` (requires Hugo with Go modules)
- Deploy: Auto-deploy on push via Netlify
- Theme: Wowchemy Documentation theme (loaded as Hugo module)
