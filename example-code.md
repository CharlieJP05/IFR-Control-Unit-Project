# Instructions

## How to write

Each instruction in word form should be written as:  
rotate to+meta | var1(x)  
null           | var1(y)  
null           | var1(z)  
null           | var1(w)  

But for ease, the pseudo version is as such:  
var1 : 2sCompliment, etc.  
rotate to var1  

## Constants

These all reside in the last memory locations:  
- StationPos  
- GunPos  
- ShopPos  

## Instruction Set

As the instruction bit is 4 bits (for now), we get 16 instructions.  
More detailed ones can be below them:  

- `0000`: null/empty location/comment (disabled code, etc.)  
- `0001`: data (stores value)  
- `0010`: face (face a vector or direction, not yet figured out)  
- `0011`: thrust (turns on certain thrust at certain powers)  
- `0100`: thrustVec (does math to thrust at a certain power in a certain direction)  
- `0101`: settings (dampen, lock, etc.)  
- `0110`: input (??)  
- `0111`:  
- `1000`: gotopos (uses other instructions to go somewhere?)  
- `1001`:  
- `1010`:  
- `1011`: display data?  
- `1100`: bra  
- `1101`: brp  
- `1110`: brz  
- `1111`: end  

#### Pseudocode Example
```cpp
n/a
```

---

[Back to README](./README.md)