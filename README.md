# KAZCODE — The Cultural Code of Kazakhstan

A static cultural dictionary designed for GitHub Pages. Built with HTML, CSS and JavaScript; the 100 concepts are stored in `data/concepts.json`.

## Publish on GitHub Pages (no programming required)

1. Download and unzip `KAZCODE.zip`.
2. On GitHub, create a **Public** repository named `kazcode`.
3. Open the repository and choose **Add file → Upload files**. Upload the *contents* of this folder (including `index.html`, `assets`, `data`, `concepts`, etc.), not the ZIP itself. Commit the files to the `main` branch.
4. Open **Settings → Pages**. Under Build and deployment, choose **Deploy from a branch**, select `main` and `/ (root)`, then press **Save**.
5. Wait a minute or two. Your site will be at `https://YOUR-USERNAME.github.io/kazcode/`.

## QR-code URL configuration

The site calculates its URL from the current page by default, which works with a GitHub Pages project URL. If you later use a custom domain, open `assets/js/config.js` and set `baseUrl` to the full public base URL, with no trailing slash, for example:

```js
window.KAZCODE_CONFIG = { baseUrl: 'https://your-domain.example', siteName: 'KAZCODE' };
```

QR codes are generated in the browser using qrcodejs loaded from a CDN. Most site functions work without that library, but QR generation and PNG download require an internet connection to load the library.

## Features

- 100 concepts with nine source sections each
- Search across Kazakh, Latin and English text
- Seven category filters and alphabetical sorting
- Dedicated concept URLs under `/concepts/<slug>/`
- Favorites saved in localStorage
- Share/copy link and QR-code PNG download
- Responsive layout, dark mode and keyboard-accessible navigation

## Data and academic integrity

`data/concepts.json` is the website's data source. `SOURCE_REVIEW_NOTES.md` records extraction caveats. The site does not independently validate scholarly claims; entries marked Draft or Preliminary should be treated accordingly. Review the data before formal academic publication.

## Local preview

Because the pages fetch JSON files, opening `index.html` directly as a `file://` URL may block data loading in some browsers. The most reliable preview is to publish through GitHub Pages. Alternatively, run a local static server if you already have one.
