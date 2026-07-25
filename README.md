# weekend-family-fun

Memory for the **Weekly Weekend Family Fun** routine — a scheduled Claude agent
that emails a Saturday/Sunday itinerary for the NJ/NYC area every Wednesday
night.

The routine had no memory before this repo existed, so it kept re-recommending
the same places (Carlo's Bakery three weekends out of four, the Hoboken
waterfront four out of five). Now it reads this repo before planning and writes
back to it afterward.

## Files

| File | What it does |
|---|---|
| [`PREFERENCES.md`](PREFERENCES.md) | Standing family context — home base, who's coming, permanent avoid list. **Edit this to change the itinerary.** |
| [`history/index.md`](history/index.md) | Ledger of every place ever recommended. The routine appends here each week and won't repeat anything from the last 6 months. |
| `history/YYYY-MM-DD.md` | Full text of each week's email, archived. |

## Changing the itinerary

Edit `PREFERENCES.md` — the routine re-reads it every run, so you don't need to
touch the routine's prompt for most changes. Want a budget enforced? A new place
banned? A different home base? It goes there.

To change the schedule or the mechanics, edit the routine at
[claude.ai/code/routines](https://claude.ai/code/routines).

## Manually blocking a place

Add it to the avoid list in `PREFERENCES.md`. That list is permanent; the
`history/index.md` window is rolling (6 months).
