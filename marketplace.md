# Marketplace & Sellback

## P2P Land Market

Players can list their land plots for sale. Other players can buy them directly.

### How It Works

1. **List:** Set your price and list the plot
2. **Buy:** Another player pays the listed price
3. **Fee:** 10% commission goes to the mayor, 90% to the seller

### What Gets Sold

- **Empty plot** -- just the land rights
- **Plot with active building** -- land + building transfer to the buyer (building keeps earning)
- **Plot with completed building** -- land + completed building (buyer can demolish and rebuild)

### Why Trade Land?

- **Speculation** -- buy cheap land early, sell when the city grows
- **Location** -- central plots are worth more (OG status)
- **Late entry** -- new players can buy prime locations from existing players instead of waiting for mayor sales
- **Liquidity** -- if you need BNB, sell your plot instead of waiting for building earnings

### Marketplace Fees

| Operation | Fee | Goes To |
|-----------|-----|---------|
| Primary sale (from mayor) | 100% | Mayor (admin) |
| P2P resale | 10% | Mayor (admin) |
| P2P resale | 90% | Seller |

## Sellback

You can sell a building back to the pool instead of waiting for its cap to complete. This is useful when you want to exit early or restructure your portfolio.

### How Sellback Works

1. Your building must have a **7-day cooldown** since its last action (compound, claim, or boost activation)
2. A commission is deducted based on how much you've already claimed
3. The remaining value is returned to your wallet

### Sellback Commission

The commission scales with your claim ratio -- the more you've already extracted, the higher the fee:

| Claim Ratio | Commission |
|-------------|------------|
| 0% claimed | 15% commission |
| 50% claimed | ~57% commission |
| 100% claimed | 100% commission |

The commission scales linearly from 15% to 100% based on how much of your cap you've already claimed. The dev wallet receives 10% of the commission amount.

### When to Use Sellback

- You want to exit a position early
- You want to reallocate capital to a different tier
- The adaptive rate has dropped and you want to rebuild at current conditions
- You need liquidity but selling land on the marketplace is too slow

### Sellback vs. Waiting

Sellback is a trade-off: you get immediate liquidity but pay a commission. If your building still has significant cap remaining and the rate is healthy, it's usually better to let it complete naturally.
