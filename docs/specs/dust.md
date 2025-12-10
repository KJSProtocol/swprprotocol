# Dust Specification

This document defines what qualifies as **dust** within the SWPR Dust Recovery Protocol.

## Definition
Dust is a token balance that:

1. Is too small to be transacted efficiently, AND  
2. Cannot be swapped, bridged, staked, or spent without losing a majority of its value to fees.

## Typical Dust Sources
- Swap remainders (decimal leftovers)
- Bridge fragments
- Failed transaction residues
- Gas micro-remainders on EVM chains
- Airdrop micros
- NFT mint leftovers
- Staking residue under minimum thresholds

## Classification Thresholds
A balance may be classified as dust if:

- The cost to move it is higher than 20–100× its value  
- The minimum on-chain action exceeds 90% of the fragment’s worth  
- Token protocols enforce minimum transfer restrictions  
- Liquidity pools reject the amount as too low to quote

Thresholds may vary per chain or per token family.

## Purpose of Classification
The dust definition determines:
- which balances the scanner collects  
- how the aggregator batches them  
- which conversion paths are used  
- how the user’s recovered value is calculated
