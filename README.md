# Digital Business Card (vCard)

A lightweight, single-page digital business card — a self-contained "tap to view" profile with a one-click **Download vCard** button, dark/light toggle, and social links. Built as a static site, no backend or build step required to deploy.

Live demo: https://mfahadiqbalofcl.github.io/Digital-Business-Card/

> Note: the repository and current demo URL contain a typo ("Buiness"). Renaming the repo to `Digital-Business-Card` and updating the Pages URL is recommended.

## Features

- Clean, responsive card layout that works on mobile and desktop
- Light/dark mode toggle
- One-click **Add to Contact** — downloads a standard `.vcf` (vCard 3.0) the visitor can import into their phone's contacts
- Social links (LinkedIn, GitHub, Instagram, X/Twitter, Telegram, personal site)
- Animated preloader
- SEO + Open Graph / Twitter Card meta tags

## Tech Stack

- HTML5
- SASS/SCSS compiled to CSS (`assets/css/sass/`)
- Vanilla JavaScript + a small bit of jQuery (`assets/js/main.js`)
- Font Awesome 6 and Google Fonts (Roboto), loaded via CDN with Subresource Integrity

## Project Structure

```
.
├── index.html              # The card markup
├── assets/
│   ├── css/sass/           # main.scss source + compiled main.css
│   ├── js/main.js          # toggle + preloader logic
│   ├── images/             # avatar / profile photo
│   └── docs/vcard.vcf      # downloadable contact file
├── favicon.* / preloader.gif
├── LICENSE
└── README.md
```

## Running Locally

No build tooling is required — it's a static site. Clone and serve the folder:

```bash
git clone https://github.com/mfahadiqbalofcl/Digital-Business-Card.git
cd Digital-Business-Card

# Option A: open index.html directly in a browser
# Option B: serve it (recommended, so relative paths and the .vcf download behave correctly)
python3 -m http.server 8000
# then visit http://localhost:8000
```

If you edit `assets/css/sass/main.scss`, recompile it with any SASS toolchain, e.g.:

```bash
sass assets/css/sass/main.scss assets/css/sass/main.css
```

## Customizing It For Yourself

1. Edit `index.html` — name, headline, location, bio, and social URLs.
2. Replace `assets/images/` with your own photo and update the `.avatar` background in the SCSS.
3. Regenerate `assets/docs/vcard.vcf` with your own contact details (any online vCard generator works).
4. Update the favicons and the Open Graph `og:image`.

## Screenshot

<!-- TODO: add a screenshot or GIF of the card here -->
![Digital Business Card preview](./assets/images/screenshot.png)

## License

Released under the [MIT License](LICENSE).