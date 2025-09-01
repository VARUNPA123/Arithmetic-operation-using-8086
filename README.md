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
| 1200:12                 | 24:1204                  |
| 1201:34                 | 68:1205                  |
| 1202:12                 | 00:1206                  |
| 1203:34                 | C4:1207                  |


#### Manual Calculations

(Add your calculation here)

---

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="637" height="395" alt="mpmc_add" src="https://github.com/user-attachments/assets/4504a489-38d3-4316-924e-b61b7ef55b9c" />

<img width="637" height="402" alt="mpmc_addout" src="https://github.com/user-attachments/assets/707a6219-1aac-436a-92ea-e7067f7421ba" />



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



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |                          |

#### Manual Calculations

(Add your calculation here)

---


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="637" height="398" alt="mpmc_sub" src="https://github.com/user-attachments/assets/a4214887-90ff-4ce9-9e3a-8d736f9a947d" />

<img width="635" height="400" alt="mpmc_subout" src="https://github.com/user-attachments/assets/17a99766-836c-48fb-892b-87ab07c0bf81" />



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
|                         |                          |

#### Manual Calculations

(Add your calculation here)

---

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="640" height="398" alt="mpmc_mul" src="https://github.com/user-attachments/assets/4fe62bed-81f2-4a2b-b207-d28a9058af1e" />

<img width="632" height="397" alt="mpmc_mulout" src="https://github.com/user-attachments/assets/4c533a4c-9393-4608-be45-6ad5273fae64" />



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
|                         |                          |

#### Manual Calculations

(Add your calculation here)

---
## OUTPUT FROM MASM SOFTWARE

<img width="637" height="402" alt="mpmc_div" src="https://github.com/user-attachments/assets/471d3213-c320-4f9b-9c4a-c9cd9cf76230" />

<img width="637" height="401" alt="mpmc_divout" src="https://github.com/user-attachments/assets/83c273bb-91d0-47a8-8b7f-d1655428e32d" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
