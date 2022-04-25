---
description: 使用代币进行付款
---

# Pay

这个方法允许用户通过ERC20的代币来对订单进行付款，如果商户配置只收USDC时，Blockpurse会替商户将订单收取的代币替换为USDC结算给商户，如果商户未选择只收USDC时，Blockpurse会按照当时市场价收等同于订单金额的代币数量。

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

### Web前端使用方式

```
let contract = new web3.eth.Contract(contractAbi,contractAddress);
        await contract.methods.pay(orderId,payAmountWei, orderAmountWei,merchantAdress, tokenAddress).send({from: walletAddress})
            .on('transactionHash', function(hash){
               ...
            }).on('confirmation', function(confirmationNumber){
                ...
            }).on('receipt', function(receipt){
                ...
            }).on('error', function(error) { 
            });
```
