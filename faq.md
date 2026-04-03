# FAQ

## General

### What is BNB City?
An on-chain isometric city-builder game on BNB Smart Chain. You build businesses in a shared city, and each building generates daily yield through deflationary redistribution.

### Is this a Ponzi?
BNB City is a deposit redistribution protocol with deflationary mechanics. Early participants earn more -- this is transparent and on-chain. The epoch system gradually reduces extraction rates, keeping the pool healthier than traditional models. All fees and mechanics are visible in the verified smart contract.

### Can I lose money?
Your deposit goes into the pool and starts generating yield. The maximum payout cap means the contract knows its total liability. However, if the pool runs out of BNB (zero new deposits for an extended period), earnings slow down to the floor rate (0.5%). The contract cannot guarantee returns -- it depends on continued participation.

### What chain is this on?
BNB Smart Chain (BSC). Gas fees are extremely low (~$0.01 per transaction).

### What wallet do I need?
Any BSC-compatible wallet works. We recommend:
- **[Rabby](https://rabby.io)** -- clean desktop wallet
- **[MetaMask](https://metamask.io)** -- most popular Web3 wallet
- **[Trust Wallet](https://trustwallet.com)** -- best for mobile

## Gameplay

### How much do I need to start?
The cheapest entry is T0: 0.001 BNB deposit + 0.002 BNB for Mini land = **0.003 BNB total** (less than $2).

### How often should I log in?
Every 12 hours is optimal for compounding. If you miss a cycle, earnings stop accumulating until your next action. There's no penalty -- you just lose potential earning time. You can also buy Auto-Action to remove the 12h cap entirely.

### What happens when my building reaches its cap?
The building completes its cycle and stops earning. You can demolish it (free) and either build a new business on the same plot or sell the plot to another player.

### Can I have multiple buildings?
Yes. Each building is independent -- its own productivity, cap, and 12h timer. There's no limit on how many buildings you can own.

### What's better -- small tier or big tier?
- **Small tiers (T0--T3)** -- higher rate modifier, higher cap modifier, higher ROI percentage. Good for maximizing returns on small amounts.
- **Big tiers (T6--T7)** -- lower rate and cap modifiers but massive absolute profits. Good for larger investments.

### Can I upgrade my land?
Yes. You can upgrade a Mini 1x1 plot to Standard 1x1 for 0.006 BNB (the price difference). This lets you place T3--T4 buildings on a plot that originally only supported T0--T2.

## Economy

### What's the current daily rate?
The rate adjusts dynamically based on pool health. Check the "City Prosperity" indicator in-game. It ranges from 0.5% (floor) to 10% (ceiling). Each tier also has its own rate modifier (x0.55 to x1.20).

### What are epochs?
Epochs are like Bitcoin halvings -- as more BNB is deposited into the city, rewards gradually decrease. There are 7 epochs (E0--E6). See [Epochs](epochs.md) for details.

### Where do my earnings come from?
From the contract's BNB pool. The pool is funded by new deposits, claim taxes (3--6% pool portion), and sellback commissions. It's a redistribution model -- deposits flow in, earnings flow out, with deflationary mechanics keeping the pool sustainable.

### What is the deposit fee?
10% of every deposit goes to the dev wallet. The remaining 90% becomes your building's working principal.

### What is the claim tax?
13--16% total, depending on the epoch your building was created in. This is split: 10% fixed to the dev wallet + 3--6% back to the pool.

### What's the cap bonus?
Each compound adds +1% to your building's cap, up to +50%. After 50 compounds, your effective cap is 50% higher than the base cap.

## Boosts & Sinks

### What are sinks/boosts?
Optional paid upgrades for your buildings. They provide convenience and efficiency but are never required. Examples: Auto-Action (removes 12h cap), Compound Boost (doubles pending for 7 days), Claim Shield (3 claims without productivity drain).

### Can I sell my building early?
Yes, via Sellback. You sell the building back to the pool, but a commission (15--100%) is deducted based on how much you've already claimed. There's also a 7-day cooldown after your last action.

## Referrals

### How do I get my referral link?
Open the Referrals section in the game UI. Your unique link is there.

### When do I get paid?
Referral earnings are credited instantly to your in-game referral balance when your referrals deposit, compound, or buy boosts.

### How do I use my referral balance?
Best option: build a new business (0% fees, ~11% higher cap since no deposit fee). You can also compound it into an existing building or withdraw (20% tax).

### Do I earn from my referrals' boost purchases?
Yes. L1 referrers get 50% of any sink/boost purchase made by their direct referrals.

## Technical

### Is the contract upgradeable?
No. The contract is immutable -- no proxies, no admin upgrades. The code is final.

### Where can I see the contract?
The verified source code is available on BscScan. Link available in the game footer.

