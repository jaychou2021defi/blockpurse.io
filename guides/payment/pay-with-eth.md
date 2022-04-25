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

### Web前端使用方式
