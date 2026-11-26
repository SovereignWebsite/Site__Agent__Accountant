# Cost-reduction ledger for account 6: method only

Asked for by cl-6.conductor@PrompTugal.dinis on 26 Nov 2026 (about 15:50Z), quoting Dinis. This repository and its published site are public, and Dinis asked that the figures stay out of public pages until he says what can be published. So **no figures are committed here**: only the method. The figures are held privately by cl-6.accountant@dinis until Dinis names a non-public home for them (open question, sent to the conductor).

## Method
1. **Baseline B0:** cumulative tokens (cache read, cache write, input, output), cost and context per session from `get_session`, taken before a change. Per-wake figures need two readings of the same session either side of a wake; the first per-wake baselines come from the second reading.
2. **Events:** each change is a dated row with a source: session resets (session, time, context before and after), moves to Sonnet, fewer wakes, the CI speed-up (11.3 to about 5.3 minutes), sub-agents stopped. A change with no date or source is listed as named, not dated.
3. **Effect:** cost and tokens per day and per wake, before against after, for the sessions the change touched, with a comparison group that did not change. A reset is seen as a fall in a session's context between two readings, or a new session id.
4. **Uncertainty:** cost is the sessions' own reported API-equivalent figure; readings are hours apart, so a change is placed within a reading interval; the wake count comes from Telemetry; work mix changes between days.
5. **Cost per useful output:** the unit is a site release, a published article, a reviewed fact, counted from the website's release counter and Telemetry; cost per unit before and after, so a saving from doing less is not reported as a saving.
6. **Cadence:** a first ledger today, then daily, each reading dated from `date -u`.

Status at the time of writing: baseline B0 taken; events E0 to E4 named by Dinis, none yet dated; Telemetry's files not yet located (path asked of cl-6.telemetry).
