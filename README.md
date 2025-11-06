# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Manual Calculations
![WhatsApp Image 2025-11-06 at 19 09 39_3db019f4](https://github.com/user-attachments/assets/0027b404-2e99-4290-bb15-2d0f71c3e011)




## OUTPUT IMAGE FROM MASM SOFTWARE
![WhatsApp Image 2025-11-06 at 19 18 09_7775ec2c](https://github.com/user-attachments/assets/7d0610e9-224c-4ad6-8852-7694dda187eb)

## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Manual Calculations
![WhatsApp Image 2025-11-06 at 19 13 44_af3b2cfc](https://github.com/user-attachments/assets/4efb526f-fae0-426d-80b5-6e237793a359)





## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-11-06 at 19 18 56_c7633fd6](https://github.com/user-attachments/assets/e312e913-3b08-48be-8fdc-8f92d8153220)


## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Manual Calculations
![WhatsApp Image 2025-11-06 at 19 10 39_06668b3e](https://github.com/user-attachments/assets/4af3d45e-90b1-4ef7-bb7b-f19533c73046)




## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-11-06 at 19 19 34_45fa07f6](https://github.com/user-attachments/assets/f5360731-4ab6-453e-9904-30fbc920e350)

## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Manual Calculations
![WhatsApp Image 2025-11-06 at 19 11 58_c15de37a](https://github.com/user-attachments/assets/526d3308-47b1-4035-9899-75ba8ccd488d)


## OUTPUT FROM MASM SOFTWARE
![WhatsApp Image 2025-11-06 at 19 20 34_eaa3ba02](https://github.com/user-attachments/assets/34203869-e141-4fa7-8d92-ba638ede7509)




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

