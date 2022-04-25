---
description: 更新商户结算账户（地址）
---

# Set Settle Account

这个方法允许商户更新商户结算账户（地址）。

### 合约方法

```
 
 
 function setSettleAccount(
     address payable _account
 ) external;
 
 
```

#### Parameters

1. address: \_account \_\_ 结算账户,或 0x0000000000000000000000000000000000000000



### Web3示例

```

let contract = new web3.eth.Contract(contractAbi, contractAddress);

await contract.methods.setSettleAccount(settleAccount).send({from: walletAddress})
    .on('transactionHash', function(hash){
                
    })
    .on('confirmation', function(confirmationNumber){
        
    })
    .on('receipt', function(receipt){
       
    })
    .on('error', function(error) {
       
    });
    
    
```
