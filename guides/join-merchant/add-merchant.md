---
description: 注册为Blockpurse商户
---

# Add Merchant

这个方法允许用户注册为Blockpurse平台商户，通过Blockpurse使用去中心化协议进行支付结算。

### 合约方法

```

function addMerchant(
    address payable _settleAccount, 
    address _settleCurrency, 
    bool _autoSettle, 
    bool _isFixedRate, 
    address[] memory _tokens
) external;


```



#### Parameters

1. address_:_    \_settleAccount 结算账户（地址），与\_autoSettle组合使用，当商户设置为自动结算时，用户完成支付时Blockpurse会自动将待结算加密货币提取至该地址
2. address:    \_settleCurrency 商户结算币种，设置后Blockpurse会自动将用户付款的加密货币兑换为等价的结算币种作为商户的待结算金额
3. bool:    \_autoSettle 商户是否为自动结算
4. bool:    \_isFixedRate  Blockpurse平台是否按照单笔固定收费（每笔1USDC），若为falseBlockpurse平台按照0.5%收取手续费（具体数字以官网最新公布为准）
5. address\[]:    \_tokens 商户支持用户选择付款的加密货币列表

__

### Web3示例



```


let contract = new web3.eth.Contract(contractAbi, contractAddress);

await contract.methods.addMerchant(settleAccount, settleToken, autoSettle, isFixedRate, tokens).send({from: walletAddress})
    .on('transactionHash', function(hash){
                
    })
    .on('confirmation', function(confirmationNumber){
        
    })
    .on('receipt', function(receipt){
       
    })
    .on('error', function(error) {
       
    });

```
