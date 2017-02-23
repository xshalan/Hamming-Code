# Hamming-Code
A simple code to calculate hamming code for an entry bits of data.

What is **Hamming code** ? 
Hamming code is a set of error-correction code s that can be used to detect and correct bit errors that can occur when computer data is moved or stored. Hamming code is named for R. W. Hamming of Bell Labs.

Like other error-correction code, Hamming code makes use of the concept of parity and parity bit s, which are bits that are added to data so that the validity of the data can be checked when it is read or after it has been received in a data transmission. Using more than one parity bit, an error-correction code can not only identify a single bit error in the data unit, but also its location in the data unit.
> Definition from [whatis](http://whatis.techtarget.com/definition/Hamming-code)  

Example 
---------------  
A byte of data: 10011010
Create the data word, leaving spaces for the parity bits: `_ _ 1 _ 0 0 1 _ 1 0 1 0`
Calculate the parity for each parity bit (a ? represents the bit position being set):


----------


  

    Position 1 checks bits 1,3,5,7,9,11: 

- ? _ 1 _ 0 0 1 _ 1 0 1 0. Even parity so set position 1 to a 0: 0 _ 1 _ 0 0 1 _ 1 0 1 0 
  ---------- 

     ` Position 2 checks bits 2,3,6,7,10,11:`

- 0 ? 1 _ 0 0 1 _ 1 0 1 0. Odd parity so set position 2 to a 1: 0 1 1 _ 0 0 1 _ 1 0 1 0
  ----------

      `Position 4 checks bits 4,5,6,7,12:`

- 0 1 1 ? 0 0 1 _ 1 0 1 0. Odd parity so set position 4 to a 1: 0 1 1 1 0 0 1 _ 1 0 1 0
  ----------

      `Position 8 checks bits 8,9,10,11,12:`

- 0 1 1 1 0 0 1 ? 1 0 1 0. Even parity so set position 8 to a 0: 0 1 1 1 0 0 1 0 1 0 1 0
  ----------

`Code word: 011100101010.`
