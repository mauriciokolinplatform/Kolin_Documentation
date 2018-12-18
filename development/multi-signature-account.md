# Multi-Signature Account

Suppose that there are 3 people in the community team and they hold common funds for marketing purposes. It is convenient for the team to make a decision about the allocation of common funds according to the majority decision, and they create a multi-signature account to perform this. The implemented multi-sig account is created by SetScriptTransaction:

  
**SetScriptTransaction:**

let userPubKey = base58’B1Yz7fH1bJ2gVDjyJnuyKNTdMFARkKEpV’

let translatorPubKey = base58’7hghYeWtiekfebgAcuCg9ai2NXbRreNzc’

let moderatorPubKey = base58’BVqYXrapgJP9atQccdBPAgJPwHDKkh6A8’ let userSigned = if\(sigVerify\(tx.bodyBytes, tx.proofs\[0\], alicePubKey\)\) then 1 else 0

translatorSigned = if\(sigVerify\(tx.bodyBytes, tx.proofs\[1\], bobPubKey\)\) then 1 else 0

let moderatorSigned = if\(sigVerify\(tx.bodyBytes, tx.proofs\[2\], cooperPubKey\)\) then 1 else 0

userSigned + translatorSigned + moderatorSigned &gt;= 3

Here users gather 3 public keys in proof\[0\], proof\[1\] and proof\[2\]. The account is funded by the team members and after that, when at least 2 of 3 team members decide to spend money, they provide their signatures in a single transaction. The smart account script validates these signatures with proofs and if 2 of 3 are valid then the transaction is valid too, or else the transaction does not pass to the blockchain. Note that after the SetScriptTransaction operation all non-multi-signature transactions are discarded.

