# Tuesday
* #### Interpreted And Compiled Programming Languages
    ```
    Basically an interpreted programming language executes the code we wrote line by line. On the other hand a compiled language, 
    as the name implies, must compile the whole code and then we execute the compiled version.
    
    An interpreted language is slower than a compiled one, because it does check every instruction on the run, meanwhile the
    compiled ones only check the code when it gets compiled.
    
    One of the most important disadvantages of compiled languages is the plataform dependence, this means that if you compile
    a program on Windows it cannot run on Linux
    ```
    
* #### Is Java compiled or interpreted, or both?
  ```
  Java is a special type of language because uses both features (compiled and interpreted) of languages. Programs in Java runs 
  on Java Virtual Machine (JVM). So when we what to run a programm wrote in Java we must follow a two-step compilation processes
  1. Java uses a compilation process to transform the high level code to a low one (bytecode)
  2. When the code is in bytecode, Java uses JVM to interpret that code on the run, this is basically the definition of 
  interpreted languages
  ```
  
* #### Pseudocode Currency Converter
Available Instructions
  ```
  Starting point: START
  Input: READ, GET_JSON([url])
  Output: PRINT
  Math: +, -, *, /
  Assignation: <--
  Get item in JSON: getItem([item])
  End point: END
  ```
  
Algorithm
  ```
  1. Start
  2. data <-- GET_JSON(https://api.coinbase.com/v2/prices/BTC-USD/buy)
  3. btcPriceInUSD <-- data.getItem(data).getItem(amount)
  3. usdAmount <-- READ
  4. conversionValue <-- usdAmount / btcPriceInUSD
  5. PRINT(You will get $conversionValue BTC for $usdAmount USD)
  ```
# Wednesday
* #### Your date of birth in the matrix?
```
Date of birth: 1997 -> 11111001101
```
| 2^10 | 2^9 | 2^8 | 2^7 | 2^6 | 2^5 | 2^4 | 2^3 | 2^2 | 2^1 | 2^0 |
| ---- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1024 | 512 | 256 | 128 | 64  | 32  | 16  | 8   | 4   | 2   | 1   |
| ---- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1    | 1   | 1   | 1   | 1   | 0   | 0   | 1   | 1   | 0   | 1   |
* #### MIPS
Create a program that adds any two given numbers provided by the user
```
.data
          number1: .asciiz "\nType in the first number: "
          number2: .asciiz "\nType in the second number: "
          result1: .asciiz "\nThe sum of "
          result2: .asciiz " and "
          result3: .asciiz " is: "
  .text
	      main:
              li $v0, 4
              la $a0, number1
              syscall

              li $v0, 5
              syscall

              move $t0, $v0

              li $v0, 4
              la $a0, number2
              syscall

              li $v0, 5
              syscall

              move $t1, $v0
              
              add $t2, $t0, $t1

              li $v0, 4
              la $a0, result1
              syscall
              
              li $v0, 1
              move $a0, $t0
              syscall
              
              li $v0, 4
              la $a0, result2
              syscall
              
              li $v0, 1
              move $a0, $t1
              syscall
              
              li $v0, 4
              la $a0, result3
              syscall
              
              li $v0, 1
              move $a0, $t2
              syscall
```
Create a program that displays your name
```
.data
	      myName: .asciiz "\nEleazar Jared Lopez Osuna"
.text
	      main:
              li $v0, 4
              la $a0, myName
              syscall
```



















