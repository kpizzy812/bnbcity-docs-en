# Fees & Taxes

## All Fees at a Glance

| When | Fee | Where It Goes |
|------|-----|---------------|
| Build (deposit) | 10% | Dev wallet |
| Claim earnings | 13--16% | 10% dev + 3--6% back to pool |
| Withdraw referral balance | 20% | Back to pool |
| P2P land/building resale | 10% | Mayor (admin) |
| Primary land sale | 100% | Mayor (admin) |
| Sellback | 15--100% | Pool (dev gets 10% of commission) |

## Deposit Fee (10%)

When you build, 10% of your deposit goes directly to the dev wallet. The remaining 90% becomes your building's `real_deposit`, which determines your cap and earning power.

**Example:** You deposit 1 BNB -> 0.1 BNB goes to dev -> 0.9 BNB is your real deposit.

## Claim Tax (13--16%)

When you withdraw earnings, a combined tax is deducted. It consists of two parts:

- **10% fixed** -- always goes to the dev wallet (CLAIM_TAX_DEV_BPS = 1000)
- **3--6% pool tax** -- goes back into the pool, varies by epoch

| Building Epoch | Dev Tax | Pool Tax | Total Tax |
|---------------|---------|----------|-----------|
| E0--E1 | 10% | 3% | 13% |
| E2--E3 | 10% | 4% | 14% |
| E4--E5 | 10% | 5% | 15% |
| E6 | 10% | 6% | 16% |

The pool portion helps sustain payouts for everyone. The dev tax is fixed and never changes.

## Referral Withdraw Tax (20%)

When you withdraw your referral balance to your wallet, 20% stays in the pool. This incentivizes reinvesting referral earnings into new buildings (which has 0% withdraw fee since money stays in the contract).

## Building from Referral Balance

Building a new business using your referral balance has special benefits:
- **0% deposit fee** (money is already in the contract)
- **0% referral credits** (no new inflow to credit)
- **Higher real deposit** (100% vs 90% from regular deposits)
- **~11% higher cap** compared to building with fresh BNB
- Money stays in the contract (good for pool health)

## Sellback Commission (15--100%)

When you sell a building back to the pool:
- Commission scales linearly with your claim ratio (how much you've already extracted)
- At 0% claimed: 15% commission
- At 100% claimed: 100% commission
- The dev wallet receives 10% of the commission amount
- Requires 7-day cooldown since last building action

## Marketplace Fee (10%)

When a building or land plot is sold on the P2P marketplace, 10% goes to the mayor (admin) and 90% goes to the seller.

## Sink/Boost Fees

All boost purchases go to the dev wallet, except:
- **L1 referrer gets 50%** of any sink purchase made by their direct referral

| Boost | Cost |
|-------|------|
| Auto-Action 7d | 5% of tier deposit |
| Auto-Action 30d | 15% of tier deposit |
| Productivity Recharge | 5% of tier deposit |
| Compound Boost | 20% of tier deposit |
| Claim Shield | 5% of tier deposit |
| Epoch Lock | 20% of tier deposit |
| Landmark | 0.005 BNB flat |
| Batch Compound | 0.001 BNB per building |

## Real Player Returns

After all fees (10% deposit fee + claim tax), here's what the cap means for the player:

| Tier | Epoch | Gross Cap | Deposit Fee | Claim Tax | Approx. Real Multiplier |
|------|-------|-----------|-------------|-----------|------------------------|
| T0 | E0 | 3.75x | 10% | 13% | ~2.94x on deposit |
| T3 | E0 | 3.45x | 10% | 13% | ~2.70x on deposit |
| T4 | E0 | 3.15x | 10% | 13% | ~2.47x on deposit |
| T7 | E0 | 2.40x | 10% | 13% | ~1.88x on deposit |

These numbers improve with cap bonus from compounding (up to +50%).
