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


### ⭐️ Extras&#x20;

{% embed url="https://fravoll.github.io/solidity-patterns" %}
