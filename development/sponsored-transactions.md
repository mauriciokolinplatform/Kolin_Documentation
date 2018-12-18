# Sponsored transactions

  
Since September 14th, 2018 Kolin is an autonomous asset as end users do not need any other assets for paying fees \(no need to pay 0.001 WAVES per transaction\). This was achieved by activating SponsoredFeeAssetTransaction with following fields:

Asset Id: FiKspxSpkpzT4pMUA9ccZkbJmVXTdu4JhFDXNNXr5noW

Sponsored or not \(true/false\): True

Transaction fee: 200 Kolin

![https://kolinplatform.com](../.gitbook/assets/image%20%2813%29.png)



After this transaction was confirmed, it becomes possible to use the Kolin asset as a fee \(automatically for all miners\). When transaction with sponsored fee appears any miner just puts it to forged block. Instead of just transferring fee asset to miner's balance Waves blockchain does a bit different thing: It automatically moves fee asset to sponsor's \(issuer's\) account and transfers standard transaction cost in waves from sponsor's to miner's accounts.

