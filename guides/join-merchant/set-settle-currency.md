---
description: 更新商户结算币种
---

# Set Settle Currency

这个方法允许商户更新商户结算币种。

### 合约方法

```
 
 
 function setSettleCurrency(
     address payable _currency
 ) external;
 
 
```



#### Parameters

1. address_:    \_tokens_ 结算币种(USDC),或 0x0000000000000000000000000000000000000000

__

### Web3示例



```


let contract = new web3.eth.Contract(contractAbi, contractAddress);

await contract.methods.setSettleCurrency(currency).send({from: walletAddress})
    .on('transactionHash', function(hash){
                
    })
    .on('confirmation', function(confirmationNumber){
        
    })
    .on('receipt', function(receipt){
       
    })
    .on('error', function(error) {
       
    });
    
    
```
