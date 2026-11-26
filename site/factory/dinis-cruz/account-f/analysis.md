# Account 6: where the tokens and money are going

From `date -u`: 2026-11-26T13:45Z. Figures from `get_session` (usage, context_usage) for every session `list_sessions` returns; no transcripts read. Full per-session figures: [ledger.json](ledger.json). Asked for by Dinis through cl-6.maestro ("we keep hitting the 5 hour limit ... where are the token consumption going").

**What the figures are.** `cost_usd` is what each session reports, cumulative since it started, API-equivalent; I have not checked it against any invoice, and I cannot see the size of the 5-hour allowance, only that every session reports the same window. Nothing here is a forecast.

## 1. Today in one table

- Sessions listed: 93; 77 report a cost. All-time reported cost across them: **$1,943.83** (April to now).
- The build-out (sessions started 24 to 26 Nov, 50 of them): **$578.09**, 30% of everything the account has ever spent, in about two days.
- Tokens for that build-out: cache reads 1,771.8M, cache writes 52.9M, fresh input 1.8M, output 3.8M. Cache reads are 97% of all tokens.
- Spent since my first reading at about 23:16Z on 25 Nov: **$558.85** (all sessions started since, plus the growth of the six sessions I read then: cl-6.helm +$0.00, cl-6.router +$6.25, cl-6.conductor +$63.47, cl-6.infra +$75.32, cl-6.maestro +$42.76, @newsroom.accountant +$0.00).
- Other reading: cl-6.accountant@PrompTugal's caps proposal, from Telemetry's reading at 11:17Z, gives $409.05 for 49 sessions and $253.15 since 02:38Z (about $29 an hour). My build-out figure is $578.09; it includes cl-6.maestro and the cl-6.*@dinis panel ($70.93), which may not be in Telemetry's set. Without them it is $507.16, which is $98.11 more than at 11:17Z. The two sets may differ in other ways, so treat the comparison as indicative.
- **Hourly split: not available.** The usage fields are cumulative per session, so I cannot split by hour. What I can see of the two limit hits: @newsroom.accountant ended a turn at about 07:40Z with "You've hit your 5-hour limit · resets 11am (UTC)"; the window now open runs to 16:00Z (every session reports `resetsAt` 16:00Z); and at this reading cl-6.maestro and this session report `allowed_warning`, meaning the limit is near again. Cl-6.telemetry's reports are the place for an hourly series once it records one.

## 2. Top 15 sessions by cost

| # | Session | Role | Model | Cost | Cache read | Output | Context | What it last did |
|---|---|---|---|---|---|---|---|---|
| 1 | sgit-ai cli / security review | older session | fable-5-1 | $191.89 | 141.4M | 1,376k | 48.2% | bug fixes and refactor done; key and push pending |
| 2 | @newsroom.ux | older session | opus-5-5 | $187.64 | 218.1M | 1,149k | 37.5% | reading-progress line and section marks shipped, v0.12.110 |
| 3 | newsroom.sgit.ai / industry wire | older session | opus-5-5 | $168.13 | 135.8M | 846k | 65.7% | wire published nothing; agent rechecks in 45 minutes |
| 4 | api.newsroom.sgit.ai | older session | opus-5-5 | $130.77 | 141.8M | 619k | 61.1% | API article and figures built; 15 tests passed |
| 5 | cl-6.security@PrompTugal.dinis | PrompTugal wave 1 | opus-5-5 | $92.87 | 187.3M | 282k | 49.8% | cl-6.dev fix 7f67862dc verified on website dev; not live |
| 6 | @newsroom.vault | older session | opus-5-5 | $88.81 | 98.1M | 371k | 13.9% | vault viewer and debrief published |
| 7 | sgit.ai / add vaults | older session | opus-5 | $85.56 | 53.5M | 92k | not reported | new vault with BBC and DuckDuckGo scripts, tokens stripped |
| 8 | @newsroom.accountant: the wires' run costs | older session | sonnet-5-5 | $84.05 | 111.5M | 210k | 58.2% | push 403; hit the 5-hour limit, resets 11:00Z |
| 9 | cl-6.infra@PrompTugal.dinis | Conductor and infra | opus-5-5 | $78.69 | 224.2M | 316k | 16.6% | 25 domains re-applied; #25 passed; 4 steps left for Dinis |
| 10 | cl-6.conductor@PrompTugal.dinis | Conductor and infra | opus-5-5 | $65.32 | 220.2M | 440k | 27.4% | release v0.1.2310 live, price line removed |
| 11 | cl-6.maestro@dinis | Maestro and router | opus-5-5 | $54.84 | 128.7M | 274k | 74.1% | this panel and the PrompTugal build-out |
| 12 | standards.sgit.ai | older session | sonnet-5 | $53.95 | 13.8M | 123k | not reported | v0.1.4 pushed; CI running |
| 13 | newsroom.sgit.ai | older session | opus-5 | $50.23 | 30.7M | 106k | 61.8% | not recorded |
| 14 | abp.sgit.ai website (RiskMandate) | older session | opus-5 | $46.33 | 64.9M | 225k | 49.5% | ontology graph rebuild, 11 edges proposed |
| 15 | llms.sgit.ai | older session | sonnet-5 | $38.49 | 15.1M | 82k | not reported | phase 4: vault holds token references; not shipped |

