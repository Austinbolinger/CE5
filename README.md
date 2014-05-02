CE5
===
Austin Bolinger

##Task 1

<div class="center" style="width: auto; margin-left: auto; margin-right: auto;">lw	  $s0, 44  
#load 44 into register 0
</div> 

<div class="center" style="width: auto; margin-left: auto; margin-right: auto;">lw	  $s1, -37   
#load -37 into register 1
</div> 

<div class="center" style="width: auto; margin-left: auto; margin-right: auto;">addi 	$s2, $s0, $s1 
#add register 1 and 0 and put the answer in register 2</div> 

<div class="center" style="width: auto; margin-left: auto; margin-right: auto;">sw	  $s2, 0x54($0)   
#store what is in register 2 into Hex 54</div> 

| Op Code       | Code          | Hex Code   |Comments|
|:-------------:| --------------|:----------:| -------|
| addi          | $s0, $0, 44   | 0x20100016 |load 44 into save register 0 |
| addi          | $s1, $0, -37  | 0x2012FFDD |load -37 into save register 1|
| add           | $s2, $s0, $s1 | 0x02508810 |add registers 1 and 0. Then, put the answer in register 2|
| sw            | $s2, 0x54($0) | 0xAC120036 |store what is in register 2 into Hex 54|
 
