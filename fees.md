# Fees & Taxes

Every fee in BNB City is hardcoded into the smart contract. Nobody can change them -- not the team, not anyone. Here's exactly where your money goes and why each fee exists.

## Complete fee overview

| When | Fee | Where it goes | Why it exists |
|------|-----|--------------|---------------|
| Building (deposit) | 10% | Dev wallet | Funds development and operations |
| Claiming earnings | 13--16% | 10% dev + 3--6% pool | Sustains the ecosystem |
| Withdrawing referral balance | 20% | Back to pool | Incentivizes reinvestment |
| Primary land sale | 100% | Protocol | City expansion funding |
| Sellback | 15--100% | Pool (dev gets 10% of commission) | Exit mechanism |

## The deposit fee (10%)

When you build, 10% goes to the dev wallet. The remaining 90% becomes your building's working capital.

**What this means in practice:**
- You deposit 0.05 BNB ($30) -> 0.005 BNB ($3) goes to dev -> 0.045 BNB ($27) earns yield
- Your payout cap is calculated on the real deposit (0.045), not the full amount

**Why it's fair:** This is a straightforward revenue model. The team builds and maintains the game; the fee pays for it. There are no hidden fees, no changing terms, no surprise charges later.

## The claim tax (13--16%)

When you withdraw earnings, a combined tax is deducted. Two parts:

- **10% fixed** -- always goes to the dev wallet (this never changes)
- **3--6% pool tax** -- goes back into the pool (varies by epoch of building creation)

| Building created in | Dev tax | Pool tax | Total claim tax |
|--------------------|---------|----------|-----------------|
| Epoch 0--1 | 10% | 3% | 13% |
| Epoch 2--3 | 10% | 4% | 14% |
| Epoch 4--5 | 10% | 5% | 15% |
| Epoch 6 | 10% | 6% | 16% |

**The pool tax is the key to sustainability.** Every time someone claims, a portion goes back to the pool -- funding payouts for everyone. Later-epoch buildings contribute slightly more (6% vs 3%), which keeps the system healthy as it grows.

**What you actually receive:** If you claim 0.01 BNB in earnings and your building was created in E0, you get 0.0087 BNB (87% of 0.01). The math is transparent and predictable.

## The referral withdraw tax (20%)

When you withdraw referral earnings to your wallet, 20% stays in the pool. This is by design -- it nudges you toward the smarter play: **reinvesting referral earnings into new buildings**.

When you build using referral balance:
- **0% deposit fee** (money is already in the contract)
- Your entire referral balance becomes real deposit (100% vs. 90% from fresh BNB)
- This gives you roughly **11% higher cap** compared to a normal deposit
- The money stays in the contract, which is good for pool health

**The choice is yours:** Withdraw and lose 20%, or reinvest at 0% fee and get an 11% cap bonus. Most experienced players reinvest.

## Sellback commission (15--100%)

When you sell a building back to the pool, the commission scales with how much you've already extracted:

| Your claim ratio | Commission | You receive |
|-----------------|------------|-------------|
| 0% claimed | 15% | 85% of remaining deposit |
| 25% claimed | ~36% | ~64% |
| 50% claimed | ~57% | ~43% |
| 75% claimed | ~79% | ~21% |
| 100% claimed | 100% | Nothing |

The dev wallet gets 10% of whatever the commission is. The rest returns to the pool.

**The logic:** If you've barely claimed anything, the pool can afford to refund most of your deposit. If you've already extracted most of your cap, there's little to refund. This prevents gaming the sellback system.



Primary land sales (buying fresh plots from the mayor) go 100% to the protocol -- this funds the city's expansion.

## Boost costs

All boost purchases go to the dev wallet, minus 50% which goes to your L1 referrer:

| Boost | Cost |
|-------|------|
| Auto-Earn 7d | 5% of tier deposit |
| Auto-Earn 30d | 15% of tier deposit |
| Productivity Recharge | 5% of tier deposit |
| Compound Boost | 20% of tier deposit |
| Claim Shield | 5% of tier deposit |
| Epoch Lock | 20% of tier deposit |
| Landmark | 0.005 BNB flat |
| Batch Compound | 0.001 BNB per building |

## What your money actually returns (net of all fees)

Here's the bottom line -- what a player actually receives after all fees, assuming full cap completion with active compounding:

| Tier | Epoch | Total invested (with land) | Gross cap (base) | With +50% cap bonus | Net after 13% claim tax | Net multiplier |
|------|-------|---------------------------|------------------|---------------------|------------------------|----------------|
| T0 | E0 | $1.80 | $2.03 | $3.04 | $2.64 | ~1.47x |
| T3 | E0 | $10.80 | $18.63 | $27.95 | $24.31 | ~2.25x |
| T4 | E0 | $34.80 | $85.05 | $127.58 | $110.99 | ~3.19x |
| T6 | E0 | $627 | $1,296 | $1,944 | $1,691 | ~2.70x |

*These are best-case scenarios with maximum cap bonus (+50% from 50 compounds). Actual returns depend on the adaptive rate and your compounding consistency.*

**The transparency promise:** Every number on this page is hardcoded in a verified, immutable smart contract. Nobody can change the fees after deployment. What you see is what you get -- permanently.

---

**See also:** [Economy](economy.md) | [Referral System](referral.md)
