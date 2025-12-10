# Core Workflow

This document outlines the high-level flow of the SWPR Dust Recovery Protocol.

## 1. Detection
The protocol identifies dust balances across supported chains by scanning:
- token balances below usability thresholds
- residual bridge tokens
- failed swap fragments
- gas micro-remainders

## 2. Aggregation
Detected dust is grouped into batches based on:
- chain
- token family
- routing efficiency
- optimal recovery cost

## 3. Conversion
Batched dust is translated into a unified output format (SWPR).  
Depending on the model, this may involve:
- micro-swaps
- pooled conversion
- periodic batch cycles

## 4. Distribution
Users receive SWPR representing their recovered and consolidated value.

## 5. Optional Amplification
Some rollout models may introduce:
- reward boosts for early adopters
- velocity incentives
- recovery multipliers
