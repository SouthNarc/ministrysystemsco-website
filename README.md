# Ministry Systems Co. website

Static HTML/CSS site hosted on Cloudflare Pages from this repository's main branch.

## Publishing

Commit changes to main. Cloudflare automatically deploys the repository root.
Framework: None. Build command: exit 0. Build output directory: .

## Public pages and SEO

Indexable customer-facing pages are https://ministrysystemsco.com/ and https://ministrysystemsco.com/articles.
Home, About, Resources, Church Tech Toolbox, Sunday-Proof Livestream, and Contact are anchor sections of that page, not separate routes. Checkout is hosted externally at https://payhip.com/b/UTCz6.

sitemap.xml includes the canonical homepage and Articles landing page. Do not add fragment URLs, checkout URLs, assets, this README, or the 404 page. Add new canonical page URLs when genuinely separate public HTML pages are introduced. robots.txt allows normal crawling and references https://ministrysystemsco.com/sitemap.xml.

The homepage has one h1, section h2 headings, and subsection h3 headings. It targets church tech resources and small-church livestream guides, including Sunday-Proof Livestream. Metadata includes a page title, description, canonical URL, Open Graph and X/Twitter fields using the existing product cover. No design or body wording changed in the SEO update.

404.html has noindex; Cloudflare serves unknown routes with a real 404 status. _headers excludes this README from indexing with X-Robots-Tag: noindex. www and pages.dev copies retain the non-www canonical homepage. Pages automatically redirects /index.html to /.

## Google Search Console

1. Open https://search.google.com/search-console/.
2. Add a Domain property for ministrysystemsco.com.
3. Verify using the supplied DNS TXT record in Cloudflare (or its offered Cloudflare verification flow). Keep the verification record after verification.
4. Open Sitemaps and submit https://ministrysystemsco.com/sitemap.xml.
5. Use URL Inspection for https://ministrysystemsco.com/, run Test live URL, then request indexing if eligible.
6. Check the Sitemaps status and Page indexing report later. Submission does not guarantee immediate indexing or ranking.

## Editing

index.html contains visible text and SEO metadata. styles.css controls the design. Keep the actual paid PDF in Payhip, not in this public repository. When prices or product scope change, update the visible content and search/social descriptions together.

## Articles

/articles is the public Articles landing page, served by articles.html. It is now included in sitemap.xml. The homepage links to it in the navigation and Articles section.

To publish an article:
1. Ask Codex to prepare your draft as a page, or copy the private article template supplied with the project.
2. Use a descriptive filename such as church-livestream-reliability.html (Cloudflare serves /church-livestream-reliability).
3. Set a unique title, description, canonical URL, social title/description/URL, and one h1. Update article text and publication date.
4. Add an article card linking to it in articles.html and its canonical URL in sitemap.xml.
5. Upload the article HTML, articles.html, and sitemap.xml to main. Cloudflare deploys automatically.
6. Test the live link. The existing submitted sitemap will be reread by Google; request indexing for the new article if desired.

Keep draft text and templates outside the public repository. There is no sign-in or writing editor on this static site; Codex can turn a draft into the upload files.
