CE5
===
Austin Bolinger

##Task 1

lw	  \t$s0, 44        \t #load 44 into register 0

lw	 \t $s1, -37        \t#load -37 into register 1

addi 	\t$s2, $s0, $s1   \t#add register 1 and 0 and put the answer in register 2

sw	  \t$s2, 2B($0)    \t #store what is in register 2 into Hex 54
