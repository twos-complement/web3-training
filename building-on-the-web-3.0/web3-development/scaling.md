# Scaling

As the number of people using Ethereum has grown, the blockchain has reached certain capacity limitations. This has driven up the cost of using the network, creating the need for "scaling solutions." There are multiple solutions being researched, tested and implemented that take different approaches to achieve similar goals.

### Optimistic Rollups

With Optimistic rollups, transactions are written to the main Ethereum chain as `calldata`, optimising them further by reducing the gas cost.

Optimistic rollups don't compute the transaction, so there needs to be a mechanism to ensure transactions are legitimate and not fraudulent. This is where fraud proofs come in. If someone notices a fraudulent transaction, the rollup will execute a fraud-proof and run the transaction's computation, using the available state data. This means you may have longer wait times for transaction confirmation than a ZK-rollup because the transaction could get challenged.

{% embed url="https://youtu.be/7pWxCklcNsU" %}

#### Optimisim

Optimistic Ethereum is a rollup scaling solution that allows users to submit transactions on the Ethereum network and get them executed faster for a much lower gas cost.

{% embed url="https://research.paradigm.xyz/optimism" %}

#### Arbitrum

Arbitrum uses interactive proving because it could be more efficient and more flexible. Much of the design of Arbitrum follows from this fact.

{% embed url="https://developer.offchainlabs.com/docs/inside_arbitrum" %}

#### Boba Network

Boba Network is an Optimistic Rollup that combines the great open source work done by Optimism with the research and development effort of the Enya & Boba team on swap-based onramp, fast exit and cross-chain bridging. Boba choses to build on Optimism because it is essentially a modified version of Ethereum, which makes it relatively easy to ensure EVM and Solidity compatibility, minimizing the efforts required to migrate smart contracts from L1 to L2.

{% embed url="https://docs.boba.network/faq" %}

### Zero-knowledge rollups <a href="zk-rollups" id="zk-rollups"></a>

\
**Zero-knowledge rollups (ZK-rollups)** bundle (or "roll-up") hundreds of transfers off-chain and generate a cryptographic proof, known as a SNARK (succinct non-interactive argument of knowledge). This is known as a validity proof and is posted on layer 1.

The ZK-rollup smart contract maintains the state of all transfers on layer 2, and this state can only be updated with a validity proof. This means that ZK-rollups only need the validity proof instead of all transaction data. With a ZK-rollup, validating a block is quicker and cheaper because less data is included.



### Sidechains

Coming soon...







