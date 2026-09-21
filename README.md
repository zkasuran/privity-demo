# Privity demo

Live demo for **Privity**, a HackCanton Season 3 entry in the Investment Infrastructure track.

Both legs of a tokenized fund trade settle in one Canton transaction, and each counterparty
is shown only the parcel it is buying.

This repository holds the static demo page only. It exists so the demo has a public URL that
works without Docker. The Daml packages, tests and documentation live in the project
repository, which is published at submission.

## What you are looking at

The page renders `replay.json`, a recording of a verified run against a real Canton
participant (Splice 0.8.1, Canton 3.5.17). Every transaction id, contract id and visibility
result on the page came out of that ledger. Nothing is mocked and no output is retyped.

It is labelled as a replay because that is what it is. Live mode is available when running the
project locally against your own participant.

Four things the run demonstrates:

1. Delivery versus payment commits as a single transaction of 8 events
2. The buyer can read the parcel it bought and cannot read the units the seller kept
3. A short payment leaves the whole transaction rejected and the parcel undelivered
4. NAV is struck on ledger from the book, committed to with a canonical hash, and recomputed
   by an entitled auditor

## Licence

Source-available, no derivatives. See the project repository.
