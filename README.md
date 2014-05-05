CE5
===
Austin Bolinger

##Task 1 & 2

| Op Code       | Code          | Hex Code   |Comments|
|:-------------:| --------------|:----------:| -------|
| addi          | $s0, $0, 44   | 0x2010002C |load 44 into save register 0 |
| addi          | $s1, $0, -37  | 0x2011FFDB |load -37 into save register 1|
| add           | $s2, $s0, $s1 | 0x02119020 |add registers 1 and 0. Then, put the answer in register 2|
| sw            | $s2, 0x54($0) | 0xAC120054 |store what is in register 2 into Hex 54|
| sw            | $s3, $s2, 8000| 0x36531F40 |ors register 2 with the immediate value and stores in register 3|


####Documentation

I used this website to check my conversions into mips hex because I originally keep getting the wrong values and messed up my test bench.
http://www.mipshelper.com/mips-converter.php?binary=&binaryR1=&binaryR2=&binaryR3=&binaryR4=&binaryR5=&binaryR6=&binaryI1=&binaryI2=&binaryI3=&binaryI4=&binaryJ1=&binaryJ2=&hex=&instruction=addi+%24s0%2C+%240%2C+44&submit=Convert
