---
description: Learn how to write robust smart contracts by using design patterns.
---

# Solidity Design Patterns

Programming robust smart contracts in Solidity is a sophisticated task beause the special features of the language and how to smart contracts work.

These are some of the characteristics we should take in count when coding a smart contract:

* Code and  data are public.
* Once deployed, code cannot change.
* Writing costs gas.
* Reading is free.&#x20;
* Returning variable-lengh arrays is not allowed.
* Keys for maps are not stored.

### Control Patterns

#### Guard Check

The desired behavior of a smart contract would be to check for all required circumstances and only proceed if everything is as intended. In case of any shortcomings, the contract is expected to revert all changes that have been made to its state.

{% embed url="https://fravoll.github.io/solidity-patterns/guard_check.html" %}

#### State Machine

Enable a contract to go through different stages with different corresponding functionality exposed.

{% embed url="https://fravoll.github.io/solidity-patterns/state_machine.html" %}

#### Oracle

Gain access to data stored outside of the blockchain.

{% embed url="https://fravoll.github.io/solidity-patterns/oracle.html" %}

{% embed url="https://ethereum.org/en/developers/docs/oracles" %}

#### Randomness

Randomness in computer systems and especially in Ethereum is notoriously difficult to achieve. While it is hard or even impossible to generate a truly random number via software, the need for randomness in Ethereum is high

{% embed url="https://fravoll.github.io/solidity-patterns/randomness.html" %}

{% embed url="https://hackernoon.com/how-to-generate-random-numbers-in-solidity-lh7rj39s9" %}

### Authorization Patterns

#### Access Restriction

Not all the functionality of a smart contract should be available for everyone, it should be restricted according to suitable criteria.

{% embed url="https://fravoll.github.io/solidity-patterns/access_restriction.html" %}

#### &#x20;Multi Authorization

Sometimes in blockchain-based applications, activities might need to be authorised by multiple blockchain addresses.&#x20;

{% embed url="https://research.csiro.au/blockchainpatterns/general-patterns/security-patterns/multiple-authorization" %}

#### Off-Chain Secret Enabled Dynamic Authorisation

In blockchain-based applications, the party(ies) that can authorise a given activity may be unknown when the corresponding smart contract is deployed or the corresponding transaction is submitted to the blockchain.

{% embed url="https://research.csiro.au/blockchainpatterns/general-patterns/security-patterns/off-chain-secret-enabled-dynamic-authorization" %}

#### Ownership & Role Based Access Control

A deployed contract can have dedicated role-based operation & access, like in any traditional system. The roles allocation and administration can be done by enforcing ownership & role based access control rules.

{% hint style="info" %}
The standard implementation for this pattern is available in the OpenZeppelin [library](https://github.com/OpenZeppelin/openzeppelin-contracts/tree/master/contracts/access?ref=hackernoon.com).
{% endhint %}

{% embed url="https://hiddentao.com/archives/2020/03/21/advanced-role-based-access-control-in-solidity" %}
\

{% endembed %}

### ⭐️ Extras&#x20;

#### Interact with the outside world patterns

A set of patterns for interacting with offchain data.

{% embed url="https://research.csiro.au/blockchainpatterns/general-patterns/interacting-with-the-external-world" %}
