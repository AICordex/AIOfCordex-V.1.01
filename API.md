# API Reference

## `getTokenDetails(tokenAddress)`
Fetches metadata of a Solana token.

**Parameters**:
- `tokenAddress` (string): The token’s blockchain address.

**Returns**:
```json

{
  "name": "TokenName",
  "symbol": "TKN",
  "decimals": 6,
  "totalSupply": "1000000"
}

## **6. Tests (Unit Testing)**  
Write test cases using **Jest** for validation.

### **Install Jest**
```bash
npm install --save-dev jest

import { getTokenDetails } from "../src/blockchainUtils";

test("Fetch valid token details", async () => {
  const token = await getTokenDetails("ValidTokenAddress");
  expect(token).toHaveProperty("name");
  expect(token).toHaveProperty("symbol");
});
npm test
