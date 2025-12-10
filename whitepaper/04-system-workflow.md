# System Workflow

The SWPR Protocol follows a predictable and verifiable pipeline for transforming unusable dust into unified SWPR value.  
The workflow is designed to be simple for users, efficient for developers, and transparent for auditors.

---

## 1. Detection
Users initiate a scan through a wallet or dApp interface.  
The Dust Scanner evaluates balances on supported chains and identifies fragments that qualify as dust.

The scanner checks for:
- token amounts below usability thresholds  
- bridge leftovers  
- failed swap fragments  
- gas remainders  
- micro-airdrops  
- staking residuals  

No funds move during this step—only analysis.

---

## 2. Aggregation
Detected dust fragments are grouped into batch objects.  
Batching is based on:
- chain  
- token family  
- routing efficiency  
- value density  

This minimizes gas usage and ensures the highest possible recovery value.

---

## 3. Conversion
Aggregated batches are processed by the Conversion Engine.  
Depending on the rollout model, conversion may involve:
- micro-swaps  
- pooled conversions  
- periodic batch cycles  

The output is a unified SWPR value representing the recovered worth of the dust.

---

## 4. Distribution
Converted value is delivered to users in SWPR tokens.  
Users receive:
- their recovered value  
- conversion logs  
- batch IDs  
- optional incentive multipliers (model-dependent)  

---

## 5. Verification
All steps in the pipeline are transparent:
- detection lists  
- batch objects  
- conversion logs  
- distribution receipts  

Users and developers can independently validate the results.

---

## Workflow Summary
**Detect → Aggregate → Convert → Distribute → Verify**

This workflow makes it possible to recover value that would otherwise be permanently lost.
