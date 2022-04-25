---
description: 获取商户的结算币种
---

# Get Settle Currency

这个方法可以获取商户的结算币种

### 合约方法

```
 
 
function getSettleCurrency(
    address _merchant
) external view returns(address);
 
 
```

#### Parameters

1. address \_merchan 商户钱包地址



#### Response

1. address 商户设置的结算币种（0x0000000000000000000000000000000000000000为未设置)

### Web3示例

```

let contract = new web3.eth.Contract(contractAbi, contractAddress);

let settleCurrency= await contract.methods.getSettleCurrency(merchantAddress).call();


```
