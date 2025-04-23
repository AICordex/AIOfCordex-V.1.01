# **API Reference**

## `getTokenDetails(tokenAddress)`
Retrieves metadata for a given Solana token directly from the blockchain.

### **Parameters**
- `tokenAddress` (`string`): The public address of the token on the Solana blockchain.

### **Returns**
A `Promise` resolving to a JSON object with the token’s core metadata:
```json
{
  "name": "TokenName",
  "symbol": "TKN",
  "decimals": 6,
  "totalSupply": "1000000"
}
```

### **Example Usage**
```javascript
import { getTokenDetails } from "./src/blockchainUtils.js";

const tokenAddress = "YourTokenAddressHere";

getTokenDetails(tokenAddress)
  .then((data) => console.log(data))
  .catch((err) => console.error("Error fetching token details:", err));
```

---

# **Testing**

NycthIA includes a robust suite of **unit tests** using **Jest**, ensuring reliability and confidence in every call to the Solana blockchain.

### **Install Jest**
To begin testing, install Jest as a development dependency:

```bash
npm install --save-dev jest
```

> Ensure `"type": "module"` is present in your `package.json` if you're using ES Modules.

### **Sample Test Case**
```javascript
// File: __tests__/blockchainUtils.test.js

import { getTokenDetails } from "../src/blockchainUtils.js";

test("Fetch valid token details", async () => {
  const token = await getTokenDetails("ValidTokenAddressHere");
  expect(token).toHaveProperty("name");
  expect(token).toHaveProperty("symbol");
  expect(token).toHaveProperty("decimals");
  expect(token).toHaveProperty("totalSupply");
});
```

### **Configure package.json**
Make sure to add the following to your `package.json`:

```json
"scripts": {
  "test": "jest"
}
```

### **Run Tests**
Launch the test suite with a simple command:

```bash
npm test
```

---
