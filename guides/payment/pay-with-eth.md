---
description: 使用ETH进行付款
---

# Pay With ETH

这个方法允许用户通过ETH来对订单进行付款，如果商户配置只收USDC时，Blockpurse会替商户将订单收取的代币替换为USDC结算给商户，如果商户未选择只收USDC时，Blockpurse会按照当时市场价收等同于订单金额的ETH数量。

### 合约方法

```
function payWithETH(
        string memory _orderId,
        address _merchant,
        uint256 _orderAmount
) external payable returns(bool)
```

###

#### Parameters

1. _string:    orderId 商户平台生成的订单号，需要保持唯一，不可重复_
2. address:    \_merchant Blockpurse注册商户钱包地址
3. uint256:    \_orderAmount 订单金额（已USDC计算)



Response

* _bool:   调用结果_

__

### Web3示例



```


let contract = new web3.eth.Contract(contractAbi, contractAddress);

await contract.methods.payWithETH(orderId,merchantAdress, payAmount).send({from: walletAddress, value: payAmount})
    .on('transactionHash', function(hash){
                
    })
    .on('confirmation', function(confirmationNumber){
        
    })
    .on('receipt', function(receipt){
       
    })
    .on('error', function(error) {
       
    });

```
