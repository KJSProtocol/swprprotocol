# SWPR Protocol Flow Diagrams

## Dust → Value Lifecycle

## Deposit Flow

1. User approves token  
2. Calls `depositDust(token, amount)`  
3. Collector increments pool balance  

## Sweep Flow

1. Anyone calls `sweepToken(tokenIn, tokenOut, minAmountOut)`  
2. Collector zeroes pool balance  
3. Router executes safe swap  
4. Treasury receives swapped value  

## Distribution Flow

Treasury allocates value across:

- Founder  
- Reserve  
- Incentives  

All using BPS-defined percentages.