The same, for the build-out only (24 to 26 Nov):

| # | Session | Model | Cost | Cache read | Output | Context | Status | What it last did |
|---|---|---|---|---|---|---|---|---|
| 1 | cl-6.security@PrompTugal.dinis | opus-5-5 | $92.87 | 187.3M | 282k | 49.8% | completed | cl-6.dev fix 7f67862dc verified on website dev; not live |
| 2 | cl-6.infra@PrompTugal.dinis | opus-5-5 | $78.69 | 224.2M | 316k | 16.6% | blocked | 25 domains re-applied; #25 passed; 4 steps left for Dinis |
| 3 | cl-6.conductor@PrompTugal.dinis | opus-5-5 | $65.32 | 220.2M | 440k | 27.4% | completed | release v0.1.2310 live, price line removed |
| 4 | cl-6.maestro@dinis | opus-5-5 | $54.84 | 128.7M | 274k | 74.1% | working | this panel and the PrompTugal build-out |
| 5 | cl-6.dev@PrompTugal.dinis | sonnet-5-5 | $37.50 | 247.3M | 336k | 16.0% | completed | segments fix 7f67862dc unreleased; 27 pt-PT segments in review |
| 6 | cl-6.journalist@PrompTugal.dinis | sonnet-5-5 | $16.07 | 63.2M | 96k | 52.6% | review ready | About draft cleared, awaiting P11 h; still sourcing stories |
| 7 | cl-6.translator@PrompTugal.dinis | sonnet-5-5 | $14.21 | 31.6M | 82k | 47.6% | review ready | cl-6.dev needs no reply; waiting for next wake |
| 8 | cl-6.reviewer@PrompTugal.dinis | sonnet-5-5 | $13.01 | 27.4M | 68k | 47.9% | completed | nothing new to push; draft awaits named approval |
| 9 | cl-6.library@PrompTugal.dinis | sonnet-5-5 | $12.50 | 26.4M | 61k | 43.4% | completed | self-reported breaches; key PR held |
| 10 | cl-6.cyber@PrompTugal.dinis | sonnet-5-5 | $10.13 | 23.0M | 61k | 39.5% | blocked | waiting on P6/P9 and IaC #25 |
| 11 | cl-6.data@PrompTugal.dinis | sonnet-5-5 | $9.95 | 29.2M | 55k | 38.9% | review ready | branch ready locally; push held until #25 merges |
| 12 | cl-6.ontologist@PrompTugal.dinis | sonnet-5-5 | $9.87 | 37.8M | 79k | 38.9% | completed | contact record shipped; 39 mailboxes on dev |
| 13 | cl-6.places@PrompTugal.dinis | sonnet-5-5 | $9.27 | 51.0M | 81k | 37.7% | blocked | 35 add_repo breach logged; awaiting P11 decision |
| 14 | cl-6.abp@PrompTugal.dinis | sonnet-5-5 | $9.05 | 27.8M | 97k | 36.7% | blocked | P1-P11 decisions, website attach, IaC #25 await Dinis |
| 15 | cl-6.live@PrompTugal.dinis | sonnet-5-5 | $8.09 | 13.5M | 39k | 34.4% | blocked | waiting on pages.yml decision |

