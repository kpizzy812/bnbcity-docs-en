# FAQ

Real questions, honest answers.

---

## Getting started

### What is BNB City?

A shared isometric city-builder game on BNB Smart Chain where every building is a real income-generating asset. You buy land, build businesses, and earn daily yield. Everything runs on a single smart contract -- no middlemen, no accounts, no "trust us."

### How much do I need to start?

The absolute minimum is **0.003 BNB** (~$1.80) -- that's a Mini plot (0.002) plus a T0 building (0.001). You can test the entire system for less than a cup of coffee.

For a more meaningful experience, most players start at T3 or T4: **0.018 to 0.058 BNB** ($10--$35 total including land).

### What wallet do I need?

Any wallet that supports BNB Smart Chain:
- **[Rabby](https://rabby.io)** -- our recommendation for desktop
- **[MetaMask](https://metamask.io)** -- the most widely used option
- **[Trust Wallet](https://trustwallet.com)** -- best for mobile

Gas fees on BSC are around $0.01 per transaction, so gas is never a concern.

### What chain is this on?

BNB Smart Chain (BSC). Fast, cheap, widely supported. If your wallet is set to Ethereum by default, just switch the network to BSC.

---

## Gameplay

### How often should I log in?

**Twice a day is optimal** -- once every 12 hours. Your building earns for 12 hours, then pauses. Logging in to compound restarts the timer.

If you can't do twice a day, once a day still works -- you just earn for 12 out of 24 hours. And if even that's too much, the **Auto-Action boost** removes the 12h limit entirely for 7 or 30 days.

There's never a penalty for being away. You just miss potential earning time.

### Can I have multiple buildings?

Yes, and there's no limit. Each building runs independently -- its own productivity, cap, timer, and earnings. Many experienced players run 3--5+ buildings across different tiers and land plots.

### What happens when my building reaches its cap?

The building completes its lifecycle and stops earning. You demolish it (free, one click) and either build a new business on the same plot or sell the plot. This is the natural cycle -- build, grow, harvest, repeat.

### What's better -- small tier or big tier?

It depends on your goals:

- **Small tiers (T0--T3):** Higher percentage returns (5.25--6% daily). Best for maximizing ROI on smaller amounts. Great for learning the system.
- **Big tiers (T6--T7):** Lower rates (2.75--3.5%) but massive absolute profits. A T6 building earns ~$18.90/day at base rate -- that's real income.
- **Mid tiers (T4--T5):** The sweet spot for most players. Balanced rates and meaningful daily earnings.

### Can I upgrade my land?

Yes. A Mini plot can be upgraded to Standard for **0.006 BNB** ($3.60) -- just the price difference. This lets you place T3--T4 buildings on a plot that originally only supported T0--T2. You keep your exact location.

---

## Money questions

### How much can I actually earn?

Here's a realistic scenario for a T4 building in Epoch 0:

- Total investment: 0.058 BNB ($34.80) including land
- Daily earnings (5% rate, 100% productivity): ~$1.35/day
- With daily compounding over 30 days: principal grows significantly, daily earnings accelerate
- Gross cap with +50% cap bonus from active compounding: ~$127
- Net after 13% claim tax: ~$111
- **Net return: ~3.2x your investment** with active play

Returns vary based on the adaptive rate and your compounding consistency, but the math favors active players.

### Where do the earnings come from?

From the contract's BNB pool. The pool is funded by new deposits (90% of each goes to the pool), the pool portion of claim taxes (3--6% of every claim), sellback commissions, and referral withdraw taxes.

It's a redistribution model. BNB flows in from deposits; earnings flow out from claims. The adaptive rate is the balancing mechanism -- if the pool gets thin, the rate drops. If the pool is healthy, the rate rises. The system seeks equilibrium.

### Is this a Ponzi?

Let's be direct: BNB City is a deposit redistribution protocol with deflationary mechanics. Early players earn more than later players -- this is transparent, intentional, and hardcoded.

What makes it different from a typical Ponzi:
- **Self-regulating rate** -- the adaptive rate drops when outflows exceed inflows, preventing the pool from draining
- **Known max liability** -- every building's cap is set at creation, so the contract always knows its worst-case obligation
- **Deflationary epochs** -- extraction rates decrease over time, keeping the pool healthier as it grows
- **Full transparency** -- every mechanic, fee, and parameter is in a verified smart contract anyone can read

Can you lose money? If the pool becomes severely depleted (near-zero new deposits for an extended period), the rate drops to the 0.5% floor. You'd still earn, but slowly. The contract cannot guarantee returns -- it depends on continued participation, just like any economic system.

### What is the deposit fee?

10% of every deposit goes to the dev wallet. Your remaining 90% becomes your building's working capital. This fee is hardcoded and cannot be changed.

### What is the claim tax?

13--16% total, depending on the epoch your building was created in:
- 10% always goes to the dev wallet
- 3--6% goes back to the pool (higher in later epochs)

The pool portion is what keeps the ecosystem sustainable -- every claim partially refills the pool for everyone.

### What's this "cap bonus" I keep hearing about?

Every time you compound, your building's payout cap grows by +1%, up to a maximum of +50%. After 50 compounds, your building can pay out 50% more than its base cap.

This is the game's biggest reward for active players. Someone who logs in and compounds daily will earn significantly more total profit than someone who compounds once a week.

---

## Boosts & marketplace

### Are boosts worth it?

Depends on the boost, but generally yes -- each one has a clear ROI:

- **Auto-Action** -- pays for itself in ~1 day of extra earnings if you'd otherwise miss the 12h window
- **Compound Boost** -- doubles earnings for 7 days; the accelerated principal growth often returns 2--3x the cost
- **Claim Shield** -- cheap protection for your productivity during claim phases
- **Epoch Lock** -- permanent rate freeze; one of the highest-value plays in early epochs

See [Boosts & Upgrades](boosts.md) for detailed ROI breakdowns.

### Can I sell my building before it finishes?

Two options:
1. **Marketplace** -- list your plot (with the building) on the P2P market. Another player buys it and inherits your running business.
2. **Sellback** -- sell the building back to the pool. Commission ranges from 15% (if you've barely claimed) to 100% (if you've claimed everything). Requires a 7-day cooldown.

---

## Referrals

### How do referrals work?

Share your link. When someone builds through it, you earn:
- **2%** of their deposits (Level 1)
- **1%** of their invites' deposits (Level 2)
- **0.5%** of third-degree deposits (Level 3)
- **10%** of your L1 referrals' compounds
- **50%** of your L1 referrals' boost purchases

All credited instantly to your in-game referral balance.

### How should I use my referral balance?

**Build a new business with it.** You get 0% deposit fee (vs. 10% normally) and roughly 11% higher cap. It's the most efficient use by far.

Withdrawing costs a 20% tax. Reinvesting costs nothing and gives you better returns. The math is clear.

---

## Trust & security

### Is the contract upgradeable?

No. It's immutable. No proxy, no admin upgrade path. The deployed code is final and permanent.

### Can the team change the fees or rates?

No. Every parameter is hardcoded. The only admin function is changing the dev wallet address. That's it.

### Where can I verify the contract?

The source code is verified on BscScan. Link available in the game footer. Anyone can read the code and confirm everything documented here.

### What if the team disappears?

The contract keeps running. It has no pause function, no kill switch. Even if the website goes offline, the contract remains on BSC and can be interacted with directly through any blockchain explorer. Your buildings keep earning.
