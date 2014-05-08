CE5
===
Austin Bolinger

##Task 1 & 2

| Op Code       | Code          | Hex Code   |Comments|
|:-------------:| --------------|:----------:| -------|
| addi          | $s0, $0, 44   | 0x2010002C |load 44 into save register 0 |
| addi          | $s1, $0, -37  | 0x2011FFDB |load -37 into save register 1|
| add           | $s2, $s0, $s1 | 0x02119020 |add registers 1 and 0. Then, put the answer in register 2|
| ori           | $s3, $s2, 8000| 0x36531F40 |ors register 2 with the immediate value and stores in register 3|
| sw            | $s2, 0x54($0) | 0xAC120054 |store what is in register 2 into Hex 54|

![Test Bench Full](https://github.com/Austinbolinger/CE5/blob/master/tbfull.JPG?raw=true "test bench full")
![TB 50ns](https://github.com/Austinbolinger/CE5/blob/master/tb50.JPG?raw=true "test bench 50ns")

###Analysis 2
Task 2 worked. If you look at the 20ns mark on the aluout data line, you can see that the data output is x7. This is what happens when you add x2c and xffffffdb (44+-37), you get x7 (7).  When x54 shows up in the aluout, I am writing data (wd) to address x54.

##Extended Functionality Table
![Table](https://github.com/Austinbolinger/CE5/blob/master/task3table.JPG?raw=true "Table")

##Additional Functionality
![Schematic](https://github.com/Austinbolinger/CE5/blob/master/mipsSchematic.JPG?raw=true "Schematic")

![Task 3 TB](https://github.com/Austinbolinger/CE5/blob/master/task3tb45.JPG?raw=true "task 3 tb")

###Analysis 3
Task 3 worked as well. If you look at the 20 ns mark on the aluout data line again, you will see that data output is again x7. Which is the add function. Then, the ori ors that value with x8000 which should result in a x8007 value. If you look at the aluout data line at 30 ns, you will see x8007 as expected. Then, again, x54 is the address to which it saves.


####Documentation
I used this website to check my conversions into mips hex because I originally keep getting the wrong values and messed up my test bench.
http://www.mipshelper.com/mips-converter.php?binary=&binaryR1=&binaryR2=&binaryR3=&binaryR4=&binaryR5=&binaryR6=&binaryI1=&binaryI2=&binaryI3=&binaryI4=&binaryJ1=&binaryJ2=&hex=&instruction=addi+%24s0%2C+%240%2C+44&submit=Convert

C3C Pluger: whenever I found an idea of what to change, I would bounce it off of him as a sanity check. Often, he would ask why I was doing something, and I would realize that I should be doing something a little bit different. 

