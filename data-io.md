# Data I/O

## Memory Layout

### Single Memory Drive  
```
0000               0000 0000 0000  
instruction   data  
```  
- Doesn't leave much room for data.  
- A `0-65535` value would not fit, but a rotation vector might.  

### Alternate Ideas  

1. **Instruction - Location**  
   Use a second memory drive or the latter half of the first drive.  

2. **Vector Memory Drive**  
   - Each position stores 8 lines of info.  
   - One line is for instructions, the rest for data.  

---

## Instruction and Data Layout

From here on:  
```
0000 0000 0000 0000 | 0000 0000 0000 0000                 instruction | data  
0000 0000 0000 0000 | 0000 0000 0000 0000                             data | data  
0000 0000 0000 0000 | 0000 0000 0000 0000                             data | data  
0000 0000 0000 0000 | 0000 0000 0000 0000                             data | data  
```  

Each part is dealt in words:  
```
word | word  
word | word  
word | word  
```  

This gives 5 data words and 1 instruction word. However, the instruction word does contain metadata (signed, etc.).  

---

[Back to README](./README.md)