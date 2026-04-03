# Buildings & Tiers

## 8 Building Tiers

Each tier requires a specific land type and deposit amount. Higher tiers have larger absolute profits but lower ROI percentage.

| Tier | Deposit | Land Required | Total Entry | Cap Modifier | Eff. Cap (Epoch 1) |
|------|---------|---------------|-------------|-------------|-------------------|
| T0 | 0.001 BNB | Mini 1×1 | 0.002 BNB | ×1.25 | 3.75x |
| T1 | 0.002 BNB | Mini 1×1 | 0.003 BNB | ×1.20 | 3.60x |
| T2 | 0.005 BNB | Mini 1×1 | 0.006 BNB | ×1.18 | 3.54x |
| T3 | 0.01 BNB | Standard 1×1 | 0.015 BNB | ×1.15 | 3.45x |
| T4 | 0.05 BNB | Standard 1×1 | 0.055 BNB | ×1.05 | 3.15x |
| T5 | 0.25 BNB | Large 2×2 | 0.275 BNB | ×1.00 | 3.00x |
| T6 | 1 BNB | Large 2×2 | 1.025 BNB | ×0.80 | 2.40x |
| T7 | 5 BNB | Premium 3×3 | 5.125 BNB | ×0.65 | 1.95x |

## How Tiers Differ

The daily rate is **the same** for all tiers. The difference is in the **cap modifier**:

- **Small tiers (T0-T3):** Higher cap = longer cycle, higher ROI%. Best for smaller players who want maximum return percentage.
- **Large tiers (T5-T7):** Lower cap = shorter cycle, lower ROI%, but massive absolute profit. Best for larger players who want fast cycles.

**Example (Epoch 1, healthy pool):**

| Tier | Daily Rate | Cycle | ROI | Profit |
|------|-----------|-------|-----|--------|
| T3 (0.01 BNB) | 5% | 81 days | +211% | ~$14 |
| T5 (0.25 BNB) | 5% | 72 days | +171% | ~$282 |
| T7 (5 BNB) | 5% | 63 days | +76% | ~$2,505 |

## Building Categories

When building, you choose a visual category. This is purely cosmetic — it doesn't affect earnings.

- **Residential** — Houses, apartments, mansions
- **Commercial** — Shops, offices, warehouses, malls
- **Industrial** — Factories, farms

Each category has multiple random sprite variants. Your building gets a unique look.

## Building Lifecycle

```
Buy land → Build (deposit) → Compound daily → Claim earnings →
→ Cap reached (cycle complete) → Demolish → Build again or sell land
```

## Visual States

Buildings change appearance based on their state:
- **Construction** — animated building process
- **Active** — normal look, windows lit based on activity level
- **Developed** — enhanced visuals after 3+ compounds
- **Maximum** — premium look after 7+ compounds
- **Completed** — distinct style when cap is reached

## Compound (Expand Business)

When you compound:
1. Pending earnings are added to your principal
2. Activity meter gets +15% boost (can overcharge up to 500%)
3. Compound count increases (affects visual level)
4. 12h timer resets
5. Your L1 referrer gets 10% of the compound amount

**Important:** Compound grows your principal but does NOT increase your cap. The cap is fixed at deposit time.

## Claim (Withdraw Earnings)

When you claim:
1. All pending earnings are paid out (up to remaining cap)
2. Claim tax is deducted (7-10% depending on building epoch)
3. Activity meter drops by -15%
4. 12h timer resets
5. If total claimed reaches cap — building completes its cycle

Claims are always full withdrawals. You cannot do partial claims.
