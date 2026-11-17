# London Calling — Harris Family

A mobile-first, public, installable itinerary site hosted on Netlify.

## Publish with GitHub + Netlify

1. On GitHub, create a new repository, e.g. `london-calling`. Since the app is public, **do not store secrets or private documents in this repository**.
2. Upload the files in this folder to the **root** of the repository (not inside a nested `london-calling` folder). Commit the files.
3. In Netlify, choose **Add new project → Import an existing project → GitHub**, authorize access, and select your repository.
4. Build command: **leave blank**. Publish directory: **`.`** (repository root). Deploy.
5. Open the generated `*.netlify.app` URL on your phone. Share the URL with family. On iPhone use Safari → Share → Add to Home Screen; on Android use Chrome → menu → Install app / Add to Home screen.

## Update the itinerary

1. Open `itinerary.json` in GitHub and click the pencil icon to edit.
2. Make a small change, preserving JSON syntax (commas and quotation marks). Click **Commit changes**.
3. Netlify automatically deploys the new commit. Once deployment finishes, tap **Refresh** in the app to load the new itinerary.
4. If JSON is malformed, the app falls back to its last saved version; fix the JSON and redeploy. You can validate JSON with a JSON validator before committing.

## Structure

- `itinerary.json` — single source of truth for trip activities, notes, and directions.
- `index.html`, `styles.css`, `app.js` — app presentation and logic.
- `manifest.webmanifest`, `icon-*.png`, `sw.js` — home-screen installation and limited offline support.

## Weather and directions

Weather is fetched from Open-Meteo's public forecast API for central London. The forecast is limited to the days available from the provider; dates outside the window show sensible default clothing advice. Weather needs an internet connection. Google Maps and Apple Maps open in separate tabs/apps. Written travel guidance is approximate and should be checked against live service conditions.

## Important before the trip

- Check Wednesday's **Christmas Lights Bus Tour meeting point** against the ticket and add the precise address.
- Add Thursday's **The Play That Goes Wrong** curtain time and verify the theatre on the ticket.
- Verify the **Check It Vintage** store address before adding a map link.
- Confirm the Friday **Winter Wonderland** entry requirements and the **Harrods Ralph Lauren pop-up**.
- Confirm that the Saturday **10:00 AM Transfeero return pickup** is still correct; it supersedes an earlier 12:30 PM plan.
- Consider removing booking reference numbers from the public itinerary if you prefer. Never publish passport numbers, full tickets, private phone numbers or payment information.

## Testing

Open the deployed site on iPhone and Android. Try each day, optional sections, Google Maps and Apple Maps links, Refresh, airplane-mode offline view after an initial successful load, and home-screen installation.
