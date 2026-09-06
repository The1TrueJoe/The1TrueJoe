# Joseph Telaak

Computer engineer. CEO of [Parkeze](https://parkeze.com), where we build ultra-low-power
IoT parking sensors and the cloud that reads them. I work from PCB design and bare-metal
firmware up through distributed backend systems, and most of what I put here is somewhere
on that range.

**[telaak.dev](https://telaak.dev)** · [Résumé (PDF)](https://telaak.dev/The1TrueJoe/resume.pdf) · [LinkedIn](https://www.linkedin.com/in/jtelaak/)

## What I'm working on

- **[openHC](https://github.com/The1TrueJoe/openHC)** — open, kernel-up firmware for
  Control4 controllers. Modern Linux built from source on hardware the vendor shipped
  locked; four boards proven across three SoC families.
  [Docs and hardware research →](https://telaak.dev/openHC/)
- **[sgx545-ce](https://github.com/The1TrueJoe/sgx545-ce)** — Linux driver for the
  Imagination PowerVR SGX545 as found in the Intel Atom CE5310.
- **[t2i-zephyr](https://github.com/The1TrueJoe/t2i-zephyr)** — Zephyr firmware for the
  RTI T2i Zigbee + RF remote.
- **[openSpeakerPoint](https://github.com/The1TrueJoe/openSpeakerPoint)** — Buildroot
  firmware for the 2006 Control4 SpeakerPoint.

More at [PROJECTS.md](PROJECTS.md), and writeups on [telaak.dev](https://telaak.dev/#work).

## This repository

| File | What it is |
| --- | --- |
| `resume.tex` → [`resume.pdf`](https://telaak.dev/The1TrueJoe/resume.pdf) | One-page résumé. Compiled by GitHub Actions on every push. |
| `cv.tex` → `cv.pdf` | The long version. |
| [`PROJECTS.md`](PROJECTS.md) | Index of the things worth finding. |
| [`STATS.md`](STATS.md) | Language breakdown. |
| `skylines/` | GitHub Skyline models, 2019–2021. |

`resume.tex` is also the source of the Résumé section on
[telaak.dev](https://telaak.dev/#resume): that site fetches this file at build time and
parses it, so the page and the PDF can never disagree. A `% tags: a, b, c` comment under
a `\resumeSubheading` becomes that entry's tag row on the site and is invisible to LaTeX.

Editing the résumé updates both. Pushing here compiles the PDF and, via
[`notify-site.yml`](.github/workflows/notify-site.yml), tells telaak.dev to rebuild. That
ping needs a repository secret `SITE_DISPATCH_TOKEN` — a fine-grained PAT with
*Actions: read & write* on `The1TrueJoe/The1TrueJoe.github.io`. Without it the site still
picks the change up on its nightly build.
