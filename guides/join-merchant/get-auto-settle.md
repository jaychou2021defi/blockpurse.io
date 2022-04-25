---
description: 获取商户是否自动结算
---

# Get Auto Settle

这个方法可以获取商户是否自动结算

### 合约方法

```
 
 
function getAutoSettle(
    address _merchant
) external view returns(bool);
 
 
```

#### Parameters

1. address \_merchan 商户钱包地址



#### Response

1. bool 是否自动结算

### Web3示例

```

let contract = new web3.eth.Contract(contractAbi, contractAddress);

let isAutoSettle = await contract.methods.getAutoSettle(merchantAddress).call();


```
