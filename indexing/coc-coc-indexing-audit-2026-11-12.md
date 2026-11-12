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


## Sitemap index inventory supplied by the site owner

The site owner supplied the Yoast sitemap-index listing on 2026-11-12. It contains **24 sitemap entries**:

### Content sitemaps (11)
- `post-sitemap.xml` — last modified 2026-11-12 09:29 +00:00
- `post-sitemap2.xml` — last modified 2026-11-12 09:29 +00:00
- `page-sitemap.xml` — 2026-11-11 07:57 +00:00
- `blocks-sitemap.xml` — 2026-10-31 08:54 +00:00
- `ban-va-cho-thue-sitemap.xml` — 2026-07-30 16:34 +00:00
- `can-ho-sitemap.xml` — 2026-11-11 07:50 +00:00
- `dat-nen-sitemap.xml` — 2026-06-22 19:31 +00:00
- `doanh-nhan-sitemap.xml` — 2026-04-13 18:23 +00:00
- `du-an-sitemap.xml` — 2026-11-11 07:58 +00:00
- `nghi-duong-sitemap.xml` — 2025-12-30 06:26 +00:00
- `tai-lieu-sitemap.xml` — 2026-11-11 07:57 +00:00

### Taxonomy sitemaps (12)
- `category-sitemap.xml` — 2026-11-12 09:29 +00:00
- `post_tag-sitemap.xml` — 2026-11-12 09:26 +00:00
- `danh-muc-bvct-sitemap.xml` — 2026-07-30 16:34 +00:00
- `danh-muc-can-ho-sitemap.xml` — 2026-03-13 14:15 +00:00
- `danh-muc-dat-nen-sitemap.xml` — 2026-06-22 19:31 +00:00
- `danh-muc-du-an-sitemap.xml` — 2026-11-11 07:58 +00:00
- `danh-muc-nghi-duong-sitemap.xml` — 2025-12-30 06:26 +00:00
- `danh-muc-tai-lieu-sitemap.xml` — 2026-11-11 07:57 +00:00
- `tag-bvct-sitemap.xml` — 2026-07-30 16:34 +00:00
- `tag-tai-lieu-sitemap.xml` — 2026-11-11 07:57 +00:00
- `tags-sitemap.xml` — 2026-11-11 07:58 +00:00
- `tag-page-sitemap.xml` — 2026-11-11 07:57 +00:00

### Author sitemap (1)
- `author-sitemap.xml` — 2026-09-16 04:39 +00:00

## Sitemap inventory assessment

1. The index covers the principal public content types seen in the WordPress REST inventory: posts, pages, projects, apartments, land, listings, resorts, business profiles, and documents.
2. The two post sitemap files are consistent with Yoast splitting a large post collection. Their actual URL counts must be read from each XML file before confirming coverage.
3. UX Blocks sitemap needs special review. Reusable layout blocks are usually not independent search landing pages; include them only if each URL is intentionally public, useful, canonical, and suitable for search. Otherwise review noindex/exclusion from sitemap.
4. Taxonomy sitemap entries should not be submitted indiscriminately. Keep category/tag archives only when they have distinct search intent, useful introductions, curated content, and no substantial duplication. Thin or near-empty archives should be assessed for noindex/exclusion.
5. Author archive should be reviewed for meaningful author biography, editorial expertise, and useful article listing. Do not assume it deserves indexing solely because it is in the sitemap.
6. Older last-modified dates on some sitemap files are not evidence of an error or deindexing; they may simply indicate no recent content changes in those sections.
7. Sitemap last-modified values are not crawl timestamps and do not confirm Cốc Cốc has fetched or indexed any URL.

## Live XML verification status

The supplied sitemap-index table is accepted as owner-provided evidence of the 24 listed entries. Attempts to fetch the sitemap index, robots.txt, and selected child sitemaps through the available web fetch returned inaccessible/cache-miss errors. Therefore the following remain unverified: HTTP status, XML validity, number of URLs per child sitemap, actual URL contents, canonical destinations, and URL coverage against WordPress.

## Recommended Cốc Cốc submission priority (provisional)

