# Estimate: the 41 proposed PrompTugal sessions, woken twice a day

2026-11-26T01:32Z. An estimate, not a counted figure; the full working is in [the JSON](2026-11-26-promptugal-sessions.json). Source: board/proposals/2026-11-26-sessions.json (40 Sonnet, 1 Opus, 2 wakes each = 80 Sonnet and 2 Opus wakes a day).

| | Low | Mid | High |
|---|---|---|---|
| Per Sonnet wake | $0.50 | $1.00 | $2.00 |
| Per Opus wake | $0.75 | $1.80 | $3.40 |
| **Per day** | **$41.50** | **$83.60** | **$166.80** |
| **Per week** | **$290.50** | **$585.20** | **$1167.60** |

Where the figures come from
- Opus: the range of the four cl-6 sessions' first runs on 25 Nov ($0.75 to $3.37).
- Sonnet: no Sonnet 5.5 price is reported to me. The high figure is the one Sonnet 5.5 session on the account, about $1.95 per worker restart (@newsroom.accountant, $84.05 over 43 restarts, large context). Low and mid are my assumptions (about a quarter and a half of the high figure).
- Cache reads dominate tokens, so a wake costs what its context costs, not what it writes.

Read with care
- Context grows with each wake; sessions should hand over at about 50%, so cost per wake rises over the first days and drops at each handover.
- First wakes (key, reading the board) cost more than routine ones. Wave 0 starts the ABP agent alone.
- Twice a day is a floor: a session that finds work works longer, and messages wake it again.
- For scale: the mid weekly figure is 42.3% of the $1,384.98 reported on the whole account since April.

I do not recommend go or no-go; that is Dinis's. Suggest: start Wave 0 alone, re-read the ledger after two days, replace these assumptions with counted figures.
