# Core Mechanics

## How Yield Works

Every building generates daily yield based on a per-tier formula:

```
Daily earnings = Principal x effectiveRate x (Productivity / 100)
```

Where:
- **Principal** -- your building's current power (initial deposit after fee, grows with compounds)
- **effectiveRate** -- calculated per-tier: `adaptiveRate x TIER_RATE_MOD[tier] / 100`
- **Productivity** -- your building's productivity level (0% to 500%)

This means different tiers earn at different speeds. A T0 building earns 20% faster than T4, while a T7 building earns 45% slower.

## Adaptive Rate (City Prosperity)

The base daily rate self-adjusts based on the health of the city's economy:

```
adaptiveRate = baseRate x (contractBalance / activeDeposits)
```

- When the pool is healthy (more BNB than obligations) -- rate goes up
- When the pool is stressed (many withdrawals) -- rate goes down
- **Floor: 0.5%** -- guaranteed minimum, you always earn something
- **Ceiling: 10%** -- maximum cap, protects against excessive payouts

The base rate depends on the current epoch (5.0% in Epoch 0, down to 2.0% in Epoch 6).

In the game UI, this appears as **"City Prosperity"** -- a visual indicator of the city's economic health.

## Per-Tier Rate Modifiers

Each tier has its own rate modifier applied on top of the adaptive rate:

| Tier | Rate Mod | Effect |
|------|----------|--------|
| T0 | x1.20 | Earns 20% faster |
| T1 | x1.15 | Earns 15% faster |
| T2 | x1.10 | Earns 10% faster |
| T3 | x1.05 | Earns 5% faster |
| T4 | x1.00 | Base rate (no modifier) |
| T5 | x0.85 | Earns 15% slower |
| T6 | x0.70 | Earns 30% slower |
| T7 | x0.55 | Earns 45% slower |

This is a deliberate design choice: smaller tiers compensate for their lower absolute deposits with a higher earning rate, while larger tiers trade rate for sheer volume.

## Max Payout Cap

Every building has a maximum total payout, determined at construction time:

```
maxPayout = deposit x epochCap x tierCapMod
```

**Example (T3, Epoch 0):**
- Deposit: 0.01 BNB
- Epoch cap: 3.0x
- Tier cap modifier: x1.15
- Max payout: 0.01 x 3.0 x 1.15 = **0.0345 BNB**

## Cap Bonus

Every compound adds **+1%** to your building's cap bonus, up to a maximum of **+50%**. This bonus extends the maximum payout:

```
effectiveCap = maxPayout x (1 + capBonus / 100)
```

After 30 compounds, your cap is 30% higher. After 50 compounds, it's 50% higher. This rewards consistent engagement.

## Why Compound?

Compounding is powerful for three reasons:

1. **Grows your principal** -- bigger daily earnings
2. **Grows your cap** -- +1% cap bonus per compound (max +50%)
3. **Boosts productivity** -- +15% per compound (can overcharge to 500%)

| Strategy | Effect |
|----------|--------|
| Compound daily | Fastest growth, highest eventual payout |
| Claim daily | Immediate cash but shrinking productivity and no cap bonus |
| Mix (compound then claim) | Balanced approach, build up then extract |

Compound = faster cycles = more profit over time.

## The 12-Hour Cycle

Each building has its own 12-hour timer:
1. Earnings accumulate for 12 hours
2. After 12h -- earnings stop (but don't disappear)
3. Compound or claim to restart the timer
4. Timer is per-building, not global

This means there's no advantage to botting -- everyone gets one action per 12 hours per building. If you want continuous earning, activate the Auto-Action boost (see [Boosts & Upgrades](boosts.md)).

## Deposit Fee

When you build, **10% of your deposit goes to the dev wallet**. The remaining 90% becomes your building's real deposit, which determines your cap and earning power.

**Example:** You deposit 1 BNB -> 0.1 BNB goes to dev -> 0.9 BNB is your real deposit.

## Claim Tax

When you withdraw earnings, a combined tax is deducted:
- **10% fixed** goes to the dev wallet
- **3--6%** goes back to the pool (varies by epoch)
- Total: **13--16%** depending on which epoch the building was created in

The pool portion helps sustain payouts for everyone. See [Fees & Taxes](fees.md) for the full breakdown.
