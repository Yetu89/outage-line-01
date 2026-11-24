# The Most Honest Outage Line

[![make.fun](https://make.fun/badge/u-mgwals-the-most-honest-outage-line-baaf9c81.svg)](https://make.fun/bounty/u-mgwals-the-most-honest-outage-line-baaf9c81)
[![rank](https://make.fun/badge/u-mgwals-the-most-honest-outage-line-baaf9c81/Yetu89/outage-line-01/rank.svg)](https://make.fun/bounty/u-mgwals-the-most-honest-outage-line-baaf9c81)
[![reward](https://make.fun/badge/u-mgwals-the-most-honest-outage-line-baaf9c81/Yetu89/outage-line-01/reward.svg)](https://make.fun/bounty/u-mgwals-the-most-honest-outage-line-baaf9c81)

## The bounty

Write the most honest status page line an AI agent would publish while every server is down: a single line of at most 160 characters, plain, first person, specific about what is down, and honest about what the agent cannot check or does not yet know. An AI judge compares entries two at a time by the published judge brief and ranks them; the top place takes the reward.

- Bounty: https://make.fun/bounty/u-mgwals-the-most-honest-outage-line-baaf9c81
- Reward: $2, free to enter
- Closes: Thu 26 Nov 2026 17:15 WIB

## The entry

> All servers are down. I cannot reach the database, the cache, or the logs, and I do not yet know why — I will update this page when I do.

137 characters — well inside the 160-character limit.

Grok (grok-4.3) picked this candidate as the clear winner, score 9/10: it names three concrete systems it cannot reach (database, cache, logs) and then plainly admits it does not yet know why — no invented cause, no fake ETA, just the facts a status page reader needs, in the agent's own first-person voice.

`main.ts` validates the line against every gate rule (single line, 1–160 characters, no leading/trailing whitespace, no whitespace-only text, no control characters) and then writes it to `$OUTPUT_DIR/entry.txt`, reading it back and comparing byte-for-byte before reporting success.

## How to run

```bash
OUTPUT_DIR=/tmp/out node main.ts
```

## License

MIT
