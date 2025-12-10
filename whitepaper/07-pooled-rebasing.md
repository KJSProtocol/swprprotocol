# Pooled Rebasing Model

The Pooled Rebasing Model allows multiple users’ dust fragments to be combined into a shared pool before conversion.  
This enables deeper liquidity, better routing, and more efficient micro-swaps — resulting in proportional value increases for every participant.

---

## Why Pooled Rebasing Exists
Individual dust fragments are often too small to convert efficiently.  
Pooling solves this by:
- increasing the total convertible value  
- accessing better liquidity routes  
- reducing gas and swap costs  
- improving batch-level outcomes  

The savings and efficiency gains are redistributed proportionally to all users in the pool.

---

## How It Works (High-Level)
The workflow is similar to the base model, with one key difference:  
**multiple users share a batch.**

### Steps:
1. Users approve scans  
2. Dust fragments enter a shared pool  
3. The pool undergoes optimized conversion  
4. Total recovered value is calculated  
5. Users receive proportional SWPR allocations  
6. A rebasing adjustment ensures exact fairness  

---

## Allocation Formula (Simple Version)
Each user receives:

Where:
- `user_share` is the value of their dust  
- `total_pool` is the sum of all dust in the batch  
- `total_recovered_value` is the SWPR generated after conversion  

Rebasing ensures perfect proportional distribution.

---

## Benefits
- better swap prices  
- lower gas cost per fragment  
- deeper liquidity routes  
- higher total recovered value  
- frictionless fair distribution  

Pooling turns “weak fragments” into strong, efficient batches.

---

## When This Model Is Ideal
- high-volume chains  
- periods of network congestion  
- community pool events  
- integrated dApp / wallet features  

Pooled Rebasing is especially powerful for wallets that perform automatic dust cleanup for their users.

---

## Summary
Pooled Rebasing transforms micro-fragments into a **collective value engine**, improving efficiency and lifting everyone together through proportional rebasing.

