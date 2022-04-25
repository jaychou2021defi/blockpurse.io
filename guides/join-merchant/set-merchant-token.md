---
description: 更新商户支持的加密货币列表
---

# Set Merchant Token

这个方法允许商户更新商户支持的加密货币列表。

### 合约方法

```
 
 
 function setMerchantToken(
     address[] memory _tokens
 ) external;
 
 
```



#### Parameters

1. address_:    \_tokens_ 商户支持的加密货币列表

__

### Web3示例



```


let contract = new web3.eth.Contract(contractAbi, contractAddress);

await contract.methods.setMerchantToken(tokens).send({from: walletAddress})
    .on('transactionHash', function(hash){
                
    })
    .on('confirmation', function(confirmationNumber){
        
    })
    .on('receipt', function(receipt){
       
    })
    .on('error', function(error) {
       
    });
```
