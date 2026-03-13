NAME : D VEDHALAKSHMI
21224050058
## Aim:

To write 8085 microprocessor programs to find the greatest and smallest number from the given 8-bit numbers.

## Apparatus Required:

•	Laptop with an internet connection

## Finding the Greatest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the greatest).
3.	Load the next number and compare it with A.
4.	If the new number is greater, update A.
5.	Repeat the process for all numbers.
6.	Store the greatest number in 4300H.

## Program:
```
LDA 4200H  ;   
MOV C, A  ; 
LXI H, 4201H  ;
MOV A, M  ;    
INX H   ;    
DCR C   ;     
LOOP: CMP M ;
JC NEXT  ;    
MOV A, M  ;    
NEXT: INX H ;
DCR C ;        
JNZ LOOP ;      
STA 4301H ;    
HLT ;
```

## Output:
<img width="1800" height="732" alt="image" src="https://github.com/user-attachments/assets/c3e1bd90-b359-459c-8f38-ee5dd40d9114" />
<img width="305" height="575" alt="image" src="https://github.com/user-attachments/assets/9aca82b2-585c-4bb4-872e-80d2bd42b7d8" />
<img width="307" height="445" alt="image" src="https://github.com/user-attachments/assets/8d0ffa97-9a09-48f2-9549-455f2729e181" />




## Finding the Smallest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the smallest).
3.	Load the next number and compare it with A.
4.	If the new number is smaller, update A.
5.	Repeat the process for all numbers.
6.	Store the smallest number in 4301H.

## Program:
```
LDA 4200H  ;   
MOV C, A  ; 
LXI H, 4201H  ;
MOV A, M  ;    
INX H   ;    
DCR C   ;     
LOOP: CMP M ;
JNC NEXT  ;    
MOV A, M  ;    
NEXT: INX H ;
DCR C ;        
JNZ LOOP ;      
STA 4301H ;    
HLT ;
```

## Output:
<img width="1809" height="743" alt="image" src="https://github.com/user-attachments/assets/01f17a65-fdd5-4521-b372-cb87a2362d47" />
<img width="304" height="586" alt="image" src="https://github.com/user-attachments/assets/cec6c74f-b4cd-45c5-9706-5c3eebb49085" />
<img width="287" height="342" alt="image" src="https://github.com/user-attachments/assets/703caeac-6922-4476-a57b-af54aae664fb" />



## Result:

The 8085 microprocessor successfully finds the greatest and smallest numbers from multiple inputs and stores them in memory.
