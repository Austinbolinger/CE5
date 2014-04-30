CE5
===
Austin Bolinger

##Task 1

lw	  $s0, 44         #load 44 into register 0

lw	  $s1, -37        #load -37 into register 1

addi 	$s2, $s0, $s1   #add register 1 and 0 and put the answer in register 2

sw	  $s2, 2B($0)     #store what is in register 2 into Hex 54
