# Aggregation Specification

This document defines how dust is grouped into efficient batches before conversion.

## Purpose
Aggregation reduces gas usage and increases recovery efficiency by processing multiple dust fragments together.

## Inputs
The Aggregator receives:
- verified dust fragments  
- chain identifiers  
- token families  
- routing metadata  
- gas cost estimates  

## Batching Rules
Dust fragments may be batched based on:

### 1. **Chain**
Dust is grouped per chain to avoid unnecessary cross-chain operations.

### 2. **Token Family**
Examples:
- ERC-20  
- ERC-404  
- SPL (Solana)  
- Cosmos-SDK assets  

### 3. **Value Density**
Dust amounts below a certain density may be merged to create a single viable batch.

### 4. **Routing Efficiency**
Batches may be formed to minimize:
- gas usage  
- micro-swap costs  
- bridge fees (if applicable)  

### 5. **Operational Size Limits**
Batches should not exceed:
- maximum on-chain transaction size  
- maximum number of fragments per batch  
- conversion engine’s capacity  

## Output
The Aggregator produces a **Batch Object** containing:
- chain  
- token family  
- fragment list  
- total recoverable value  
- recommended conversion route  

Batch objects are passed to the **Conversion Engine**.