- **Priority 1:** Canonical project pages (`du-an`), high-value project support pages, useful public articles, and genuinely useful documents.
- **Priority 2:** Other valuable public CPT entries and well-maintained category archives.
- **Review before submission:** Tags, author archive, UX Blocks, thin taxonomy archives, legacy or outdated pages.
- **Exclude from submission:** Noindex pages, redirects, 404/soft-404, duplicate/canonicalized URLs, private/internal pages, and low-value system/layout URLs.

This is a prioritization recommendation only. No sitemap, robots, noindex, or WordPress settings were changed.


## robots.txt content supplied by the site owner

The owner pasted the following logical rules (the displayed labels are Vietnamese translations in the supplied text):

- `coccocbot`: empty `Disallow` value.
- Yoast wildcard group: `User-agent: *`, empty `Disallow`.
- `coccocbot-web`: `Allow: /`.
- General wildcard group: `Disallow: /wp-admin/`, `Allow: /wp-admin/admin-ajax.php`.
- Sitemap declarations:
  - `https://realestateproject.vn/wp-sitemap.xml`
  - `https://realestateproject.vn/sitemap.xml`
  - `https://realestateproject.vn/sitemap_index.xml` (appears twice)

### robots.txt assessment

1. If the raw file really contains standard English directives with these values, the explicit `coccocbot` group is not blocking paths (empty Disallow), and the `coccocbot-web` group explicitly allows `/`.
2. The general wildcard rule blocks `/wp-admin/` and allows `/wp-admin/admin-ajax.php`, a common WordPress configuration.
3. Robots group selection is user-agent-specific. Do not assume wildcard rules are merged into a matching specific group; verify the behavior against the crawler's exact user-agent token and Cốc Cốc documentation.
4. Three sitemap locations are declared, and the Yoast sitemap index is declared twice. Repeated sitemap declarations are generally redundant, not proof of a crawl error. However, the site should choose a clearly maintained canonical sitemap index and verify whether the other two endpoints exist, overlap, redirect, or contain stale/duplicate URLs.
5. **Translation warning:** the owner-pasted text displays translated directive labels such as `Tác nhân người dùng`, `Cấm`, `Cho phép`, and `Sơ đồ trang web`. Robots.txt syntax requires the literal standard directives `User-agent`, `Disallow`, `Allow`, and `Sitemap`. If these Vietnamese words are literally present in the raw file rather than being browser auto-translation, the file is malformed and must be corrected. Confirm the raw source with browser translation disabled or by viewing page source before making any change.
6. No configuration was edited. Direct fetch attempts for robots.txt and all three sitemap endpoints failed in the available web fetch surface, so HTTP status and raw bytes remain unverified.

### Provisional recommendation

Keep the current access rules unchanged pending raw-file verification. If the raw syntax is valid, do not add more bot allow rules merely for duplication. Next, inspect all three sitemap endpoints and determine which one is the authoritative index. Prefer the Yoast `/sitemap_index.xml` only if it is live, valid XML and contains the intended canonical URL inventory. Do not remove `/wp-sitemap.xml` or `/sitemap.xml` until their behavior and dependencies are confirmed.


## 8. Đánh giá robots.txt theo nội dung người dùng cung cấp (2026-11-12)

Người dùng cung cấp nội dung robots.txt với các quy tắc:
- `User-agent: coccocbot` và `Disallow:` để trống.
- Khối Yoast có `User-agent: *` và `Disallow:` để trống.
- `User-agent: coccocbot-web` với `Allow: /`.
- Khối `User-agent: *` chặn `/wp-admin/`, đồng thời cho phép `/wp-admin/admin-ajax.php`.
- Khai báo ba sitemap: `/wp-sitemap.xml`, `/sitemap.xml`, `/sitemap_index.xml` (sitemap_index được khai báo lặp lại).

### Kết luận

