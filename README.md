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
![WhatsApp Image 2025-09-22 at 12 40 29_f77c4a90](https://github.com/user-attachments/assets/d5924502-5f3e-4d2d-8914-163c7a789b69)



## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="1092" height="619" alt="Screenshot 2025-09-22 000441" src="https://github.com/user-attachments/assets/5de19720-6037-40c4-a4aa-1442e97fb696" />

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
![WhatsApp Image 2025-09-22 at 12 46 15_7645bb21](https://github.com/user-attachments/assets/692f4c40-f6bf-4bde-be8e-ab098db01562)




## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="1099" height="629" alt="Screenshot 2025-09-22 073731" src="https://github.com/user-attachments/assets/0e1c9be0-f051-4d98-a4ff-0edbbbdb6707" />

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

![WhatsApp Image 2025-09-22 at 12 56 37_4bb08ab5](https://github.com/user-attachments/assets/54c4f780-e1fa-43a5-9164-3a9bd456c7c3)



## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-09-22 at 12 57 02_b4374189](https://github.com/user-attachments/assets/58ebd63a-cf55-4f33-983c-acf9e9946fff)

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
![IMG_20250922_121353](https://github.com/user-attachments/assets/1f8328e3-8362-48f0-81dd-90b92beabf0f)

## OUTPUT FROM MASM SOFTWARE
![WhatsApp Image 2025-09-22 at 12 40 33_d8cde06b](https://github.com/user-attachments/assets/7e82f6ba-f4cb-4c0b-a704-b799c07e0f00)



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

