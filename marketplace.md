# Sell Building -- Your Exit Button

Sometimes you want to close a position before a building finishes its payout cap. Maybe the rate dropped, maybe you want to restructure, maybe you just need the BNB. You can sell any building back to the city pool for instant liquidity.

## How it works

1. Wait for the **7-day cooldown** after your last action (compound, claim, or boost)
2. Click "Sell Building"
3. The contract calculates your refund (deposit minus commission)
4. BNB goes to your wallet, building is dissolved
5. Your land plot stays -- you can build again on it

## Commission: 15% to 100%

The commission depends on how much you've already claimed from the building:

| How much you've claimed | Commission | You receive |
|-------------------------|------------|-------------|
| Nothing (0%) | 15% | 85% of deposit |
| Quarter (25%) | ~36% | ~64% |
| Half (50%) | ~57% | ~43% |
| Three quarters (75%) | ~79% | ~21% |
| Everything (100%) | 100% | Nothing |

The dev wallet receives 10% of the commission amount. The rest returns to the city pool.

**The logic is fair:** if you haven't earned much yet, the pool refunds most of your deposit. If you've already profited significantly, there's less to refund.

## Cooldown: 7 days

After selling one building, you must wait 7 days before selling another. This prevents rapid mass withdrawal.

## When selling makes sense

- **Need liquidity now** -- instant exit, no waiting
- **Building nearly finished** -- remaining earnings are minimal, take the rest
- **Strategy pivot** -- sell the old building, build something different
- **Rate dropped significantly** -- cut losses and restart with better conditions

## Sell or wait it out?

If your building still has significant cap remaining and the rate is healthy, it's almost always better to let it complete naturally. Selling is a flexibility tool, not the default strategy.

**Best case for selling:** The building is young, you've barely claimed, and you want to reallocate capital. A 15% commission on a barely-claimed building is a reasonable price for instant liquidity.

---

**See also:** [Buildings & Tiers](buildings.md) | [Fees & Taxes](fees.md)
