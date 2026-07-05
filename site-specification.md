# Site Specification

## Configuration
- **Site Type**: General (personal / one-page profile — a "hire me" card)
- **Design Language (Starting Point)**: Technology (terminal / developer aesthetic)
- **Target Audience**: Potential clients and collaborators looking for a Python / Web / Security / CI/CD / SaaS developer
- **Primary Goal**: Credibility + a single conversion — "Let's talk!" (contact via LinkedIn)

## Content (verbatim from hire.nejczupan.com — preserved)
- **Name**: Nejc Zupan (phonetic: Neyts Zupan)
- **Tagline**: "Helping you grow your code and business."
- **Bio**: "Geek since I was able to walk. Bootstrapped & powered by Open Source. Can help you with anything Python, Web, Security, CI/CD and SaaS."
- **CTA**: "Let's talk!" → https://www.linkedin.com/in/nzupan/
- **Socials**: X @nzupan, GitHub zupo, LinkedIn nzupan

## Design Evolution
- **Starting aesthetic**: Technology design language — GitHub-dark terminal surface, monospace accents, high-contrast text.
- **User customizations**: None yet. Built as a modern reinterpretation of the original light-only personal card, moved to a dark terminal aesthetic.
- **Current style**:
  - **Background**: `#0D1117` (216 28% 7%) with a subtle technical grid and a drifting green glow, vignetted toward the edges.
  - **Surface/card**: `#161B22`-ish terminal window with a macOS-style title bar (`nejc@zupan: ~`).
  - **Primary**: terminal green `#39D353` (133 64% 52%) — used for the CTA and `$` prompts.
  - **Accent**: bright blue `#58A6FF` (212 100% 67%).
  - **Foreground**: off-white `#C9D1D9`; muted `#8B949E`.
  - **Typography** (Astro Fonts API, Google): **Sora** (display, 400–800) for the name; **Instrument Sans** (body) for prose; **JetBrains Mono** for prompts, labels, chips, CTA.
  - **Motion**: CSS-only staggered `rise` entrance on load, drifting glow, blinking terminal cursor. All disabled under `prefers-reduced-motion`.

## Structure
- Single page (`src/pages/index.astro`): terminal-window card containing portrait, name, phonetic subtitle, tagline, bio, skill chips (Python / Web / Security / CI/CD / SaaS), "Let's talk!" CTA, and X / GitHub / LinkedIn icon links.
- `src/pages/404.astro`: terminal-styled not-found page.
- JSON-LD `Person` schema wired via the Layout `schema` prop.

## Deploy notes
- `astro.config.mjs` `site` is set to `https://nejczupan.com`. Update if the production domain differs (e.g. `hire.nejczupan.com`).
- OG image at `public/og.jpg` is the existing headshot card — replace with a new dark-theme social card when convenient.
