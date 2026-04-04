# Economy

BNB City's economy is designed to be self-regulating, transparent, and sustainable. This page explains the core mechanics -- not as formulas in a textbook, but as a system you can understand, predict, and profit from.

## How your buildings earn money

Every building generates daily yield. The amount depends on three things:

1. **Your principal** -- how much working capital your building has (grows every time you compound)
2. **The effective rate** -- the city's adaptive rate, adjusted by your building's tier modifier
3. **Your productivity** -- how efficiently your building is running (100% is normal, can go up to 500%)

In simple terms: bigger principal x higher rate x higher productivity = more daily income.

**Real example (T4, Epoch 0, healthy pool):**
- Principal after 10% fee: 0.045 BNB ($27)
- Effective rate: 5.0%/day (base rate 5% x T4 modifier x1.00)
- Productivity: 100%
- Daily earnings: $1.35

Compound every day for a week, and that daily income keeps growing as your principal increases. This is the snowball effect that makes compounding so powerful.

## The adaptive rate: a self-healing economy

This is the most important innovation in BNB City's design. Instead of a fixed yield rate (which always breaks eventually), the rate **adjusts itself** based on the health of the city's treasury:

- **When the pool is flush** (lots of deposits, healthy balance) -- the rate rises, rewarding players
- **When the pool is stressed** (many withdrawals, balance shrinking) -- the rate drops, slowing outflows
- **Floor: 0.5%/day** -- you always earn something, no matter what
- **Ceiling: 10%/day** -- prevents unsustainable payouts during euphoric periods

The formula is elegant: the rate tracks the ratio of the contract's BNB balance to total active deposits. If there's more BNB in the contract than total obligations, the rate goes up. If obligations exceed the balance, the rate comes down.

**Why this matters to you:** Unlike fixed-rate protocols that boom and bust, BNB City's economy has a built-in thermostat. It self-corrects. When things get too hot, it cools down. When activity slows, it rewards those who stay. This is why the system can sustain itself through market cycles.

In the game, you see this as **"City Prosperity"** -- a visual meter showing the current economic health.

## Per-tier rate modifiers: fair by design

Not all buildings earn at the same rate. Each tier has its own modifier:

| Tier | Rate modifier | What it means |
|------|--------------|---------------|
| T0 | x1.20 | Earns 20% faster than baseline |
| T1 | x1.15 | Earns 15% faster |
| T2 | x1.10 | Earns 10% faster |
| T3 | x1.05 | Earns 5% faster |
| T4 | x1.00 | The baseline |
| T5 | x0.85 | Earns 15% slower |
| T6 | x0.70 | Earns 30% slower |
| T7 | x0.55 | Earns 45% slower |

**The design principle:** Small players deserve proportionally better returns. If you can only invest $2, you should earn a higher percentage than someone investing $3,000. The tier modifiers make this happen. It's a progressive system that keeps the game accessible and fair.

At the same time, large players still earn massive absolute profits. A T7 building at 2.75%/day on a $2,700 principal is $74.25/day -- far more in dollar terms than a T0 earning 6% on $0.54.

## The payout cap: sustainable by math

Every building has a maximum total payout. This is critical to sustainability -- the contract always knows its maximum liability.

The cap is determined at construction:
- **Epoch cap** (3.0x in E0, decreasing to 2.4x in E6) x **Tier cap modifier** (x0.80 to x1.25) x **Your real deposit** (after fee)

**Example -- T3 building, Epoch 0:**
- Real deposit: 0.009 BNB (0.01 minus 10% fee)
- Cap: 0.009 x 3.0 x 1.15 = 0.031 BNB ($18.63)
- That's a 3.45x gross return on your $6 deposit

**But it gets better.** Every compound adds +1% to your cap bonus, up to +50%. After 50 compounds:
- Effective cap: 0.031 x 1.50 = 0.04658 BNB ($27.95)
- That's a **5.18x gross return** for an active player

This cap bonus is the game's biggest reward for engagement. Passive players get the base return. Active compounders can push their returns 50% higher.

## Compounding: the engine of wealth

Compounding is the single most important action in BNB City. When you compound:

| What happens | Why it matters |
|-------------|---------------|
| Pending earnings are added to your principal | Tomorrow you earn on a bigger base |
| Productivity gets +15% boost | Can overcharge up to 500%, multiplying your earnings |
| Cap bonus increases by +1% (max +50%) | Your building can pay out more total |
| 12h timer resets | New earning cycle begins |
| Your L1 referrer gets 10% of the compound | Costs you nothing, rewards your network |

**The compound vs. claim tradeoff:**

| Strategy | Daily income growth | Productivity trend | Cap bonus | Best for |
|----------|--------------------|--------------------|-----------|----------|
| Compound every day | Accelerating | Rising (can reach 500%) | +1%/day | Maximum total profit |
| Claim every day | Flat or declining | Falling (-15%/claim) | None | Immediate cash (not recommended) |
| Compound 7--10 days, then claim | Strong growth, periodic harvest | Stable cycle | Building steadily | Most players |

## The 12-hour cycle: level playing field

Each building earns for 12 hours, then stops. You must compound or claim to restart the timer.

This design choice has important consequences:
- **No botting advantage** -- a bot and a human both get one action per 12 hours
- **No urgency to check every hour** -- just log in twice a day
- **Idle time is wasted time** -- but there's no penalty, just missed opportunity
- **Auto-Earn boost** removes the limit entirely for players who want passive income

## Where the money comes from (and goes)

BNB City is a redistribution protocol. Here's the flow:

**Money flowing IN:**
- New deposits (90% of each deposit enters the pool)
- Pool portion of claim taxes (3--6% of every claim goes back to the pool)
- Sellback commissions
- Referral withdraw taxes (20%)

**Money flowing OUT:**
- Claim payouts (earnings withdrawn by players)
- Sellback refunds
- Referral withdrawals

**Money to the dev wallet:**
- 10% of deposits
- 10% of claims (fixed)
- 10% of sellback commissions
- Boost/sink purchases (minus 50% referral bonus)

The adaptive rate is the balancing mechanism. When more money flows in than out, the rate rises -- rewarding players. When more flows out, the rate falls -- protecting the pool. The system seeks equilibrium naturally.

## The bottom line

BNB City's economy works because it combines three things that most DeFi projects get wrong:

1. **Self-regulating yields** -- no fixed rate that inevitably breaks
2. **Known maximum liability** -- every building's cap is set at creation, so the contract always knows its worst-case obligations
3. **Deflationary pressure** -- epochs progressively reduce extraction rates, keeping the pool healthy as the city grows

The result is a system where early players earn more (because early epochs have better rates), active players earn more (because compounding increases principal, productivity, and cap), and the pool stays healthy through mathematical self-correction.
