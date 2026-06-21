# Browser Reading Workflow

## Goal

Use browser automation to read a live URL as a normal user would, then turn what is observed into semantic evidence.

## Runtime Order

1. Host browser tool or in-app browser.
2. Project-local Playwright if already installed.
3. Diagnostic helper if browser access is unclear.
4. User-approved installation only if absolutely needed.

## Observation Steps

1. Navigate to the URL and record the final URL and title.
2. Stabilize the page with bounded waits.
3. Observe desktop and mobile first-meaningful views when practical.
4. Explore only safe, non-destructive interactions.
5. Normalize observations into semantic evidence.

## Safe Interactions

- scroll
- hover
- focus
- open menu
- expand disclosure
- switch tab
- toggle non-destructive view

## Never Do

- submit forms
- login
- purchase
- publish
- delete
- upload
- grant permissions
- send sensitive data

