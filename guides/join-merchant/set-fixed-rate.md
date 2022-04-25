---
description: 更新商户是否采用单笔固定收费模式
---

# Set Fixed Rate

这个方法允许商户更新商户是否采用单笔固定收费模式

### 合约方法

```
 
 
 function setFixedRate(
    bool _fixedRate
 ) external;
 
```

#### Parameters

1. bool \_autoSettle 是否自动结算（true/false)



### Web3示例

```

let contract = new web3.eth.Contract(contractAbi, contractAddress);

await contract.methods.setFixedRate(isFixedRate).send({from: walletAddress})
    .on('transactionHash', function(hash){
                
    })
    .on('confirmation', function(confirmationNumber){
        
    })
    .on('receipt', function(receipt){
       
    })
    .on('error', function(error) {
       
    });
    
    
```
