# **Mia-Terminal**  

**Accuracy, clarity, and valuable insights for traders and developers.**  

## **Overview**  

Mia Terminal is a powerful command-line tool designed to analyze tokens on the **Solana blockchain**. It connects directly to the blockchain using the **Solana SDK (@solana/web3.js)**, providing **real-time, detailed insights** on token information, associated accounts, and balances.

## **Features**  

✅ **Direct Blockchain Access** – Connects directly to Solana via the SDK, bypassing intermediaries.  
✅ **Comprehensive Token Insights** – Retrieve token **name, symbol, total supply, and decimals**.  
✅ **Associated Account Details** – Fetch token holders and account balances.  
✅ **Fast & Reliable** – Optimized for traders, developers, and crypto enthusiasts.  
✅ **Easy Integration** – Simple **JavaScript functions** for fetching Solana token details.

## **Technology Stack**  

- **Language**: JavaScript  
- **Blockchain**: Solana  
- **Library**: `@solana/web3.js`  
- **Runtime**: Node.js  

## **Installation**  

1. Clone this repository:  
   ```bash
   git clone https://github.com/yourusername/Leonord-Scanner-Terminal.git
   cd Leonord-Scanner-Terminal
   ```
2. Install dependencies:  
   ```bash
   npm install
   ```
3. Run the scanner:  
   ```bash
   node scanner.js
   ```

## **Usage**  

### **1. Fetch Token Details**
```javascript
import { getTokenDetails } from "./blockchainUtils.js";

const tokenAddress = "YourTokenAddressHere"; // Replace with a real token address

getTokenDetails(tokenAddress)
  .then((details) => console.log(details))
  .catch((error) => console.error(error));
```
📌 **Retrieves:**  
- Token Name  
- Symbol  
- Decimals  
- Total Supply  

### **2. Fetch Associated Accounts**  
```javascript
import { getAssociatedAccounts } from "./blockchainUtils.js";

const tokenAddress = "YourTokenAddressHere";

getAssociatedAccounts(tokenAddress)
  .then((accounts) => console.log(accounts))
  .catch((error) => console.error(error));
```
📌 **Retrieves:**  
- Account Addresses Holding the Token  
- Account Balances  

### **3. Full Token Analysis**  
```javascript
import { analyzeToken } from "./scanner.js";

const tokenAddress = "YourTokenAddressHere";

analyzeToken(tokenAddress);
```
📌 **Logs:**  
- Token Details  
- Associated Accounts & Balances  

## **Example Output**  
```bash
Token Details:
Name: ExampleToken
Symbol: EXMPL
Decimals: 6
Total Supply: 1,000,000

Associated Accounts:
1. Address: ABC123...XYZ, Balance: 500
2. Address: DEF456...XYZ, Balance: 250
```

## **Error Handling**  
The scanner includes robust error handling for:  
- Invalid token addresses  
- Network issues  
- Missing token data  

Example error output:  
```bash
Error fetching token data: Token data not found for this address.
```

## **Contributing**  
Contributions are welcome! Feel free to fork the repo and submit a pull request.

## **License**  
📜 MIT License – Free to use and modify.  
