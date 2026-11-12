# Cốc Cốc Indexing Audit – Real Estate Project

**Audit date:** 2026-11-12  
**Scope:** Read-only review. No WordPress settings, robots.txt, sitemap, or content were changed.

## Executive summary

- WordPress site confirmed: `https://realestateproject.vn`, Jetpack-connected site ID `258612076`.
- Yoast SEO is active (v28.8); IndexNow plugin is active (v1.0.4); WP Robots Txt plugin is active (v1.3.6).
- WordPress permalink pattern: `/%category%/%postname%.html`.
- Published content inventory exposed by WordPress REST/MCP:
  - Posts: 1,290
  - Pages: 249
  - `du-an`: 301
  - `can-ho`: 74
  - `dat-nen`: 17
  - `ban-va-cho-thue`: 443
  - `nghi-duong`: 9
  - `doanh-nhan`: 1
  - `tai-lieu`: 141
  - `blocks` (UX Blocks): 31
  - `oum-location`: 0
- The sum of the listed public content records is 2,556 including UX Blocks, or 2,525 excluding UX Blocks. This is a WordPress REST inventory, **not a verified sitemap URL count**. Attachments, taxonomies, archives, and post types outside the REST namespace are not included.
- Published pages endpoint reports 249 pages; sample results include AIO CITY supporting pages and the homepage.

## Access limitations

Attempts to retrieve the live endpoints directly through the available web/container fetch surfaces failed:
- `https://realestateproject.vn/robots.txt`
- `https://realestateproject.vn/sitemap_index.xml`

The web fetch returned an inaccessible/internal error and the container fetch could not resolve the host. This does **not** prove the URLs are broken or misconfigured. Their actual HTTP status, response body, redirect chain, XML validity, and URL coverage remain unverified.

The WordPress site-settings endpoint returned general, reading, and permalink settings successfully, but the SEO settings subsection failed with HTTP 403. No inference is made about Yoast's sitemap include/exclude settings.

## Plugin observations

Active plugins relevant to indexing:
- Yoast SEO 28.8 – XML sitemap generation and SEO metadata.
- IndexNow 1.0.4 – supports IndexNow submission (not evidence of Cốc Cốc accepting IndexNow).
- WP Robots Txt 1.3.6 – robots.txt editing capability.
- Code Snippets 4.0.0 and WPCode Lite 2.4.0 – may contain custom output/filters; not inspected.
- Site Kit by Google 1.191.0 – Google integration, not Cốc Cốc indexing.

Do not assume IndexNow automatically submits to Cốc Cốc. Confirm supported endpoints and recipient services before relying on it.

## Official Cốc Cốc guidance checked

Cốc Cốc's official Search Console documentation says:
1. A site owner can submit individual URLs through its "Đưa trang web của bạn lên Tìm kiếm Cốc Cốc" form.
2. Sitemap paths can be declared using one or more `Sitemap:` directives in robots.txt.
3. Cốc Cốc robots include `coccocbot`, `coccocbot-web`, `coccocbot-image`, `coccocbot-fast`, `coccocbot-ads`, and `coccocbot-shopping`.
4. Robots.txt must be reachable; the crawler requests it before other URLs. The docs say an unavailable response can cause the site to be temporarily excluded from crawling.
5. URLs need discoverable, crawlable links, no blocking robots rules, and no noindex directive to be eligible for indexing.
6. Cốc Cốc recommends the `site:` operator to check whether pages appear in its index.

Official documentation:
- https://coccoc.com/search/console/vn/introduction
- https://coccoc.com/search/console/get-your-website-on-coc-coc-search
- https://coccoc.com/search/console/submit-sitemap-to-coc-coc-search
- https://coccoc.com/search/console/robots.txt
- https://coccoc.com/search/console/coc-coc-robots

## Important interpretation

- Crawl permission is not an indexing guarantee.
- Sitemap submission is a discovery signal, not a guarantee that every listed URL will be indexed.
- The 2,525 REST-exposed published records excluding UX Blocks should not all be submitted blindly. First exclude duplicate, redirected, noindex, thin, private, and low-value URLs.
- Public listing records, historical posts, document pages, project CPTs, and ordinary posts need separate indexation rules.
- Do not assume `coccocbot-web` is currently allowed until the live robots.txt response is inspected.
- A remembered previous intention to allow Cốc Cốc Bot is not a substitute for verifying the current live response.

## Next verification checklist (no changes yet)

1. Retrieve live robots.txt from hosting/cPanel or a network path that can access the origin; record HTTP status, content type, final URL, and full body.
2. Retrieve Yoast sitemap index and every child sitemap; record HTTP status, XML parse validity, URL count, lastmod fields, and included post types.
3. Compare sitemap URLs against WordPress published content and identify omissions/excess URLs.
4. For each sitemap URL, check HTTP status, canonical target, meta robots, robots.txt accessibility, and index-worthiness.
5. Inspect access logs for authentic Cốc Cốc user agents; validate IPs with the reverse/forward DNS method documented by Cốc Cốc.
6. Verify site presence with Cốc Cốc's `site:` operator and submit the sitemap/selected URLs in Cốc Cốc Search Console after site ownership is confirmed.
7. Record submissions and subsequent crawl/index observations in a controlled queue.

## Safety and change control

This audit made no changes to WordPress, plugins, robots.txt, sitemap, content, or hosting configuration. Any proposed robots or sitemap change must be reviewed against existing Yoast directives, WP Robots Txt, Code Snippets, and WPCode configuration before approval.
