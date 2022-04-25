---
description: 判断一个地址是否为Blockpurse注册商户
---

# Is Merchant

这个方法可以判断一个地址是否为Blockpurse注册商户

### 合约方法

```
 
function isMerchant(
    address _merchant
) external view returns(bool)
 
```

#### Parameters

1. address \_merchan 需要校验的地址



#### Response

1. bool 是否Blockpurse注册商户

### Web3示例

```

let contract = new web3.eth.Contract(contractAbi, contractAddress);

let isMerchant = await contract.methods.isMerchant(merchantAddress).call();

```
