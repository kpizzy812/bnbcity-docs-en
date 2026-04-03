# Fees & Taxes

## All Fees at a Glance

| When | Fee | Where It Goes |
|------|-----|---------------|
| Build (deposit) | 3% | Dev wallet |
| Claim earnings | 7-10% | 4% dev + 3-6% back to pool |
| Withdraw referral balance | 20% | Back to pool |
| P2P land resale | 10% | Mayor (admin) |
| Primary land sale | 100% | Mayor (admin) |

## Deposit Fee (3%)

When you build, 3% of your deposit goes directly to the dev wallet. The remaining 97% becomes your building's `real_deposit`, which determines your cap.

**Example:** You deposit 1 BNB → 0.03 BNB goes to dev → 0.97 BNB is your real deposit.

## Claim Tax (7-10%)

When you withdraw earnings, a tax is deducted based on the epoch your building was created in:

| Building Epoch | Total Tax | To Dev | To Pool |
|---------------|-----------|--------|---------|
| 1-2 | 7% | 4% | 3% |
| 3-4 | 8% | 4% | 4% |
| 5-6 | 9% | 4% | 5% |
| 7 | 10% | 4% | 6% |

Dev always gets a fixed 4%. The growing portion goes back into the pool, helping sustain payouts for everyone.

## Real Player Returns

After all fees, here's what you actually get:

| Tier | Epoch | Gross Cap | After Fees | Real Multiplier |
|------|-------|-----------|------------|-----------------|
| T3 (0.01 BNB) | 1 | 3.45x | ~3.12x | ~3.12x on deposit |
| T5 (0.25 BNB) | 1 | 3.00x | ~2.71x | ~2.71x on deposit |
| T7 (5 BNB) | 1 | 1.95x | ~1.76x | ~1.76x on deposit |

## Referral Withdraw Tax (20%)

When you withdraw your referral balance to your wallet, 20% stays in the pool. This incentivizes reinvesting referral earnings into new buildings (which has 0% fee).

## Building from Referral Balance

Building a new business using your referral balance has special benefits:
- **0% deposit fee** (money is already in the contract)
- **0% referral credits** (no new inflow to credit)
- **Higher real deposit** (100% vs 97% from regular deposits)
- **~3% higher cap** compared to building with fresh BNB

## Premium Features (Optional Sinks)

| Feature | Cost | Effect |
|---------|------|--------|
| Auto-action (7/30 days) | 1-3% of tier deposit | Earnings not limited to 12h cycles |
| Battery Recharge | 5% of tier deposit | Activity restored to 100% |
| Compound Boost | 5% of tier deposit | Each compound doubled for 7 days |
| Claim Shield | 1% of tier deposit | 3 claims without activity drain |
| Epoch Lock | 20% of tier deposit | Lock current adaptive rate permanently |
| Landmark | 0.05 BNB | Gold frame on city map (30 days) |

All premium features are optional and go to the dev wallet. They provide convenience, not unfair advantage.
