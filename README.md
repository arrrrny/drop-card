# DROP CARD
## MISS, BUT LOUD

Software tells you when you are wrong. It screams on a failed test, a thrown
exception, a red build. It assumes the miss is a defect to be fixed and
forgotten.

That assumption is small. A mis-fire is not always a mistake. Sometimes the code
did exactly what it does, you expected something else, and what actually happened
is the interesting part. The unexpected outcome is where the real discoveries
hide.

A DROP CARD is how you catch it instead of stepping over it.

## THE RULE

At the gym, when an agent first enters, it is handed this instruction: if at any
point there is a mis-fire, STOP. Do not push through. Do not fix it silently.
Drop a card.

The card is one sentence, filled in by the agent:

    I did X, expecting Y and Z happened, SO I DROPPED.

- X — what you did
- Y — what you expected
- Z — what actually happened

That is the whole capture. No root-cause required. No blame. The card is a
receipt for an unexpected moment.

## WHERE IT DROPS

By default, a drop is REDUNDANT — it lands in two places:

1. A local file: `drops/DROP-<agent>-<date>.md`
2. A GitHub issue: the same card, opened where the work lives

Two copies, one truth. The folder is the archive you keep. The issue is the
signal that pulls a human's eyes to it. A mis-fire deserves extra attention, so
we make sure it gets some.

## WHY

A mis-fire is not a mistake. It is a signal. The outcome you did not predict can
be a huge discovery — a behavior nobody documented, a path nobody walked, a
feature hiding in the gap between intent and result. Step over it and it is gone.
Drop it and it becomes something you can study.

We are always open to growth. The drop card is how the system grows: it keeps the
misses instead of burying them.

## THE FORMAT

    I did <X>, expecting <Y> and <Z> happened, SO I DROPPED.

Fill it. Drop it. Move on sharper than you came in.

## RUN IT

    node drop.mjs --agent <id> --did "<X>" --expected "<Y>" --happened "<Z>" \
                  [--where "<context>"] [--discovery]

The helper writes `drops/DROP-<agent>-<date>.md` and opens a GitHub issue if `gh`
is present. The GYM this slots into lives at
[github.com/arrrrny/gym](https://github.com/arrrrny/gym).

WTF or nothing.
