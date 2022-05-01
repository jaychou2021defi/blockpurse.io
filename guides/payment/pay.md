---
description: 使用代币进行付款
---

# Pay

这个方法允许用户通过ERC20的加密货币来对订单进行付款，如果商户配置只收USDC时，Blockpurse会替商户将订单收取的代币替换为USDC结算给商户，如果商户未选择只收USDC时，Blockpurse会按照当时市场价收等同于订单金额的加密货币数量。

### 合约方法

```
 function pay(
        string memory _orderId,
        uint256 _paiAmount,
        uint256 _orderAmount,
        address _merchant,
        address _currency
    ) external returns(bool);
```

#### Parameters

1. _string: orderId 商户平台生成的订单号，需要保持唯一，不可重复_
2. uint256: \_paidAmount 用户预估需要支付的加密货币金额（价值约等于订单金额的USDC）
3. uint256: \_orderAmount 订单金额（已USDC计算)
4. address: \_merchant Blockpurse注册商户钱包地址
5. address: \_currency 用户选择支付的加密货币

Response

* _bool: 调用结果_

\_\_

### Web3示例

```

let contract = new web3.eth.Contract(contractAbi, contractAddress);

await contract.methods.pay(orderId,payAmount, orderAmount,merchantAdress, DAI).send({from: walletAddress})
    .on('transactionHash', function(hash){
                
    })
    .on('confirmation', function(confirmationNumber){
        
    })
    .on('receipt', function(receipt){
       
    })
    .on('error', function(error) {
       
    });
```