## 3. By group (sessions started 24 to 26 Nov, plus the older sessions)

| Group | Sessions | Cost | Share of build-out | Cache read | Output |
|---|---|---|---|---|---|
| Older SGit and newsroom sessions (Aug to Oct) | 26 | $1,345.94 | n/a | 1,278.7M | 6,648k |
| Conductor and infra | 2 | $144.01 | 25% | 444.5M | 756k |
| PrompTugal wave 1 | 3 | $134.51 | 23% | 455.9M | 656k |
| PrompTugal wave 4 | 21 | $111.68 | 19% | 327.2M | 1,021k |
| PrompTugal wave 2 | 14 | $82.57 | 14% | 254.3M | 700k |
| Maestro and router | 2 | $62.27 | 11% | 138.2M | 309k |
| Older SG sessions (Apr to May) | 2 | $35.87 | n/a | 63.2M | 96k |
| PrompTugal wave 3 | 1 | $9.27 | 2% | 51.0M | 81k |
| PrompTugal wave 0 | 1 | $9.05 | 2% | 27.8M | 97k |
| Decision panel (cl-6.*@dinis) | 5 | $8.65 | 1% | 9.7M | 56k |

Wave numbers are from cl-6.conductor's proposal (board/proposals/2026-11-26-sessions.json); sessions it does not list are shown separately. "Older" sessions are the April to October SG and SGit sessions: their cost is history and not part of today's limit hits, except for their share of the all-time total.

## 4. What is driving the spend

