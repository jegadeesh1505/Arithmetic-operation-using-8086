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
<img width="450" height="500" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


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
|              1200 : 12   |      	1204 : 24         |
 |1201 : 34	              |       1205 : 68          |
 | 1202 : 12	              |        1206 : 00          |
| 1203 : 34	             |        1207 : C4           |

#### Manual Calculations

![WhatsApp Image 2025-09-02 at 19 44 11_266857ec](https://github.com/user-attachments/assets/617b0030-22b5-44d9-b051-f2920791fb94)

---

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="600" height="450" alt="Screenshot (7)" src="https://github.com/user-attachments/assets/7f55c9ce-90db-4ece-97f4-5479feeb3c0b" />


## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="450" height="500" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


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
|         1200 : 12       |    	1204 : 00           |
|       1201 : 34	         |           1205 : 00      |
|    1202 : 12	            |           1206 : 00      |
|    1203 : 34	           |           1207 : C4      |

#### Manual Calculations
![WhatsApp Image 2025-09-02 at 19 44 11_77c0e8ea](https://github.com/user-attachments/assets/6ce34849-3ead-43fb-b294-ef0f4902c5d2)

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="600" height="450" alt="Screenshot (8)" src="https://github.com/user-attachments/assets/d75c9471-238c-4f2c-9f78-6d2e383949f5" />



## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="450" height="500" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



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
|          1200 : 12      |     	1204 : 44           |
 | 1201 : 34	            |         1205 : 51       |
|1202 : 12	               |         1206 : 97       |
|1203 : 34	              |        1207 : 0A       |                      |                          |

#### Manual Calculations

![WhatsApp Image 2025-09-02 at 19 44 11_86752697](https://github.com/user-attachments/assets/34bf4ff4-9c6e-4525-9be5-882b46df2462)

---

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="600" height="450" alt="Screenshot (6)" src="https://github.com/user-attachments/assets/4414eda7-0a21-42e6-90eb-031df801d987" />


## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="450" height="500" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


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
|     1200 : 12	        |        1204 : 01        |      
 |1201 : 34	             |           1205 : 00       |
| 1202 : 12                |         	1206 : 00       |
| 1203 : 34	              |         1207 : 00        | 

#### Manual Calculations

![WhatsApp Image 2025-09-02 at 19 44 11_4df94393](https://github.com/user-attachments/assets/df0877de-9e3e-4582-b1b3-72992a70c814)

---
## OUTPUT FROM MASM SOFTWARE
<img width="600" height="450" alt="Screenshot (9)" src="https://github.com/user-attachments/assets/d3e6143a-25cc-434a-b2c1-a760588d4694" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
