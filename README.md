
#8-bit-simulator-JC-62-machine-
GUI software implementation of very first computer. 
(COMPUTER ORGANISATION AND ARCHITECTURE)
JC-62 simulator help us to perform all the instructions of JC-62 machine. JC-62 is
a simple computer which helps us to perform simple addition, subtraction and
branching. A single 12-bit-wide bus provides for exchange of information between
pairs of registers within the data path section. The registers and the 256 X 12 bit
RAM memory are controlled by 16 control signals. Most of the registers have Load
(L) and Enable (El signals. An active L signal to a register causes the contents of
the bus to be clocked into that register on the next rising pulse from the system
clock. An active E signal enables the tristate outputs of the register, thereby
making its contents available to the bus.

Processing of data is done by the Arithmetic-Logic-Unit (ALU), a circuit that is
capable of adding or subtracting the 8-bit numbers contained in its two input
registers : the accumulator (ACC) and register B. The operation performed by the
ALU is selected by the Add (A) or Subtract(S) control signals. The accumulator also
contains a single flip-flop that is set whenever its contents are negative
(i.e. whenever the leading bit is set,meaning a negative, two's complement of
number.) The value of this "negative flag" provides input to the controller/
sequencer, and, as we shall see, permits implementation of conditional branching
instructions .
The machine's RAM memory is accessed by first placing the 8-bit address in the
Memory Address Register (MAR). An active Read (R) control signal to the RAM will
then cause the selected word from the RAM to appear in the Memory Data
Register(MDR) . An active Write (W) signal, on the other hand, will cause the word
contained in the MDR to be stored in the RAM at the address specified by the
MAR .

This JC-62 simulator helps us to perform all types of code that can run through
JC-62 machine.

#Registers & Components:
  1. Program Counter
  2. MAR
  3. MDR
  4. ALU
  5. ACCUMULATOR
  6. B Register
  7. IR
#Flags
  1. Negative Flag

#Instruction Set
  1. LDA X : Load the accumalator(ACC) with X
  2. MBA : Move the value contained in ACC to register B
  3. STA Z : Store the result contained in ACC to some variable Z
  4. ADD : Addition of value in register B to ACC
  5. SUB : Subtract the value contained in B from ACC
  6. JMP X : The flow of code jumps to the X memory address.
  7. JN X : Jump if negative. Loops only if the condition is negative.
  8. HLT : Halt, this is where the execution of the code stops.

#How to run
  On the left hand side is a text window where you write your code.
  In the middle there is table which corresponds to the memory. 
  Double click on any address then edit its name and value below the table, hit "Set Values" to set them.
  Eg. You choose address 1 change the label from NULL to X and value to 12. Now your variable X contains 12.
  After setting the values, next part is to type in the code and see the flow of memory in registers.
  Write your code on the left side and hit submit.
  Last but not the least hit "Step" to see how it runs.
 
#Sample code
  LDA X 
  MBA   
  LDA Y 
  ADD
  STA Z 
  HLT 

#Execution of sample code
  LDA X (Say you have set the label as X and value as 12, so it will load ACC with value of X)
  MBA   (Move: B <- A)
  LDA Y (Say you have set another label as Y and value as 13, so it will load ACC with value of Y)
  ADD (ACC <- ACC + B)
  STA Z (Store the contents on ACC onto a new variable)
  HLT (Stop)

This project is done in python 3 and GUI framwork used is Tkinter.

To study more about this framework : https://www.youtube.com/watch?v=RJB1Ek2Ko_Y&list=PL6gx4Cwl9DGBwibXFtPtflztSNPGuIB_d
