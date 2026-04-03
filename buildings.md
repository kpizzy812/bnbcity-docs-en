# Buildings & Tiers

## 8 Building Tiers

Each tier requires a specific land type and deposit amount. Tiers differ not only in cap but also in their **rate modifier** -- smaller tiers earn at a higher effective rate, while larger tiers earn slower but generate bigger absolute profits.

| Tier | Deposit | Land Required | Cap Mod | Rate Mod | Effective Rate* |
|------|---------|---------------|---------|----------|-----------------|
| T0 | 0.001 BNB | Mini 1x1 | x1.25 | x1.20 | 6.00% |
| T1 | 0.002 BNB | Mini 1x1 | x1.20 | x1.15 | 5.75% |
| T2 | 0.005 BNB | Mini 1x1 | x1.18 | x1.10 | 5.50% |
| T3 | 0.01 BNB | Standard 1x1 | x1.15 | x1.05 | 5.25% |
| T4 | 0.05 BNB | Standard 1x1 | x1.05 | x1.00 | 5.00% |
| T5 | 0.25 BNB | Large 2x2 | x1.00 | x0.85 | 4.25% |
| T6 | 1 BNB | Large 2x2 | x0.80 | x0.70 | 3.50% |
| T7 | 5 BNB | Mega 3x3 | x0.80 | x0.55 | 2.75% |

*Effective rate shown assumes Epoch 0 base rate (5.0%) and healthy pool (adaptive rate = base rate).

## Rate Formula

The effective daily rate for each building is calculated per-tier:

```
effectiveRate = adaptiveRate x TIER_RATE_MOD[tier] / 100
```

Where `adaptiveRate` is the global rate (0.5%--10%) and `TIER_RATE_MOD` is the tier-specific multiplier. This means T0 earns 20% faster than T4, while T7 earns 45% slower.

## Cap Modifier and Cap Bonus

Every building has a maximum payout cap set at construction:

```
maxPayout = deposit x epochCap x tierCapMod
```

Additionally, each compound adds **+1% to your cap bonus**, up to a maximum of **+50%**. This means active compounders can significantly extend their building's lifecycle.

```
effectiveCap = maxPayout x (1 + capBonus/100)
```

## How Tiers Differ

- **Small tiers (T0--T3):** Higher rate modifier + higher cap modifier = faster earning rate and longer cycle. Best for smaller players who want maximum ROI percentage.
- **Medium tiers (T4--T5):** Balanced rate and cap. Good middle ground.
- **Large tiers (T6--T7):** Lower rate modifier + lower cap modifier = slower earning but massive absolute profits. Best for larger players who want big numbers.

## Total Entry Cost

Don't forget land cost when calculating your total investment:

| Tier | Deposit | Land Cost | Total Entry |
|------|---------|-----------|-------------|
| T0 | 0.001 BNB | 0.002 BNB | 0.003 BNB |
| T1 | 0.002 BNB | 0.002 BNB | 0.004 BNB |
| T2 | 0.005 BNB | 0.002 BNB | 0.007 BNB |
| T3 | 0.01 BNB | 0.008 BNB | 0.018 BNB |
| T4 | 0.05 BNB | 0.008 BNB | 0.058 BNB |
| T5 | 0.25 BNB | 0.045 BNB | 0.295 BNB |
| T6 | 1 BNB | 0.045 BNB | 1.045 BNB |
| T7 | 5 BNB | 0.125 BNB | 5.125 BNB |

## Building Categories

When building, you choose a visual category. This is purely cosmetic -- it doesn't affect earnings.

- **Residential** -- Houses, apartments, mansions
- **Commercial** -- Shops, offices, warehouses, malls
- **Industrial** -- Factories, farms

Each category has multiple random sprite variants. Your building gets a unique look.

## Building Lifecycle

```
Buy land -> Build (deposit) -> Compound daily -> Claim earnings ->
-> Cap reached (cycle complete) -> Demolish -> Build again or sell land
```

## Visual States

Buildings change appearance based on their state:
- **Construction** -- animated building process
- **Active** -- normal look, windows lit based on productivity level
- **Developed** -- enhanced visuals after 3+ compounds
- **Maximum** -- premium look after 7+ compounds
- **Completed** -- distinct style when cap is reached

## Compound (Expand Business)

When you compound:
1. Pending earnings are added to your principal
2. Productivity gets +15% boost (can overcharge up to 500%)
3. Cap bonus increases by +1% (max +50%)
4. Compound count increases (affects visual level)
5. 12h timer resets
6. Your L1 referrer gets 10% of the compound amount

**Important:** Compounding grows your principal AND your cap bonus, making it doubly effective.

## Claim (Withdraw Earnings)

When you claim:
1. All pending earnings are paid out (up to remaining cap)
2. Claim tax is deducted (13--16% depending on epoch: 10% dev + 3--6% pool)
3. Productivity drops by -15% (scaled with current level)
4. 12h timer resets
5. If total claimed reaches cap -- building completes its cycle

Claims are always full withdrawals. You cannot do partial claims.
