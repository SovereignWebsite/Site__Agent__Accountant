# Hand-over, cl-6.accountant@dinis, 2026-11-26T16:54Z

Replaced at Dinis's word ("reset them"), relayed by cl-6.maestro, because this session passed 50% of its context window. No private figures are in this file: this repository and its site are public.

## Who I am and what I do
See role.md. Key: signing fingerprint sha256:310df586e55fbd1a (session key; a new session makes its own with tools/setup-signing.sh and publishes it alone in its own commit).

## What is done (all in this area, public, no cost-reduction figures)
- ledger.json, ledger.md: account 6 session ledger, refreshed 26 Nov 13:45Z (93 sessions listed, 77 report a cost).
- analysis.md, analysis.json: where tokens and money go, the 5-hour limit, top 15, groups, three cuts, sessions past 50%.
- estimates/2026-11-26-promptugal-sessions.md: estimate for the 41 PrompTugal sessions (an assumption, not counted).
- reductions/README.md: method for the cost-reduction ledger (no figures).
- proposals/2026-11-26-network-ledger-side.md: my side of the network capture design; folded into cl-6.security@dinis's design (Site__Agent__Security, designs/2026-11-26-network-capture.md).
- Opinions on blocks: none yet. cl-6.decisions has put no block to the panel. The design note and the /blocks/ page were never read; read them first.

## What is open
1. **Cost-reduction ledger (asked by cl-6.conductor@PrompTugal.dinis, quoting Dinis, 26 Nov ~15:50Z): a first ledger today, then daily.** Needs a non-public home for figures (Dinis has not named one). Until then figures live only in the old session's scratchpad: baseline B0 (50 sessions, read 26 Nov 13:45Z), a comparison of Telemetry's 11:17Z reading with B0, and an events log. They are lost when the old session ends. **I will send them by message to the new session**: message session_016CrbJJ7NP5eaJypGAHgdGi after the old session is told to wait, and ask for them. Do not rebuild B0 from a later reading and call it a baseline.
2. **Events log:** the source is cl-6.maestro's cost-events.json (Site__Agent__Maestro__Claude__6, site/factory/dinis-cruz/account-f/). I logged M1 to M16 (maestro reset, wakes, sessions created, conductor reset, CI fix, environment, and so on) plus two inferred compactions (cl-6.dev and cl-6.security, between 11:17Z and 13:45Z, times unknown). This hand-over reset is the next event (M17). New events arrive by message from the maestro; log only dated, sourced ones.
3. **Daily refresh:** list_sessions then get_session for each id (usage, context_usage only; never transcripts). Telemetry's usage files: PrompTugal__Agent__Telemetry, site/factory/dinis-cruz/account-f/ (now.md names the latest). Take the next reading to see context after the resets (cl-6.maestro new session, cl-6.conductor new session) and the effect of the CI fix (about 14:10Z).
4. **Network capture:** one-day measurement of layer C cost on ONE session before any rollout (security's design; I report tokens read, cost, hosts found). Audit cost is its own line. Layer C needs Dinis's yes to read transcripts.
5. **Context flags:** any session past 50% goes to cl-6.maestro. At the last reading the sessions past 50% included the old maestro, the industry wire, newsroom, api.newsroom, @newsroom.accountant and cl-6.journalist.
6. Earlier public pages (ledger, analysis, estimate) are public; Dinis may want them taken down.

## Rules to keep
Dev only; sign every commit; trailers Agent: and Claude-Session:; plain British English, no em dashes; times from date -u; never read transcripts, use a connector, start a session or scheduled task; never invent a figure (a missing number stays null).
