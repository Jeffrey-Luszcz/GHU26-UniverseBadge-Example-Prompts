# GitHub Universe 2026 Badge Prompts

A collection of Copilot prompts for exploring the GitHub Universe 2026 badge. For more about the badge, visit [badger/home](https://github.com/badger/home).

## Prompts

### Tide Clock for Fort Mason Prompt - uses remote APIS and Wifi to make a dashboard

Use hyb26-skill to build a MicroPython Universe 2026 badge tide clock for Fort Mason, San Francisco. Create a GitHub-dark dashboard with an orange Golden Gate Bridge, cyan daily tide curve, predicted height in feet (MLLW), rising/falling status, and high/low times. Use NOAA station 9414290 and Pacific time with DST. Cache seven days of tides and retain verified UTC in the hardware RTC so restarts work offline. Sync over Wi-Fi only when cached data/time is unavailable or Down is pressed; no background refresh. Preserve good cache on failure, flag expired data, reserve Home for the launcher, and include an icon and README. Skip tests.

<img width="320" height="240" alt="tide-clock-screenshot-2026-10-24-1410" src="https://github.com/user-attachments/assets/e221fa4d-df3e-42d6-b5be-eb1f0b6d15d4" />

### Art Frame to download art from the Cleveland Museum of Art Prompt - uses remote APIS and Wifi to make an updating art picture frame

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

### Shake to Roll Dice and Coin Toolbox Prompt - uses the accelerometer to simulate and animate dice rolls and coin flips

Use hyb26-skill to build a MicroPython MonaOS dice app for the GitHub Universe 2026 badge. Start on 1d6; UP/DOWN cycles through 2d6, coin, d4, d8, d10, d12, d20, and d100. Show the selected type, animate tumbling while shaking, and settle into random results when still. Require a deliberate jerk to roll, with quiet rearming and cooldown to prevent accidental rerolls. Show d6 pips, other dice’s numbers, 2d6 totals, and heads/tails. Include SELECT-to-roll, HOME-to-exit, a dice icon, tests, and physical-badge validation.

<img width="320" height="240" alt="dice-2d6" src="https://github.com/user-attachments/assets/13ae6a7d-3c07-467b-a2ab-8796f427bf10" />

### Sand Art - tilt to shake colored sand in a frame - uses the accelerometer to simulate flowing sand of different colors and densities in a frame

Use hyb26-skill to build a MicroPython Universe 2026 badge sand-art frame, two-thirds filled with liquid. Use the accelerometer for natural tilt, inversion, and shake-driven currents. Render tiny midnight-blue/black, red, light-blue, and gold-speckled grains with different densities that settle into layers. Prioritize smooth animation (~30 FPS) over precise physics using simplified simulation and fast framebuffer rendering. SELECT pauses, BACK remixes, MENU shows help, and HOME exits. Include an icon, tests, and README; validate and deploy to the connected badge.

<img width="160" height="120" alt="sand-art-badge" src="https://github.com/user-attachments/assets/3b4fda82-94fb-4bb1-9987-dad96f7fc79b" />

## License

This repository is dedicated to the public domain under [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).