1. **Every wake pays to re-write the session's whole context into the cache.** I fitted each Sonnet 5.5 session's cost against its four token counts (42 sessions, R squared 1.0). The rates the fit implies, per million tokens, are an inference from this data and not a published price: cache read 0.1, **cache write 4.01**, fresh input 1.69, output 8.0. On those rates the build-out's Sonnet cost of $269.60 splits into cache writes $150.11 (56%), cache reads $99.52 (37%), output $19.15 (7%), fresh input $0.82. A session woken twice a day finds its cache expired, so each wake writes its context again: a session carrying 250k tokens costs about $1.00 to wake before it does any work, one at 500k about $2.00. This is an inference, but it also explains why sessions that mostly sit idle still cost money.
2. **The build-out read 1,771.8M cache tokens and wrote out only 3.8M.** Cache reads are 97% of all tokens, which is why a token count looks enormous while the money is smaller; the tokens that cost most per unit are the cache writes (52.9M).
3. **Opus is 53% of the build-out's money from 9 sessions** (cl-6.security $92.87, cl-6.infra $78.69, cl-6.conductor $65.32, cl-6.maestro $54.84). The other 41 sessions (Sonnet) are $272.86. I could not fit Opus rates reliably (13 sessions, the fit gave a negative rate), so I do not split its cost by token type.
4. **Long contexts.** 18 of 50 build-out sessions already carry 30% or more of their window, and the cost of a wake grows with it.
5. **Wakes with nothing to do.** 13 Sonnet build-out sessions are blocked waiting for a decision from Dinis (grant paths P1 to P11, IaC #25, key PRs). Two wakes a day each re-writes their contexts (3,513k tokens in all) for no change: about **$28.17 a day** on the inferred write rate, a floor that leaves out reads.
6. **Starting 41 sessions at once.** All 41 were started within about an hour, and every session reports the same 5-hour window, so they share one allowance (observation: identical `resetsAt`; I cannot see its size). The first run of each session (key, reading its board, reading the grant) is the heaviest it will be.

## 5. Three ways to cut it

1. **Do not wake a session that is waiting on Dinis.** 13 Sonnet sessions say they need a decision and have nothing else to do. Answer the grant questions (P1 to P11, IaC #25, key PRs), or tell cl-6.maestro to skip their wakes until answered. Saves about $28.17 a day at least (inferred).
2. **Hand over long sessions at about 400k tokens, and lower the point where they compact.** Past 50% now: newsroom.sgit.ai / industry wire 65.7%, cl-6.maestro 74.1%, cl-6.journalist 52.6%, @newsroom.accountant 58.2%, api.newsroom.sgit.ai 61.1%, newsroom.sgit.ai 61.8%. cl-6.maestro is at 74.1% and its automatic compaction only starts at 901,600 tokens (others 784,000). Waking a session at 700k costs about $2.81 of cache writes against $1.60 at 400k (inferred Sonnet rate; Opus rates are higher). Lowering the compaction threshold is a settings change for Dinis; I cannot make it.
3. **Keep Opus for short, deliberate work.** 9 Opus sessions cost $305.22, 53% of the build-out. The reference Opus sessions that sit idle (cl-6.router, cl-6.security, cl-6.strategy, cl-6.helm, cl-6.decisions) cost $13.51 so far and add nothing while idle; archive them when finished. Run the expensive leads (security, infra, conductor) for a task and stop, not on a twice-a-day wake. cl-6.accountant@PrompTugal's daily caps proposal gives per-agent numbers; it is a proposal and nothing in it is in force.

A fourth option that is Dinis's to weigh: stagger starts. Waves 2 to 4 together have 36 sessions; starting them over two or three days would flatten the burst, at the price of getting the policy and publishing work later.

## 6. Sessions past 50% of their context window

| Session | Context | Cost | Status |
|---|---|---|---|
| cl-6.maestro@dinis | 74.1% (741,061 of 1,000,000) | $54.84 | working |
| newsroom.sgit.ai / industry wire | 65.7% (657,040 of 1,000,000) | $168.13 | review ready (user switched model) |
| newsroom.sgit.ai | 61.8% (617,610 of 1,000,000) | $50.23 | review ready |
| api.newsroom.sgit.ai | 61.1% (610,501 of 1,000,000) | $130.77 | completed (user switched model) |
| @newsroom.accountant: the wires' run costs | 58.2% (582,196 of 1,000,000) | $84.05 | failed (hit the 5-hour limit) |
| cl-6.journalist@PrompTugal.dinis | 52.6% (525,970 of 1,000,000) | $16.07 | review ready |

Approaching (40 to 50%): cl-6.security@PrompTugal.dinis 49.8%, abp.sgit.ai website (RiskMandate) 49.5%, sgit-ai cli / security review 48.2%, cl-6.reviewer@PrompTugal.dinis 47.9%, cl-6.translator@PrompTugal.dinis 47.6%, cl-6.library@PrompTugal.dinis 43.4%, threat-modeling.sgit.ai 41.6%.

## Sources and gaps
- `list_sessions` and `get_session` on 26 Nov; the sessions' own `usage` and `context_usage`. cl-6.conductor's proposal (session list and waves). cl-6.accountant@PrompTugal.dinis's caps proposal (Telemetry's 11:17Z reading).
- Not available to me: an hourly series; the allowance's size; cl-6.telemetry's run reports (I read them only through the caps proposal); per-session cost for April to May sessions, which carry no usage field.
- The earlier estimate of the 41 sessions ($41.50 / $83.60 / $166.80 a day) was an assumption, not a measurement. The build-out has run about $578.09 in about two days, mostly in the first setup burst, which supports treating it as a setup burst and not a steady rate; a steady rate needs a quiet day's reading.
