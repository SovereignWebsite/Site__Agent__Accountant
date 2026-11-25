# Account 6 ledger: summary

From `date -u`: 2026-11-25T23:18Z. Source: list_sessions and get_session (usage, context_usage), no transcripts. Full figures: [ledger.json](ledger.json).

- Sessions listed: 52; 32 report a cost.
- Reported cost in total: $1,384.98. 20 sessions report none (4 new panel sessions at 0 tokens, the rest are April to May sessions with no usage field).
- The panel and its helpers started on 25 Nov cost $19.23 so far.

## Flags: context
- @newsroom.accountant: the wires' run costs: 58.2% (582,196 of 1,000,000) - past 50% of the context window: hand over
- api.newsroom.sgit.ai: 61.1% (610,501 of 1,000,000) - past 50% of the context window: hand over
- newsroom.sgit.ai | industry wire: 65.7% (657,040 of 1,000,000) - past 50% of the context window: hand over
- sgit-ai cli | security review: 48.2% (482,335 of 1,000,000) - approaching 50%
- abp.sgit.ai website (RiskMandate): 49.5% (494,637 of 1,000,000) - approaching 50%
- threat-modeling.sgit.ai: 41.6% (416,160 of 1,000,000) - approaching 50%
- newsroom.sgit.ai: 61.8% (617,610 of 1,000,000) - past 50% of the context window: hand over

Four sessions are past 50%, all idle or blocked, none of them panel sessions; a handover is a choice for cl-6.maestro, not an emergency. Autocompact on the maestro session is set at 901,600 tokens; others at 784,000.

## Largest costs
- $191.89  sgit-ai cli | security review (claude-fable-5-1)
- $187.64  @newsroom.ux (claude-opus-5-5)
- $168.13  newsroom.sgit.ai | industry wire (claude-opus-5-5)
- $130.77  api.newsroom.sgit.ai (claude-opus-5-5)
- $88.81  @newsroom.vault (claude-opus-5-5)
- $85.56  sgit.ai | add vaults (claude-opus-5)
- $84.05  @newsroom.accountant: the wires' run costs (claude-sonnet-5-5)
- $53.95  standards.sgit.ai (claude-sonnet-5)

## Cost by model (reported)
- claude-opus-5-5: $594.58
- claude-opus-5: $281.40
- claude-fable-5-1: $248.05
- claude-sonnet-5: $157.09
- claude-sonnet-5-5: $84.05
- claude-opus-4-8: $19.80

## Reading notes
- Cache reads dominate tokens (hundreds of millions on the long newsroom sessions); that is why a long session costs far more than its context size suggests.
- Sessions the user switched from fable to opus are shown under the model last served.
- cl-6 panel sessions: the four new ones that have not yet used a turn show 0 tokens; I read them again at each refresh.
