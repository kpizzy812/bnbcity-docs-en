# Smart Contract & Security

## Architecture

BNB City runs on a **single immutable smart contract** on BNB Smart Chain:

- **One contract** — all game logic in one place
- **No proxy** — no upgradability, no admin can change the rules
- **No pause** — the contract runs forever, cannot be stopped
- **No external dependencies** — only OpenZeppelin's ReentrancyGuard
- **Solidity 0.8.24** — built-in overflow protection

## What the Admin Can Do

The admin (mayor) has only **one** privileged function:
- `setDevWallet()` — change the address that receives dev fees

The admin **cannot**:
- Change fees, rates, caps, or epoch thresholds
- Pause or stop the contract
- Withdraw player funds
- Modify building parameters after creation
- Change referral percentages

## Security Measures

| Attack Vector | Protection |
|--------------|------------|
| Reentrancy | OpenZeppelin ReentrancyGuard + Checks-Effects-Interactions pattern |
| Flash loan manipulation | Rate is based on `activeDeposits`, not `balance` — flash loans can't change it |
| Sandwich attacks | Fixed deposit amounts, no slippage |
| Dust/spam attacks | Minimum 0.001 BNB deposit + land cost. Gas makes spam unprofitable |
| Self-referral | `referrer != msg.sender` check |
| Referral loops | Referrer set once, immutable |

## On-Chain Guarantees

These properties are enforced by the smart contract code:

1. **Total payouts can never exceed contract balance** — solvency invariant
2. **A building's cap and tax are fixed at creation** — no retroactive changes
3. **Adaptive rate is always between 0.5% and 10%** — clamped range
4. **Each building's total claimed can never exceed its cap**
5. **Active deposits are correctly adjusted** when buildings complete

## Verification

The contract source code is verified on BscScan. Anyone can read and audit the code.

## Testing

The contract is tested with:
- **Hardhat tests** — integration tests with time manipulation
- **Foundry fuzz tests** — randomized invariant testing (256+ runs)
- **Testnet E2E** — multi-wallet real-world scenarios on BSC Testnet
