# Instructions

## Example Instruction

Take `0101` to mean "rotate to":

```
0101 0000 0000 0110 | 1010 0101 0110 1010
0000 0000 0000 0000 | 1010 0101 0110 1010
0000 0000 0000 0000 | 1010 0101 0110 1010
0000 0000 0000 0000 | 1010 0101 0110 1010
```

- First byte is the instruction.
- Fourth byte represents signs: `+x -y -z +w`.
- Right bits are signed data for x, y, z, w based on the signed bit.