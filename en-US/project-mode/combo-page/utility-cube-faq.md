# Utility Cube FAQ

## ● Utility cubes

### What is Send Token?

As it says, Send Token cube lets you send token to your designated address. Some use case can be

* Send token to multiple addresses
* Send multiple tokens to one address
* Move all your dust tokens to another wallet

### What is WETH?

When you "wrap" ETH, you aren't really wrapping so much as trading via a smart contract for an equal token called WETH. If you want to get plain ETH back you need to "unwrap" it. AKA trade it back for plain ETH.

To learn more about WETH, visit[ weth.io](https://weth.io/)

### What is Add Funds?

Add Funds cube is used when you need to send ETH or tokens to Furucombo **during the execution** of a combo.&#x20;

For example, when you wanna claim your CRV and sell them to DAI, you must use "Add Funds" to complete the combo. This is because when you claim CRV, the claimed CRV tokens go straight to your wallet but not Furucombo. In order to continue sending those CRV to Uniswap, you need to send the CRV to Furucombo first. See the correct setup below.

<figure><img src="../../.gitbook/assets/image (18).png" alt="Add Fund cube"><figcaption><p>Add Fund cube</p></figcaption></figure>

### What is Return Funds?

Return Funds cube is used when you want to send ETH or tokens back to your wallet **during the execution** of the combo. Although Furucombo sends all the funds back to users upon completing the execution of the combo, in some cases, Return Funds must be added to successfully execute the combo.&#x20;

For example (see below image), you want to swap your collaterals on Compound, say cDAI to cETH. When you borrow ETH from flashloan and supply the ETH to Compound, the cETH you see in the second cube is actually sent to Furucombo's proxy. Your cDAI are locked until you have enough cETH supporting your debt, so here we need "Return Funds" cube which transfers cETH from Furucombo's proxy to your wallet. And in the next cube, you move your cDAI to Furucombo's proxy by "Add Funds" cube!

<figure><img src="../../.gitbook/assets/image (35).png" alt="Compound cToken Collateral Swap"><figcaption><p>Compound Collateral Swap</p></figcaption></figure>
