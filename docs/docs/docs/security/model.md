# Security Model

SWPR Protocol is intentionally designed with a **minimal, risk-reducing architecture**.  
Instead of using complex upgrade paths, layered strategies, or custom AMMs,  
SWPR focuses on a small number of single-purpose modules that are easy to reason about and easy to audit.

This significantly reduces the potential attack surface.

---

## 🔵 Core Security Principles

### 1. **No Proxy Upgrades**
SWPR v1 does **not** use upgradeable proxy patterns.  
Each module is immutable after deployment, preventing:

- Storage collisions  
- Misconfigured proxies  
- Malicious implementation swaps  
- Governance capture via upgrades  

Upgrades require **new deployments**, protecting users.

---

### 2. **Minimal Attack Surface**
The contracts are deliberately small:

- No dynamic routing logic  
- No complex math  
- No token wrapping/unwrapping  
- No on-chain calculations requiring oracles  
- No cross-contract reentrancy points  

Small code = fewer bugs, fewer vulnerabilities, safer operations.

---

### 3. **Zeroing State Before External Calls**
Before calling external routers or token transfers,  
the DustCollector zeroes its internal pool:

This prevents:

- Reentrancy  
- Multi-trigger exploits  
- Pool inflation attacks  

Zero-first is one of the strongest hardening patterns.

---

### 4. **No Price Oracles**
SWPR does **not** rely on:

- Chainlink oracles  
- TWAPs  
- AMM spot prices  
- Volatility measurements  

Sweep calls are permissionless & caller-defined, with `minAmountOut` providing safety.

This removes an entire category of oracle manipulation risks.

---

### 5. **SafeERC20 Everywhere**
All token transfers use **OpenZeppelin SafeERC20**, protecting against:

- Missing return values  
- Non-standard ERC-20s  
- Transfer reverts  
- Token quirks  

This is considered the industry standard.

---

### 6. **Vetted Swap Routers Only**
The router contract **does NOT** perform swapping logic itself.  
Instead, it wraps a **known, audited, established DEX router**, such as:

- Uniswap  
- 1inch  
- SushiSwap (optional)  
- Aggregators (future safe whitelisted)

This means SWPR does not need to audit or maintain custom AMM logic.

---

### 7. **Permissionless Sweeping**
Anyone can call `sweepToken`.  
There are:

- No special sweeper privileges  
- No gatekeeping  
- No allowlists  

This reduces governance risk and eliminates centralized control.

---

### 8. **Strict Access Control**
Admin roles are extremely limited and scoped to:

- Whitelisting tokens  
- Adjusting thresholds  
- Setting BPS values  
- Updating treasury addresses  

There is **no “god mode”** or multi-function admin surface.

---

### 9. **No User Balances Stored**
SWPR does NOT track:

- User deposits  
- User positions  
- User shares  

Dust is global, not per-user.  
This removes:

- Accounting vulnerabilities  
- Withdrawal bugs  
- Balance inconsistencies  

---

### 10. **Thickness at the Edges, Thinness at the Core**
The core protocol modules remain light and immutable.  
More complex integrations (UI, automation, governance) live **outside** the core.

This keeps the heart of the protocol secure and stable.

---

## Summary

SWPR Protocol prioritizes:

- Minimalism  
- Immutable logic  
- Safety-first routing  
- Minimal admin power  
- BPS-based deterministic distribution  
- Zero oracle risk  
- Transparent value flows  

The security approach is simple:  
**The safest system is the one with the fewest moving parts.**

