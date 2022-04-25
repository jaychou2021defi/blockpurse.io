---
description: 获取商户是否单笔固定收费
---

# Get Fixed Rate

这个方法可以获取商户是否自动结算

### 合约方法

```
 
 
function getFixedRate(
    address _merchant
) external view returns(bool);
 
 
```

#### Parameters

1. address \_merchan 商户钱包地址



#### Response

1. bool 单笔固定收费

### Web3示例

```

let contract = new web3.eth.Contract(contractAbi, contractAddress);

let isFixedRate= await contract.methods.getFixedRate(merchantAddress).call();


```
