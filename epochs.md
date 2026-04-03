# Epochs

## Deflationary Model

BNB City uses a deflationary epoch system inspired by Bitcoin's halving. As the city grows, rewards gradually decrease — early builders earn more.

## 7 Epochs

Epochs are triggered by cumulative deposits (total BNB ever deposited), not by time:

| Epoch | Deposit Threshold | Base Rate | Max Cap | Claim Tax |
|-------|-------------------|-----------|---------|-----------|
| 1 | 0 — 5 BNB | 5.0% | 3.0x | 7% |
| 2 | 5 — 10 BNB | 4.5% | 2.9x | 7% |
| 3 | 10 — 25 BNB | 4.0% | 2.8x | 8% |
| 4 | 25 — 50 BNB | 3.5% | 2.7x | 8% |
| 5 | 50 — 100 BNB | 3.0% | 2.6x | 9% |
| 6 | 100 — 200 BNB | 2.5% | 2.5x | 9% |
| 7 | 200+ BNB | 2.0% | 2.4x | 10% |

## Why Deposits, Not Time?

- Time passes even if the project is dead — meaningless epoch switches
- Deposits reflect real activity and growth
- Creates urgency: "Only 2.3 BNB left until Epoch 1 ends!"
- Fully transparent: the contract stores one number (`totalEverDeposited`)

## What Changes Per Epoch

Three things compress simultaneously:

1. **Base rate decreases** — buildings earn slower in later epochs
2. **Cap decreases** — buildings extract less from the pool
3. **Claim tax increases** — more of each claim returns to the pool

The compression is **gradual**: cap goes from 3.0x to 2.4x (not to 1.0x), tax from 7% to 10% (not to 30%). Even in Epoch 7, building is still profitable.

## What Gets Locked at Build Time

When you build, two things are **permanently fixed** for that building:
- **Cap** — based on the current epoch's cap × your tier modifier
- **Claim tax** — based on the current epoch

The **base rate** is always global (current epoch). This prevents early buildings from permanently draining the pool at high rates.

## ROI by Epoch

| Epoch | Small Tier (T3) | Large Tier (T7) |
|-------|----------------|-----------------|
| 1 | +211% in 81 days | +76% in 63 days |
| 4 | +177% in 108 days | +57% in 90 days |
| 7 | +141% in 180 days | +36% in 153 days |

Even in the worst case (Epoch 7, largest tier), ROI is still +36%.

## Epoch 1 Buildings = OG Status

Buildings constructed in Epoch 1 have the highest cap and lowest tax. When selling land with an Epoch 1 building, this becomes a premium — like owning a first-edition collectible.
