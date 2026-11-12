# AIO CITY – SEO metadata and secondary keyword review

Audit date: 2026-11-12  
Scope: 15 newly published AIO CITY PR posts (IDs 31718, 31721, 31723, 31725, 31727, 31729, 31731, 31733, 31734, 31735, 31736, 31737, 31738, 31739, 31740).

## Completed metadata normalization

All 15 posts remain published. SEO title and meta description were updated only; visible post titles, article content, images, shortcodes, layouts, and URLs were not changed.

- SEO title length: 55–60 characters for all 15 posts.
- Meta description length: 150–160 characters for all 15 posts.
- Focus keyphrase: present for all 15 posts.
- Related keyphrases field `_yoast_wpseo_focuskeywords`: blank on all 15 posts at audit time. It was intentionally not written because the field's expected Yoast storage format has not been verified. The following are editorial suggestions for the secondary-keyword plan, not yet saved into Yoast.

## Secondary keyword recommendations

| Post ID | Focus keyphrase | Suggested related keywords |
|---|---|---|
| 31718 | AIO City Hoa Lâm An Gia | Hoa Lâm AIO City; An Gia Group AIO City; chủ đầu tư AIO City; đơn vị phát triển AIO City |
| 31721 | vị trí AIO City Bình Tân | AIO City khu Tên Lửa; vị trí căn hộ AIO City; kết nối khu Tên Lửa; căn hộ Bình Tân |
| 31723 | tiện ích AIO City | tiện ích nội khu AIO City; tiện ích ngoại khu Bình Tân; tiện ích khu Tên Lửa; tiện ích căn hộ |
| 31725 | quy hoạch AIO City | mặt bằng AIO City; quy hoạch dự án AIO City; hồ sơ quy hoạch căn hộ; tổng mặt bằng dự án |
| 31727 | thị trường căn hộ Bình Tân | thị trường bất động sản Bình Tân; căn hộ khu Tây TP.HCM; mua căn hộ Bình Tân; nguồn cung căn hộ |
| 31729 | thiết kế căn hộ AIO City | mặt bằng căn hộ AIO City; thiết kế căn hộ Bình Tân; công năng căn hộ; diện tích sử dụng |
| 31731 | tài chính mua căn hộ AIO City | ngân sách mua căn hộ; vay mua căn hộ; dòng tiền mua nhà; tổng chi phí sở hữu |
| 31733 | Có nên mua AIO City | đánh giá AIO City; ưu nhược điểm AIO City; rủi ro mua căn hộ; kinh nghiệm chọn căn hộ |
| 31734 | Shophouse AIO City | shophouse Bình Tân; shophouse khu Tên Lửa; đầu tư shophouse AIO City; khai thác shophouse |
| 31735 | Các loại căn hộ AIO City | diện tích căn hộ AIO City; chọn căn hộ theo nhu cầu; loại hình căn hộ; công năng căn hộ |
| 31736 | Pháp lý AIO City | hồ sơ pháp lý dự án AIO City; điều kiện bán căn hộ; kiểm tra pháp lý căn hộ; hồ sơ giao dịch |
| 31737 | Hạ tầng khu Tây TP.HCM | hạ tầng giao thông khu Tây; kết nối Bình Tân; giao thông khu Tên Lửa; hạ tầng TP.HCM |
| 31738 | Dự án căn hộ Bình Tân | so sánh căn hộ Bình Tân; dự án căn hộ khu Tây; kinh nghiệm chọn căn hộ; tiêu chí so sánh dự án |
| 31739 | AIO City Bình Tân | lịch sử dự án AIO City; quá trình phát triển AIO City; thông tin AIO City qua các giai đoạn |
| 31740 | Tiện ích AIO City | tiện ích gia đình AIO City; tiện ích cho trẻ em; tiện ích người cao tuổi; tiện ích khu dân cư |

## Internal-link audit notes

- All 15 posts contain internal links; counts range from 2 to 7 internal links per article.
- New PR cluster cross-links are present, especially between posts 31727, 31733, 31738, 31739 and 31740.
- Project hub `/du-an/aio-city.html` is linked from all 15 articles.
- Links to the legal and pricing pages under `/gkey-homes/aio-city/` are present in multiple articles. Automated web retrieval could not access those two URLs, so their HTTP status and page health remain unverified; do not label them broken based only on crawler inaccessibility.
- Legacy post 3003 is linked from posts 31721 and 31729. That legacy post was separately flagged for a confidential-content review; do not add further links to it until the user approves the narrowly scoped cleanup.
- Post 31738's incorrect link to post 31733 was corrected and re-fetched from WordPress to verify the old URL is absent and the correct URL is present.
- The direct public crawler could not retrieve the canonical URL for post 31733, although WordPress API confirms post ID 31733 is published. Treat as a crawl/indexability check to investigate, not a confirmed 404.

## Next actions

1. Confirm Yoast's supported storage format for related keyphrases before writing `_yoast_wpseo_focuskeywords`.
2. Verify the two Gkey Homes landing pages from WordPress and/or browser HTTP status; if they are not intended canonical pages, replace links only after confirming target URLs.
3. Inspect indexability/canonical/redirect behavior for post 31733.
4. Continue the broader internal-link inventory beyond these 15 new PR posts.
