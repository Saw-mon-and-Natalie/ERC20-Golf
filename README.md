# ERC20-Golf

[@the_ethernaut](https://twitter.com/the_ethernaut/status/1516131583593394176) :

> EVM golf #9:
> 
> Warning: Hardcore level!
> 
> Smallest bytecode fully compliant ERC20 implementation.

Deployed contract on Rinkeby: [`0x8b38be1ff7c640079acc30833148055086631a1e`](https://rinkeby.etherscan.io/address/0x8b38be1ff7c640079acc30833148055086631a1e)

|bytecode|deployed bytecode|
|---|---|
|273 bytes| 187 bytes|

Deployed bytecode:
```
0x60206001588060063d3560f51c600b160602601601565b602e565b6033565b603a565b6065565b6087565b60a4565b3860b1565b80355460b1565b6024358135336044565b82815481811060b75703815581805484019055913d52908354853da38160b1565b604435602435823533813d525952593d20805480851160b75784900390556044565b80356024358082333d525952593d20553d52333d54853da38160b1565b6040813d37593d205460b1565b3d52823df35b3d3dfd
```

Encrypted version to be tweeted (subtweet zone, push1 values are not encoded for better readability):

```
P20CP04!P06ZLPf5}P0b&/*P16+JDP2eJDP33JDP3aJDP65JDP87JDPa4JD_Pb1JD@LsPb1JDP24L@LEP44JD#@s@@<Pb7j-@S@!s%+WSwZMW$s^Zl@Pb1JDP44LP24L#LE@ZMmMmZK!s!^>Pb7j%W-WSP44JD!LP24L!#EZMmMmZKSZMEZs^Zl@Pb1JDP40@ZOmZKsPb1JDZM#ZRDZZr
```

Encryption Legend
```
push1           P   📌

swap1           W   💱
swap2           w   🔁

dupX            shift + X
dup1            !   🕐
dup2            @   🕑
dup3            #   🕒
dup4            $   🕓
dup5            %   🕔
dup6            ^   🕕

pc              C   ⏱ 
returndatasize  Z   0️⃣
codesize        _   ⚖

jump            J   🦘
jumpi           j   ❓
jumpdest        D   🎯

mstore          M   🏪
msize           m   📏
sstore          S   🏬
sload           s   🔎

calldataload    L   📥
calldatacopy    O   📠
caller          E   📞

log3            l   📘
return          R   🆗
revert          r   🔥

add             +   ➕
sub             -   ➖
mul             *   ✖
mod             /   🧨
and             &   ⚡
shr             }   ➡
sha3            K   🔐
lt              <   ◀
gt              >   ▶
```

Encrypted emoji version:

```
📌20📌01⏱🕐📌060️⃣📥📌f5➡📌0b⚡🧨✖📌16➕🦘🎯📌2e🦘🎯📌33🦘🎯📌3a🦘🎯📌65🦘🎯📌87🦘🎯📌a4🦘🎯⚖📌b1🦘🎯🕐📥🔎📌b1🦘🎯📌24📥🕑📥📞📌44🦘🎯🕒🕑🔎🕑🕑◀📌b7❓➖🕑🏬🕑🕐🔎🕔➕💱🏬🔁0️⃣🏪💱🕓🔎🕕0️⃣📘🕑📌b1🦘🎯📌44📥📌24📥🕒📥📞🕑0️⃣🏪📏🏪📏0️⃣🔐🕐🔎🕐🕕▶📌b7❓🕔💱➖💱🏬📌44🦘🎯🕐📥📌24📥🕐🕒📞0️⃣🏪📏🏪📏0️⃣🔐🏬0️⃣🏪📞0️⃣🔎🕕0️⃣📘🕑📌b1🦘🎯📌40🕑0️⃣📠📏0️⃣🔐🔎📌b1🦘🎯0️⃣🏪🕒0️⃣🆗🎯0️⃣0️⃣🔥
```

Unfortunately, Twitter counts emojis as 2 characters. It would have been nice to post the emoji version on Twitter if emojis were counted as 1.

## Notes
- event topics are stored in storage for bytecode optimization, but it will add to runtime gas cost
- special storage allocation for mappings

# TODO

- [x] refactor `allowance_slot` macro
- [x] hoist up some of the repeated constants up and use `dupN` opcodes, might not be good for gas.

# Issues

- [x] `etk` doesn't allow comment only lines in macros

# Ref

- [Ethernaut EVM Golf 9](https://twitter.com/the_ethernaut/status/1516131583593394176)