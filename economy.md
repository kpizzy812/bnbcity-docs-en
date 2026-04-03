# Core Mechanics

## How Yield Works

Every building generates daily yield based on a simple formula:

```
Daily earnings = Principal × Effective rate × (Activity / 100)
```

Where:
- **Principal** — your building's current power (grows with compounds)
- **Effective rate** — the city's current daily rate (0.5% to 10%)
- **Activity** — your building's activity meter (0% to 500%)

## Adaptive Rate (City Prosperity)

The daily rate self-adjusts based on the health of the city's economy:

```
Rate = Base rate × (Contract balance / Active deposits)
```

- When the pool is healthy (more BNB than obligations) → rate goes up
- When the pool is stressed (many withdrawals) → rate goes down
- **Floor: 0.5%** — guaranteed minimum, you always earn something
- **Ceiling: 10%** — maximum cap, protects against excessive payouts

In the game UI, this appears as **"City Prosperity"** — a visual indicator of the city's economic health.

## Max Payout Cap

Every building has a maximum total payout, determined at construction time:

```
Max payout = Deposit × Epoch cap × Tier cap modifier
```

Once you've claimed this amount, the building completes its cycle. You demolish it and build anew.

**Example (T3, Epoch 1):**
- Deposit: 0.01 BNB
- Epoch cap: 3.0x
- Tier modifier: ×1.15
- Max payout: 0.01 × 3.0 × 1.15 = **0.0345 BNB**

After fees, the real multiplier for the player is approximately **2.7x** on the initial deposit.

## Why Compound?

Compounding doesn't increase your cap — but it makes you reach the cap **faster**:

| Strategy | Cycle Length | ROI |
|----------|-------------|-----|
| Compound daily | ~81 days | +211% |
| Claim daily | ~120+ days | Lower (activity drains) |

Compound = faster cycles = more profit over time.

## The 12-Hour Cycle

Each building has its own 12-hour timer:
1. Earnings accumulate for 12 hours
2. After 12h — earnings stop (but don't disappear)
3. Compound or claim to restart the timer
4. Timer is per-building, not global

This means there's no advantage to botting — everyone gets one action per 12 hours per building.
