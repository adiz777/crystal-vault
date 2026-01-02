AVN - AGENCIA VENEZOLANA DE NOTICIAS
=====================================
Source: https://avn.info.ve
Collected: 2026-01-01
Status: LIVE (200 OK)

API ENDPOINTS COLLECTED:
------------------------
/wp-json/                    - API root discovery
/wp-json/wp/v2/users         - Staff/journalists
/wp-json/wp/v2/media         - Uploaded images/files
/wp-json/wp/v2/posts         - News articles
/wp-json/wp/v2/categories    - Post categories

FILES IN THIS FOLDER:
---------------------
AVN_api_root.json      - Full API namespace discovery
AVN_users.json         - User accounts (page 1, 100 per page)
AVN_media_p1.json      - Media library page 1
AVN_posts_p1.json      - Posts page 1
AVN_categories.json    - All categories

NOTES:
------
- State news agency
- High volume media uploads
- Check media for EXIF/GPS data
- May contain government event photos

NEXT STEPS:
-----------
[ ] Paginate through all media pages
[ ] Extract EXIF from downloaded images
[ ] Cross-reference users with other sources
