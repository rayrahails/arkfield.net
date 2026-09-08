# Arkfield

**Social campaigns that turn attention into momentum.**

A lightweight, responsive holding page for [arkfield.net](https://arkfield.net), introducing Arkfield’s services while the full website is being prepared.

Arkfield focuses on social media strategy, campaign management, content creation, and performance reporting. Supporting services include content writing, technical writing, and STEM practice-test item writing.

## Current website

- White background with Arkfield’s teal, green, orange, and dark-navy identity.
- Responsive layout with a prominent website-upgrade notice.
- Semantic HTML, a skip link, descriptive image text, and reduced-motion support.
- Page title, description, canonical URL, social-sharing metadata, and Organization structured data.
- Plain HTML and inline CSS; no framework, build step, package installation, or runtime JavaScript.

The full service website is planned; this repository currently contains the holding page.

## Website files

| File | Purpose |
| --- | --- |
| `index.html` | Holding-page content, styles, and metadata |
| `Arkfield_logo_social-content-campaigns.svg` | Main website logo |
| `favicon.svg` | Browser icon |
| `robots.txt` | Search and AI crawler preferences |

The original PNG brand artwork and `Arkfield_Services_Professional.docx` are reference materials, not required website assets. A sitemap is not included; it will be supplied separately.

## Preview locally

Open `index.html` in a browser for a quick preview. To check root-relative navigation, serve the project folder over HTTP. With Python 3 installed, run this command from the repository root:

```sh
python3 -m http.server 4173 --bind 127.0.0.1
```

Visit [localhost:4173](http://localhost:4173). Press `Ctrl+C` in the terminal to stop the server.

## Publish

Upload these four files to the hosting provider’s public document root, keeping their filenames unchanged:

```text
index.html
Arkfield_logo_social-content-campaigns.svg
favicon.svg
robots.txt
```

Upload the separately prepared `sitemap.xml` to the same location when ready. To advertise it to crawlers, add this line to `robots.txt` after uploading it:

```text
Sitemap: https://arkfield.net/sitemap.xml
```

The production domain is `https://arkfield.net/`. Canonical, social-sharing, and structured-data URLs currently point there. Update those URLs if the production domain changes. The header home link assumes the site is served from the domain root.

Only the four website files above and the optional sitemap are needed for deployment. Publishing the entire repository as a static site may also expose reference documents and artwork.

## Search and AI crawler policy

`robots.txt` allows conventional search crawlers, including Googlebot and Bingbot, and disallows the explicitly listed AI crawlers and assistants. It also includes the optional `Content-Signal` declaration requesting search use while declining AI training and AI-input use.

These directives express preferences; they do not enforce access control. Unlisted or noncompliant crawlers may still access public content, and not all tools recognize `Content-Signal`. Allowing search crawlers also does not guarantee exclusion from search engines’ AI features. Server or CDN controls are needed for additional enforcement.

Review the named crawler list periodically as operators change their agents. Keep ordinary search crawler access enabled when updating it.

## Editing

- Update the headline, introduction, services, and return message in `index.html`.
- Adjust shared colors through the CSS variables in `:root`.
- Maintain the logo’s aspect ratio when changing its display size.
- Update the return message and copyright year when appropriate.
- Check desktop and mobile layouts, logo loading, and keyboard navigation after visual changes.

Before publishing, confirm that the page, logo, favicon, and `robots.txt` load at their expected public URLs. Check the sitemap separately when it is available.
