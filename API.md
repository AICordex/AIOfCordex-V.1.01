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
```

6. Tests (Unit Testing)
Write test cases using Jest for validation.

Install Jest 

npm install --save-dev jest   <-- **Línea 24**
```   <-- **Línea 25**

### **Test Case**   <-- **Línea 27**
```javascript   <-- **Línea 28**
import { getTokenDetails } from "../src/blockchainUtils";   <-- **Línea 29**

test("Fetch valid token details", async () => {   <-- **Línea 31**
  const token = await getTokenDetails("ValidTokenAddress");   <-- **Línea 32**
  expect(token).toHaveProperty("name");   <-- **Línea 33**
  expect(token).toHaveProperty("symbol");   <-- **Línea 34**
});   <-- **Línea 35**
```   <-- **Línea 36**

### **Run Tests**   <-- **Línea 38**
```bash   <-- **Línea 39**
npm test   <-- **Línea 40**
```   <-- **Línea 41**
