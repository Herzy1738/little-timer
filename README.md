# Little Timer

A simple visual timer for toddlers. No ads, no accounts, no tracking. It works offline after the first time it's opened.

## How it works

- Pick a time (30 sec to 30 min buttons, or − / + for anything from 30 seconds to 60 minutes) and tap **Start**.
- The colored circle shrinks clockwise as time runs out.
- While it runs, a toddler tap does nothing. To pause, **press and hold** the ⏸ button in the corner for 1 second.
- When time is up, a gentle chime plays twice, a star bounces, and confetti falls. **Again** restarts the same time.
- Pick the circle color with the dots. The speaker button turns the chime on or off.
- **Kid photo reveal:** a random photo hides under the color and is slowly revealed as time runs out. When time is up, it's shown big on the "All done!" screen. The same photo is never shown twice in a row (as long as there are at least 2).
- It remembers the last time and color. If the phone closes the app mid-timer, it picks back up where it was.
- The screen stays on while the timer runs.

## Putting it on her iPhone or iPad

An iPhone can only add a web page to the Home Screen from a web address, so the folder needs to be put online once. Both of these are free:

**Option A: Netlify Drop (about 2 minutes)**
1. On a computer, go to https://app.netlify.com/drop
2. Drag this whole `visual-timer` folder onto the page.
3. Make a free account when asked. Otherwise the site is deleted after an hour.
4. You'll get an address like `https://something-random.netlify.app`. You can rename it under Site settings.

**Option B: GitHub Pages**
1. Make a new public repository on github.com and upload the files in this folder.
2. Go to Settings → Pages → Source: "Deploy from a branch" → `main` / root → Save.
3. The address will be `https://<username>.github.io/<repo-name>/`.

**Then on her iPhone or iPad:**
1. Open the address in **Safari**. This needs Safari, not Chrome.
2. Tap the **Share** button (the square with an arrow pointing up).
3. Tap **Add to Home Screen**. If it isn't listed, tap "Edit Actions" first. Make sure "Open as Web App" is on, then tap **Add**.
4. Open it once from the new Home Screen icon. After that it works without internet too.

## Adding kid photos

iPhone doesn't let websites browse the photo library or search it for "kids". The app can only see photos she picks herself. She only has to do this once:

1. Open Little Timer **from the Home Screen icon**, not from Safari. On iPhone they keep separate storage, so photos added in Safari won't show up in the Home Screen app.
2. The first time it opens, an **"Add photos of your kids"** screen walks her through it. Tap **Choose kid photos**, then **Photo Library**.
3. In the picker, go to **Albums** (or **Collections**) and open her Kids album, or **People** and tap a child. Select at least 2 photos, then tap **Add**.
4. Tap **Start using Little Timer**.

"Skip for now" is at the bottom of that screen, but it only skips until the next time the app is opened. While there are no photos, the setup screen comes back each time. To add or remove photos later, tap the picture button next to the color dots.

Tips:
- To get a "kids" set fast, first make an album called Kids in the Photos app (or use the People album for each child), then pick from it here.
- The photos are shrunk and saved inside the app on her phone. They are never uploaded anywhere. Removing them here doesn't touch the Photos app.
- New photos aren't picked up automatically. Add more any time the same way.
- The "Reveal a photo" switch in the photo screen turns the photo reveal off without deleting the photos. With it off, the setup screen doesn't appear.

## Good to know

- **Sound:** turn the volume up. The chime is designed to play even with the silent switch on, but test it once on her phone to be sure.
- **Keep the app open:** iPhones pause web apps in the background. If she switches apps or the phone locks, the chime can't play until she comes back. The timer still keeps the right time.
- **Guided Access (optional):** to stop toddlers from leaving the app, go to Settings → Accessibility → Guided Access. Then triple-click the side button while the timer is open.

## Files

- `index.html`: the whole app
- `manifest.webmanifest`, `icon-180.png`, `icon-512.png`: Home Screen name and icon
- `sw.js`: makes it work offline. If you change `index.html` later, bump the version in `little-timer-v3` (to `v4`, and so on) so phones pick up the new copy.
