Control Unit project:
an alternate type of CPU that doesnt deal in add, sub on values, but instructions are more like
face xyz
thrust main
loop
dampen on



if doing in one memory drive:
0000               0000 0000 0000
instruction   data
doesnt leave much room for data, a 0-65535 would not fit but a rotation vector would?

alternate idea:
have it as instruction - location
and use a second memory drive, or the latter half of it

alternate idea:
store data using the vector memory drive
each position stores 8 lines worth of info, have one be instruction and rest be data

if still wanted the full signal in it it can be compressed:

x+ x-
y+ y-
z+ z-
w+ w-

0000 0000 0000 0000 | 0000 0000 0000 0000
0000 0000 0000 0000 | 0000 0000 0000 0000
0000 0000 0000 0000 | 0000 0000 0000 0000
0000 0000 0000 0000 | 0000 0000 0000 0000

iiii 0000 0000 ssss | xxxx xxxx xxxx xxxx 
0000 0000 0000 0000 | yyyy yyyy yyyy yyyy
0000 0000 0000 0000 | zzzz zzzz zzzz zzzz
0000 0000 0000 0000 | wwww wwww wwww wwww

i = instruction nibble
s = sign bits for x y z w
rest is free data for now




example:
take 0101 to mean "rotate to"
0101 0000 0000 0110 | 1010 0101 0110 1010
0000 0000 0000 0000 | 1010 0101 0110 1010
0000 0000 0000 0000 | 1010 0101 0110 1010
0000 0000 0000 0000 | 1010 0101 0110 1010

first byte is instruction, 4th is signs: +x -y -z +w
right bits are signed data of the x y z w based on signed bit

rest of zeros can depend per instruction, if its 2 vecs, could store both in this


from here on:
0000 0000 0000 0000 | 0000 0000 0000 0000                 instruction | data
0000 0000 0000 0000 | 0000 0000 0000 0000                             data | data
0000 0000 0000 0000 | 0000 0000 0000 0000                             data | data
0000 0000 0000 0000 | 0000 0000 0000 0000                             data | data

each part is dealt in words so
word | word
word | word
word | word
giving 5 data words and 1 instruction word.howver the instruction word does contain metadata(signed ect)
