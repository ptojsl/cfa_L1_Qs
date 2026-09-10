# CFA Level I Burn-Down

A single-file study tracker for the CFA Level I question bank. Counts what is
left across all 11 Practice topics plus the 16 mock exam sessions, works out the
daily pace needed to finish before the exam, and tracks mock scores.

Everything lives in `index.html` — no build step, no dependencies, no server.

## Publishing it on GitHub Pages

1. Create a new repository (public or private — Pages works with both on paid
   plans; public is simplest).
2. Upload `index.html` to the root of the repo.
3. **Settings → Pages → Build and deployment**, set Source to *Deploy from a
   branch*, branch `main`, folder `/ (root)`. Save.
4. Wait a minute. The site appears at
   `https://<your-username>.github.io/<repo-name>/`.

Bookmark that URL. On a phone, open it and use Share → Add to Home Screen.

## Where your data lives

In your browser's `localStorage`, under the key `cfa-l1-burndown-v1`. It never
leaves your machine and is never sent anywhere.

That means it is **per browser and per device**. Your laptop and your phone keep
separate copies. Clearing site data, or a private window, wipes it.

So: press **Export** now and then. It downloads a JSON file of everything.
**Import** loads one back — that is also how you move progress from one device
to another.

`progress.json` in this repo is a starting snapshot as of 5 September 2026.
Import it on first run so you begin from the right numbers.

## Using it

- **Just did N questions in X** — the quick-add bar at the top of the topic
  table. It adds to the running total so you never work out the new number.
- The number field on each row is the running total if you would rather set it
  directly. **All** marks a topic complete.
- **Undo / Redo**, or Ctrl/⌘+Z, reverses anything — including an accidental
  "All" and an import.
- Mock sessions: tap one to mark it done, or type a score and it marks itself.
- **Days/week** changes the pace maths. It defaults to 6.
- **Exam-day sheet** — the button in the bottom-right corner.

## The numbers behind it

Question counts were taken from the CFA Institute Learning Ecosystem
(Practice › CFA Program Level I 2026) on 5 September 2026: 2,958 topic questions
across 11 topics, plus 16 mock sessions of 90 = 1,440. Whole bank: 4,398.

Exam topic weights are the published 2026 Level I ranges, unchanged from 2025.
The plan line runs from 1,251 answered on 5 September to the full bank by
15 November 2026, the day before the exam.

If CFA Institute changes the bank, edit the `TOPICS` array near the top of the
script block in `index.html` — each entry has the topic's total, module count,
exam weight and its largest module.
