CORREO DEL ORINOCO
==================
Source: http://correodelorinoco.gob.ve
Collected: 2026-01-01
Status: LIVE (200 OK)

API ENDPOINTS COLLECTED:
------------------------
/wp-json/                    - API root discovery
/wp-json/wp/v2/users         - Staff accounts
/wp-json/wp/v2/media         - Uploaded images/files
/wp-json/wp/v2/posts         - News articles

FILES IN THIS FOLDER:
---------------------
Correo_api_root.json    - Full API namespace discovery
Correo_users.json       - User accounts (page 1)
Correo_media_p1.json    - Media library page 1
Correo_posts_p1.json    - Posts page 1

NOTES:
------
- State newspaper
- Official government communications
- May contain internal event photos
- HTTP (not HTTPS) - less secure

NEXT STEPS:
-----------
[ ] Paginate through all media pages
[ ] Check for sensitive document uploads
[ ] Extract EXIF from images
