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
|         1200 : 12       |      1204 : 24           |
|         1201 : 34	     |      1205 : 68           |
|         1202 : 12	     |       1206 : 00          |
|        1203 : 34        |       1207 : C4          |

#### Manual Calculations

![WhatsApp Image 2025-09-02 at 19 44 11_2f9ebf89](https://github.com/user-attachments/assets/fbf0397b-5744-4dce-bc79-16a5f8e49eb5)
---
## OUTPUT IMAGE FROM MASM SOFTWARE
![WhatsApp Image 2025-09-02 at 22 40 18_f9a61b78](https://github.com/user-attachments/assets/aeb36721-0552-489c-b423-9c8908c83c1a)



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
|    1200 : 12           |         1204 : 00                 |
|     1201 : 34          |       1205 : 00          |
|       1202 : 12         |        1206 : 00         |
|        1203 : 34        |        1207 : C4
#### Manual Calculations
![WhatsApp Image 2025-09-02 at 19 44 11_0c800d66](https://github.com/user-attachments/assets/e4bb18b9-2b16-4248-83e1-46a1b519f530)

---
## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-09-02 at 22 40 59_dbbe3570](https://github.com/user-attachments/assets/cea8c90a-9954-4b95-9d0f-be89e01e2fde)


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
|        1200 : 12	      |        1204 : 44        |                  
|         1201 : 34	      |      1205 : 51          |
|        1202 : 12	      |          1206 : 97       |
|         1203 : 34	      |        1207 : 0A          |

#### Manual Calculations
![WhatsApp Image 2025-09-02 at 19 44 11_5044d0fb](https://github.com/user-attachments/assets/b76d675e-6023-4381-8c85-e09ee5dfedd8)

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (6)" src="https://github.com/user-attachments/assets/b338b622-902a-4445-8fc9-a3d210cc8dcf" />


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
|        1200 : 12	      |      1204 : 01           |    
| 1201 : 34                 |	    1205 : 00            |
|   1202 : 12               |	1206 : 00                 |
| 1203 : 34                 |	1207 : 00                  

#### Manual Calculations
![WhatsApp Image 2025-09-02 at 19 44 11_a081a38d](https://github.com/user-attachments/assets/3ee68d0a-5639-4ae6-bddb-e6fac84da11a)

---
## OUTPUT FROM MASM SOFTWARE
![WhatsApp Image 2025-09-02 at 22 42 07_7083a66e](https://github.com/user-attachments/assets/e19da14c-5e6d-4d36-a2dd-d2b0deae25fd)


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
