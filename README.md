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
|           1200          |          68              |
|           1201          |         24               |
|           1202          |          00              |
|           1203          |        E8                |
|           1204          |      8C                  |

#### Manual Calculations

![WhatsApp Image 2025-09-22 at 08 41 26_a91ebec9](https://github.com/user-attachments/assets/d4e9ec02-9cd5-4454-bc96-47cd62a35b55)


---

## OUTPUT IMAGE FROM MASM SOFTWARE

![Add](https://github.com/user-attachments/assets/5717b518-84c2-4f16-bd5e-b5c736e2f060)


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
|        1200             |   00                     |
|           1201          |       00                 |
|           1202          |     18                   |
|           1203          |   12                     |
|           1204          |   8C                     |
|           1205          |        62                |

#### Manual Calculations

![WhatsApp Image 2025-09-22 at 08 42 48_0607cb7a](https://github.com/user-attachments/assets/4d48df39-b596-4078-8a58-a6629e500068)



## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="789" height="458" alt="image" src="https://github.com/user-attachments/assets/d7506902-4513-4ea8-989f-82db66867dec" />


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
|         2000            |      31                  |
|         2001            |      12                  |
|         2002            |      34                  |
|         2003            |      12                  |
|         2004            |      90                  |
|         2005            |      5A                  |
|         2006            |      4B                  |
|         2007            |      01                  |

#### Manual Calculations

![WhatsApp Image 2025-09-22 at 08 43 07_77111ba8](https://github.com/user-attachments/assets/9d9c0893-20c1-43fb-8c03-0dfc67d7d0d5)


---

## OUTPUT SCREEN FROM MASM SOFTWARE
![mul in](https://github.com/user-attachments/assets/c6cc3dad-9a87-4262-b954-afc2cbae352a)



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
|         2000            |            34            |
|         2001            |            12            |
|         2002            |            34            |
|         2003            |            12            |
|         2004            |            00            |
|         2005            |            00            |
|         2006            |            00            |
#### Manual Calculations
![WhatsApp Image 2025-09-22 at 08 41 59_1800286c](https://github.com/user-attachments/assets/c9c17f1e-5274-4a42-b0cf-f73d6c76f309)

## OUTPUT FROM MASM SOFTWARE
![WhatsApp Image 2025-09-22 at 08 34 10_0c125775](https://github.com/user-attachments/assets/0bc6f79e-081d-481d-a769-feabc51dd16c)



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

