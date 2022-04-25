---
description: 获取商户结算账户
---

# Get Settle Account

这个方法可以获取商户结算账户

### 合约方法

```
 
 
function getSettleAccount(
    address _merchant
) external view returns(address);
 
 
```

#### Parameters

1. address \_merchan 商户钱包地址



#### Response

1. address 商户设置的结算账户

### Web3示例

```

let contract = new web3.eth.Contract(contractAbi, contractAddress);

let settleAccount= await contract.methods.getSettleCurrency(merchantAddress).call();


```
