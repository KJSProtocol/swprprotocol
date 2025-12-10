# System Architecture

The SWPR Protocol is built from modular components that work together to detect, aggregate, convert, and distribute dust-derived value.  
Each module is independent, upgradeable, and designed for cross-chain support.

## 1. Dust Scanner
The scanner identifies dust fragments across supported chains.  
It performs:
- balance checks  
- micro-threshold evaluations  
- token-family classification  
- fragment extraction  

The scanner never moves funds—only analyzes balances with user approval.

## 2. Aggregator
The Aggregator groups dust fragments into batch objects based on:
- chain  
- token family  
- value density  
- routing efficiency  

Batching dramatically reduces gas use and improves conversion outcomes.

## 3. Conversion Engine
The Conversion Engine transforms batches into unified SWPR value.  
It may operate using:
- micro-swaps  
- pooled conversions  
- periodic batch cycles  

All conversion rules are transparent and verifiable through logs.

## 4. Distribution Layer
After conversion, users receive SWPR tokens proportional to the recovered value.  
This layer ensures:
- fair distribution  
- optional incentive multipliers  
- stable user-facing outcomes  

## 5. Optional Incentive Layer
This layer enhances the base protocol by offering:
- early user boosts  
- velocity/staking-like benefits  
- recovery multipliers  
- community growth incentives  

This layer is **never required** but adds strategic value during rollout phases.

## Architecture Summary
SWPR’s architecture follows a simple pipeline:

**Detect → Aggregate → Convert → Distribute → (Optional) Amplify**

This modular design allows SWPR to scale across chains and integrate with wallets and dApps easily.
