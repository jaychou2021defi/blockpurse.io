---
description: 提取待结算加密货币
---

# ClaimToken

这个方法允许商户提取已经在Blockpurse上获得的待结算加密货币余额。

### 合约方法

```
function claimToken(
    address _token,
    uint256 _amount,
    address _to
) external
    
    
```

###

#### Parameters

1. _address: \_token 需要提取的加密货币_
2. uint256: \_amount 需要提取的加密货币金额
3. _address_: \_to 提取加密货币到指定地址

### Web3示例

```

let contract = new web3.eth.Contract(contractAbi, contractAddress);

await contract.methods.claimToken(DAI,'10000000000000000', walletAddress).send({from: walletAddress})
    .on('transactionHash', function(hash){
                
    })
    .on('confirmation', function(confirmationNumber){
        
    })
    .on('receipt', function(receipt){
       
    })
    .on('error', function(error) {
       
    });
```
