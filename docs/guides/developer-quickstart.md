# Developer Quickstart

This quickstart provides the simplest possible steps for developers integrating with the SWPR Protocol.

## 1. Install Required Libraries
Depending on language and tooling, developers may use:
- API clients  
- SDKs  
- direct JSON-RPC calls  
- REST endpoints (when available)  

Example (pseudo-code):
```js
import { SwprClient } from "@swpr/sdk";
const client = new SwprClient("mainnet");
const results = await client.scanForDust(walletAddress);
const tx = await client.recoverDust(results.fragments);
