# Online Toolbox

A small collection of browser-based utilities, gathered in one place.

## Included tools

- **Calculator**: quick arithmetic using the existing calculator page.
- **Overview**: the landing page for browsing tools.

## Run locally

This is a static site, so no build step or dependencies are required. Open `index.html` directly in a browser, or serve the folder with any local static file server.

For example, with Python installed:

```sh
python3 -m http.server
```

Then visit <http://localhost:8000>.

## Deploy

The site can be hosted directly from a Git repository. Use these settings for either provider:

- **Build command**: none
- **Build output directory**: `/` (the repository root)
- **Functions or environment variables**: none

### GitHub Pages

1. Push the repository to GitHub.
2. Open **Settings > Pages** for the repository.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select the branch and the `/ (root)` folder, then save.

GitHub Pages will publish `index.html` at the repository's Pages URL. The tool files use relative paths, so the calculator will also work when the site is hosted under a project path.

### Cloudflare Pages

1. In Cloudflare, open **Workers & Pages** and choose **Create application > Pages > Connect to Git**.
2. Select the repository.
3. Leave the framework preset blank and use the settings above.
4. Save and deploy.

Cloudflare Pages will publish the root `index.html` as the site entry point.

## Add a tool

1. Add the tool's HTML file to this folder.
2. Add a tab and a tab panel in `index.html`.
3. Load the tool in its panel, following the existing calculator tab pattern.
4. Add a card to the Overview panel so the tool is discoverable.
