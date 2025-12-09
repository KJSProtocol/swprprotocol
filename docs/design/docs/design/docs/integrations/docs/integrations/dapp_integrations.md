# dApp Integration Guide

Decentralized applications can integrate SWPR Protocol to eliminate leftover token fragments created during user interactions.

Examples of operations that often leave dust:

- Liquidity migrations  
- Reward harvests  
- Airdrop distributors  
- Vault exits  
- Bridge returns  
- LP unwinding  
- Token streaming / vesting leftover amounts  

SWPR allows dApps to convert these residual amounts into meaningful value for users or for the protocol.

---

## 🔵 How dApps Integrate SWPR

Most dApps will use:

```solidity
collector.depositDust(token, leftoverAmount);
collector.depositDust(rewardToken, leftover);
