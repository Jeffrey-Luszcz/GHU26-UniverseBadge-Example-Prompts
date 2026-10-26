# GitHub Universe 2026 Badge Prompts

A collection of Copilot prompts for exploring the GitHub Universe 2026 badge. For more about the badge, visit [badger/home](https://github.com/badger/home).

## Prompts

### Tide Clock for Fort Mason Prompt 
Use hyb26-skill to build a MicroPython Universe 2026 badge tide clock for Fort Mason, San Francisco. Create a GitHub-dark dashboard with an orange Golden Gate Bridge, cyan daily tide curve, predicted height in feet (MLLW), rising/falling status, and high/low times. Use NOAA station 9414290 and Pacific time with DST. Cache seven days of tides and retain verified UTC in the hardware RTC so restarts work offline. Sync over Wi-Fi only when cached data/time is unavailable or Down is pressed; no background refresh. Preserve good cache on failure, flag expired data, reserve Home for the launcher, and include an icon and README. Skip tests.

<img width="320" height="240" alt="tide-clock-screenshot-2026-10-24-1410" src="https://github.com/user-attachments/assets/e221fa4d-df3e-42d6-b5be-eb1f0b6d15d4" />

### Art Frame to download art from the Cleveland Museum of Art Prompt

use the hyb26-skill, Build a MicroPython MonaOS app for the GitHub Universe badge that displays CC0 paintings from the Cleveland Museum of Art on its 320×240 screen. Fetch randomized 
painting candidates from `https://openaccess-api.clevelandart.org/api/artworks/` (filter for paintings with images and CC0 access), then use `https://images.weserv.nl/` to resize 
images to 320z240 PNGs for low-memory decoding. 

Use the badge's `badgeware` APIs and Wi-Fi credentials from `/secrets.py`. Show a boot screen, cached artwork, artwork details (title, artist, year), and Wi-Fi/status/error screens; 
support UP/DOWN to fetch another painting, A to toggle details, and HOME to return to MonaOS. Refresh every 10 minutes, cache artwork and metadata safely, handle offline failures 
gracefully, and include tests for artwork selection and storage. Controls 
UP/DOWN: Download another painting 
A: Show or hide title, artist, and year 
HOME: Return to MonaOS 
TEST_MODE in ArtFrame/ArtFrame/app.py is disabled by default, so paintings refresh every 10 minutes. Set it to True for a 10-second test interval.


## License

This repository is dedicated to the public domain under [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).