- Theo nội dung được cung cấp, không có quy tắc Disallow áp dụng trực tiếp để chặn nội dung công khai của website đối với `coccocbot` hoặc `coccocbot-web`.
- Quy tắc chặn `/wp-admin/` là thông lệ hợp lý; ngoại lệ `admin-ajax.php` được cho phép.
- Chưa có căn cứ để yêu cầu mở rộng `Allow: /` cho mọi user-agent; không nên thay đổi cấu hình chỉ vì mục đích “cho phép tất cả”.
- Ba sitemap được khai báo không đồng nghĩa cả ba URL đều tồn tại, trả về XML hợp lệ hoặc chứa các URL khác nhau. Cần kiểm tra trực tiếp mã phản hồi HTTP, nội dung XML, canonical sitemap index và mức độ trùng lặp trước khi quyết định giữ/bỏ khai báo nào.
- `sitemap_index.xml` xuất hiện hai lần trong robots.txt. Việc lặp khai báo thường không tạo thêm giá trị khám phá; có thể tinh gọn sau khi xác minh các sitemap, nhưng hiện tại không chỉnh sửa theo yêu cầu chỉ kiểm tra.
- Đây là đánh giá dựa trên văn bản robots.txt người dùng dán, chưa phải xác minh độc lập nội dung đang được máy chủ phân phối tại thời điểm kiểm tra.

### Bước kiểm tra tiếp theo

Mở và kiểm tra trực tiếp ba endpoint sitemap; đối chiếu mã HTTP, XML hợp lệ, số URL trong từng sitemap, URL trùng lặp và việc các sitemap con có nằm trong sitemap index của Yoast hay không. Không thay đổi robots.txt hoặc sitemap trước khi hoàn tất đối chiếu.


## 9. Đối chiếu XML Sitemap Index gốc do người dùng cung cấp

Ngày 2026-11-12, người dùng cung cấp nội dung XML của `https://realestateproject.vn/sitemap_index.xml`. Đã phân tích cấu trúc XML index (không phải nội dung các sitemap con).

### Kết quả đọc từ XML index

- Tổng số sitemap con được khai báo: **24**.
- Sitemap nội dung: **11** — `post-sitemap.xml`, `post-sitemap2.xml`, `page-sitemap.xml`, `blocks-sitemap.xml`, `ban-va-cho-thue-sitemap.xml`, `can-ho-sitemap.xml`, `dat-nen-sitemap.xml`, `doanh-nhan-sitemap.xml`, `du-an-sitemap.xml`, `nghi-duong-sitemap.xml`, `tai-lieu-sitemap.xml`.
- Sitemap taxonomy: **12** — `category-sitemap.xml`, `post_tag-sitemap.xml`, `danh-muc-bvct-sitemap.xml`, `danh-muc-can-ho-sitemap.xml`, `danh-muc-dat-nen-sitemap.xml`, `danh-muc-du-an-sitemap.xml`, `danh-muc-nghi-duong-sitemap.xml`, `danh-muc-tai-lieu-sitemap.xml`, `tag-bvct-sitemap.xml`, `tag-tai-lieu-sitemap.xml`, `tags-sitemap.xml`, `tag-page-sitemap.xml`.
- Sitemap tác giả: **1** — `author-sitemap.xml`.

### Nhận xét

1. Sitemap index có cấu trúc sitemap chuẩn của Yoast: root `sitemapindex`, namespace Sitemaps.org, mỗi mục có `loc` và `lastmod`, kèm stylesheet XSL.
2. Có hai tệp bài viết; cần tải từng tệp để đếm số URL, xem phân trang và đối chiếu trùng lặp.
3. Nhóm CPT (bất động sản, căn hộ, mua bán/cho thuê, đất nền, nghỉ dưỡng, doanh nhân, tài liệu) đang được đưa vào sitemap. Cần đánh giá URL thực tế trong từng sitemap, không thể kết luận chỉ từ tên.
4. Nhóm taxonomy có nhiều sitemap theo taxonomy chung và taxonomy riêng của CPT. Cần kiểm tra số lượng term, nội dung archive, canonical và noindex trước khi quyết định giữ hay loại.
5. `blocks-sitemap.xml` cần kiểm tra xem các URL block có thực sự là trang công khai hữu ích cho tìm kiếm hay chỉ là thành phần dựng giao diện.
6. `author-sitemap.xml` cần đánh giá trang tác giả có hồ sơ chuyên môn và giá trị biên tập hay không.
7. XML index được cung cấp không cho biết tổng số URL trang/bài bên trong các sitemap con. Không suy diễn số URL từ số sitemap hoặc `lastmod`.

### Giới hạn xác minh

Đã đọc được nội dung XML index do người dùng cung cấp. Chưa có nội dung XML của 24 sitemap con nên chưa thể đếm tổng URL, phát hiện URL trùng, kiểm tra URL lỗi/noindex/redirect hoặc đối chiếu độ bao phủ giữa các nguồn sitemap.
