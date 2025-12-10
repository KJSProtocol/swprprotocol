# Full Protocol Lifecycle

The SWPR Protocol lifecycle describes how dust moves through its stages:  
**Deposit → Pool → Sweep → Convert → Treasury → Allocate**.

Each step is on-chain, permissionless, and fully transparent.

---

## 🔵 Stage 1: Deposit (User → DustCollector)

Users deposit tiny, otherwise unusable fragments of tokens:

1. Approve DustCollector  
2. Call `depositDust(token, amount)`  
3. Internal pool for that token increases  
4. Event emitted: `DustDeposited`  

No accounting by user is stored.  
Dust pools are **global**, not per-user.

---

## 🔵 Stage 2: Dust Pool Accumulation

Each token has its own independent dust pool:

Pools continue accumulating across users until one or more thresholds are reached:

- `minSweepAmount`
- Sufficient liquidity available
- Favorable gas conditions

---

## 🔵 Stage 3: Sweep Trigger (Anyone)

Anyone can trigger a sweep:

```solidity
sweepToken(tokenIn, tokenOut, minAmountOut)
tokenIn → tokenOut
SwprTreasury
distribute(token)
Deposit → Pool → Sweep → Convert → Treasury → Allocate → Reset

