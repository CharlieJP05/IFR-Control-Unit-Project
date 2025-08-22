
# Instructions

## How to write

each instruction in word form should be written as:
rotate to+meta | var1(x)
null   		   | var1(y)
null  		   | var1(z)
null    	   | var1(w)

but for ease the pseudo version is as such:
var1 : 2sCompliment, ect
rotate to var1

## Constants
these all reside in the last memory locations

StationPos
GunPos
ShopPos

## Instruction Set
as the instruction bit is 4 bits (for now) we get 16 instructions
more detailed ones can be below them

0000: null/empty location/comment(idfk how it would be a comment but yeah)/disabled code ig
0001: data (stores value)
0010: face (face a vector or direction, havent figured that out yet)
0011: thrust (turns on certain thrust at certain powers)
0100: thrustVec (does math to thrust at a certain power at a certain direction)
0101: settings (dampen, lock, ect)
0110: input (??)
0111: 
1000: gotopos (uses otehr instructions to go somewhere?)
1001: 
1010: 
1011: display data?
1100: bra
1101: brp
1110: brz
1111: end

#### Pseudocode Example
```cpp
n/a
```

---

[Back to README](./README.md)