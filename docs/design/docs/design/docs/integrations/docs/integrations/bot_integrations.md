# Bot & Automation Integration Guide

SWPR Protocol enables permissionless sweeping.  
This makes it ideal for automation bots, keeper networks, and custom scripts.

Bots help execute sweeps efficiently as dust pools reach conversion thresholds.

---

## 🔵 How Bots Interact With SWPR

Bots primarily call:

```solidity
collector.sweepToken(tokenIn, tokenOut, minAmountOut);
