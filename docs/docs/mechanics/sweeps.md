# Sweep Mechanics

Sweeps are the core of the SWPR Protocol:  
the moment where pooled dust is converted into meaningful, usable value.

Sweeps are **permissionless**, **transparent**, and **fully on-chain**.

---

## 🔵 What Is a Sweep?

A sweep is a conversion event that:

1. Reads the pooled dust balance for a token  
2. Zeroes that pool BEFORE performing any external calls  
3. Executes a safe DEX swap via the router  
4. Sends ALL output tokens directly to the treasury  
5. Emits a detailed event for transparency  

---

## 🔵 sweepToken() Function

```solidity
function sweepToken(
    address tokenIn,
    address tokenOut,
    uint256 minAmountOut
) external returns (uint256 amountOut);
event SweepExecuted(
    address indexed tokenIn,
    uint256 amountIn,
    address indexed tokenOut,
    uint256 amountOut
);
