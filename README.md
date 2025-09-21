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
| 2000  |  79    |
| 2001  |  88    |
| 2002  |  23    |
| 2003  |  02    |

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 2004  |  9C    |
| 2005  |  8A    |
| 2006  |  00    |


#### Manual Calculations

![WhatsApp Image 2025-09-21 at 22 05 23_9e4e4ea7](https://github.com/user-attachments/assets/ebc9c1a6-5491-405e-bd25-5fc1f7d2d60f)


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="995" height="659" alt="Screenshot 2025-09-21 213712" src="https://github.com/user-attachments/assets/6f0fa8c8-642a-4596-90a2-1bf4b9cb92cc" />


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
| 2000  |  79    |
| 2001  |  88    |
| 2002  |  23    |
| 2003  |  02    |

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 2004  |  56    |
| 2005  |  86    |
| 2006  |  00    |


#### Manual Calculations

![WhatsApp Image 2025-09-21 at 22 05 24_41d75227](https://github.com/user-attachments/assets/a1ed5b42-6739-41b5-82ae-012716020457)


---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="992" height="681" alt="Screenshot 2025-09-21 213245" src="https://github.com/user-attachments/assets/84d32173-8a7d-47ee-b2c0-d09c3e9f9806" />



## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

## FLOWCHART

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
| 2000  |  02    |
| 2001  |  00    |
| 2002  |  03    |
| 2003  |  00    |

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 2004  |  06    |
| 2005  |  00    |
| 2006  |  00    |


#### Manual Calculations

![WhatsApp Image 2025-09-21 at 22 05 24_d2155456](https://github.com/user-attachments/assets/ec20f4e5-dab5-4d81-93d9-df8886489f16)


---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="996" height="673" alt="Screenshot 2025-09-21 213536" src="https://github.com/user-attachments/assets/ad304ded-c727-4a84-a5b1-2048c1fc5257" />


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
| 2000  |  69    |
| 2001  |  24    |
| 2002  |  23    |
| 2003  |  12    |

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 2004  |  02    |
| 2005  |  00    |
| 2006  |  01    |


#### Manual Calculations

![WhatsApp Image 2025-09-21 at 22 05 23_9dfce4ac](https://github.com/user-attachments/assets/760af448-709f-4a19-a6a8-7a3e1085c446)


---
## OUTPUT FROM MASM SOFTWARE
<img width="993" height="669" alt="Screenshot 2025-09-21 213829" src="https://github.com/user-attachments/assets/963299a5-ac58-4063-bdcf-9b6dd80400c5" />

## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

