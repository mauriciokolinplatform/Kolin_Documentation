# Atomic Swap

An atomic swap is the exchange of one cryptocurrency for another without the participation of third parties. In the Wave’s RIDE language an atomic swap can be written as:

let Bob = Address\(base58’$BobBC1’\)

let Alice = Address\(base58’$AliceBC1’\)

match tx {

case ttx: TransferTransaction =&gt;

let txToBob = \(ttx.recipient == Bob\) && \(sha256\(ttx.proofs\[0\]\)

== base58’$shaSecret’\) && \(\(20 + $beforeHeight\)

&gt;= height\)

let backToAliceAfterHeight = \(\(height &gt;= \(21 + $beforeHeight\)\)

&& \(ttx.recipient == Alice\)\)

txToBob \|\| backToAliceAfterHeight

case other =&gt; false

}

where $shaSecret is sha256 of “some secret message from Alice”, and $beforeHeight is some predefined height.

For example, the transaction’s list will be:

1. TransferTransactionV2 from AliceBC1 to swapBC1

2. TransferTransactionV2 from swapBC1 to BobBC1 OR after some height from swapBC1 to AliceBC1 



Atomic swaps will be implemented for integrating inter-chain swaps in the Kolin exchange when needed.

