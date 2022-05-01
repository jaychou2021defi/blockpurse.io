---
description: 获取商户支持的加密货币
---

# Get Merchant Tokens

这个方法可以获取商户支持的加密货币

### 合约方法

```
 
 
function getMerchantTokens(
    address _merchant
) external view returns(address[] memory);
 
 
```

#### Parameters

1. address \_merchan 商户钱包地址

#### Response

1. address\[] 商户支持的加密货币

### Web3示例

```
let contract = new web3.eth.Contract(contractAbi, contractAddress);

let tokens = await contract.methods.getMerchantTokens(merchantAddress).call();

```
