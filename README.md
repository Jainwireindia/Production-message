# Production Note (v1.1.0)

A phone-friendly typing tool for supervisors. They type the day's production once, in one fixed format, and send it to the WhatsApp group.
Everything is kept in the phone's browser only. No sheet, no login.

## What the supervisor does
1. First open: type **Your Name :** (asked once; tap the name at the top to change it).
2. Pick the **date** (type it, or tap the calendar button), **Day / Night**, and what is being reported: **BB1 · BB2 · Chainlink · Barbed**.
3. Fill the 3 ready lines (add more with **+ Add a line**). When a team / machine has something in it, **+ Next …** appears.
   - **BB1:** Team 1, 2, … each item has how many, unit and weight per piece.
   - **BB2:** machines M-2 / M-3, each with a **Team** (A to D) and **Stopped** tick. Each item has rolls, Normal / Lite and the **average kg per roll**. Type the thickness (e.g. `1.95` or `2`) and tap the suggested **17x17x1.95mm** name, then tap 3ft / 4ft / 5ft. Anything else typed is accepted as it is. The **Wire used** cells are always shown; the **Coiling machine** comes from **+ Add Coiling machine**.
   - **Chainlink:** machines M1, M2, M3 (no teams). Each item has rolls, total kg and **Wire used** + kg given (+ 2nd wire if two wires were given). Leave the wire kg empty or 0 when no new wire was given.
   - **Barbed:** one machine (no choice). Same item and wire cells as chainlink.
4. **Save & send to WhatsApp**, then pick the group. (**Copy** copies the text instead.)

Saved notes stay at the bottom of the page: **Open** to correct and resend, **Send** to share again, ✕ to delete.

## Put it online (needed for "Add to Home screen" / offline)
Upload the whole folder to GitHub Pages, for example `ims/note/`, so all 7 files sit together:
index.html, manifest.webmanifest, sw.js, icon.svg, icon-192.png, icon-512.png, apple-touch-icon.png.
Open the link on the phone: Chrome menu → **Install app / Add to Home screen** (iPhone: Share → Add to Home Screen).
After the first open it works without internet (sending to WhatsApp still needs internet).
When the files are changed later, edit `CACHE = 'prodnote-v2'` in sw.js to `v3`, so phones pick up the new version.
