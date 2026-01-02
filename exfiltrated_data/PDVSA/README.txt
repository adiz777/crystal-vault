PDVSA - PETROLEOS DE VENEZUELA SA
==================================
Source: http://www.pdvsa.com / https://pdvsa.com
Probed: 2026-01-01
Status: UNREACHABLE - DNS RESOLUTION FAILURE

CONNECTION ATTEMPTS:
--------------------
http://www.pdvsa.com/wp-json/    - Timeout (exit code 28)
http://pdvsa.com/wp-json/        - DNS failure (exit code 6)
https://pdvsa.com/wp-json/       - DNS failure (exit code 6)

ANALYSIS:
---------
- Domain may be geo-blocked outside Venezuela
- May require Venezuela-based VPN/proxy
- Possible CANTV DNS blocking
- OFAC-sanctioned entity - may have additional protections

PRIORITY: CRITICAL TARGET
- State oil company
- OFAC-sanctioned
- Oil infrastructure intel
- Executive/board member data
- Refinery locations
- Production data

NEXT STEPS:
-----------
[ ] Retry with Tor exit node in Venezuela-friendly country
[ ] Try Venezuela VPN/proxy
[ ] Check if domain is accessible via alternative DNS
[ ] Monitor for accessibility changes
