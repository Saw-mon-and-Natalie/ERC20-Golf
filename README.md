# ERC20-Golf

[@the_ethernaut](https://twitter.com/the_ethernaut/status/1516131583593394176) :

> EVM golf #9:
> 
> Warning: Hardcore level!
> 
> Smallest bytecode fully compliant ERC20 implementation.

Deployed contract on Rinkeby: [`0xf8B33db61c072264bEBB1333c8064BA43C3a6347`](https://rinkeby.etherscan.io/address/0xf8b33db61c072264bebb1333c8064ba43c3a6347)

|bytecode|deployed bytecode|
|---|---|
|360 bytes| 337 bytes|

## Notes
- event topics are not stored in storage for gas optimization
- storage is only used for balances and allowances

# TODO

- [ ] refactor `allowance_slot` macro
- [ ] hoist up some of the repeated constants up and use `dupN` opcodes, might not be good for gas.

# Issues

- [ ] `etk` doesn't allow comment only lines in macros

# Ref

- [Ethernaut EVM Golf 9](https://twitter.com/the_ethernaut/status/1516131583593394176)