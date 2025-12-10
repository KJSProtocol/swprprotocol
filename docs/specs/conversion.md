# Conversion Specification

This document defines how aggregated dust batches are converted into unified SWPR value.

## Purpose
The Conversion Engine translates unusable dust into a redeemable token format (SWPR), providing users with consolidated value.

## Inputs
The engine receives a **Batch Object** containing:
- chain  
- token family  
- fragment list  
- total recoverable value  
- recommended route  

## Conversion Methods

### 1. Micro-Swaps
Small token swaps performed only when:
- gas < 20–30% of fragment value
- routing liquidity is available
- slippage is minimal

### 2. Pooled Conversion
Multiple small dust amounts are merged and converted together, allowing:
- better routing efficiency  
- reduced per-user cost  
- periodic processing cycles  

### 3. Scheduled Batch Cycles
Instead of real-time conversion, the system may:
- collect dust fragments over a period  
- convert at interval-based cycles  
- distribute proportional SWPR value  

## Output
The engine produces a **Converted Batch** with:
- calculated SWPR value  
- multiplier (if applicable)  
- transaction metadata  
- user allocation data  

## Guarantees
- No user receives less than their dust’s recoverable value after fees  
- Conversion logic is deterministic for the given batch  
- Users may verify results through published conversion logs  
