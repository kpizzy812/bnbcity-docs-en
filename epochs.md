# Epochs

## Deflationary Model

BNB City uses a deflationary epoch system inspired by Bitcoin's halving. As the city grows, rewards gradually decrease -- early builders earn more.

## 7 Epochs (E0--E6)

Epochs are triggered by cumulative deposits (total BNB ever deposited), not by time:

| Epoch | Deposit Threshold | Base Rate | Max Cap | Pool Tax | Total Claim Tax |
|-------|-------------------|-----------|---------|----------|-----------------|
| E0 | 0 -- 5 BNB | 5.0% | 3.0x | 3% | 13% |
| E1 | 5 -- 10 BNB | 4.5% | 2.9x | 3% | 13% |
| E2 | 10 -- 25 BNB | 4.0% | 2.8x | 4% | 14% |
| E3 | 25 -- 50 BNB | 3.5% | 2.7x | 4% | 14% |
| E4 | 50 -- 100 BNB | 3.0% | 2.6x | 5% | 15% |
| E5 | 100 -- 200 BNB | 2.5% | 2.5x | 5% | 15% |
| E6 | 200+ BNB | 2.0% | 2.4x | 6% | 16% |

**Total claim tax** = 10% fixed dev tax + pool tax for that epoch.

## Why Deposits, Not Time?

- Time passes even if the project is dead -- meaningless epoch switches
- Deposits reflect real activity and growth
- Creates urgency: "Only 2.3 BNB left until Epoch 0 ends!"
- Fully transparent: the contract stores one number (`totalEverDeposited`)

## What Changes Per Epoch

Three things compress simultaneously:

1. **Base rate decreases** -- buildings earn slower in later epochs
2. **Cap decreases** -- buildings extract less from the pool
3. **Pool tax increases** -- more of each claim returns to the pool

The compression is **gradual**: cap goes from 3.0x to 2.4x (not to 1.0x), pool tax from 3% to 6% (not to 30%). Even in Epoch 6, building is still profitable.

## What Gets Locked at Build Time

When you build, two things are **permanently fixed** for that building:
- **Cap** -- based on the current epoch's cap x your tier modifier
- **Pool tax** -- based on the current epoch

The **adaptive rate** is always global (current epoch). This prevents early buildings from permanently draining the pool at high rates.

## Epoch Lock Boost

For buildings created in Epochs 0--3, you can purchase the **Epoch Lock** boost (20% of tier deposit). This permanently locks your building's current adaptive rate, protecting it from future epoch changes. See [Boosts & Upgrades](boosts.md) for details.

## Epoch 0 Buildings = OG Status

Buildings constructed in Epoch 0 have the highest cap and lowest tax. When selling land with an Epoch 0 building, this becomes a premium -- like owning a first-edition collectible.

