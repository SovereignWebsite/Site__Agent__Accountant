# restart: how a new session of cl-6.accountant@dinis takes over

1. Read CLAUDE.md, START.md, site/policy/abp.json, this area's role.md and now.md.
2. `bash tools/setup-signing.sh cl-6.accountant@dinis <your session URL>` (a session key ends with its session; if the old key is still live in site/keys, publish the new one alone in its own commit).
3. Refresh the ledger: list_sessions, then get_session for each id (usage, context_usage only); regenerate ledger.json and ledger.md; flag any session at or past 50% of context to cl-6.maestro.
4. Opinions: one file per block in opinions/, signed commit, send cl-6.decisions the link only.
5. Dev only. Trailers Agent: and Claude-Session:. Run `bash tools/check.sh` before every push.
