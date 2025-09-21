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

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 2000:34                 | 2000:55                  |
| 2001:12                 | 2005:55                  |
| 2002:21                 | 2006:00                  |
| 2003:43                 |                          |

#### Manual Calculations

![WhatsApp Image 2025-09-21 at 17 08 07_ecf50387](https://github.com/user-attachments/assets/50a67f9c-78f0-4184-8a9c-37c5db11b542)

---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="662" height="433" alt="Screenshot 2025-09-21 143403" src="https://github.com/user-attachments/assets/b3f2e067-6fa3-4685-8c5a-6ddbcabe8f58" />


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


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 2000:45                 | 2000:04                  |
| 2001:A4                 | 2005:72                  |
| 2002:41                 | 2006:00                  |
| 2003:32                 |                          |                 

#### Manual Calculations

![WhatsApp Image 2025-09-21 at 17 08 20_70c2cffc](https://github.com/user-attachments/assets/64bc85ad-d495-4765-bf32-8c8e11dac6a2)

---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="635" height="426" alt="Screenshot 2025-09-21 144020" src="https://github.com/user-attachments/assets/a9b6c1f4-8504-4b62-a46b-45f2c9f73e7c" />


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

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 2000:22                 | 2000:A8                  |
| 2001:21                 | 2005:CC                  |
| 2002:14                 | 2006:57                  |
| 2003:21                 | 2007:02                  |                 


#### Manual Calculations

![WhatsApp Image 2025-09-21 at 17 08 44_409e3528](https://github.com/user-attachments/assets/7436494d-37f5-44a1-8d05-2c52f396e1ee)

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="627" height="444" alt="Screenshot 2025-09-21 145243" src="https://github.com/user-attachments/assets/ca85eb30-b06c-4500-a468-041e1549c46c" />


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

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 2000:33                 | 2000:03                  |
| 2001:33                 | 2005:00                  |
| 2002:11                 | 2006:00                  |
| 2003:11                 | 2007:00                  |                                                                                             

#### Manual Calculations

![WhatsApp Image 2025-09-21 at 17 09 01_9d6b61d0](https://github.com/user-attachments/assets/cdfd1715-036a-44c8-9b66-ac43522dca13)

---
## OUTPUT FROM MASM SOFTWARE
<img width="645" height="430" alt="Screenshot 2025-09-21 150219" src="https://github.com/user-attachments/assets/8de04198-3de3-48f1-9c44-7554b86d1ef3" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
