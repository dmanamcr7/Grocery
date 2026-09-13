# Groceries

A shared shopping list and house-stock tracker. One HTML file, no install, runs in the phone browser.

- **At home** — what you keep in the house, how many, which are critical (!), and what each store charges.
- **List** — builds itself from anything at zero, split into Critical and If budget allows. Tick an item when it's in the trolley and it goes straight back into the house.
- **Shared** — both phones use the same household code, so the list and stock stay in step.

## Setup

1. GitHub Pages serves this repo. Open `https://<username>.github.io/<repo>/groceries.html` on your phone and add it to the Home Screen.
2. Tap the gear → enter the household code and paste the config line:
   `{ "databaseURL": "https://<your-db>.firebasedatabase.app" }`
3. Do the same on the other phone with the same code and config.

## Notes

- Household code and config are stored on each phone, not in this file. Updating `groceries.html` never touches your data.
- Data is a single record in Firebase Realtime Database at `households/<code>/grocery`.
- Backup/restore from the At home tab (Export / Import).
