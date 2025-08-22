# Instructions

## Example Instruction

Take `0101` to mean "rotate to":  
```
0101 0000 0000 0110 | 1010 0101 0110 1010  
0000 0000 0000 0000 | 1010 0101 0110 1010  
0000 0000 0000 0000 | 1010 0101 0110 1010  
0000 0000 0000 0000 | 1010 0101 0110 1010  
```  

- First nibble in the first word is the instruction.  
- Fourth nibble in the first word represents signs: `+x -y -z +w`. 0=+ 1=- by 2's complement rules.  
- Right-side words are signed data for x, y, z, w based on the signed bit.  

---

[Back to README](./README.md)