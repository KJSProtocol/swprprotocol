# System Flow (Text Overview)

This document provides a clear, step-by-step description of how value moves through the SWPR Protocol.

## 1. User Wallet → Dust Scanner
- User signs a scan request  
- Protocol checks balances on supported chains  
- Identifies dust amounts below usability thresholds  

## 2. Dust Scanner → Aggregator
- Detected dust is grouped into batches  
- Batching reduces gas use and improves conversion efficiency  

## 3. Aggregator → Conversion Engine
- Batches are prepared for micro-swaps or pooled conversion  
- Multiple dust sources may be merged for optimal processing  

## 4. Conversion Engine → Distribution Layer
- Dust is converted into unified value (SWPR)  
- Conversion rules depend on the selected rollout model  

## 5. Distribution Layer → User
- Recovered value is returned as SWPR tokens  
- Optional multipliers, boosts, or rewards may apply  

## 6. Optional Incentive Layer
This layer can:
- reward consistent recovery  
- boost value during network growth  
- enable protocol-level velocity dynamics
