---
description: 更新商户是否自动结算
---

# Set Auto Settle

这个方法允许商户更新商户是否自动结算

### 合约方法

```
 
 
 function setAutoSettle(
     bool _autoSettle
 ) external;
 
 
```

#### Parameters

1. bool \_autoSettle 是否自动结算（true/false)



### Web3示例

```

let contract = new web3.eth.Contract(contractAbi, contractAddress);

await contract.methods.setAutoSettle(_autoSettle).send({from: walletAddress})
    .on('transactionHash', function(hash){
                
    })
    .on('confirmation', function(confirmationNumber){
        
    })
    .on('receipt', function(receipt){
       
    })
    .on('error', function(error) {
       
    });
    
    
```
