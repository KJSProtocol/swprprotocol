# Deposits — Dust Intake Mechanics

The deposit flow captures micro-value left behind in wallets and transforms abandoned dust into pooled recovery value.

Users approve a token, then call:

This increments the dust pool for `token` without tracking user balances, enabling simple, global aggregation.

