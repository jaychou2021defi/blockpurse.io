# Set Auto Settle



这个方法允许商户更新商户结算账户（地址）。

### 合约方法

```
 
 
 function setAutoSettle(
     bool _autoSettle
 ) external;
 
 
```



#### Parameters

1. bool_:_    \_autoSettle 是否自动结算（true/false)

__

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
