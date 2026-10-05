# hivedominion-site

The public website for the iOS game **Hive Dominion** (`com.jamesmscreations.hivedominion`): the privacy
policy and support pages linked from the App Store listing. Served by GitHub Pages from `main` (`/`).

- Home: https://jamesms-creations.github.io/hivedominion-site/
- Privacy Policy URL: https://jamesms-creations.github.io/hivedominion-site/privacy/
- Support URL: https://jamesms-creations.github.io/hivedominion-site/support/

This repository is public. It contains only the website: plain HTML and CSS, no build step, no scripts, no
external fonts, no cookies, trackers or analytics. Never add game code, secrets or internal documents here.
`.nojekyll` must stay: it stops GitHub Pages' Jekyll from treating `{{...}}` as template tags.

## TODO before App Store submission

Replace every placeholder (`grep -rn "{{" --include=*.html .` must print nothing when done):

- [ ] `{{SUPPORT_EMAIL}}` -> the dedicated support email address (not a personal address).
      Appears 18 times: `index.html` (2), `privacy/index.html` (10), `support/index.html` (6), half of them inside
      `mailto:` links.
- [ ] `{{OPERATOR_NAME}}` -> the legal name of whoever operates the game (your name as an Individual developer,
      matching the App Store seller name, or the company name later). Appears 5 times: `index.html` (2),
      `privacy/index.html` (2), `support/index.html` (1).

Then:

- [ ] Re-read `privacy/index.html` and update it (and the "Last updated" date) if anything below changes:
      in-app purchases go live (the purchase-history row and the 7-year purchase-record retention assume
      the server-side purchase ledger as planned), Sign in with Apple ships, Unity Cloud Diagnostics is or is not switched on, backup or log
      retention changes, or a new service provider is added.
- [ ] Check https://jamesms-creations.github.io/hivedominion-site/privacy/ and `/support/` load after the edit
      (App Review opens both).
