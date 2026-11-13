# Campus Resources

Independent UC Berkeley student resource field guide: 32 official resources, six curated starting points, guided checklists, and a device-local backpack. No analytics, paid API, account system, or server database.

## Local use

Requires Node.js 22+. Run `npm run dev` and open http://127.0.0.1:4450. No runtime dependencies. Run `npm test` for core checks. For browser checks, run `npm install`, install Google Chrome, start the server, then `npm run test:browser`.

## Features

Search by need with synonyms; filter category, student level, and documented no-cost options. Save official links, share resource links, download plans and the directory, export/import validated backups, and download selected Fall 2026 dates as an ICS file. Guide assets work offline after a successful first visit; provider sites require internet. Updated service workers activate after existing tabs close.

## Sources and limits

Source summaries reviewed November 12, 2026. Each resource links to its official provider in `public/data.mjs`. Calendar dates come from the Registrar 2026–27 calendar, with exclusive all-day end dates. Confirm current hours, availability, costs, and eligibility directly with providers. This is not an official university website, a monitored support service, or a clinical assessment.

Saved IDs and checklist progress stay in browser local storage. Anyone sharing the browser or an exported backup can see those choices. No automatic cross-device sync. Browsers may clear stored data; export backups when important. Hosting providers receive normal page requests.

## Validation and deployment

Executed Chrome flows are recorded in `docs/browser-validation.json`; HTTP results and redirects in `docs/link-check.json`. These checks do not guarantee future availability or establish screen-reader usability, university endorsement, or field validation. Core tests cover directory integrity, search, audience filters, backup validation, and calendar end dates. Browser tests cover saves/reload, invalid imports, guided plans, malformed links, unsafe search input, mobile overflow, and offline reload.

Static output is `public/`; deploy to the existing Vercel project `campus-resources`. Preserve its audience unless the owner requests a change. Previous production rollback ID: `dpl_LWzfTkBYNS7hcw2KQ4QwWTrRGx9G`. Original campus SVG artwork is included. Inter font license is in `public/FONT-LICENSE.txt`.
