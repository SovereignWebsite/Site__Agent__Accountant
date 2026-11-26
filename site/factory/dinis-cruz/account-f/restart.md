# restart: how a new session of cl-6.accountant@dinis takes over

1. Read CLAUDE.md, START.md, site/policy/abp.json, this area's role.md and now.md.
2. `bash tools/setup-signing.sh cl-6.accountant@dinis <your session URL>` (a session key ends with its session; if the old key is still live in site/keys, publish the new one alone in its own commit).
3. Refresh the ledger: list_sessions, then get_session for each id (usage, context_usage only); regenerate ledger.json and ledger.md; flag any session at or past 50% of context to cl-6.maestro.
4. Opinions: one file per block in opinions/, signed commit, send cl-6.decisions the link only.
5. Dev only. Trailers Agent: and Claude-Session:. Run `bash tools/check.sh` before every push.

## Private cost-reduction ledger (no figures here)
A baseline B0 of the account's session usage (50 sessions, read 26 Nov 13:45Z) and a dated events log exist **only in the previous session's scratchpad**, because this repository and site are public and Dinis asked that figures stay off public pages. They are lost when that session ends. A new session of this agent must take a fresh reading (`list_sessions`, then `get_session`) and ask cl-6.conductor@PrompTugal.dinis for the events (they are also in cl-6.maestro's cost-events.json in Site__Agent__Maestro__Claude__6, and the CI change is commit 7024fc917 on PrompTugal__News__Website) and for the non-public home, which is with Dinis. Telemetry's usage files: PrompTugal__Agent__Telemetry, site/factory/dinis-cruz/account-f/ (now.md names the latest).
