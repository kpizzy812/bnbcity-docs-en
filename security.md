# Security & Trust

In DeFi, trust comes from code -- not promises. BNB City is built so you don't need to trust anyone -- just verify the contract.

## Your money stays yours

This is the most important thing to understand: **all player BNB is held inside the smart contract on the blockchain, not in anyone's personal wallet.**

When you build, your BNB goes into the contract and stays there. Not into the developer's account, not into an exchange, not into some "pool" under someone's control. It sits inside a program that operates strictly by its hardcoded rules.

**Nobody -- not the developer, not the team, not a hacker -- can simply withdraw funds from the contract.** BNB can only leave the contract in three ways:
- A player claims their earned yield (minus claim tax)
- A player uses the sellback function
- Developer fees are automatically calculated and distributed by the code

That's it. No other withdrawal paths exist in the code. This is not a promise -- it's math.

## One contract, no backdoors

BNB City runs on a **single Solidity smart contract** on BNB Smart Chain (~1,170 lines):

- **No proxy pattern** -- the contract cannot be upgraded or swapped out. The code running today runs forever.
- **No pause function** -- nobody can freeze or stop it. Not the team, not anyone.
- **No external dependencies** -- no oracles, no bridges, no "we rely on this other protocol" risk.

## What the admin can and cannot do

**The admin can:**
- Change the dev wallet address (where dev fees are sent)

That's the only admin function. It doesn't give access to player funds. **The admin cannot:**
- Change deposit fees, claim taxes, or any economic parameter
- Pause, stop, or kill the contract
- Withdraw player deposits or earnings
- Modify building parameters after creation
- Change referral percentages or boost costs
- Add new functions or alter existing logic

This is not a "trust us" situation. These limitations are enforced by the smart contract code itself. The admin literally does not have the functions to do these things.

## Every parameter is hardcoded

These values are burned into the contract and cannot be changed by anyone, ever:

| What | Value | Can it change? |
|------|-------|---------------|
| Deposit fee | 10% | No |
| Claim tax (dev portion) | 10% | No |
| Claim tax (pool portion) | 3--6% by epoch | No |
| Referral levels | 2% / 1% / 0.5% | No |
| Referral withdraw tax | 20% | No |
| Marketplace fee | 10% | No |
| Tier deposits | 0.001 -- 5 BNB | No |
| Land prices | 0.002 -- 0.125 BNB | No |
| Epoch thresholds | 5 -- 200 BNB | No |
| Rate floor / ceiling | 0.5% -- 10% | No |

If someone tells you "the team might change the fees" -- they physically cannot. The contract doesn't have a function for it.

## Protection against common attacks

| Attack type | How BNB City handles it |
|------------|------------------------|
| **Reentrancy** | OpenZeppelin ReentrancyGuard + Checks-Effects-Interactions pattern (industry gold standard) |
| **Flash loan manipulation** | The adaptive rate uses `activeDeposits`, not contract balance. Flash loans can deposit BNB but can't change the rate calculation. |
| **Sandwich attacks** | All deposit amounts are fixed by tier. There's no slippage to exploit. |
| **Dust/spam** | Minimum deposit is 0.001 BNB plus land cost. Gas fees make spam unprofitable on BSC. |
| **Self-referral** | Hardcoded check: `referrer != msg.sender`. Cannot refer yourself. |
| **Referral loops** | Referrer is set once and can never be changed. Circular chains are impossible. |

## On-chain guarantees

These aren't promises -- they're mathematical properties enforced by the code:

1. **The contract cannot pay out more than it holds.** The solvency invariant is baked into the code. Every payout checks the contract balance first.
2. **Your building's cap and tax are fixed at creation.** No retroactive changes. A building created in Epoch 0 keeps its Epoch 0 parameters forever.
3. **The adaptive rate always stays between 0.5% and 10%.** Clamped range, hardcoded. Can't go to zero, can't go to infinity.
4. **Buildings can never exceed their cap.** The code checks every claim against the remaining cap.
5. **Sellback requires a 7-day cooldown.** Prevents rapid exploitation of the exit mechanism.

## Verification

The contract source code is **verified on BscScan**. This means anyone can read the actual deployed code and confirm it matches what's documented here. No hidden functions, no obfuscated logic.

## Testing

Before deployment, the contract was tested with:
- **Hardhat integration tests** -- scenario-based testing with time manipulation
- **Foundry fuzz tests** -- randomized input testing (256+ runs) that try to break invariants
- **Testnet E2E tests** -- real multi-wallet scenarios on BSC Testnet

## The bottom line on trust

You don't need to trust the BNB City team. You need to trust the math. The contract is immutable, verified, and publicly readable. Every fee, every rate, every mechanic is transparent and unchangeable. That's the whole point of building on-chain.
