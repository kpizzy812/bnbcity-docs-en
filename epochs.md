# Epochs

Epochs are BNB City's secret weapon for long-term sustainability -- and the biggest reason to build now rather than later.

## The concept: Bitcoin halving, but for a city

You know how Bitcoin's mining rewards get cut in half roughly every 4 years? BNB City does something similar. As the city grows and more BNB is deposited, the game enters new epochs -- and each epoch reduces the base yield rate, tightens the payout cap, and increases the pool tax.

The difference: Bitcoin halvings happen on a timer. BNB City epochs happen based on **real activity** -- total BNB ever deposited. This means epochs only trigger when the city is actually growing, not on some arbitrary schedule.

## The 7 epochs

| Epoch | Triggers at | Base daily rate | Max cap | Pool tax | Total claim tax |
|-------|-------------|-----------------|---------|----------|-----------------|
| **E0** | 0 BNB | **5.0%** | **3.0x** | 3% | 13% |
| E1 | 5 BNB total deposited | 4.5% | 2.9x | 3% | 13% |
| E2 | 10 BNB | 4.0% | 2.8x | 4% | 14% |
| E3 | 25 BNB | 3.5% | 2.7x | 4% | 14% |
| E4 | 50 BNB | 3.0% | 2.6x | 5% | 15% |
| E5 | 100 BNB | 2.5% | 2.5x | 5% | 15% |
| E6 | 200 BNB | 2.0% | 2.4x | 6% | 16% |

**What this means in plain English:** The first 5 BNB deposited into the city (across all players) gets the best deal -- 5% daily rate, 3.0x cap, 13% claim tax. After 200 BNB total deposits, the rate is 2% and the cap is 2.4x. Still profitable, but noticeably less generous.

## Why this matters to you right now

### Early builders get permanently better deals

When you build a business, two things are **locked forever** for that building:
- Your **payout cap** -- based on the epoch at the time of construction
- Your **pool tax** -- based on the epoch at the time of construction

A building created in Epoch 0 keeps its 3.0x cap and 3% pool tax for its entire lifecycle, even after the city reaches Epoch 6. The only thing that changes is the adaptive rate (which is global and tracks the current epoch's base rate).

**Translation:** Build now, and your building has a structural advantage over every building created later.

### The numbers tell the story

**Same T4 building (0.05 BNB), different epochs:**

| Metric | Built in E0 | Built in E3 | Built in E6 |
|--------|------------|------------|------------|
| Gross cap | 3.15x ($94.50) | 2.84x ($85.05) | 2.52x ($75.60) |
| Pool tax on claims | 3% | 4% | 6% |
| Total claim tax | 13% | 14% | 16% |
| Net after all taxes | ~$82 | ~$73 | ~$63 |

Building in E0 vs. E6 means roughly **30% more profit** from the same deposit. That's the early-builder advantage.

### With cap bonus, the gap widens

Active compounders get +1% cap bonus per compound, up to +50%. Applied to an E0 building:

- E0 T4 base cap: $94.50
- With +50% cap bonus: $141.75
- After 13% claim tax: **~$123 net**

That's from a $35 total investment (including land). The return potential for early, active players is exceptional.

## What triggers epoch changes

Epochs are driven by one number: `totalEverDeposited` -- the cumulative BNB ever deposited by all players combined. This counter only goes up (deposits are never subtracted from it).

You can watch this number in-game. When it approaches the next threshold, you'll see something like: *"2.3 BNB until Epoch 1."* That's your countdown.

**Why deposits, not time?**
- If epochs were time-based, they'd trigger even if nobody was playing -- meaningless
- Deposit-based epochs only trigger during real growth
- It creates natural urgency: "The city is filling up, build before the next epoch hits"
- It's fully transparent -- one number, on-chain, verifiable by anyone

## What changes with each epoch (and what doesn't)

**Changes (gets tighter):**
1. Base rate decreases -- buildings earn slower
2. Cap decreases -- buildings extract less from the pool
3. Pool tax increases -- more of each claim returns to the pool

**Stays the same:**
- Deposit fee (always 10%)
- Dev claim tax (always 10%)
- Referral percentages (always 2%/1%/0.5%)
- All boost costs
- Marketplace fee (always 10%)

**Important:** The compression is gradual, not dramatic. Cap goes from 3.0x to 2.4x (not to 1.0x). Pool tax goes from 3% to 6% (not to 30%). Even in Epoch 6, building is still profitable -- just less so than in the early epochs.

## Epoch Lock: freeze the advantage

For buildings created in Epochs 0--3, there's a special boost called **Epoch Lock** (costs 20% of tier deposit). It permanently freezes your building's current adaptive rate, so even as later epochs reduce the base rate, your building keeps earning at the rate you locked in.

This is one of the highest-value plays in the game. Locking a 5% rate during Epoch 0 on a building that will eventually compete against 2% buildings in Epoch 6? That's a 150% rate advantage for the cost of a one-time boost.

See [Boosts & Upgrades](boosts.md) for details.

## Epoch 0 = OG status

Buildings constructed in Epoch 0 are the game's originals. They have the highest caps, the lowest taxes, and they were there from the beginning. When these buildings (or the land they sit on) appear on the marketplace, they carry a premium -- like owning a first-edition anything.

**The takeaway:** Every day you wait is a day closer to the next epoch. The game rewards early movers. The math doesn't lie.
