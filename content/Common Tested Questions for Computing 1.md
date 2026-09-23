# Table of Contents

| Topic                                                                                                         | Subtopics                                                                                                                                                                                                                                                |
| ------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Data Representation](#toc-data-representation)                                                               | [Denary to Binary](#toc-data-representation-denary-to-binary)<br>[Denary to Hexi](#toc-data-representation-denary-to-hexi)                                                                                                                               |
| [Encoding](#toc-encoding)                                                                                     | [ASCII code](#toc-encoding-ascii-code)                                                                                                                                                                                                                   |
| [Data Validation and Verification](#toc-data-validation-and-verification)                                     | [Data Validation](#toc-data-validation-and-verification-data-validation)<br>[Program Errors](#toc-data-validation-and-verification-program-errors)                                                                                                       |
| [Ethics](#toc-ethics)                                                                                         | [Personal Data Protection Act](#toc-ethics-personal-data-protection-act)                                                                                                                                                                                 |
| [Algorithms, Pseudocode, Flowcharts & Decision Tables](#toc-algorithms-pseudocode-flowcharts-decision-tables) | [Pesudocode](#toc-algorithms-pseudocode-flowcharts-decision-tables-pesudocode)                                                                                                                                                                           |
| [Recursion](#toc-recursion)                                                                                   | [Definition](#toc-recursion-definition)                                                                                                                                                                                                                  |
| [Object-Oriented Programming](#toc-object-oriented-programming)                                               | [Class Diagram](#toc-object-oriented-programming-class-diagram)<br>[4 Pillars of OOP](#toc-object-oriented-programming-4-pillars-of-oop)                                                                                                                 |
| [Searching Algorithms](#toc-searching-algorithms)                                                             | [Binary Search](#toc-searching-algorithms-binary-search)<br>[HashTable Search](#toc-searching-algorithms-hashtable-search)                                                                                                                               |
| [Sorting Algorithms](#toc-sorting-algorithms)                                                                 | [Insertion](#toc-sorting-algorithms-insertion)<br>[Merge Sort](#toc-sorting-algorithms-merge-sort)                                                                                                                                                       |
| [Stacks](#toc-stacks)                                                                                         | [Core Operations](#toc-stacks-core-operations)                                                                                                                                                                                                           |
| [Queues](#toc-queues)                                                                                         | [Circular Queue](#toc-queues-circular-queue)                                                                                                                                                                                                             |
| [Linked Lists](#toc-linked-lists)                                                                             | [Definition](#toc-linked-lists-definition)<br>[Ordered Insertion](#toc-linked-lists-ordered-insertion)                                                                                                                                                   |
| [Trees](#toc-trees)                                                                                           | [Binary Search Tree (BST) Creation](#toc-trees-binary-search-tree-bst-creation)<br>[Binary Search Tree (BST) Search](#toc-trees-binary-search-tree-bst-search)                                                                                           |
| [Data Management](#toc-data-management)                                                                       | [Backup](#toc-data-management-backup)                                                                                                                                                                                                                    |
| [Relational Databases](#toc-relational-databases)                                                             | [SQL Queries](#toc-relational-databases-sql-queries)<br>[ER (Entity Relationship) Diagram](#toc-relational-databases-er-entity-relationship-diagram)<br>[Database Normalisation](#toc-relational-databases-database-normalisation)                       |
| [Non-relational Databases](#toc-non-relational-databases)                                                     | [Syntax](#toc-non-relational-databases-syntax)                                                                                                                                                                                                           |
| [Computer Networks](#toc-computer-networks)                                                                   | [LAN (Local Area Network)](#toc-computer-networks-lan-local-area-network)<br>[Internet](#toc-computer-networks-internet)<br>[Packets](#toc-computer-networks-packets)<br>[TCP/IP Model](#toc-computer-networks-tcp-ip-model)                             |
| [Network Security](#toc-network-security)                                                                     | [Malware Attacks](#toc-network-security-malware-attacks)<br>[Secure access method](#toc-network-security-secure-access-method)<br>[Digital signature](#toc-network-security-digital-signature)<br>[Authentication](#toc-network-security-authentication) |

---

<a id="toc-data-representation"></a>

# Data Representation

<a id="toc-data-representation-denary-to-binary"></a>

### Denary to Binary

##### 2025 RI Prelim P1 Q5)

**5 A microcontroller stores sensor data in binary and transmits the values to a monitoring system, which displays the readings in hexadecimal.**

**The system receives the decimal reading 178, which must be stored and displayed in both binary and hexadecimal.**

(a) Showing your working clearly, convert the decimal number 178 to:

(i) binary, [2]

> [!Answer]
>
> * 178 ÷ 2 = 89, remainder 0
>
> * 89 ÷ 2 = 44, remainder 1
>
> * 44 ÷ 2 = 22, remainder 0
>
> * 22 ÷ 2 = 11, remainder 0
>
> * 11 ÷ 2 = 5, remainder 1
>
> * 5 ÷ 2 = 2, remainder 1
>
> * 2 ÷ 2 = 1, remainder 0
>
> * 1 ÷ 2 = 0, remainder 1
>
> **Binary** (read from bottom to top): 10110010
> 10110010

(ii) hexadecimal. [2]

> [!Answer]
> **Hexadecimal**
>
> * 178 ÷ 16 = 11 remainder 2
>
> * 11 in **hexadecimal** is B
>
> B2

**The following function is used to convert a non-negative decimal number into its binary equivalent.**

**The algorithm uses a loop to divide the number by 2 repeatedly and builds the binary string.**

```text
1 FUNCTION ConvertToBinary(number: INTEGER) RETURNS STRING
2   DECLARE result ← ""
3   WHILE number > 0 DO
4    remainder ← number MOD 2
5    result ← <insert code here>
6      number ← number DIV 2
7   ENDWHILE
8   RETURN result
9 ENDFUNCTION

```

**(b) What code should <insert_code_here> be so that the binary digits are in the correct order? [1]**

> [!Answer]
>
> ```text
> result ← STR(remainder) + result
>
> ```
>
> Prepending ensures most significant digit is on the left.

**(c) Rewrite the ConvertToBinary function as a recursive version that returns the binary string. [4]**

> [!Answer]
>
> ```text
> FUNCTION ConvertToBinary(number: INTEGER) RETURNS STRING
>     IF number = 0 THEN
>         RETURN ""
>     ELSE
>         RETURN ConvertToBinary(number DIV 2) + STR(number MOD 2)
>     ENDIF
> ENDFUNCTION
>
> ```
>
> * correct **base case**
>
> * correct **recursive call**
>
> * converting remainder to string
>
> * returning the concatenated result in correct order

---

<a id="toc-data-representation-denary-to-hexi"></a>

### Denary to Hexi

##### 2025 NYJC Prelim P1 Q1)

**1 A programmer is writing a program to manage and search for records. The records include phone numbers, which comprise 8 decimal digits.**

(a) Convert the phone number 62842281 to:

(i) Hexadecimal representation [2]

> [!Answer]
> $62842281 = 3 \times 16^{6} + 11 \times 16^{5} + 14 \times 16^{4} + 14 \times 16^{3} + 5 \times 16^{2} + 10 \times 16^{1} + 9 \times 16^{0}$
>
> * 3BEE5A9

**(ii) ASCII values. ('0' has an ASCII value of 48 and '9' has an ASCII value of 57.) [2]**

> [!Answer]
> Map each **ASCII** decimal character to **ASCII** value
>
> * 54, 50, 56, 52, 50, 50, 56, 49

(b) Determine the minimum number of bits required to store the phone number 62842281 as:

(i) an integer [2]

> [!Answer]
> $\log_2(62842281) = 25.9\ldots$
>
> * 26 **bits** (alternatively, 7 hex digits x 4 **bits** per hex digit = 28 **bits**)

(ii) a string. [2]

> [!Answer]
> Each **ASCII** character is 7 **bits**
>
> * 56 **bits**

**(c) The programmer decides to store phone numbers in an array as integers instead of strings for binary search. Suggest two reasons for this. [2]**

> [!Answer]
> Integers are quicker to compare; comparing an 8-char string requires up to 8 comparisons
>
> * Takes up less space in memory

**(d) The programmer’s supervisor suggests a binary search tree instead of a sorted array for managing phone numbers instead. Suggest two reasons for the supervisor’s advice. [3]**

> [!Answer]
> BST has lower **time complexity** for adding items
>
> * BST maintains items in sorted order, whereas array may require re-sorting
>
> * Appropriate mentions and comparisons of **time complexity** for above algorithms

**A function Search(data, target, start, end) takes in data an array of phone numbers, target a phone number to be searched, and two integers start and end representing the start and end indexes respectively. Search implements a recursive binary search and return s the index of the matching phone number, or -1 if the phone number is not found. Contacts is an array that has the following phone numbers: [61625074, 90923657, 93197564, 93289273, 99108357, 99283918, 99561273]**

**(e) Complete the following table, expanding it as necessary to show each successive recursive call. [3]**

Function call Return value
Search(Contacts, 62842281, 0, 6)

> [!Answer]
> Search(Contacts, 62842281, 0, 2)
>
> * Search(Contacts, 62842281, 0, 0)
>
> Depending on implementation, may also include an additional call to reach **base case** (not penalised if incorrect/missing):
> Search(Contacts, 62842281, 1, 0)
>
> * **base case** returns -1

(f) Write the function Search using pseudocode. [5]

> [!Answer]
> function correctly declared, returns an integer
>
> * function handles a base case (start > end or other appropriate condition)
>
> * function compares target with the middle item
>
> * function updates the search range using a recursive call with a larger value for start or smaller value for end
>
> * function correctly returns -1 or an index

**(g) Besides 62842281, suggest 3 other suitable test values for target for the above array. [3]**

> [!Answer]
> Extreme case: 0, 99999999, etc
>
> * Abnormal case: 628422B1, etc
>
> * Normal case (found in array): 61625074, etc

---

##### 2025 VJC Prelim P1 Q1)

**A programmer is writing a program to manage and search for records. The records include phone numbers, which comprise 8 decimal digits.**

**Convert the phone number 62842281 to: Hexadecimal representation [2]**

> [!Answer]
>
> * $62842281 = 3 \times 16^{6} + 11 \times 16^{5} + 14 \times 16^{4} + 14 \times 16^{3} + 5 \times 16^{2} + 10 \times 16^{1} + 9 \times 16^{0}$
>
> * Or repeated division by 16 3BEE5A9

**ASCII value for each digit.**

('0' has an ASCII value of 48 and '9' has an ASCII value of 57.)[2]

> [!Answer]
> Map each **ASCII** decimal character to **ASCII** value 54, 50, 56, 52, 50, 50, 56, 49

**The programmer’s supervisor suggests a binary search tree instead of a sorted array for managing phone numbers.**

Suggest two reasons for the supervisor’s advice.[2]

> [!Answer]
>
> * BST has lower **time complexity** for adding items
>
> * BST maintains items in sorted order, whereas array may require re-sorting

**A recursive function countPaths is designed to find the number of different possible paths from the top-left corner to the bottom-right corner of a grid. The function can only move right or down at each step. For example, in a $2 \times 2$ grid, where row = 2 and col = 2, there are two possible paths from the top-left corner to the bottom-right corner of the grid: Right → Down Down → Right The function is defined as follows:**

```text
01 FUNCTION countPaths(row : INTEGER, col : INTEGER) RETURNS INTEGER
02   IF row = 1 OR col = 1 THEN
03     RETURN 1
04   ENDIF
05   RETURN countPaths(row - 1, col) + countPaths(row, col - 1)
06 ENDFUNCTION

```

**An example of a trace tree diagram showing countPaths(2,2) is shown as follows: countPaths(2,2)countPaths(2,2)countPaths(1,2)countPaths(1,2)countPaths(2,1)countPaths(2,1)Return 1Return 1Return 1Return 1Return 1+1=2Return 1+1=2**

Use the above example to create a trace tree diagram for the recursive function call countPaths(3,2).[4]

> [!Answer]
>
> * Correct root node showing countPaths(3,2)
>
> * Correct first level of recursive calls
>
> * Correct first level of return values
>
> * Correct final return calculation and value (2+1=3)
>
> * Note: Second level of recursive calls given in examplecountPaths(3,2)countPaths(3,2)countPaths(2,2)countPaths(2,2)countPaths(3,1)countPaths(3,1)Return 1+1=2Return 1+1=2Return 1Return 1Return 2+1=3Return 2+1=3Return 1Return 1countPaths(2,1)countPaths(2,1)Return 1Return 1countPaths(1,2)countPaths(1,2)

Explain how the base case in lines 02 to 03 prevents infinite recursion.[2]

> [!Answer]
>
> * Explanation that **base case** is reached when either dimension becomes 1
>
> * Explanation that this ensures termination by returning a value
>
> * When the function is called, it checks if either row or col is equal to 1. If this condition is met, the function returns 1, indicating that there is exactly one way to reach the destination when either dimension is reduced to 1. This means that the function will no longer call itself recursively, effectively terminating the **recursion** when it reaches this **base case**, thus preventing the function from running indefinitely

Write an iterative version of the original countPaths function.[5]

> [!Answer]
>
> ```text
> Correct array/table initialization [1]Proper handling of edge cases [1]Correct nested loop structure [1]Correct cell value calculation [1]Return correct final value [1]
> FUNCTION countPathsIterative(row : INTEGER, col : INTEGER) RETURNS INTEGER
> DECLARE grid : ARRAY[1:row, 1:col] OF INTEGER    // Initialize the first row and first column
> FOR i ← 1 TO row DO        grid[i,1] ← 1
> NEXT i
> FOR j ← 1 TO col DO        grid[1,j] ← 1
> NEXT j    // Fill the rest of the paths matrix
> FOR i ← 2 TO row DO
> FOR j ← 2 TO col DO            grid[i,j] ← grid[i – 1,j] + grid[i,j – 1]
> NEXT j
> NEXT i
> RETURN grid[row,col]
> ENDFUNCTION
>
> ```

---

##### 2025 YIJC Prelim P1 Q1)

**The smart irrigation system decides whether to water based on soil moisture, rain forecast, and time of day. The rules are as follows: Watering is skipped if the soil is wet or rain is expected. If the soil is dry and rain is not expected, the system will water: for 30 minutes if it is currently morning, or for 15 minutes if it is currently evening.**

Create a decision table to show these conditions and actions.[4]

> [!Answer]
>
> | Soil Dry / Wet | Rain Expected | Evening / Morning | No Watering | 15 mins Watering | 30 mins Watering |
> | -------------- | ------------- | ----------------- | ----------- | ---------------- | ---------------- |
> | Dry            | Yes           | Evening           | √           |                  |                  |
> | Dry            | Yes           | Morning           | √           |                  |                  |
> | Dry            | No            | Evening           |             | √                |                  |
> | Dry            | No            | Morning           |             |                  | √                |
> | Wet            | Yes           | Evening           | √           |                  |                  |
> | Wet            | Yes           | Morning           | √           |                  |                  |
> | Wet            | No            | Evening           | √           |                  |                  |
> | Wet            | No            | Morning           | √           |                  |                  |

Remove the redundancies from the decision table. [2]

> [!Answer]
>
> | Soil Dry / Wet | Rain Expected | Evening / Morning | No Watering | 15 mins Watering | 30 mins Watering |
> | -------------- | ------------- | ----------------- | ----------- | ---------------- | ---------------- |
> | Dry            | Yes           | -                 | √           |                  |                  |
> | Dry            | No            | Evening           |             | √                |                  |
> | Dry            | No            | Morning           |             |                  | √                |
> | Wet            | -             | -                 | √           |                  |                  |

**The system records the sensor inputs and the watering actions using a 5-bit binary number, defined as follows:**

| Bit   | Meaning                                                          |
| ----- | ---------------------------------------------------------------- |
| 1     | Soil Moisture (1 = Dry, 0 = Wet)                                 |
| 2     | Rain Forecast (1 = Rain Expected, 0 = Rain Not Expected)         |
| 3     | Time of Day (1 = Evening, 0 = Morning)                           |
| 4 – 5 | Watering Duration:00 = No Watering01 = 15 minutes10 = 30 minutes |

**On a particular day, the soil was dry in the evening, and there was no rain expected.**

Write the 5-bit binary number recorded by the system.[1]

> [!Answer]
> $10101_2$

Convert the 5-bit binary number in (i) to a hexadecimal number. Show your working clearly.[2]

> [!Answer]
> $10101_2 = 0001,0101_2 = 0x15 = 15_{16}$

Explain one benefit of using a multi-bit binary number to represent the watering durations.[1]

> [!Answer]
>
> * Multi-bit **Binary** Encoding
>
> * Advantage :Supports multiple distinct output values / Allows the system to represent more than just “on” or “off” (e.g. 00 = No watering, 01 = 15 mins, 10 = 30 mins).

---

<a id="toc-encoding"></a>

# Encoding

<a id="toc-encoding-ascii-code"></a>

### ASCII code

##### 2025 DHS Prelim P1 Q6)

**6 A computer uses the ASCII character set.**

**(a) State with reason the number of characters that can be represented by the ASCII character set. [2]**

> [!Answer]
> State the number of characters that can be represented by the **ASCII** character set.
> number of characters = 2
> 7 = 128

**(b) Unicode is a different character set.**

**The Unicode value for the character ‘1’ is denary value 49.**

(i) Write the hexadecimal value for the Unicode character ‘1’. Show your working. [1]

> [!Answer]
> 16    | 49    49 divided by 16
>
> * Quotient    3      Remainder 1
>
> * 4910 = 3116

(ii) Write the denary value for the Unicode character ‘5’. Show your working. [1]

> [!Answer]
> Denary value of character ‘1’  = 49
> Table 1 Comparing Nlog2N and N2   (2)
> N  Nlog2N N2
>
> * 512 4,608  262,144
>
> * 1,024 10,240  1,048,576
>
> * 2,048 22,458  4,194,304
>
> * 8,192 106,496  67,108,864
>
> 16,384 229,376  268,435,456
> 32,768 491,520  1,073,741,824
>
> * Denary value of character ‘5’  = 49 + 4 = 53       [Or 49 + (5-1) ]

---

<a id="toc-data-validation-and-verification"></a>

# Data Validation and Verification

<a id="toc-data-validation-and-verification-data-validation"></a>

### Data Validation

##### 2025 ASRJC Prelim P1 Q2)

2 (a) State what is meant by data integrity. [1]

> [!Answer]
> **Data integrity** refers to the accuracy, consistency and reliability of data throughout its entire lifecycle (creation, storage, transmission).

**Sonars Service Centre handles repairs of their proprietary Sonars audio products. When customers bring equipment for repair, technicians would need to enter the product serial number into the system. Each serial number consists of 10 digits, where the last digit is a check digit calculated using this algorithm:In the first pass, multiply each of the first 9 digits of the serial number by weights: 9, 8, 7, 6, 5, 4, 3, 2, 1 respectively (e.g. position 1 gets weight 9). Sum these products to obtain subtotal. In the second pass, using the same 9 digits of the serial number, multiply each digit by the sum of its own value and its position number (e.g. if the first digit is 5, we get a product of 5 x (5 + 1) = 30 for that digit). Sum these products to obtain another subtotal. Add the two subtotals from the two passes to obtain a combined total. Divide the combined total by 13 to obtain the remainder. Subtract the remainder from 13 to derive the check digit.**

(b) (i) It is given that 284736197X is a valid serial number, where X represents the check digit. Calculate the value of X, showing your workings. [3]

> [!Answer]
> For the first pass, subtotal = 2x9 + 8x8 + 4x7 + 7x6 + 3x5 + 6x4 + 1x3 + 9x2 + 7x1 = 219
> For the second pass, subtotal = 2x(2+1) + 8x(8+2) + 4x(4+3) + 7x(7+4) + 3x(3+5) + 6x(6+6) + 1x(1+7) + 9x(9+8) + 7x(7+9) = 560
> Combined total = 219 + 560 = 779
>
> ```text
> Remainder = 779 MOD 13 = 12
>
> ```
>
> Check digit, X = 13 – 12 = 1

(ii) Briefly explain why check digit alone is insufficient to ensure data integrity. [1]

> [!Answer]
> Check digit cannot catch all possible data entry errors, such as multiple errors that might cancel each other out. While it verifies mathematical correctness based on the algorithm, it cannot detect whether the serial number exists for an actual product.

(iii) Describe two data verification methods that can be used when manually entering serial numbers into the system. [2]

> [!Answer]
> Double entry: requiring user to enter the same serial number twice in separate input fields. The system compares both entries to ensure they are identical before accepting the data.
> Visual confirmation: displaying a message box showing the entered number and prompting the user to confirm that it matches the serial number on the physical device.

**When a Sonars amplifier system arrives for diagnosis, the technician checks for these symptoms:whether the power LED is OFFwhether the audio output is abnormalwhether the amplifier is overheatingThe following describes the actions the technician would take:If the power LED is off, check the power supply and fuse only regardless of other symptoms. If the power LED is on and the audio output is abnormal (but the amplifier is not overheating), test the input connections. If the amplifier is overheating, clean the ventilation system and fans. If the audio is abnormal and the amplifier is overheating, also check the output transistors, as they may be faulty. If none of the 3 symptoms are present, perform exterior cleaning. It is desired to draw a decision table for the above information.**

(c) (i) Explain what a decision table is. [2]

> [!Answer]
> A decision table is a tabular method to document decision-making logic. It systematically shows all possible combinations of conditions, with each of the corresponding actions to take.

(ii) Create a complete decision table based on the description above. [4]

> [!Answer]
> Decision table with 8 rules:
>
> |                             | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
> | --------------------------- | - | - | - | - | - | - | - | - |
> | **Conditions**              |   |   |   |   |   |   |   |   |
> | Power LED is OFF            | Y | Y | Y | Y | N | N | N | N |
> | Audio output is abnormal    | Y | Y | N | N | Y | Y | N | N |
> | Amplifier is overheating    | Y | N | Y | N | Y | N | Y | N |
> | **Actions**                 |   |   |   |   |   |   |   |   |
> | Check power supply and fuse | X | X | X | X |   |   |   |   |
> | Test input connections      |   |   |   |   |   | X |   |   |
> | Clean ventilation and fans  |   |   |   |   | X |   | X |   |
> | Check output transistors    |   |   |   |   | X |   |   |   |
> | Perform exterior cleaning   |   |   |   |   |   |   |   | X |

(iii) Show a simplified decision table without redundancies. [2]

> [!Answer]
> Simplified decision table:
>
> |                             | 1 | 2 | 3 | 4 | 5 |
> | --------------------------- | - | - | - | - | - |
> | **Conditions**              |   |   |   |   |   |
> | Power LED is OFF            | Y | N | N | N | N |
> | Audio output is abnormal    | - | Y | Y | N | N |
> | Amplifier is overheating    | - | Y | N | Y | N |
> | **Actions**                 |   |   |   |   |   |
> | Check power supply and fuse | X |   |   |   |   |
> | Test input connections      |   |   | X |   |   |
> | Clean ventilation and fans  |   | X |   | X |   |
> | Check output transistors    |   | X |   |   |   |
> | Perform exterior cleaning   |   |   |   |   | X |

---

##### 2025 NYJC Prelim P1 Q2)

**2 Validation and verification are used in data entry.**

(a) (i) State the purpose of validation. [1]

> [!Answer]
> 2.0	Flowchart, application design
>
> ensure that input data meets a set of requirements

(ii) State the purpose of verification. [1]

> [!Answer]
> ensure that data entered is what the user intended to enter

**The image below shows the password change dialog box for a web application.**

**The flowchart below shows the process for changing a user’s password.**

(b) Redraw the flowchart to include, for the new password:

* one suitable validation technique

* one suitable verification technique. [6]

Display prompt
Current password
correct?
New password
different?
Password changed
Yes
Yes
No
No
Input current password
and new password

Display error
message
Display error
message

> [!Answer]
> appropriate symbol for validation, verification: decision diamond
>
> * appropriate validation check: format / length
>
> * appropriate verification technique: double entry
>
> * verify that both entries for new password match
>
> * appropriate symbol for input: parallelogram
>
> * user is asked to input new password again
>
> * Yes" -> next step, "No" -> error message
>
> * password is changed only if all conditions are met
>
> ```mermaid
> flowchart TD
>   A[Display prompt] --> B[/Input current password and new password/]
>   B --> C{Is current password correct?}
>   C -- "No" --> D[Display error message]
>   D --> A
>   C -- "Yes" --> E{New password meets format / length?}
>   E -- "No" --> D
>   E -- "Yes" --> F{Is new password different?}
>   F -- "No" --> D
>   F -- "Yes" --> G[/Input new password again/]
>   G --> H{Both entries for new password match?}
>   H -- "No" --> D
>   H -- "Yes" --> I[Password changed]
>
> ```

**(c) State two ways the password change interface can be improved using suitable application design principles. [2]**

> [!Answer]
> Help users recognise, diagnose, and recover from errors: the reason for invalid password should be displayed below the appropriate textbox / add "Forget password" functionality
> Error Prevention: disable the Save button (grayed out) until new password passes all checks
> Visibility of System Status: show message / animation while password is being changed
> Match between system and the real world: Use "Show / Hide" labels instead of eye icon

---

##### 2025 RVHS Prelim P1 Q6)

**6. A company provides an online registration form for customers. The form is shown below.**

**------------------------------------------------------**

| ABC Services - New Customer Registration                   |
| ---------------------------------------------------------- |
| Full Name:             [________________________]          |
| Date of Birth (DD/MM/YYYY):          [__________]          |
| Email Address:         [________________________]          |
| Confirm Email Address: [________________________]          |
| Contact Number:        [________________________]          |
|                                                            |
| [ Submit ]                                                 |
| **------------------------------------------------------** |

a) Define data validation and data verification in the context of data entry. [2]

> [!Answer]
> **Data validation**: an automated process that checks if the data entered is
> reasonable, sensible, and in the correct format (e.g., ensuring a date field
> contains a valid date).
> **Data verification**: a process to confirm that the data entered is accurate
> and matches the user’s intention (e.g., asking a user to enter the same data
> twice to reduce typing errors).
> 2

**b) Suggest one validation check that could be applied to the field Date of Birth. [1]**

> [!Answer]
> Check that the date entered is a valid calendar date and not a future date. 1

**The form asks the user to enter the email address twice (“Email Address” and “Confirm Email Address”).**

c) Explain the purpose of asking the user to enter the email twice. [2]

> [!Answer]
> To ensure that the user typed the email address correctly and did not make a
> typographical error.
>
> Its another purpose is to verify that the user’s intended email address
> 2

**A customer attempts to enter their Full Name using non-English characters and the system rejects it as it only supports ASCII characters.**

**d) Suggest what the company should do to allow names from different languages to be accepted. [1]**

> [!Answer]
> Use **Unicode** (e.g., UTF-8) encoding instead of **ASCII** so the system suppor
> ts characters from multiple languages.
> 1

**Under the Personal Data Protection Act (PDPA), the company has legal obligations when collecting customer personal data through this form.**

**e) State two responsibilities the company must fulfil to comply with PDPA. [2]**

> [!Answer]
> Obtain the user’s consent and state the purpose of collecting their personal
> data.
> Implement reasonable security measures  to protect **personal data** from
> unauthorized access or disclosure.
> 2

---

##### 2025 VJC Prelim P1 Q3)

**Most applications require data entry as an essential step for processing and output. During data entry, validation and verification are commonly applied.**

State the purpose of validation.[1]

> [!Answer]
> ensure that input data meets a set of requirements*Reject “check”

State the purpose of verification.[1]

> [!Answer]
> ensure that data entered is what the user intended to enter*Reject “check”

**The image below shows the password change dialog box for a web application. The flowchart below shows the process for changing a user’s password. Display promptIs current password correct? Is new password different? Password changedInput current password and new passwordDisplay error messageDisplay error messageDisplay promptIs current password correct? Is new password different? Password changedInput current password and new passwordDisplay error messageDisplay error message**
**Yes**
**Yes**
**No**
**No**

**Redraw the flowchart to include, for the new password: one suitable validation technique one suitable verification technique [6]**

> [!Answer]
>
> * appropriate symbol for validation, verification: decision diamond [1]appropriate validation check: format
>
> * OR appropriate validation check: length appropriate verification technique: double entry [1]"Yes" -> next step, [1]"No" -> error message [1]validation check is carried out before verification check
>
> ```mermaid
> flowchart TD
>   A[Display prompt] --> B[/Input current password and new password/]
>   B --> C{Is current password correct?}
>   C -- "No" --> D[Display error message]
>   D --> A
>   C -- "Yes" --> E{New password meets format / length?}
>   E -- "No" --> D
>   E -- "Yes" --> F{Is new password different?}
>   F -- "No" --> D
>   F -- "Yes" --> G[/Input new password again/]
>   G --> H{Both entries for new password match?}
>   H -- "No" --> D
>   H -- "Yes" --> I[Password changed]
>
> ```

State two ways the password change interface can be improved using suitable usability principles.[2]

> [!Answer]
>
> * Help users recognise, diagnose, and recover from errors: the reason for invalid password should be displayed below the appropriate textbox
>
> * Error Prevention: disable the Save button (grayed out) until new password passes all checks
>
> * consistency and standards and visibility of system status etc

---

<a id="toc-data-validation-and-verification-program-errors"></a>

### Program Errors

##### 2025 DHS Prelim P1 Q4)

**4 Name and explain three different types of errors that could occur in a computer program. Given an example of each type of error with Python programming language. [3]**

> [!Answer]
> **Syntax**
>
> An error that occurs when a command does not follow the expected syntax of the language
>
> ```python
> >>> prin("Hello")
> Traceback (most recent call last):
>   File "<pyshell#0>", line 1, in <module>
>     prin("Hello")
> NameError: name 'prin' is not defined
>
> >>> a = 10
> >>> if a == 10
> SyntaxError: invalid syntax
>
> >>> print ('DHS)
> SyntaxError: EOL while scanning string literal
>
> ```
>
> **Runtime or Execution**
>
> An error that only occurs when the program is running and is difficult to foresee before a program is compiled and run
>
> ```python
> >>> age/0
> Traceback (most recent call last):
>   File "<pyshell#6>", line 1, in <module>
>     age/0
> ZeroDivisionError: division by zero
>
> ```
>
> **Logical**
>
> An error that causes a program to output an incorrect answer. A logic error occurs when the programmer makes a mistake in their logic for some part of the program.
>
> ```text
> count = count – 1 should be count = count + 1
>
> ```
>
> * call the wrong sub-routine
>
> * looping too many times

---

<a id="toc-ethics"></a>

# Ethics

<a id="toc-ethics-personal-data-protection-act"></a>

### Personal Data Protection Act

##### 2025 YIJC Prelim P1 Q8)

**An education technology company, UpLiftAI, has developed an analytics platform that uses artificial intelligence (AI) to identify students at risk of academic underperformance. Teachers input recent academic grades, and the system flags students for potential intervention. However, several teachers have reported that the system's predictions appear biased. It disproportionately flags students from certain demographic backgrounds. When questioned, UpLiftAI could not clarify the model's decision-making process, citing its proprietary "black box" nature. It was later revealed that in an attempt to improve the model's accuracy and reduce false flags, the development team incorporated a historical dataset from a prior partnership with schools. This dataset includes sensitive information such as students' full names, dates of birth, detailed academic histories, and behavioural records, like attendance and disciplinary notes.**

Explain two distinct ethical concerns arising from the developers' decision to incorporate the historical dataset. For each concern, describe its potential impact on the students. [4]

> [!Answer]
>
> * **Amplification of Bias/Discrimination:** The historical data (e.g., behavioural records, academic history) likely contains human and societal biases. Using it to train the model risks encoding and amplifying these existing prejudices, making the model's biased predictions worse.
>
> * **Impact:** Students from certain backgrounds are flagged more frequently, leading to stigmatisation, lowered teacher expectations, or being unfairly channelled into lower-achievement tracks. This creates a harmful feedback loop where the prediction becomes a self-fulfilling prophecy.
>
> * **Violation of Privacy & Lack of Informed Consent:** The data was collected for a previous purpose and is now being repurposed without obtaining new, specific consent from students/parents for this specific AI profiling use case.
>
> * **Impact:** Students and families lose autonomy and control over their sensitive information. This erodes trust in the school and technology. A data breach of this highly personal dataset could lead to severe embarrassment, bullying, or other harms for the students.
>
> * **Lack of Transparency & Explainability (The "Black Box"):** The solution dodges the core problem that the model's reasoning is unexplained. Adding more complex data makes the model even more opaque.
>
> * **Impact:** Teachers and students cannot understand why a flag was generated, making it impossible to challenge erroneous decisions or to provide meaningful, targeted help. The student is left with a label but no clear path for improvement.
>
> * **Data Minimisation and Purpose Limitation:** The developers are using data (e.g., full names, behavioural history) that is excessive and not strictly necessary for the stated goal of predicting academic performance.
>
> * **Impact:** Increases the risk and severity of a potential data breach. Also, decisions may be made based on irrelevant or unfairly prejudicial factors (e.g., a past detention) rather than purely academic ones.

**An investigation further revealed that the company had not obtained consent from the school, students, or parents to use the additional data. The company was also hosting its services on an unsecured overseas cloud storage platform. UpLiftAI's actions may have breached the Personal Data Protection Act (PDPA) in several ways.**

Explain why using student data from a previous project, without obtaining consent, may be a breach of PDPA.[2]

> [!Answer]
>
> * **Consent Obligation.** Organisations must obtain consent before collecting, using, or disclosing **personal data**. Using the data for a new, unrelated purpose (AI training) without seeking fresh consent is a direct violation.
>
> * **Purpose Limitation Obligation.** **Personal data** may only be collected, used, or disclosed for purposes that a reasonable person would consider appropriate in the circumstances and, crucially, only for the purpose(s) for which consent was originally given. Repurposing the data for AI analytics exceeds the original purpose for which consent was obtained.

Identify two other obligations under the PDPA that may have been violated. For each, briefly explain how the company failed to meet it.[2]

> [!Answer]
>
> * Identify two other obligations under the **PDPA** that may have been violated. For each, briefly explain how the company failed to meet it.
>
> * 1. **Protection Obligation:** An organisation must protect **personal data** in its possession or under its control by making reasonable security arrangements to prevent unauthorised access, collection, use, or disclosure.
>
> * **Explanation of Failure:** The company failed this obligation by hosting highly sensitive student data on an unsecured cloud platform. The lack of adequate security measures (e.g., **encryption**, access controls) exposed the data to potential breaches and unauthorized access.
>
> * 2. **Transfer Limitation Obligation:** An organisation must not transfer **personal data** to a country or territory outside Singapore except in accordance with the requirements prescribed under the **PDPA** to ensure that the standard of protection is comparable to the Act's provisions.
>
> * **Explanation of Failure:** The company failed this obligation by using an overseas cloud storage platform without ensuring that the data was subject to comparable legal safeguards or without implementing appropriate contractual agreements (e.g., data transfer agreements) to guarantee that protection standard.
>
> * 3. **Accountability Obligation:** An organisation is responsible for complying with the **PDPA** and must demonstrate accountability by implementing policies and practices to meet its legal obligations.
>
> * **Explanation of Failure:** The company's overall actions—repurposing data without consent and using unsecured overseas storage—demonstrate a fundamental lack of policies and practices to ensure compliance with the **PDPA**, thus failing its accountability duty.

Suggest two possible steps the company should have taken to use the additional data compliantly.[2]

> [!Answer]
>
> * Suggest two possible steps the company should have taken to use the additional data compliantly.
>
> * **Seek New Consent:** The company should have obtained fresh, specific, and informed consent from the students and their parents (or legal guardians) for the new, specific purpose of training and operating the AI model. This would have fulfilled the Consent Obligation for the new use case.
>
> * **Anonymise the Data:** The company should have taken steps to properly anonymise the dataset before using it for model training. This means irreversibly stripping all identifying elements so that the data can no longer be linked to any individual. Properly anonymised data falls outside the scope of the **PDPA**.
>
> * **Conduct a Legitimacy and Risk Assessment:** The company should have conducted a formal assessment to determine if using the data for this new purpose was permissible under the **PDPA**. This would involve checking if the original consent covered this use, evaluating the necessity and proportionality of the data used, and identifying and mitigating risks (like bias and security) before proceeding.
>
> * **Execute a Data Transfer Agreement:** If using overseas storage was necessary, the company should have first ensured the transfer complied with the Transfer Limitation Obligation by implementing appropriate safeguards, such as binding corporate rules or contractual clauses with the cloud provider, to ensure a comparable standard of protection.

---

<a id="toc-algorithms-pseudocode-flowcharts-decision-tables"></a>

# Algorithms, Pseudocode, Flowcharts & Decision Tables

<a id="toc-algorithms-pseudocode-flowcharts-decision-tables-pesudocode"></a>

### Pesudocode

##### 2025 ACJC Prelim P1 Q3)

**3The greatest common divisor (gcd) of two positive integers m and n is the largest integer that divides both m and n with a remainder of 0. The pseudo-code below shows an attempt to write an algorithm to find the gcd of m and n.**

```text
00 INPUT m, n
01
02 DECLARE d : INTEGER
03 d ← 0
04
05 FOR i ← 1 TO m:
06     IF m MOD i = 0 OR n MOD i = 0 THEN
07         d ← i
08     ENDIF
09 ENDFOR
10
11 OUTPUT d

```

(a) State the output when the input values m = 21, n = 28 are given to the algorithm. [1]

> [!Answer]
> 21

(b) Identify the line where there is a logic error and give the correct pseudo-code to find the gcd. [2]

> [!Answer]
> 06: IF m MOD i = 0 AND n MOD i = 0

**Euclid’s Algorithm is a method to determine the greatest common divisor of two positive integers m and n. The pseudo-code for a recursive implementation of Euclid’s Algorithm is given below.**

```text
00 FUNCTION gcd(m,n : INTEGERS) RETURNS INTEGER
01
02    IF m = n THEN
03        RETURN m
04    ELSE
05        IF m > n THEN
06            RETURN gcd(m-n, n)
07        ELSE
08            RETURN gcd(m, n-m)
09        ENDIF
10    ENDIF
11
12 ENDFUNCTION

```

(c) State the features of the function gcd that make it recursive. [3]

> [!Answer]
> The function has a **base case** (line 02) and for other cases, it calls itself with smaller values (lines 06 and 08). The function would thus keep calling itself until the **base case** is reached.

(d) Draw a trace diagram for the input values m = 21, n = 28. [3]

> [!Answer]
>
> ```text
> 3(d)
>
> ```

(e) Explain what will happen to the recursion and execution of the recursive function gcd when m is positive and n is negative. [2]

> [!Answer]
> Since m > n, when the function calls itself, m will be replaced by m – n, which is larger than m and is still positive. As a result m will keep getting larger with each function call. Hence, the function will end up calling itself infinitely many times (until the computer runs out of memory or the program terminates it)

(f) Rewrite the function gcd in pseudo-code to carry out Euclid’s algorithm without using recursion. [3]

> [!Answer]
>
> ```text
> 3(f)
>
> ```

---

<a id="toc-recursion"></a>

# Recursion

<a id="toc-recursion-definition"></a>

### Definition

##### 2025 ASRJC Prelim P1 Q5)

```text
5	Refer to the following recursive function P:010203040506070809101112
FUNCTION P(x : REAL, a : INTEGER) RETURNS REAL
IF a = 0 or a = 1 THEN
RETURN x
ENDIF
IF a MOD 2 = 0 THEN        r ← P(x, a / 2)
RETURN r * r
ELSE
RETURN x * P(x, a - 1)    ENDIF
ENDFUNCTION

```

(a) With reference to relevant line numbers in the pseudocode, explain the three features seen here that make P a recursive function. [3]

> [!Answer]
> The **base case** is seen in line 02. A terminating condition is provided that stops further function calls.
>
> Lines 07 and 10 show the **recursive call**, where the function calls itself.
> Lines 07 and 10 also show function calls that move closer to the **base case**.

**The author of the function intends for it to work for all non-negative integer values of a.**

(b) Identify the intended purpose of this function. [2]

> [!Answer]
> The function is intended to calculate x raised to the power of the value a.

**(c) Upon testing, the author realises that there is a logic error in the code. Identify this error and state how the existing code should be corrected. [2]**

> [!Answer]
> When a = 0, the function wrongly returns x instead of 1.
> Lines 2 – 3 should be changed to:
>
> ```text
> IF a = 0 THEN
> RETURN 1
> ENDIF
> IF a = 1 THEN
> RETURN x
> ENDIF
>
> ```

(d) Draw a recursion trace diagram to illustrate the recursive steps and the return value calculations when computing P(3.0, 7). [3]

> [!Answer]
> **Recursion** trace:

(e) State what would happen if P(3.0, –1) is executed. [1]

> [!Answer]
> It calls P(3.0, –2), which then calls P(3.0, –1) again. This cycle repeats, leading to a **stack** overflow error, a type of runtime error.

(f) Write down what you would add to the existing pseudocode for the function to handle negative integer values of a correctly. [2]

> [!Answer]
> Before line 02, add the following code:
>
> ```text
> IF a < 0 THEN
> RETURN 1.0 / P(x, -1*a)
> ENDIF
>
> ```

---

##### 2025 RVHS Prelim P1 Q3)

**3. Study the recursive function below.**

```python
def foo(n, m):
    if n == 0:
        return 0
    else:
        return m + foo(n-1, m-2)

```

**a) An example of a trace tree diagram showing the recursive function call foo(2,6) is shown as follows:**

**return 10**

**foo(2,6)**

**return 6 + 4 = 10**

**foo(1,4)**

**return 4 + 0 = 4**

**foo(0,2)**

**Use the above example to create a trace tree diagram for the recursive function call foo(4,2) . [3]**

> [!Answer]
> foo(4,2)  # return 2 + (-6) = -4
> foo(3,0)  # return 0 + (-6) = -6
> foo(2,-2) # return -2 + (-4) = -6
> foo(1,-4) # return (-4) + 0 = -4
> foo(0,-6) # return 0
>
> Corrected version
>
> foo(4,2) # return 2 + (-6) = -4
>
> * 2 + foo(3,0) # return 0 + (-6) = -6
>
> * 0 + foo(2,-2) # return -2 + (-4) = -6
>
> * -2 + foo(1,-4) # return (-4) + 0 = -4
>
> * -4 + foo(0,-6) # return 0
>
> 3

b) Write in pseudocode the iterative version of foo(n, m). [3]

> [!Answer]
>
> ```text
> FUNCTION foo(n, m) RETURNS INTEGER
>
>
> result ← 0
> WHILE n > 0 DO
> result ← result + m
> n ← n - 1
> m ← m - 2
>
>
> END WHILE
>
>
> RETURN result
>
>
> END FUNCTION
>
> ```
>
> 3

---

<a id="toc-object-oriented-programming"></a>

# Object-Oriented Programming

<a id="toc-object-oriented-programming-class-diagram"></a>

### Class Diagram

##### 2025 ACJC Prelim P1 Q2)

**2A private school has two kinds of students, full-time students and part-time students. It uses object-oriented programming (OOP) to store data about the students. For both kinds of students, their name and date of birth are stored. For full-time students, their address and telephone number are stored. For part-time students, the list of classes they are taking is stored. Full-time students pay an annual school fee which is a constant amount. The school fee for part-time students is calculated based on the number of classes they are taking.**

**(a) Draw a class diagram that shows the following in the school as described above: The superclass; Any subclasses; Inheritance; Attributes; Appropriate methods. [6]**

> [!Answer]
> Students- Name (string)- DOB (string)+ Constructor(Name, DOB)+ get_name()+ get_dob()+ get_school_fee()Full-timePart-time- Address (string)- Phone_no (string)- Classes (list of strings)+ get_address()+ get_phone_no()+ get_school_fee()+ Constructor+ get_classes()+ get_school_fee()
>
> ```mermaid
> classDiagram
> direction TB
> class Students {
>   -Name : string
>   -DOB : string
>   +Constructor(Name, DOB)
>   +get_name()
>   +get_dob()
>   +get_school_fee()
> }
> class FullTime["Full-time"] {
>   -Address : string
>   -Phone_no : string
>   +get_address()
>   +get_phone_no()
>   +get_school_fee()
> }
> class PartTime["Part-time"] {
>   -Classes : list of strings
>   +Constructor
>   +get_classes()
>   +get_school_fee()
> }
> Students <|-- FullTime
> Students <|-- PartTime
> ```

(b) Give an example of inheritance in the class diagram in part (a). [1]

> [!Answer]
> Full-time and part-time classes inherit attributes (Name and DOB) and methods (accessor for Name and DOB) from Students parent class

(c) Explain where and how polymorphism is useful in this context. [2]

> [!Answer]
> The calculation of school fees is different for full-time and part-time students, but the get_school_fee() method can be used for both. This streamlines code that uses the school fee for other purposes.

**The school needs to back up and archive data regularly.**

(d)(i) Explain why there is a need to back up data. [2]

> [!Answer]
> Data should be backed up as it is updated so that a copy of the data exists in case the main database is damaged or deleted by accident or due to malicious action. The data can then be recovered from the **backup** copy.

(ii) Explain why there is a need to archive data. [2]

> [!Answer]
> Data that is no longer needed on a day-to-day basis (e.g. students who have already graduated) should be archived. It can still be looked up if necessary, but the data does not clog up space in the current database.

---

##### 2025 ASRJC Prelim P1 Q3)

**3 Harley Thorman Corporation is developing an inventory management system for its electronic products using Object-Oriented Programming (OOP). The main types of electronic devices that the corporation sells are display devices, audio devices and computing devices. Display devices include televisions, computer monitors and screen projectors. Audio devices include speaker systems and headphones. Computing devices include desktops, laptops and tablets.**

(a) Draw a class diagram for this system showing classes and their inheritance relationships. Do not include any attributes or methods in the diagram. [3]

> [!Answer]
> **Class diagram**:
>
> ```mermaid
> classDiagram
> direction TB
> class ElectronicDevice
> class DisplayDevice
> class AudioDevice
> class ComputingDevice
> class Television
> class ComputerMonitor["Computer Monitor"]
> class ScreenProjector["Screen Projector"]
> class SpeakerSystem["Speaker System"]
> class Headphones
> class Desktop
> class Laptop
> class Tablet
> ElectronicDevice <|-- DisplayDevice
> ElectronicDevice <|-- AudioDevice
> ElectronicDevice <|-- ComputingDevice
> DisplayDevice <|-- Television
> DisplayDevice <|-- ComputerMonitor
> DisplayDevice <|-- ScreenProjector
> AudioDevice <|-- SpeakerSystem
> AudioDevice <|-- Headphones
> ComputingDevice <|-- Desktop
> ComputingDevice <|-- Laptop
> ComputingDevice <|-- Tablet
> ```

(b) Explain why inheritance is an important feature in OOP. [1]

> [!Answer]
> **Inheritance** enables developers to reuse code efficiently, as common attributes and methods can be defined in a parent class, and all subclasses would inherit these functionalities. It eliminates the need to duplicate code across multiple classes. Updates made to the parent class automatically propagate to all subclasses. Therefore, it makes the codebase more maintainable and consistent.

(c) Suggest which class each of the following attributes should be placed in, explaining your choice:

* **CPU model**
* **product serial number. [3]**

> [!Answer]
> CPU model should be placed in the ComputingDevice class, as typically only computing devices (desktops, laptops, tablets) would include CPU model information in the specifications.
> Product serial number should be placed in the ElectronicDevice base class, as all electronic products need unique serial numbers for identification.

(d) Suggest a possible private method that one might include in the OOP system, explaining why keeping it private would be reasonable. [2]

> [!Answer]
> validateSerialNumber() would be a possible private method to include in the ElectronicDevice class. It should be private because it is an internal validation process that other classes don’t need to access directly.

**There are different types of TV display technologies, each with distinct features. LCD TVs use liquid crystal displays with backlighting, while LED TVs use LED backlighting for better energy efficiency. OLED TVs use organic light-emitting diodes that allow pixels to turn completely off, providing superior contrast ratios. QLED TVs use quantum dot technology to enhance brightness and colour accuracy. What distinguishes them is the panel technology type, which results in differences in display characteristics such as contrast ratio, peak brightness and colour gamut coverage.**

(e) Suggest how the OOP system should be updated to accommodate these different TV display technologies, justifying the approach chosen. [2]

> [!Answer]
> We should add an attribute ‘panel_technology’ (LCD/LED/OLED/QLED) to the Television class, rather than creating separate subclasses for each TV type. They would have largely similar methods and attributes, differing only in specifications.

(f) Explain what is meant by polymorphism in OOP. [1]

> [!Answer]
> **Polymorphism** refers to the ability of a method to exhibit different behaviours for different classes within the class hierarchy. This is achieved through subclasses overriding methods inherited from their parent class.

---

##### 2025 DHS Prelim P1 Q1)

**1 A software developing company needs software to calculate how much each employee should be paid.**

**(a) A bonus payment may be added to an employee’s salary. A pension payment may also be subtracted from an employee’s salary. The company needs to assess what additions and subtractions should be made to the salary of each employee. There are three conditions to check:**

* **If the employee has worked on a public holiday, they receive a 3% bonus payment.**

* **If the employee has worked 160 or more hours in a month, they receive an additional**
  **5% bonus payment.**

* **If the employee pays into a pension, the company subtracts 4% for the pension payment.**

Copy and complete the decision table to show the additions and subtractions. [3]

Rules

Conditions
Public holiday Y Y Y Y N N N N

Hours >= 160 Y Y N N Y Y N N

Pension Y N Y N Y N Y N

Actions
3% bonus payment

5% bonus payment

4% pension payment

> [!Answer]
>
> * per row Rules
>
> 3% bonus payment X X X X
>
> 5% bonus payment X X   X X
>
> 4% pension payment X  X  X  X

(b) Explain the changes in the decision table after removing redundancies. [1]

> [!Answer]
> No pair of actions for a several combinations are the same.  so no combinations can be combined,
> and no reducing the number of rules         (1)

**(c) The company has decided to implement a program for the software using object - oriented programming (OOP).**

**The following names will be used for the OOP design:**

**Employee: Each employee has a unique employeeID, name, address and date of birth (dob). There are two types of employee:**

**salary (SalaryEmployee) and**
**apprenticeship (ApprenticeshipEmployee).**

**SalaryEmployee: Salaried employees are paid a fixed monthly payment (MonthlyPayment). The hours a salary employee works in a month (HoursThisMonth) are recorded to calculate bonus payments. Status of worked on public holiday and pension are recorded. They may receive bonus payments and make pension payments (given in part(a)).**

**ApprenticeshipEmployee**
**: Apprenticeship employees are paid weekly**
**(HoursThisWeek). They receive an hourly rate of pay. Apprenticeship employees do not receive bonus payments or make pension payments.**

Draw a class diagram that shows the following for the situation described above. [10]

* the superclass
* any subclasses
* inheritance
* properties
* appropriate methods

3

> [!Answer]
> programming (OOP).
>
> * **inheritance** (arrow filled or unfilled)  (1)
>
> * 3 class names     (1)
>
> * Private attributes    (2)
>
> * Public methods    (2)
>
> * Accessors/Getters   (2)
>
> * Mutators/Setters    (2)
>
> (1)
> (1)
> (1)
>
> Private:
> HourlyRate : REAL
> HoursThisWeek : REAL/INTEGER
> Public:
> Constructor()
> SetHoursThisWeek()
> GetHourlyRate()
> GetHoursThisWeek()
> SetHourlyRate()
>
> SalaryEmployee
> Private:
> MonthlyPayment :  REAL
> HoursThisMonth: REAL
> PublicHoliday : BOOLEAN
> Pension : BOOLEAN
> Public:
>
> * Constructor()
>
> GetMonthlyPayment()
> GetHoursThisMonth()
> GetPublicHoliday()
> GetPension()
> SetMonthlyPayment()
> SetHoursThisMonth()
> SetPublicHoliday()
> SetPension()
>
> Employee
> Private:
> EmployeeID : STRING
> Name : STRING
> Address : STRING
> DateOfBirth : Date
> Public:
> Constructor()
> GetEmployeeID()
> GetName()
> GetAddress()
> GetDateOfBirth()
> SetEmployeeID()
> SetName()
> SetAddress()
> SetDateOfBirth()
>
> ```mermaid
> classDiagram
> direction TB
> class Employee {
>   -EmployeeID : STRING
>   -Name : STRING
>   -Address : STRING
>   -DateOfBirth : Date
>   +Constructor()
>   +GetEmployeeID()
>   +GetName()
>   +GetAddress()
>   +GetDateOfBirth()
>   +SetEmployeeID()
>   +SetName()
>   +SetAddress()
>   +SetDateOfBirth()
> }
> class SalaryEmployee {
>   -MonthlyPayment : REAL
>   -HoursThisMonth : REAL
>   -PublicHoliday : BOOLEAN
>   -Pension : BOOLEAN
>   +Constructor()
>   +GetMonthlyPayment()
>   +GetHoursThisMonth()
>   +GetPublicHoliday()
>   +GetPension()
>   +SetMonthlyPayment()
>   +SetHoursThisMonth()
>   +SetPublicHoliday()
>   +SetPension()
> }
> class ApprenticeshipEmployee {
>   -HourlyRate : REAL
>   -HoursThisWeek : REAL/INTEGER
>   +Constructor()
>   +SetHoursThisWeek()
>   +GetHourlyRate()
>   +GetHoursThisWeek()
>   +SetHourlyRate()
> }
> Employee <|-- SalaryEmployee
> Employee <|-- ApprenticeshipEmployee
> ```

**(d) A SalaryEmployee is paid a fixed monthly payment.**

* **If the employee has worked on a public holiday, they receive a 3% bonus payment.**
  **This is calculated from their MonthlyPayment.**

* **If the employee has worked 160 or more hours in a month, they receive an**
  **additional 5% bonus payment, calculated from their MonthlyPayment.**

* **If the employee pays into a pension, 4% will be subtracted from their**
  **MonthlyPayment.**

**Monthly salary is the final payment the employee receives.**

**For example, Ming Teck is a SalaryEmployee. His fixed MonthlyPayment is $1000. He has worked a public holiday. He has worked 163 hours this month. He pays into a pension.**

* **The public holiday bonus is $30 (3% of $1000)**
* **The hours worked bonus payment is $50 (5% of $1000)**
* **The pension payment is $40 (4% of $1000)**

**Ming Teck’s monthly salary is calculated as ($1000 + $30 + $50) − $40 = $1040**

**The function CalculateSalary() of SalaryEmployee is used to calculate the monthly salary.**

**It:**

* **takes a SalaryEmployee as a parameter**
* **using method(s) from within the class using . operator**
* **calculating the bonus payments and pension payment**
* **calculates and returns the monthly salary.**

Copy and complete the flowchart below for the function CalculateSalary(). [6]

Symbols used for flowchart design:

Start
CalculateSalary(TheEmployee: SalaryEmployee)

```text
BasicSalary ← 0
BonusPayment ← 0
PensionPayment ← 0
HoursBonus ← 0.05
HoursMonthBonus ← 160
PensionCost ← 0.04
PublicHolidayBonus ← 0.03

```

4

> [!Answer]
>
> * MonthlyPayment accessed from the parameter using Get method and store in BasicSalary
>
> * Hours, Pension and PublicHoliday accessed from the parameter using Get methods
>
> * Checking if Hours is > = 160, calculating bonus payment (BasicSalary * 0.05)
>
> * Checking if pension is true, calculation pension to pay (BasicSalary * 0.04)
>
> * Checking if public holiday is true, calculation of bonus payment (BasicSalary * 0.03)
>
> * Adding both bonus payments to basic salary and deducting pension from salary
>
> * Returning the new salary
>
> ```text
> BasicSalary ← TheEmployee.GetMonthlyPayment() (1)
>
> ```
>
> (1)
> TheEmployee.GetHoursThisMonth()
>
> > = HoursMonthBonus
>
> ```text
> BonusPayment ←
>
> ```
>
> * BasicSalary * HoursBonus
>
> TheEmployee.GetPension()
> = TRUE
>
> ```text
> PensionPayment ←
>
> ```
>
> * BasicSalary * PensionCost (1)
>
> TheEmployee.GetPublicHoliday()
> = TRUE
>
> ```text
> BonusPayment ←
>
> ```
>
> * BonusPayment + BasicSalary
>
> * * PublicHolidayBonus
>
> ```text
> MonthlySalary ← BasicSalary + BonusPayment – PensionPayment
>
> ```
>
> (1)
> (1)
>
> ```text
> RETURN MonthlySalary
>
> ```
>
> End
> (1)
>
> ```mermaid
> flowchart TD
>   A([Start]) --> B["CalculateSalary(TheEmployee: SalaryEmployee)"]
>   B --> C["BasicSalary ← 0<br/>BonusPayment ← 0<br/>PensionPayment ← 0<br/>HoursBonus ← 0.05<br/>HoursMonthBonus ← 160<br/>PensionCost ← 0.04<br/>PublicHolidayBonus ← 0.03"]
>   C --> D["BasicSalary ← TheEmployee.GetMonthlyPayment()"]
>   D --> E{"TheEmployee.GetHoursThisMonth()<br/>>= HoursMonthBonus"}
>   E -- "Y" --> F["BonusPayment ←<br/>BasicSalary * HoursBonus"]
>   E -- "N" --> G{"TheEmployee.GetPension()<br/>= TRUE"}
>   F --> G
>   G -- "Y" --> H["PensionPayment ←<br/>BasicSalary * PensionCost"]
>   G -- "N" --> I{"TheEmployee.GetPublicHoliday()<br/>= TRUE"}
>   H --> I
>   I -- "Y" --> J["BonusPayment ←<br/>BonusPayment + BasicSalary * PublicHolidayBonus"]
>   I -- "N" --> K["MonthlySalary ←<br/>BasicSalary + BonusPayment – PensionPayment"]
>   J --> K
>   K --> L["RETURN MonthlySalary"]
>   L --> M([End])
>
> ```

(e) (i) In OOP, state the purpose of polymorphism. [1]

> [!Answer]
> Allows objects or methods to exhibit different behaviors under different classes.  (1)

**(ii) What changes in design needs to be made i f the objects of class ApprenticeshipEmployee also use CalculateSalary() to calculate the weekly salary. [1]**

> [!Answer]
> What changes in design needs to be made if the objects of class
> ApprenticeshipEmployee also use CalculateSalary() to calculate the weekly
> salary.
>
> CalculateSalary() must be a public method of ApprenticeshipEmployee (1)

(f) Discuss the advantages of using modular design in software development. [2]

> [!Answer]
> Advantages including easier maintenance and debugging,  enhanced reusability of
> components, improved collaboration,  increased scalability,  faster development cycles,
> and better fault isolation.         (2)

**(g) The software design may need to change from time to time by a team of programmers. Explain how the team tracks the changes with a system. [2]**

> [!Answer]
> **Version control** is a system that tracks changes to files, typically code in software development,
> allowing teams to collaborate effectively and revert to previous versions when needed
>
> * (2)

---

##### 2025 NYJC Prelim P1 Q5)

**5 A software company is writing a program for a vehicle hire business. Both cars and vans are available for hire. For all vehicles, the data that will be stored include: Vehicle Registration Number (VRN) Total distance travelled (km) Date hired Date of return Cost per day Available for hire For cars, the additional data stored include: Fuel type (petrol, diesel, electric, hybrid) For vans, the additional data stored include: Maximum load (kg) The odometer in the vehicle displays the total distance the vehicle has travelled since manufacture. When a vehicle is hired:**

* **total distance travelled is set to the odometer’s value**

* **date hired is set to the current date**

* **return date is set to the date the vehicle is expected to be returned**

* **available for hire is set to FALSE.**
  **When a vehicle is returned:**

* **hire cost is returned as the cost per day multiplied by the number of days the vehicle was**
  **hired**

* **total distance travelled is set to the odometer value**

* **date returned is set to the current date**

* **available for hire is set to TRUE.**
  **Object-oriented programming will be used to model vehicles.**

(a) Draw a class diagram that shows the following for the situation described above.

* the superclass
* any subclasses
* inheritance
* properties
* appropriate methods.

[8]

> [!Answer]
> 5.0	Data Management, **Object-Oriented Programming**
>
> Vehicle: private attributes present
>
> * Vehicle: public getter methods and appropriate setter methods
>
> * Car and Van subclasses
>
> * correct **inheritance** relationship between Car/Van and Vehicle
>
> * additional private attributes and public getter/setter for Car: Fuel type
>
> * additional private attributes and public getter/setter for Van: Maximum load
>
> * hire_vehicle() method
>
> * return_vehicle() method
>
> * **Polymorphism**: all Vehicle instances have same method names
>
> ```mermaid
> classDiagram
> direction TB
> class Vehicle {
>   -VRN
>   -distance
>   -date_hired
>   -date_of_return
>   -cost_per_day
>   -availability
>   +get_VRN()
>   +get_distance()
>   +get_date_hired()
>   +get_date_of_return()
>   +get_cost_per_day()
>   +get_availability()
>   +set_VRN()
>   +set_distance()
>   +set_date_hired()
>   +set_date_of_return()
>   +set_cost_per_day()
>   +set_availability()
>   +hire_vehicle()
>   +return_vehicle()
> }
> class Car {
>   -fuel_type
>   +get_fuel_type()
>   +set_fuel_type()
> }
> class Van {
>   -max_load
>   +get_max_load()
>   +set_max_load()
> }
> Vehicle <|-- Car
> Vehicle <|-- Van
> ```

(b) Explain how encapsulation helps to prevent inadvertent data modification. [2]

> [!Answer]
> private attributes cannot be directly accessed or modified outside of the class, only through public methods, to prevent the object falling into an inconsistent state
>
> * e.g. hire_vehicle() method ensures the total distance, date hired, return date, and availability are updated in a consistent way

(c) Explain how inheritance promotes code reuse. [2]

> [!Answer]
> **inheritance** allows subclasses to access public methods of the **superclass**
>
> * Car and Van can access the public getter methods of Vehicle e.g. getVRN(), and do not need to duplicate the same code.

**6**
**The programmer uses a database to store vehicle hire data. Each row in the table represents a vehicle hire record. A vehicle must be hired for a minimum of one day. Vehicle hire data is stored in the following table: VRN TotalDistance DateHired DateReturned CostPerDay Available FuelType MaxLoad**

(d) (i) Identify a suitable primary key for the above table. [1]

> [!Answer]
> (VRN, DateHired)

(ii) Identify suitable SQL data types for the following columns:

1. DateHired [1]

2. Available [1]

> [!Answer]
> DateHired: DATE / STRING / TEXT
>
> * Available: BOOLEAN / INTEGER

**(e) State whether the above table is in Third Normal Form (3NF). Explain your answer. [4]**

> [!Answer]
> Not in **3NF**
>
> **3NF** requires **2NF**
>
> * non-key attributes CostPerDay, FuelType, MaxLoad depend only on VRN (name at least one appropriate non-key attribute)
>
> * and not on the entire PK (partial dependence), hence violating **2NF**

**A database consultant rewrites the above table into the following table descriptions: Vehicle (VRN, Type, TotalDistance, CostPerDay, Available) Hire (VRN, DateHired, DateReturned) Car (VRN, FuelType) Van (VRN, MaxLoad) The vehicle type is stored as either 'Car' or 'Van'.**

(f) Draw an entity-relationship (ER) diagram representing the four tables. [4]

> [!Answer]
> All entities represented: Vehicle, Hire, Car, Van
>
> * Vehicle <--1--1--> Car
>
> * Vehicle <--1--1--> Van
>
> * Vehicle <--1--n--> Hire
>
> ```mermaid
> erDiagram
>   Vehicle ||--|| Car : has
>   Vehicle ||--|| Van : has
>   Vehicle ||--o{ Hire : has
>
> ```

**(g) Write an SQL query to retrieve from the above tables the VRNs of hybrid cars and their latest date of hire. [6]**

> [!Answer]
>
> ```sql
> SELECT Hire.VRN, ... (include DateHired field)
>
> ```
>
> ```sql
> SELECT ..., MAX(DateHired)
> SELECT ..., MAX(DateHired)
>
> ```
>
> * GROUP BY Hire.VRN
>
> * FROM Hire
>
> * INNER JOIN Car ON Hire.VRN = Car.VRN
>
> (Alternatively, filter using Vehicle.Type = 'Car' with Vehicle table joined)
>
> * WHERE FuelType = 'hybrid'
>
> * Correct SQL syntax and command order

---

##### 2025 TJC Prelim P1 Q3)

**3A software company is writing a program for a vehicle hire business. Both cars and vans are available for hire. For all vehicles, the data that will be stored include: Vehicle Registration Number (VRN) Total distance travelled (km) Date hired Date of return Cost per day Availability for hire For cars, the additional data stored include: Fuel type (petrol, diesel, electric, hybrid) For vans, the additional data stored include: Maximum load (kg) The odometer in the vehicle displays the total distance the vehicle has travelled since manufacture. When a vehicle is hired: total distance travelled is set to the odometer's value date hired is set to the current date date of return is set to the date the vehicle is expected to be returned availability for hire is set to FALSE. When a vehicle is returned: hire cost is returned as the cost per day multiplied by the number of days the vehicle was hired total distance travelled is set to the odometer value date of return is set to the current date availability for hire is set to TRUE. Object-oriented programming will be used to model this situation.**

**(a) Draw a class diagram that shows the following for the situation described above. the superclass any subclasses inheritance properties appropriate methods. [8]**

> [!Answer]
> Vehicle
>
> * VRN- distance- date_hired- date_of_return- cost_per_day- availability
>
> - get_VRN()+ get_distance()+ get_date_hired()+ get_date_of_return()+ get_cost_per_day()+ get_availability()+ set_VRN()+ set_distance()+ set_date_hired()+ set_date_of_return()+ set_cost_per_day()+ set_availability()+ hire_vehicle()+ return_vehicle()
>   Car
>
> * fuel_type
>
> - get_fuel_type()+ set_fuel_type()
>   Van
>
> * max_load
>
> - get_max_load()+ set_max_load()
>   Note: Many students did not identify the methods hire_vehicle() and return_vehicle() for the Vehicle class.
>
> ```mermaid
> classDiagram
> direction TB
> class Vehicle {
>   -VRN
>   -distance
>   -date_hired
>   -date_of_return
>   -cost_per_day
>   -availability
>   +get_VRN()
>   +get_distance()
>   +get_date_hired()
>   +get_date_of_return()
>   +get_cost_per_day()
>   +get_availability()
>   +set_VRN()
>   +set_distance()
>   +set_date_hired()
>   +set_date_of_return()
>   +set_cost_per_day()
>   +set_availability()
>   +hire_vehicle()
>   +return_vehicle()
> }
> class Car {
>   -fuel_type
>   +get_fuel_type()
>   +set_fuel_type()
> }
> class Van {
>   -max_load
>   +get_max_load()
>   +set_max_load()
> }
> Vehicle <|-- Car
> Vehicle <|-- Van
> ```

(b) Explain how encapsulation helps to prevent inadvertent data modification using examples from this situation. [2]

> [!Answer]
> Private attributes cannot be directly accessed or modified outside of the class, only through public methods, to prevent the object falling into an inconsistent statee.g. hire_vehicle() method ensures the total distance, date hired, return date, and availability are updated in a consistent way

(c) Explain how inheritance promotes code reuse using examples from this situation. [2]

> [!Answer]
> **Inheritance** allows subclasses to access public methods of the superclassCar and Van can access the public getter methods of Vehicle e.g. getVRN(), and do not need to duplicate the same code.

**The programmer uses a database to store vehicle hire data. Each row in the table represents a vehicle hire record. A vehicle must be hired for a minimum of one day. Vehicle hire data is stored in the following table: VRN TotalDistance DateHired DateReturned CostPerDay Availability FuelType MaxLoad**

(d)(i) Identify the primary key for the above table. [1]

> [!Answer]
> (VRN, DateHired)Note: many students did not recognize the composite key

**(ii) Identify suitable SQL data types for the following columns: 1. DateHired [1] 2. Availability [1]**

> [!Answer]
> DateHired: TEXT / DATE / STRINGAvailability: BOOLEAN / INTEGER

(e) Explain why the above table is not in Third Normal Form (3NF). [3]

> [!Answer]
> **3NF** requires 2NFNon-key attributes CostPerDay, FuelType, MaxLoad depend only on VRN, which is part of the **primary key**,and not on the entire **primary key** (partial dependence)

**A database consultant rewrites the above table into the following table descriptions: Vehicle (VRN, Type, TotalDistance, CostPerDay, Availability) Hire (VRN, DateHired, DateReturned) Car (VRN, FuelType) Van (VRN, MaxLoad) The vehicle type is stored as either 'Car' or 'Van'.**

(f) Identify the foreign key(s) of the tables Hire, Car and Van. [1]

> [!Answer]
> VRN

(g) Draw an entity-relationship (ER) diagram showing the four tables and the relationships between them. [4]

> [!Answer]
>
> ```mermaid
> erDiagram
>   Vehicle ||--|| Car : has
>   Vehicle ||--|| Van : has
>   Vehicle ||--o{ Hire : has
>
> ```

(h) Write an SQL query to retrieve from the above tables the VRNs of hybrid cars and their latest date of hire. [6]

> [!Answer]
>
> ```sql
> SELECT Car.VRN, MAX(DateHired)FROM Hire, CarWHERE Car.VRN = Hire.VRNAND Car.FuelType = “Hybrid”GROUP BY Car.VRNORSELECT Vehicle.VRN, MAX(DateHired)FROM Vehicle  INNER JOIN Hire ON Vehicle.VRN = Hire.VRN  INNER JOIN Car ON Vehicle.VRN = Car.VRNWHERE Type = 'Car'  AND FuelType = 'hybrid'GROUP BY Vehicle.VRN
>
> ```

---

##### 2025 YIJC Prelim P1 Q4)

**The data management system used in a wildlife reserve to keep track of the tagged animals is designed using Object-Oriented Programming (OOP) to construct the Animal object.**

**Explain the purposes of encapsulation [1]**

> [!Answer]
>
> * **Encapsulation**
>
> * **Encapsulation** refers to bundling data and related methods into a single class and restricting direct access to the internal attributes of an object.This helps to protect the data, ensure **data integrity**, and prevent unintended modification from external code.

inheritance.[1]

> [!Answer]
>
> * **Inheritance**
>
> * **Inheritance** allows a **subclass** to acquire attributes and methods from a **superclass**, enabling code reuse and promoting hierarchical design.It also allows subclasses to extend or override inherited behaviours.

**The animals are classified as a bird, marine animal, or mammal. Each animal is identified by a unique identifier (UID) which consists of its species name and a unique number. For example, sunbird-457 and sunbird-087 are two different animals of the same species. Besides the species, other attributes stored in the Animal object are gender, weight, and age. Additional attributes are also recorded for the following classifications: wingspan of a bird habitat of a marine animal body temperature of a mammal.**

Using OOP principles, draw a class diagram for the Animal object used in the data management system. Your diagram should include the superclass, subclasses, inheritance, attributes, and appropriate methods. [8]

> [!Answer]
>
> * **Superclass** Animal clearly shown
>
> * Subclasses Bird, MarineAnimal, and Mammal shown
>
> * Correct **inheritance** arrows or relationships indicated
>
> * **Superclass** attributes: UID, species, gender, weight, age
>
> * **Subclass**-specific attributes included: wingspan (Bird), habitat (MarineAnimal), bodyTemperature (Mammal)
>
> * At least one relevant method shown in **superclass** (e.g., getInfo(), computeHealthIndex())
>
> * At least one method shown in a **subclass** (e.g., checkTemperature() in Mammal)
>
> * Diagram is clearly labelled and follows correct OOP conventions (e.g., visibility, clarity, structure)
>
> ```mermaid
> classDiagram
> direction TB
> class Animal {
>   -UID
>   -species
>   -gender
>   -weight
>   -age
>   +getInfo()
>   +computeHealthIndex()
> }
> class Bird {
>   -wingspan
> }
> class MarineAnimal {
>   -habitat
> }
> class Mammal {
>   -bodyTemperature
>   +checkTemperature()
> }
> Animal <|-- Bird
> Animal <|-- MarineAnimal
> Animal <|-- Mammal
> ```

**A binary search tree (BST) holds the UIDs of the animals in the array animalBST. Each element of the array contains three values. leftPtr and rightPtr are integers and UID is a string. The root of the BST is stored in an integer variable, rootPtr. The unused elements of the array are in a free space list that starts from freePtr. The UIDs of the animals are guaranteed to be unique. The contents of the array animalBST is shown below. –1 represents the null pointer.**

| Index | leftPtr | UID            | rightPtr |         |
| ----- | ------- | -------------- | -------- | ------- |
| 0     | 3       | macaque-103    | 1        |         |
| 1     | –1      | mousedeer-215  | 2        | rootPtr |
| 2     | 4       | sunbird-457    | –1       | 0       |
| 3     | –1      | kingfisher-342 | –1       |         |
| 4     | 5       | sunbird-087    | –1       |         |
| 5     | –1      | squirrel-457   | –1       | freePtr |
| 6     | 7       | –1             | 6        |         |
| 7     | 8       | –1             |          |         |
| 8     | 9       | –1             |          |         |
| 9     | –1      | –1             |          |         |

Draw the BST represented by the array animalBST.[2]

> [!Answer]
>
> * macaque-103            /           \  kingfisher-342     mousedeer-215     /                    \drongo-609            sunbird-457                      /               sunbird-087               /          squirrel-457            /        snakehead-321
>
> * Correct structure reflecting all nodes and their relationships based on pointers.
>
> * Correct left and right positioning of all nodes based on UID comparisons.

Two new animal’s UIDs, drongo-609 and snakehead-321 are to be inserted into the BST. Copy the above table to your answer booklet and show the changes to the array animalBST after the insertion.[4]

> [!Answer]
>
> * Inserted drongo-609 at index 6 and updated leftPtr of kingfisher-342 (index 3) to 6
>
> * Inserted snakehead-321 at index 7 and updated leftPtr of squirrel-457 (index 5) to 7
>
> * Set leftPtr and rightPtr of both new nodes (index 6 and 7) to –1
>
> * Updated freePtr to 8 to reflect the next available free node

**There is an option of using either a static or a dynamic data structure for the array animalBST.**

State one advantage and one disadvantage of implementing it with a static data structure.[2]

> [!Answer]
>
> * One advantage and one disadvantage of using a **static** data structure.
>
> * Advantage) **Static** arrays are simple to implement and provide fast access due to fixed memory locations (contiguous storage).Example: Direct indexing with known position.
>
> * Disadvantage) Fixed size makes the structure inflexible — once full, no new nodes can be added, which limits scalability.This can lead to wasted memory or insertion failures.

**Write the UID outputs when performing the following traversals on animalBST: in-order traversal [1]**

> [!Answer]
> drongo-609, kingfisher-342, macaque-103, mousedeer-215, snakehead-321, squirrel-457, sunbird-087, sunbird-457No slips allowed. Allow BOD if new entries are not included.

post-order traversal[1]

> [!Answer]
> drongo-609, kingfisher-342, snakehead-321, squirrel-457, sunbird-087, sunbird-457, mousedeer-215, macaque-1031 slip allowed. Allow BOD if new entries are not included.

---

<a id="toc-object-oriented-programming-4-pillars-of-oop"></a>

### 4 Pillars of OOP

##### 2025 RI Prelim P1 Q3)

**3 A robotics company is developing a simulation system for different types of warehouse robots. These robots help with tasks such as transporting items, sorting packages, and restocking shelves.**

**Each robot stores the following common data:**

* **robotID: a unique robot ID**
* **status: status (active or charging)**
* **batteryLevel: current battery level (initialised to 100)**
* **location: location in the warehouse (zone ID as a string)**

**There are three types of robots:**

* **Transport robots carry items from one zone to another. These robots have a**
  **maximum load of 100kg (kgCarried).**

* **Sorting robots identify and sort parcels. They store the number of parcels**
  **sorted per hour (parcelsPerHour)**

* **Restock robots move items from the storage area to shelves. They store the**
  **number of shelves restocked per cycle (shelvesRestocked).**

**Each robot has a method PerformTask():**

* **A transport robot’s battery level decreases by 5% for every 10kg it carries.**
* **A sorting robot’s battery level decreases by 2% for every 10 parcels sorted.**
* **A restock robot’s battery level decreases by 3% per shelf restocked.**

**When a robot’s battery level reaches 10% or less, its status is set to charging.**

**Object-oriented programming will be used to simulate these robots.**

(a) Draw a class diagram for the simulation described above. Include:

* the superclass

* any subclasses

* inheritance

* attributes

* appropriate methods [8]

> [!Answer]
>
> * +-----------------------------+
>
> * |       Robot (**Superclass**)    |
>
> * +-----------------------------+
>
> * | - robotID: String           |
>
> * | - status: String            |
>
> * | - batteryLevel: Integer     |
>
> * | - location: String          |
>
> * +-----------------------------+
>
> * | + PerformTask()             |
>
> * | + get_robotID(): String     |
>
> * | + set_robotID(String)       |
>
> * | + get_status(): String      |
>
> * | + set_status (String)       |
>
> * | + get_batteryLevel(): Int   |
>
> * | + set_batteryLevel(Int)     |
>
> * | + get_location(): String    |
>
> * | + set_location(String)      |
>
> * +-----------------------------+
>
> * /       |       \
>
> * /        |        \
>
> * /         |         \
>
> * +----------------------+    +-------------------------+   +----------------------------+
>
> * |   TransportRobot     |   |     SortingRobot        |   |     RestockRobot           |
>
> * +----------------------+   +-------------------------+   +----------------------------+
>
> * | - kgCarried: Int     |   | - parcelsPerHr: Int     |   | - shelvesRestocked: Int    |
>
> * +----------------------+   +-------------------------+   +----------------------------+
>
> * | + PerformTask()      |   | + PerformTask()         |   | + PerformTask()            |
>
> * | + get_kgCarried()    |   | + get_parcelsPerHr()    |   | + get_shelvesRestocked()   |
>
> * |      : Int           |  |      : Int              |   |      : Int                 |
>
> * | + set_kgCarried(int) |   | + set_parcelsPerHr(Int) |   | + set_shelvesRestocked(Int)|
>
> * +----------------------+   +-------------------------+   +----------------------------+
>
> Names of **superclass** and subclasses
> **Superclass** attributes
> **Superclass** getters and setters
> Subclasses all attributes
> Subclasses all getters and setters
> Polymorphic method in super and
> subclasses
> Arrows must point to **superclass**
> Private minus and public plus
>
> ```mermaid
> classDiagram
> direction TB
> class Robot {
>   -robotID : String
>   -status : String
>   -batteryLevel : Integer
>   -location : String
>   +PerformTask()
>   +get_robotID() : String
>   +set_robotID(String)
>   +get_status() : String
>   +set_status(String)
>   +get_batteryLevel() : Int
>   +set_batteryLevel(Int)
>   +get_location() : String
>   +set_location(String)
> }
> class TransportRobot {
>   -kgCarried : Int
>   +PerformTask()
>   +get_kgCarried() : Int
>   +set_kgCarried(int)
> }
> class SortingRobot {
>   -parcelsPerHr : Int
>   +PerformTask()
>   +get_parcelsPerHr() : Int
>   +set_parcelsPerHr(Int)
> }
> class RestockRobot {
>   -shelvesRestocked : Int
>   +PerformTask()
>   +get_shelvesRestocked() : Int
>   +set_shelvesRestocked(Int)
> }
> Robot <|-- TransportRobot
> Robot <|-- SortingRobot
> Robot <|-- RestockRobot
> ```

**(b)**

(i) Describe instantiation, with an example from simulation. [2]

> [!Answer]
> Instantiation is the process of creating an object from a class. For example,
> creating a new TransportRobot object called robot1 is instantiating the
> TransportRobot class.

(ii) Describe encapsulation, using an example from the simulation. [2]

> [!Answer]
> **Encapsulation** is the concept of hiding internal data of an object and allowing
> access only through methods. Accept: bundling of private data and public methods in
> a single class
> In the simulation, the robot’s batteryLevel can be made private, and only modified via
> the PerformTask() method.

(iii) Describe inheritance, using an example from the simulation. [2]

> [!Answer]
> **Inheritance** allows a **subclass** to reuse attributes and methods from a
> **superclass**. In this case, TransportRobot, SortingRobot, and RestockRobot inherit
> common attributes and methods from the Robot **superclass**.

(iv) Describe polymorphism, using an example from the simulation. [2]

> [!Answer]
> **Polymorphism** allows the same method name to have different
> implementations in different subclasses. Each **subclass** defines its own version of
> PerformTask(), which behaves differently depending on the robot type.

**(c) The system includes validation for the number of kilograms carried per trip by a transport robot. Provide examples of test data for the input variable kgCarried. [4]**

> [!Answer]
> Type of
> test Test data Reasoning
> Normal 30 A typical value within the expected range of carried
> weight
> Abnormal -5 Invalid: negative weight not allowed
> Extreme 0 or maximum allowed
> (i.e.., 100)
> Edge cases that test no load and upper limit of
> carrying capacity

---

##### 2025 RVHS Prelim P1 Q8)

**8. Read the following description.**

**“This is a conceptual system for representing and modeling home appliances, such as washing machines and refrigerators, in an object-oriented programming (OOP) context. The system consists of several classes that work together to capture the characteristics and behaviors of these appliances.**

**At the heart of each appliance is the PowerUnit, represented by a class that captures its type (AC or DC), power rating, and brand.**

**The Appliance class serves as a foundation for all appliances. It has attributes such as power unit, colour, weight, and a Boolean flag to indicate whether the appliance is switched on or off. It also provides methods for switching on, switching off, and connecting to a smart home network.**

**Washing machines and refrigerators are two types of appliances that share all the characteristics of an appliance. They have additional attributes, such as drum size for washing machines and cooling capacity for refrigerators. Interestingly, they also have distinct ways of connecting to a smart home network.”**

a) By examining the attributes and methods of these classes, draw the UML class diagram. [6]

> [!Answer]
>
> ```mermaid
> classDiagram
> direction TB
> class PowerUnit {
>   -type : str
>   -power_rating : int
>   -brand : str
>   +PowerUnit(type : str, power_rating : int, brand : str)
>   +getters_setters_of_all_attributes()
> }
> class Appliance {
>   -power_unit : PowerUnit
>   -colour : str
>   -weight : float
>   -is_on : Boolean
>   +Appliance(power_unit : PowerUnit, colour : str, weight : float, is_on : Boolean)
>   +getters_setters_of_all_attributes()
>   +turn_on()
>   +turn_off()
>   +connect_home_network()
> }
> class WashingMachine {
>   -drum_size : int
>   +WashingMachine(power_unit : PowerUnit, colour : str, weight : float, is_on : Boolean, drum_size:int)
>   +getters_setters_of_all_additional_attributes()
>   +connect_home_network()
> }
> class Refrigerator {
>   -cooling_cap : int
>   +Refrigerator(power_unit : PowerUnit, colour : str, weight : float, is_on : Boolean, cooling_cap:int)
>   +getters_setters_of_all_additional_attributes()
>   +connect_home_network()
> }
> Appliance --> PowerUnit : power_unit
> Appliance <|-- WashingMachine
> Appliance <|-- Refrigerator
> ```

b) Explain what polymorphism is. Circle the polymorphed functions. [2]

> [!Answer]
> **Polymorphism** is the ability of different classes to define the same method
> name but provide different implementations.
> Circle connect_home_network() in the sub classes

**c) Explain what data encapsulation is. Give an example using the example given. [2]**

> [!Answer]
> **Encapsulation** is the practice of restricting direct access to an object’s
> internal data and only allowing it to be accessed or modified through
> controlled methods (getters/setters).
>
> Example: In the Appliance class, the attribute powerUnit could be kept
> private, and the class could provide methods getPowerUnit() and
> setPowerUnit() to safely access or modify it.

---

<a id="toc-searching-algorithms"></a>

# Searching Algorithms

<a id="toc-searching-algorithms-binary-search"></a>

### Binary Search

##### 2025 RVHS Prelim P1 Q4)

**4. In a real-time online car racing game, once a player completes a round, the time taken is sent to the server for ranking purposes.**

**a) Explain why the finishing time records received by the server may not always arrive in strictly increasing order. [1]**

> [!Answer]
> Network delays, jitter or different **packet** routes may cause later times to arrive
> before earlier ones. [different client locations accepted]
> 1

**The server needs to maintain these records in a data structure where search operations based on finishing time are performed very frequently.**

**b) State the advantage of using a sorted array over a sorted linked list in this context. Support your answer with reference to time complexity. [2]**

> [!Answer]
> Array supports **binary search** $O(\log n)$
> **linked list** search is sequential $O(n)$.
> 2

**c) State one disadvantage of using a sorted array over a sorted linked list in this context. [1]**

> [!Answer]
> Insertion into the middle of a sorted array is $O(n)$ (shifting required), but in a
> **linked list** insertion (after locating the position) is $O(1)$.
>
> Not accepting sorted array can only accommodate fixed number of record as
> the number of expected record is known in advance.
> 1`

**In this racing game, the finishing times are generally increasing as players**

**complete their rounds one after another. d) Explain why this makes a sorted array particularly efficient for insertion in this context. [2]**

> [!Answer]
> Since finishing times usually arrive in increasing order, new records are
> appended at the end of the array.
>
> Even if the finishing time records may arrive out of order, the insertion took
> place with minimal shifts since the finishing time is generally of a large value.
> Appending takes $O(1)$ time, so in practice insertion is much faster than the
> **worst-case** $O(n)$.
> 2

**It was later discovered that some finishing time records are being altered during transmission, either accidentally or maliciously. The server must be able to detect such tampering and ensure that each record truly originates from the legitimate player.**

**e) Suggest a method the server can use to verify the authenticity and integrity of each message. [1]**

> [!Answer]
> Use a **digital signature** for each message. 1

f) Explain how this method works. [6]

> [!Answer]
> The client computes a hash digest of the finishing time message.
> The client encrypts the hash with its **private key**  to form the digital
> signature.
> The client sends both the message and the signature to the server.
> The server computes its own hash of the received message.
> The server decrypts the signature using the client’s **public key** to recover
> the original digest.
> The server compares the two digests : if they match → the message is
> authentic and unaltered; if not → it has been tampered with or forged.
> 6

---

<a id="toc-searching-algorithms-hashtable-search"></a>

### HashTable Search

##### 2025 ACJC Prelim P1 Q4)

**4A hash table is implemented inside an array of length 10. The hash table is intended to store the names and ages of people. Each record is to be stored as a tuple (name,age). The hash function is the number of characters in the name. In the event of a collision, a linear search for an empty entry would be carried out starting from the index of the collision, looping back to the start of the array if necessary.**

Copy the following array onto the answer sheet.

[1]

[2]

[3]

**[4] [5] [6] [7] [8] [9] [10] (i) Add the records into the array as they are inserted in the following order. ('Jacky', 22) ('Sam', 18) ('Joel', 20) ('Bob', 21) ('Justin', 19) [5]**

> [!Answer]
>
> * [1][2]
>
> * ('Sam', 18)
>
> * ('Joel', 20)
>
> * ('Jacky', 22)
>
> * ('Bob', 21)
>
> * ('Justin', 19)[8][9]

(ii) Describe how to look up Bob’s age in the hash table. [4]

> [!Answer]
>
> * Hashing 'Bob' gives a value of 3. Go to index 3 at the **hash table** and check the name (first item of the tuple). If it is 'Bob', we return the age (second item of the tuple). If it is not 'Bob', or the entry is empty, we perform a **linear search** through the **hash table** starting form index 3 and looping around to the beginning of the table again if necessary. If we find a tuple whose name is 'Bob', we return the age. (In this case, it is at index 6)If we come back to index 3 without having found such a tuple, then 'Bob' does not exist in the **hash table**.

**Suppose instead that the same records are to be stored in a binary search tree (BST), in order of age. The records are inserted into the BST in the same order as in part (i).**

(iii) Draw the resulting BST. [3]

> [!Answer]
> ('Jacky', 22)('Sam', 18)('Joel', 20)('Bob', 21)('Justin', 19)('Jacky', 22)('Sam', 18)('Joel', 20)('Bob', 21)('Justin', 19)

(iv) List the names in a post-order traversal of the BST. [2]

> [!Answer]
> Justin, Bob, Joel, Sam, Jacky

(v) Explain how you would use the BST to determine who is the second oldest person. [3]

> [!Answer]
> Since the root has no right child, the oldest person is the root. The second oldest person is the oldest person in the left subtree. Starting from the left child of the root, keep going right until you reach a node with no right child (Bob). This is the second oldest person in the entire tree.(If the root has a right child there are two cases. Firstly, keep going right. The oldest person is the rightmost node. If this node does not have a left child, then the second oldest person is the parent of the rightmost node. If this node has a left child, then start from the left child and keep going right until you reach a node with no right child.)

---

##### 2025 RI Prelim P1 Q2)

**2 A large e-commerce company is building its order management system. As millions of customers place, modify, and cancel orders daily, choosing the correct data structures is critical for performance.**

**The system must support the following operations efficiently:**

* **AddOrder(orderID): Adds a new order with a unique orderID**
* **CheckOrderExists(orderID): Checks whether an order exists**
* **GetMostRecentOrder(): Retrieves the latest order placed**
* **GetAllOrdersSorted(): Returns all orders sorted by orderID**

**The development team is considering various data structures:**

* **Unordered List (Array or Linked List)**
* **Hash Table**
* **Binary Search Tree (Self-balancing)**
* **Stack**

**(a) For each operation above, select the most suitable data structure from the list provided (Unordered List, Hash Table, BST, Stack), and justify your choice using Big-O notation. [4]**

> [!Answer]
>
> * AddOrder(orderID): **Hash table**, $O(1)$ average case insertion time
>
> * CheckOrderExists(orderID): **Hash table**, $O(1)$ average case lookup time
>
> * GetMostRecentOrder(): **Stack**, $O(1)$ to access top of **stack**
>
> * GetAllOrdersSorted(): **Binary Search Tree**, $O(n)$ **in-order** traversal returns
>
> sorted list in $O(n)$
>
> AddOrder - Should not be Unordered List even as insert/delete can be  $O(1)$, as
> the system will also need to support CheckOrderExists, which makes **Hash Table**
> more suitable

**(b) Explain why using a linked list to implement CheckOrderExists(orderID) would be inefficient at scale. [2]**

> [!Answer]
> A **linked list** does not support direct access to elements by key.
> To check whether an order exists, the system must traverse the list from start to end,
> resulting in $O(n)$ **time complexity**. This becomes inefficient as the number of orders
> grows.

**(c) The company is considering using a hash table to manage all active orders. Explain why using a hash table is not ideal, and propose a suitable data structure. [3]**

> [!Answer]
> The company wants to display all active orders sorted by orderID or order time on a
> dashboard for warehouse staff.
>
> 1m-Weakness of HT
> **Hash tables** do not maintain any inherent order of keys.
>
> **1m** – Explain the inefficiency
> To retrieve active orders in a sorted order, the system must first extract all values and
> then sort them manually, which adds an extra $O(n\log n)$ operation.
>
> 1m-Proposing suitable alternative
> This reduces efficiency compared to using a data structure that maintains order, such
> as a **binary search tree** or a **priority queue**.

**(d) During a Black Friday sale, the sales volume typically increases dramatically. Certain popular items may have limited stock, so it is important for the system to support a feature that allows merchants to fulfil orders in chronological order. You are tasked with selecting the most appropriate data structure to support this operation. You may choose from the list of data structures provided above, or propose an alternative. Justify your choice clearly. [2]**

> [!Answer]
> Use a **queue** to manage orders. A **queue** naturally supports first-come, first-served
> processing, which matches the requirement to fulfil orders in chronological order.
> Insertion of new orders is $O(1)$ at the rear, and fulfilling orders is $O(1)$ at the front,
> making it efficient even under high sales volumes.
>
> 1m – identify **queue** (FIFO characteristics)
>
> **1m** – Justifies enqueue and dequeue operation efficiency

---

##### 2025 RVHS Prelim P1 Q5)

**5. Hash tables are often described as providing constant-time $O(1)$, search performance.**

**a) State three different reasons why in practical, a hash table cannot always maintain $O(1)$ search time. [3]**

> [!Answer]
>
> 1. Collisions
>
> Different keys may hash to the same index (bucket).  When collisions occur,
> elements must be stored together (e.g., chaining or probing).
> This can degrade search time from $O(1)$ t o $O(n)$ in the worst case if many
> keys collide.
>
> 2. Poor hash function
>    If the hash function does not distribute keys uniformly, certain indices become
>    overloaded. This leads to long chains/clusters at a few positions, making
>    searches slower.
>
> 3. High load factor / table too full
>    As the number of stored elements approaches or exceeds the table’s
>    capacity, collisions increase.
>    Without resizing and rehashing, search time will degrade significantly beyond
>    $O(1)$.
>    3

b) Explain what is meant by collision resolution. [1]

> [!Answer]
> The method is used to handle cases when two or more keys map to the same
> hash value. (Cannot be just specific to linear probe)
> 1

**c) For each of the following situations, state whether open addressing or closed addressing is the preferred collision resolution strategy. i. When the load factor may be greater than 1. ii. When memory is very limited and space efficiency is important. [1]**

> [!Answer]
> i) Closed addressing
>
> ii) Open addressing
> 1

---

##### 2025 TJC Prelim P1 Q1)

**1An ISBN is an International Standard Book Number and is a unique identifier for each book. Each ISBN consists of 13 digits, which is made up of 5 elements with each element being separated by spaces or hyphens. Three of the five elements may be of varying length: Prefix element – currently this can only be either 978 or 979. It is always 3 digits in length Registration group element – this identifies the country, geographical region, or language area participating in the ISBN system. This element may be between 1 and 5 digits in length Registrant element – this identifies the publisher or imprint. This may be up to 7 digits in length Publication element – this identifies the edition and format of a specific title. This may be up to 6 digits in length Check digit – this is always the final single digit that mathematically validates the rest of the number. It is calculated using a Modulus 10 system with alternate weights of 1 and 3. An example of an ISBN with check digit 5 is shown below:**

| 978    | -                 | 92         | -           | 95055       | - | 02 | - | 5 |
| ------ | ----------------- | ---------- | ----------- | ----------- | - | -- | - | - |
| Prefix | Registrationgroup | Registrant | Publication | Check digit |   |    |   |   |

(a) Describe a purpose of the check digit in an ISBN. [2]

> [!Answer]
> Detect common input errors such as transcription error and transposition error which helps to maintain data accuracy in book identification systems

(b) Suggest another suitable validation technique for ISBN. [1]

> [!Answer]
>
> * Length check – check that ISBN consists of 13 digits [OR]
>
> * Format check – check that each of the elements fulfil the criteria specified

**A school library system needs to store and search for information about books using their unique ISBNs. New books are added into the library inventory and damaged or older books are condemned from time to time. The developers propose the use of a hash table to store and retrieve the book records.**

(c) Explain how the library system would use a hash function and a hash table to store and search for books by their ISBNs. [3]

> [!Answer]
> Each ISBN will be processed by the same hash function to generate an index/key, which corresponds to the position in the **hash table** where the book record will be stored. When searching for a book using its ISBN, it uses the same hash function to generate the index/key to locate the record directly.

(d) Give three features of an effective hashing algorithm. [3]

> [!Answer]
>
> * Any of the following 3:
>
> * 1. The function should reduce the chances of different keys producing the same hash (collisions). This avoids clustering and reduces the chance of collisions, which keeps lookup, insert, and delete operations efficient (close to $O(1)$).
>
> * 2. Equal probability of generating the indices or the indices generated are spread evenly across all the full range of the indices of the table. (Uniform Distribution)
>
> * 3. The same input must always produce the same hash value. This ensures that a key can be found reliably each time it is accessed. (Deterministic)
>
> * 4. Quick computation of the hash address.

(e) Explain the meaning of a collision in this context. [2]

> [!Answer]
>
> * A collision occurs when elements in a **hash table** share the same hash value. When this occurs, the book record cannot be stored in that space and an alternative space has to be sought out to store that book record.
>
> * When searching for a book record, and another book record is found, it does not mean that the search item is not in the table. A collision resolution algorithm is used to continue searching for the item at other locations before a conclusion is made.

(f) Describe one method that can be used to handle the consequence of a collision. [2]

> [!Answer]
>
> * **Linear probing** is a method to deal with collision. This is done by probing sequentially the next space or using an interval (e.g. check every 3rd slot) until an empty slot is found.[OR]
>
> * Chaining can also be used to handle the consequence of a collision. In chaining, records are stored in a node of one of the many linked lists. Each array item of the **hash table** will store the address of one **linked list**. Whenever a key of a record gets hashed to an address where another record has already been hashed to, the new record will be added to the end of the list that its hashed address points to.

**Students on an internship with the library ask their developer mentors why the book records, ordered by their ISBNs, were not stored in a linked list instead.**

(g) Describe one disadvantage of storing and searching the records ordered by ISBNs using a linked list. [2]

> [!Answer]
> Locating a book will require traversing through the **linked list** starting from the head of the **linked list**, which is slow process of $O(n)$ time complexityThis affects not just the searching process, but also the insertion and deletion process to maintain the order of the records by ISBN

---

<a id="toc-sorting-algorithms"></a>

# Sorting Algorithms

<a id="toc-sorting-algorithms-insertion"></a>

### Insertion

##### 2025 ASRJC Prelim P1 Q1)

```text
1	Below shows a pseudocode of insertion sort with blanks.
PROCEDURE InsertionSort(A : ARRAY[0 : N - 1] OF INTEGER)// using 0-indexing
FOR i ← ……(1)…… TO ……(2)……        temp ← A[i]        j ← ……(3)……
WHILE j >= 0 AND temp < ……(4)……            ……(5)…… ← A[j]            j ← ……(6)……
ENDWHILE        ……(7)…… ← temp
NEXT i
ENDPROCEDURE

```

(a) Write your answer for each blank (1) through (7) clearly. [3]

> [!Answer]
> (1) 1,  (2) N – 1,  (3) i – 1,  (4) A[j],  (5) A[j + 1],  (6) j – 1,  (7) A[j + 1]

(b) State the worst-case time complexity of insertion sort and briefly explain what that implies. [2]

> [!Answer]
> **Worst-case** **time complexity**: $O(n^2)$
> For large datasets, the number of operations required for insertion sort grows quadratically with input size.

**(c) Insertion sort is effective for small arrays due to its simplicity and low overhead. However, for larger arrays, more efficient algorithms such as merge sort are preferred. Describe how merge sort works and state its time complexity. [3]**

> [!Answer]
> **Merge sort** is a divide-and-conquer algorithm that sorts an array by recursively breaking it down and then combining them in sorted order.
>
> * Divide the array in half repeatedly until each subarray contains only one element.
>
> * Combine adjacent subarrays back together in sorted order. Continue this process until the entire sorted array is constructed.
>
> **Time complexity**: $O(n\log n)$

---

<a id="toc-sorting-algorithms-merge-sort"></a>

### Merge Sort

##### 2025 ACJC Prelim P1 Q5)

**5The pseudo-code for a bubble sort algorithm to sort an array of integers in increasing order is shown below. The indices in the array start from 1.**

```text
01 PROCEDURE BubbleSort(Arr : ARRAY OF INTEGER)
02     DECLARE N, Temp : INTEGERS
03     N ← LENGTH(Arr)
04
05     FOR i ← 1 TO N–1
06         FOR j ← 1 TO N–1
07             IF ... (A) ... THEN
08                 Temp ← Arr[j+1]
09                 Arr[j+1] ← ... (B) ...
10                 Arr[j] ← ... (C) ...
11             ENDIF
12         ENDFOR
13     ENDFOR
14 ENDPROCEDURE

```

(a) Write the correct pseudo-code for (A), (B), (C) in the algorithm above. [3]

> [!Answer]
>
> * (A): Arr[j] > Arr[j+1]
>
> * (B): Arr[j]
>
> * (C): Temp

(b) State two ways in which the time complexity of the algorithm above can be improved. [3]

> [!Answer]
>
> * First way:Line 6: Iterate j from 1 to N-i
>
> * Second way:Introduce flag variable between lines 5 and 6 that changes value if a swap in lines 8-10 happened. If the entire loop for j in line 6 runs without a swap then the list is already sorted. We can then break the loop for i and end the function there.

(c) State the worst-case time-complexity of bubble sort. [1]

> [!Answer]
> $O(n^2)$

**In a merge sort algorithm, a helper function is needed to combine two sorted lists into one sorted list. The pseudo-code for the helper function is given below. The indices in both arrays start from 1.**

```text
01 FUNCTION Combine(Arr1, Arr2 : ARRAYS OF INTEGER)
02     DECLARE N1, N2, i, j : INTEGERS
03     N1 ← LENGTH(Arr1), N2 ← LENGTH(Arr2)
04     i ← 1, j ← 1
05
06     DECLARE Arr[1:(N1 + N2)] : ARRAY OF INTEGER
07
08     WHILE ... (D) ...
09         IF ... (E) ... THEN
10              Arr[i+j-1] ← Arr1[i]
11              i ← i+1
12         ELSE
13              Arr[i+j-1] ← Arr2[j]
14              j ← j+1
15         ENDIF
16     ENDWHILE
17
18     WHILE i+j-1 <= N1 + N2
19         IF ... (F) ... THEN
20              Arr[i+j-1] ← Arr1[i]
21              i ← i+1
22         ELSE
23              Arr[i+j-1] ← Arr2[j]
24              j ← j+1
25         ENDIF
26     ENDWHILE
27
28     RETURN Arr
29 ENDFUNCTION

```

(d) Write the correct pseudo-code for (D), (E), (F) in the algorithm above. [3]

> [!Answer]
>
> * (D): i <= N1 AND j <= N2(E): Arr1[i] < Arr2[j]
>
> * (F): i <= N1 (alternatively, j > N2)

**(e) Write a function to perform merge sort, using the helper function above, in pseudo-code. [4]**

> [!Answer]
>
> ```text
> 5(e)
>
> ```

---

##### 2025 DHS Prelim P1 Q5)

**5 Merge Sort and Insertion Sort are two distinct sorting algorithms with different performance characteristics, particularly evident when analyzed using Big-O notation.**

**With selected dataset sizes (29, 210, 211, 213, 214, 215) comparing these two sorts in terms of worst-case time complexity for large datasets. [6]**

> [!Answer]
> For Merge sort, $O(N\log_2 N)$ in all cases (best, average, and worst).  This is because Merge Sort
> consistently divides the array into halves and then merges them, leading to a logarithmic number of levels
> of **recursion** and linear time for merging at each level.     (1)
> For Insertion sort, Worst Case:  $O(N^2)$ when the array is sorted in reverse order, requiring many
> comparisons and shifts for each element.       (1)
> **Merge Sort**'s **$O(N\log N)$** **time complexity** makes it significantly more efficient than **Insertion Sort**'s O(N 2)
> for large datasets.  The quadratic growth of Insertion Sort's time complexity means its performance
> deteriorates rapidly as the input size increases.      (2)

---

##### 2025 TJC Prelim P1 Q2)

**2A program implements a Merge Sort algorithm to order values into ascending order. The contents of an array are shown: 12 10 5 1 24 9 6**

**(a) Explain how the Merge Sort algorithm sorts the data in the array into ascending order. [3]**

> [!Answer]
> (a)Explain how a **Merge Sort** algorithm will sort the data in the array into ascending order.
> Divide the array into 2 smaller subarrays, repeat this step on each of the smaller subarrays  until each subarray has only one element Merge the subarrays back together in the correct (sorted) order. llustrate using the array given

(b) Using Big-O notation, state the worst-case time complexity of Merge Sort. [1]

> [!Answer]
> $O(n\log n)$

**(c)The Merge Sort algorithm uses recursion.**

(i) State three features of a successful recursive function. [3]

> [!Answer]
> A recursive algorithm must call itself, recursively.Has a **base case** or terminating condition where the function stops calling itselfA recursive algorithm must change its state and move toward the **base case**

(ii) State the purpose of the given pseudocode function:

```text
FUNCTION iterative (string1)
left = 1
right = LENGTH(string1)
WHILE left < right
IF string1[left] <> string1[right]
RETURN FALSE
END IF
left = left + 1
right = right - 1
END
WHILE
RETURN TRUE
END
FUNCTION

```

[1]

> [!Answer]
> This function checks whether string1 is a palindrome.

(iii) Rewrite the pseudocode function in (c)(ii) using recursion. [3]

> [!Answer]
>
> ```text
> FUNCTION recursive(string1)
> IF LENGTH(string1) <= 1   //Base case
> RETURN TRUE    END
> IF
> IF string1[1] <> string1[LENGTH(string1)]
> RETURN FALSE    END
> IF// SUBSTRING(string1, 2, LENGTH(string1) – 2) returns // the substring of string1 excluding 1st and last character
> RETURN recursive(SUBSTRING(string1, 2, LENGTH(string1) - 2)) END FUNCTIONNote: You may also use MID(string1, 2, LENGTH(string1) - 2) to return a substring of length LENGTH(string1) – 2 starting at position 2
>
> ```

---

<a id="toc-stacks"></a>

# Stacks

<a id="toc-stacks-core-operations"></a>

### Core Operations

##### 2025 DHS Prelim P1 Q3)

**3 Details of errors generated in a program are stored in a stack.**

**Details of each error are stored in the object of class structure namely Error.**

(a) State which error will be the first retrieved from the stack. [1]

> [!Answer]
> The last one in // most recent

**(b) The stack is implemented as a 1D array with the identifier ErrorArray.**

**The pointer LastItem stores the position of the last error in the array. Pointer will set to -1 initially.**

**(i) The function, AddItemToStack, takes the next error, the array, and pointer as parameters. If the stack is full, the function returns FALSE; otherwise, it adds the error to the stack, changes the pointer’s value and returns TRUE. Copy and complete the following pseudocode for the function AddItemToStack. [4]**

```text
FUNCTION AddItemToStack(BYREF ErrorArray : ARRAY[0 : 99] OF Error,
                  BYREF LastItem : INTEGER,
 BYVALUE Error1 : Error) RETURNS BOOLEAN
IF LastItem = ..............................................
   THEN
RETURN ...............................................
ELSE
ErrorArray[LastItem + 1] ← ...........................
LastItem ← ...........................................
RETURN ...............................................
ENDIF
ENDFUNCTION

```

> [!Answer]
> 1 for each other completed statement
>
> ```text
>  IF LastItem = 99 // ErrorArray.Length - 1
>     RETURN FALSE
>     ErrorArray[LastItem + 1] ← Error1
>     LastItem ← LastItem + 1
>     RETURN TRUE
>
> ```

**(ii) Explain the reasons why ErrorArray and LastItem are passed by reference, but Error1 is passed by value. [3]**

6

> [!Answer]
>
> * The function needs to change the values in ErrorArray and/or LastItem in main/where called
>
> * … otherwise  they would not be changed outside of the function // otherwise changes would only
>
> stay in the function
>
> * Error1's value does not change in the function // no changes to Error1's value need reflecting
>
> where it was called / to the original
>
> * BYVALUE stops the value being changed outside the function, but BYREF changes the value where
>
> called from

**(iii) The function RemoveItem takes the next error from the stack and returns it. If there are no errors in the stack, it returns the global object NullError. Copy and complete the pseudocode algorithm RemoveItem. [3]**

```text
FUNCTION RemoveItem(BYREF ErrorArray : ARRAY[0 : 99] OF Error,
  BYREF LastItem : INTEGER) RETURNS Error
DECLARE ItemToRemove : Error
IF ...............................................
THEN
RETURN .............................................
ELSE
ItemToRemove ← ErrorArray[.........................]
LastItem ← LastItem - 1
RETURN .............................................
ENDIF
ENDFUNCTION

```

> [!Answer]
>
> ```text
> FUNCTION RemoveItem(ByRef ErrorArray : ARRAY[0:99] OF Error,
>              ByRef LastItem : INTEGER) RETURNS Error
>  IF LastItem < 0 / = -1
>    RETURN NullError
>    ItemToRemove ← ErrorArray[LastItem]
>    RETURN ItemToRemove
>
> ```

(iv) The errors that have been processed are stored in a global queue, ErrorComplete.

The function Enqueue adds an error to ErrorComplete:

Enqueue(ErrorToAdd)

* Enqueue() returns TRUE if the error is successfully added to the queue and
  returns FALSE if the queue is full.
  The procedure RunError() should:

* remove an error from the stack using the function RemoveItem()

* output message "Stack empty" if there are no errors in the stack

* if an error is returned, add the error to the queue using the function Enqueue()

* if the error is added to the queue, output the message "Item added to
  queue"

* if the error is not added to the queue, output the message "Item not added
  to queue".

Copy and complete the pseudocode procedure RunError(). [5]

```text
PROCEDURE RunError(BYREF ErrorComplete : ARRAY[0 : 99] OF Error,

```

BYREF ErrorArray : ARRAY[0 : 99] OF Error,
BYREF LastItem : INTEGER)

:::

```text
ENDPROCEDURE

```

7

> [!Answer]
> Enqueue() returns TRUE if the error is successfully added to the **queue** and returns FALSE if
> the **queue** is full.
>
> * output message "**Stack** empty" if there were no errors in the **stack**
>
> * if the error is added to the **queue**, output message "Item added to **queue**
>
> * if the error is not added to the **queue**, output message "Item not added to **queue**".
>
> * Using RemoveItem(ErrorArray, LastItem) and storing return value …
>
> * …checking if return value is NullError and outputting "**stack** empty" message if it is null
>
> * … (if not NullError), calling Enqueue with return value …
>
> * … if return value is TRUE, output "added to **queue**" message …
>
> * … if return value is FALSE output "not added to **queue**" message
>
> ```text
> PROCEDURE RunError(BYREF ErrorComplete : ARRAY[0:99] OF Error,
>              BYREF ErrorArray : ARRAY[0:99] OF Error,
>  DECLARE DataItem : error
>  DataItem ← RemoveItem(ErrorArray, LastItem)
>  IF DataItem = NullError THEN
>     OUTPUT "Stack empty"
>    IF Enqueue(DataItem) = True THEN
>       OUTPUT "Item added to queue"
>      OUTPUT "Item not added to queue"
>
> ```

**(c) The stack can be implemented as a linked list with 2D arrays ErrorArray with eight (8) nodes. The first column stores Error objects, the second column stores pointer to next object. Pointers should initialize to -1.**

**Identifiers ErrorListHead, FreeSpaceListHead are used as the linked list head and free space list head respectively.**

**(i) Copy the following diagram and complete the linked list with ErrorListHead and FreeSpaceListHead and other relevant variables. The first five nodes were inserted with the following errors: 304-XX, 208-XY, 301-AB, 411-PX, 709-ZA [5]**

index
ErrorArray

1
2
3
4
5
6
7
8

> [!Answer]
> The **stack** can be implemented as a **linked list** with 2D arrays ErrorArray with eight (8) nodes.
>
> * The first column stores Error objects, the second column stores pointer to next object.  Pointers
>
> should initialize to -1.
>
> Identifiers ErrorListHead, FreeSpaceListHead are used as the **linked list** head and free
> space list head respectively.
>
> FreeSpaceListHead and other relevant variables. The first five nodes were inserted with
> the following errors:
>
> LastItem 5 (1)  ErrorArray
> ErrorListHead 1 (1) 1 304-XX 2
>
> * 2 208-XY 3
>
> * 3 301-AB 4
>
> * 4 411-PX 5
>
> * 5 709-ZA -1 (1)
>
> FreeSpaceListHead 6(1) 6  7
>
> * 7  8
>
> * 8  -1 (1)

**(ii) Show the changes with another diagram of the linked list after an error removed from the stack. [4]**

> [!Answer]
> Show the changes with another diagram of the **linked list** after an error removed from the
> **stack**.
> LastItem 4 (1)
>
> * index ErrorArray
>
> ErrorListHead 1  1 304-XX 2
>
> * 2 208-XY 3
>
> * 3 301-AB 4
>
> * 4 411-PX -1 (1)
>
> * 5 709-ZA -1 (1)
>
> FreeSpaceListHead 6 6  7
>
> * 7  8
>
> * 8  5 (1)

(iii) Explain what the free space list is? [2]

> [!Answer]
> It is a **linked list** data structure specifically designed to keep track of unallocated or "free" blocks of
> array element or memory space.         (2)

---

##### 2025 RI Prelim P1 Q4)

**4 The function EvaluatePostfix is designed to evaluate a postfix arithmetic expression at runtime. The expression is stored as a queue of tokens (either integers or operators) from left to right.**

**For example, the postfix expression 5 2 - 3 * is stored as the queue [5, 2, '-', 3, '*'],**

which corresponds to the infix expression (5 - 2) * 3.

The pseudocode is given below:

```text
01 FUNCTION EvaluatePostfix(Tokens : QUEUE) RETURNS INTEGER
02     DECLARE Stack AS EMPTY STACK
03     REPEAT
04         Token ← DEQUEUE Tokens
05         IF Token IS INTEGER THEN
06             PUSH Token TO Stack
07         ELSE
08             A ← POP Stack
09             B ← POP Stack
10             IF Token = '+' THEN
11                 PUSH (B + A) TO Stack
12             ELSE IF Token = '-' THEN
13                 PUSH (B - A) TO Stack
14             ELSE IF Token = '*' THEN
15                 PUSH (B * A) TO Stack
16             ELSE IF Token = '/' THEN
17                 PUSH (B DIV A) TO Stack
18             ENDIF
19         ENDIF
20     UNTIL Tokens IS EMPTY
21     RETURN POP Stack
22 END
FUNCTION

```

(a) Copy and complete the trace table given to determine the output of EvaluatePostfix when

```text
Tokens = [4, 5, 6, '*', '+', 2, '-'].

```

**Token Action Stack Contents 4 Push 4 [4] 5 Push 5 [5, 4] [4]**

> [!Answer]
>
> | Token | Action                               | Stack (Top → Bottom) |
> | ----- | ------------------------------------ | -------------------- |
> | 4     | Push 4                               | 4                    |
> | 5     | Push 5                               | 5, 4                 |
> | 6     | Push 6                               | 6, 5, 4              |
> | *     | Pop 6 and 5 → 5 * 6 = 30 → Push 30   | 30, 4                |
> | +     | Pop 30 and 4 → 4 + 30 = 34 → Push 34 | 34                   |
> | 2     | Push 2                               | 2, 34                |
> | -     | Pop 2 and 34 → 34 - 2 = 32 → Push 32 | 32                   |
>
> 32
>
> * Correctly showing the first three pushes (4, 5, 6) onto the **stack**.
>
> * Correctly handling the first operator * (pop 6 and 5, compute 30, push
>
> result).
>
> * Correctly handling the + operator (pop 30 and 4, compute 34, push result).
>
> * Correctly handling the final two tokens (2 and -) and reaching the final
>
> answer 32.

**(b) Explain why it is important to POP operand A before operand B, as shown in lines 8 and 9. [1]**

> [!Answer]
> Operands must be popped in reverse order: first A, then B, so the operation is
> performed as B op A, with B as the first operand and A being the second operand.
> If reversed, A op B would yield incorrect results, especially for non-commutative
> operations like subtraction and division.

**(c) Add code to the pseudocode so that it can also handle exponentiation (^). Indicate between which lines this code should be inserted. [3]**

> [!Answer]
> Modified lines (only change needed is adding another ELSE IF block):
>
> ```text
> 18     ELSE IF Token = '^' THEN
> 19         PUSH (B ^ A) TO Stack
>
> ```
>
> * Identifies correct position for insertion (between line 17
>
> and line 18).
>
> * Correct conditional test (Token = '^').
>
> * Correct push statement showing B ^ A.

**(d) Identify one possible runtime error that could occur in the code above. Describe how it may happen, and explain necessary changes to the code to prevent it. [4]**

> [!Answer]
> A **stack** underflow error may occur when the function attempts to POP from an
> empty **stack**, or when there are fewer than 2 items in the **stack** before an operator
> is processed.
> It happens when the postfix expression is invalid or malformed, such as:
>
> ```text
> Tokens = [3, "+"]
>
> ```
>
> Pushed '3' into the **stack**, reads '+', attempts to pop twice - but **stack** only have one
> single item, which will cause a **stack** underflow error
>
> ```sql
> Insert a condition before popping to verify that the stack has at least 2 items:
> 08             IF Stack.LENGTH < 2 THEN
> 09                 OUTPUT "Error: Not enough operands"
> 10                 RETURN -1
> 11             ENDIF
> 12             A ← POP Stack
> 13             B ← POP Stack
>
> ```
>
> 1. Correctly identifies the runtime
>    error as a **stack** underflow 1
> 2. Explains how it could happen,
>    e.g., processing an operator when the
>    **stack** has < 2 items 1
> 3. Proposes a valid safeguard, e.g.,
>    check **Stack**.LENGTH < 2 1
> 4. Shows correct placement or logic
>    of the safeguard in the code 1

---

<a id="toc-queues"></a>

# Queues

<a id="toc-queues-circular-queue"></a>

### Circular Queue

##### 2025 TJC Prelim P1 Q4)

**4A software company is developing a print server that handles print jobs from multiple users. Each print job has a job ID and the number of pages. The print server manages the print jobs with a linear queue.**

Explain why a linear queue would be appropriate for regular print jobs.[2]

> [!Answer]
>
> * Definition of **queue** as FIFO structure Explanation of appropriateness for print jobs (order preservation)A **queue** is a First-In-First-Out (FIFO) data structure where elements are added at one end (rear) and removed from the other end (front).
>
> * This is appropriate for print jobs as it ensures jobs are processed in the order they were submitted (effectively manage multiple print jobs without the risk of mixing them up), maintaining fairness in the printing system.

**The company decides to implement the print queue as a circular queue using a static array of size 5.**

Explain one advantage and one disadvantage of using a circular queue instead of a linear queue for this situation, where both queues are implemented using a static array of the same size.[4]

> [!Answer]
> Valid advantageSufficient explanation in the contextA linear **queue** stores print jobs sequentially and can become inefficient when it reaches capacity, as it cannot accept new print job until all the print jobs have been processed, potentially wasting space. In contrast, a **circular queue** wraps around and efficiently utilizes space by allowing a new print job to be added at the front if there is space due to dequeued job, thereby preventing wasted positions.
>
> * Valid disadvantage Sufficient explanation in the context A **circular queue** has a more complex implementation logic that requires additional calculations to handle the wraparound of the rear pointer and to determine when the **queue** is full.
>
> * For example, when adding a new print job, the program needs to check if (rear + 1) mod size equals front to determine if the **queue** is full, rather than simply checking if rear has reached the end of the array as in a linear **queue**. This increased complexity makes the code more difficult to maintain and debug if issues arise with the print job system.

**Draw a diagram showing the state of a circular queue after the following operations, showing the positions of front and rear pointers: Enqueue jobs: 101, 102, 103, 104 Dequeue two jobs Enqueue jobs: 105, 106 [3]**

> [!Answer]
> Correct array representation and element placementCorrect front pointer position (index 2)Correct rear pointer position (index 0)[106] [ ] [103] [104] [105]                ^Front (at index 2)[106] [ ] [103] [104] [105]   ^Rear (at index 0)

**The print server keeps a history of completed print jobs in a stack data structure.**

Explain how a stack data structure would be appropriate for implementing a "restore" feature that allows the system administrator to restore recently completed print jobs back to the queue.[2]

> [!Answer]
> Explanation of **stack**'s LIFO nature being suitable for restore/historyClear connection to how this benefits system administrator's restore operationsA **stack** is appropriate for implementing an undo feature because its Last-In-First-Out (LIFO) structure naturally matches the way undo operations work. When a print job is completed, it is pushed onto the **stack**, allowing the most recently completed job to be easily accessed and restored first. This means that if the system administrator decides to undo the last completed job, they can simply pop it from the **stack** and restore it back to the print **queue**. This matches the typical user expectation that undo operations will reverse the most recent actions.

Write pseudocode for a procedure restoreJobs that takes three parameters: the history stack, the print queue and an integer N. The function should restore the N most recently completed jobs from the history stack back to the print queue, maintaining their original print order.[6]

> [!Answer]
>
> ```text
> PROCEDURE restoreJobs(historyStack : STACK, printQueue : QUEUE, N : INTEGER)     // Declare temporary storage to maintain order
> DECLARE tempStack : STACK
> DECLARE count : INTEGER        count ← 0        // Check if N is valid
> IF N <= 0 THEN
> RETURN
> ENDIF        // Move up to N jobs to temporary stack to reverse order
> WHILE NOT historyStack.isEmpty() AND count < N        tempStack.push(historyStack.pop())        count ← count + 1
> ENDWHILE        // Move jobs from temporary stack to queue to restore original order
> WHILE NOT tempStack.isEmpty()        printQueue.enqueue(tempStack.pop())    ENDWHILE
> ENDPROCEDURE
>
> ```

---

##### 2025 VJC Prelim P1 Q2)

**A software company is developing a print server that handles print jobs from multiple users. Each print job has a job ID and number of pages. The system needs to handle both regular and priority print jobs. The regular print jobs use a linear queue data structure.**

Explain why a linear queue would be appropriate for regular print jobs.[2]

> [!Answer]
>
> * Definition of **queue** as FIFO structure
>
> * Explanation of appropriateness for print jobs (order preservation)
>
> * A **queue** is a First-In-First-Out (FIFO) data structure where elements are added at one end (rear) and removed from the other end (front).This is appropriate for print jobs as it ensures jobs are processed in the order they were submitted (effectively manage multiple print jobs without the risk of mixing them up), maintaining fairness in the printing system.

**The company decides to implement the queue as a circular queue.**

State one difference between a linear queue and a circular queue.[2]

> [!Answer]
>
> * Once a linear **queue** is full, no more print jobs can be added until all the queued jobs have been processed.
>
> * With a **circular queue**, print jobs can be added in positions from which the print job has been processed.
>
> * A linear **queue** stores print jobs sequentially and can become inefficient when it reaches capacity, as it cannot accept new print job until all the print jobs have been processed, potentially wasting space. In contrast, a **circular queue** wraps around and efficiently utilizes space by allowing a new print job to be added at the front if there is space due to dequeued job, thereby preventing wasted positions.

**The circular queue is implemented as a static array of size 5.**

**Draw a diagram showing the state of a circular queue after the following operations, showing the positions of front and rear pointers: Enqueue jobs: 101, 102, 103, 104 Dequeue two jobs Enqueue jobs: 105, 106 [3]**

> [!Answer]
>
> * Correct element placement
>
> * Correct front pointer position
>
> * Correct rear pointer position [1][106] [ ] [103] [104] [105]                ^Front (at index 2)[106] [ ] [103] [104] [105]   ^Rear (at index 0 or index 1 if rear is pointing to next available slot)

Explain one disadvantage of using a circular queue instead of a linear queue.[2]

> [!Answer]
>
> * Valid disadvantage
>
> * Sufficient explanation in the context
>
> * A **circular queue** has a more complex implementation logic that requires additional calculations to handle the wraparound of the rear pointer and to determine when the **queue** is full.
>
> * For example, when adding a new print job, the program needs to check if (rear + 1) mod size equals front to determine if the **queue** is full, rather than simply checking if rear has reached the end of the array as in a linear **queue**. This increased complexity makes the code more difficult to maintain and debug if issues arise with the print job system.

**The print server keeps a history of completed print jobs in a stack data structure.**

Explain how a stack data structure would be appropriate for implementing an "undo" feature that allows the system administrator to restore recently completed print jobs back to the queue.[2]

> [!Answer]
>
> * Explanation of **stack**'s LIFO nature being suitable for undo/history
>
> * Clear connection to how this benefits system administrator's restore operations
>
> * A **stack** is appropriate for implementing an undo feature because its Last-In-First-Out (LIFO) structure naturally matches the way undo operations work. When a print job is completed, it is pushed onto the **stack**, allowing the most recently completed job to be easily accessed and restored first. This means that if the system administrator decides to undo the last completed job, they can simply pop it from the **stack** and restore it back to the print **queue**. This matches the typical user expectation that undo operations will reverse the most recent actions.

Write pseudocode for a procedure restoreJobs that takes three parameters: the stack object, historyStack, the queue object, printQueue and an integer N. The pseudocode should restore the N most recently completed jobs from the historyStack back to the printQueue, maintaining their original print order.[6]

> [!Answer]
>
> ```text
> Correct procedure header with parameters [1]Appropriate use of temporary storage to maintain order [1]Correct loop to handle N items [1]Proper stack operation (pop from history) [1]Proper stack operation (push to temp) [1]Proper queue operations to preserve original print order (pop from temp and enqueue to queue) [1]
> PROCEDURE restoreJobs(historyStack : STACK, printQueue : QUEUE, N : INTEGER)     // Declare temporary storage to maintain order
> DECLARE tempStack : STACK
> DECLARE count : INTEGER        count ← 0        // Check if N is valid
> IF N <= 0 THEN
> RETURN
> ENDIF        // Move up to N jobs to temporary stack to reverse order
> WHILE NOT historyStack.isEmpty() AND count < N        tempStack.push(historyStack.pop())        count ← count + 1
> ENDWHILE        // Move jobs from temporary stack to queue to restore original order
> WHILE NOT tempStack.isEmpty()        printQueue.enqueue(tempStack.pop())    ENDWHILE
> ENDPROCEDURE
>
> ```

---

<a id="toc-linked-lists"></a>

# Linked Lists

<a id="toc-linked-lists-definition"></a>

### Definition

##### 2025 YIJC Prelim P1 Q2)

**A programmer is tasked to design a database to store a large dataset, and he needs to choose between using a fixed-sized array and a linked list data structure.**

If the programmer chooses to use a fixed-sized array, state one advantage and one disadvantage of this choice in terms of memory allocation.[2]

> [!Answer]
>
> * Fixed-Sized Array (Advantage and Disadvantage)
>
> * Advantage :Contiguous memory allocation / More efficient use of memory due to less overhead (no pointers stored).

If the programmer chooses to use a singly-linked list, state one advantage and one disadvantage of this choice in terms of memory allocation.[2]

> [!Answer]
>
> * Singly-**Linked List** (Advantage and Disadvantage)
>
> * Advantage :**Dynamic memory** allocation / Memory is allocated only as needed for new elements.

---

<a id="toc-linked-lists-ordered-insertion"></a>

### Ordered Insertion

##### 2025 YIJC Prelim P1 Q3)

**A software team is building a robust sorting utility. A junior developer suggests using Quicksort because of its faster average-case performance. However, the data to be sorted is stored in a linked list.**

As the senior developer, state and explain two reasons why Merge Sort is a more efficient choice than Quicksort for sorting data in a linked list.[4]

> [!Answer]
>
> * Quicksort's poor performance on linked lists is due to its need for random access. the partition step, which involves frequently accessing elements at opposite ends of the list and swapping them, is highly inefficient with sequential access. This leads to a **worst-case** **time complexity** of $O(n^2)$.
>
> * **Merge Sort**'s excellent performance on linked lists is due to its sequential data access pattern. both the splitting (traversing to find the mid-point) and merging phases naturally use sequential access, which is the fundamental strength of linked lists. the merge step can be done in-place by merely re-linking nodes, without the need for the auxiliary arrays often associated with the array version.

**You are given two sorted singly-linked lists, and a third empty list. The first linked list, pointed to by root1, contains the nodes with values 2, 6, 8, and 9, in that order, with the next pointer of each node connected to the following node, and the last node pointing to None to indicate the end of the list. root1 → [2] → [6] → [8] → [9] → None The second linked list, pointed to by root2, contains the nodes with values 3, 5, and 7, in that order. root2 → [3] → [5] → [7] → None The third linked list, pointed to by root3, is empty, as illustrated below: root3 → None You are required to merge the two sorted linked lists in-place into the empty linked list pointed to by root3 such that the values of its nodes are arranged in ascending order. You are to merge the lists in-place and should not create any new nodes.**

**Describe clearly, step-by-step, the process of adding the very first node to the empty linked list pointed to by root3. . You may assume that the following methods are available for each node: get_data(): to obtain the value stored in a node, and get_next(): to obtain the next node being pointed to. [4]**

> [!Answer]
>
> * Describe the process of adding the very first node to root3.
>
> * For identifying the need to compare the data of the first nodes of both input lists (root1.get_data() and root2.get_data()).
>
> * For correctly selecting the node with the smaller value (in this case, the node with value 2 from root1).
>
> * For explaining how to remove the chosen node from its original list. This is done by advancing the root1 pointer to its next node (root1 = root1.get_next()).
>
> * For explaining how to insert the chosen node into the empty root3 list. This is done by setting the chosen node's next pointer to None and then pointing root3 to this node.

After successfully adding the first node to the linked list pointed to by root3, describe clearly the subsequent algorithm to continue merging the remaining nodes from the two sorted lists.[4]

> [!Answer]
>
> * Describe the subsequent algorithm to add the remaining nodes.
>
> * For introducing a current pointer (or equivalent) that tracks the last node in the growing root3 list. This is crucial for efficiently appending new nodes.
>
> * For describing the main loop logic.it continues while both root1 and root2 are not None.compare the current nodes of each list, take the smaller one, and update the pointers of the current pointer and the respective source list pointer (root1 or root2).
>
> * For describing the final step: after the loop terminates (when one list is exhausted), the next pointer of the current node is set to the head of the non-empty list, as all remaining nodes there are already sorted and simply need to be appended.

Draw the final state of all three linked lists after the merging is completed.[2]

> [!Answer]
>
> * Draw the final state of all three linked lists.
>
> * For correctly drawing the complete, merged root3 list in the exact order: 2 -> 3 -> 5 -> 6 -> 7 -> 8 -> 9 -> None.
>
> * For correctly showing that the original root1 and root2 lists are now empty (i.e., root1 -> None and root2 -> None). This demonstrates an understanding that the merge was performed "in-place" by moving nodes rather than copying them.

---

<a id="toc-trees"></a>

# Trees

<a id="toc-trees-binary-search-tree-bst-creation"></a>

### Binary Search Tree (BST) Creation

##### 2025 RVHS Prelim P1 Q2)

**2. The following pseudocode performs an operation on a Binary Search Tree (BST). The parameter root refers to the root node of the BST, and Stack is a dynamic data structure implemented using linked nodes.**

```text
01  FUNCTION foo(root):
02      stack ← Stack()
03      current ← root
04
05      WHILE current <> NULL OR NOT stack.isEmpty():
06          WHILE current <> NULL:
07              stack.push(current)
08              current ← current.left
09
10          current ← stack.pop()
11          OUTPUT current.data
12          current ← current.right

```

**13**
**14 END FUNCTION**

a) Draw a flow chart for the pseudocode above. [5]

> [!Answer]
> 5
>
> Start
>
> ```text
> stack ← Stack()
> current ← root
>
> ```
>
> Current <> NULL
> OR NOT
> **stack**.isEmpty()?
> current
> <> NULL?
> **stack**.push(current)
>
> ```text
> current ← current.left
> current ← stack.pop()
> OUTPUT current.data
> current ← current.right
>
> ```
>
> END
> Y
> N
> Y
> N
> *root is the root of node of the
> BST
>
> ```mermaid
> flowchart TD
>   A([Start]) --> B["stack ← Stack()<br/>current ← root"]
>   B --> C{"Current <> NULL<br/>OR NOT stack.isEmpty()?"}
>   C -- "N" --> Z([END])
>   C -- "Y" --> D{"current <> NULL?"}
>   D -- "Y" --> E["stack.push(current)<br/>current ← current.left"]
>   E --> D
>   D -- "N" --> F["current ← stack.pop()<br/>OUTPUT current.data<br/>current ← current.right"]
>   F --> C
>
> ```

b) State the purpose of foo(root). [1]

> [!Answer]
> Output BST nodes data In order 1

c) Identify the exact line where dynamic memory allocation occurs. [1]

> [!Answer]
> 07 1

**A BST with root as the root of the tree is as follows.**

**d) Draw a trace table to trace the current, stack and the OUTPUT when foo(root) is called. [4]**

4
3
9
7

3

> [!Answer]
> line current **stack** OUTPUT
> 03 4 empty
> 07 4 [4
> 08 3
> 07 3 [4,3
> 08 None
> 10 3 [4
> 11   3
> 12 None
> 10 4 empty
> 11   4
> 12 9
> 07  [9
> 08 7
> 07  [9, 7
> 08 None
> 10 7 [9
> 11   7
> 12 None
> 10 9 empty
> 11   9
> 12 None

**e) The following numbers are inserted in the above BST in the same order as shown below: 20, 15, 6, 25 Draw the BST after these numbers are inserted. [2]**

> [!Answer]
>
> * 3                    9
>
> * 7            20
>
> * 6         15         25
>
> 2

f) State the pre-order and post-order of the BST. [2]

> [!Answer]
> **Pre-order**: 4, 3, 9, 7, 6, 20, 15, 25
> **Post-order**: 3, 6, 7, 15, 25, 20, 9 , 4
> 2

---

<a id="toc-trees-binary-search-tree-bst-search"></a>

### Binary Search Tree (BST) Search

##### 2025 ASRJC Prelim P1 Q4)

**4 You are given the following sequence of words (which represent different generative AI platforms): perplexity, claude, gemini, deepseek, chatgpt, copilot, qwen, ernie**

**(a) These words are inserted one by one into an empty binary search tree (BST) in the given order, with nodes arranged based on lexicographical (alphabetical) order. Draw the complete BST after insertion. [2]**

(b) List the nodes visited in pre-order and post-order traversals. [2]

> [!Answer]
> **pre-order**: perplexity, claude, chatgpt, gemini, deepseek, copilot, ernie, qwen
>
> * **post-order**: chatgpt, copilot, ernie, deepseek, gemini, claude, qwen, perplexity

(c) What property does the in-order traversal have for the BST? [1]

> [!Answer]
> **in-order** traversal of a BST produces nodes in sorted alphabetical order.

**(d) If we replace the word ‘perplexity’ with ‘grok’ in the insertion sequence while maintaining the same order of insertions, will the resulting BST structure be different? Explain your reasoning without reconstructing the BST. [2]**

> [!Answer]
> No, the BST structure will not be different. Replacing ‘perplexity’ with ‘grok’ maintains the same relative lexicographical ordering with respect to other words. All words on the left subtree of ‘perplexity’ are still lexicographically smaller than ‘grok’, and all words on the right subtree are larger than ‘grok’. Therefore, no changes in the final tree structure will result.

(e) Write, in pseudocode, a recursive function Search(root, target) to perform a binary tree search for the value target. It should return a boolean indicating whether the target value is present in the tree. [4]

> [!Answer]
>
> ```text
> FUNCTION Search(root, target) RETURNS BOOLEAN    // Base case (empty tree or reached end)
> IF root = NULL THEN
> RETURN FALSE
> ENDIF     // Found target
> IF root.data = target THEN
> RETURN TRUE
> ENDIF
> IF target < root.data THEN        // search left
> RETURN Search(root.left, target)
> ELSE        // search right
> RETURN Search(root.right, target)    ENDIF
> ENDFUNCTION
>
> ```

(f) Write, in pseudocode, a recursive function CountNodes(root) that returns the total number of nodes present in the BST. [3]

> [!Answer]
>
> ```text
> FUNCTION CountNodes(root) RETURNS INTEGER    // Base case (empty tree)
> IF root = NULL THEN
> RETURN 0
> ENDIF    // Count nodes in subtrees    leftCount ← CountNodes(root.left)    rightCount ← CountNodes(root.right)
> RETURN 1 + leftCount + rightCountENDFUNCTION
>
> ```

(g) For the case where many words need to be stored, explain the advantage of using a binary search tree compared to a sorted linked list. [2]

> [!Answer]
> Significantly faster search (or insertion) operations: For BST, **time complexity** is $O(\log n)$ on average for word lookup. This is because through one comparison at a node, you can eliminate half the remaining search space.
> For a sorted linked list, it requires $O(n)$ time complexity as it requires sequential traversal starting from the head. This difference is significant for large word collections.

---

<a id="toc-data-management"></a>

# Data Management

<a id="toc-data-management-backup"></a>

### Backup

##### 2025 NYJC Prelim P1 Q3)

**3 A company, ImageMaps, wishes to develop an application that scans a user ’s device for photographs, detect the associated location, and display the images on a map using the associated locations.**

**(a) State the actions ImageMaps must take to secure critical business data against catastrophic hardware failure. [4]**

> [!Answer]
> 3.0	Applications, Data Security
>
> Backups of critical data must be made
>
> * Backups should be made regularly
>
> * Multiple copies should be made and stored offsite / in different locations, to minimise risk of complete data loss
>
> * The backups should be tested to ensure that data recovery can succeed

(b) State the consequences, should ImageMaps suffer such a hardware failure. [2]

> [!Answer]
> Catastrophic failure resulting in data loss can mean loss of business continuity (business is unable to operate), loss of revenue, loss of customer / stakeholder trust, etc
> Failure to protect critical data, especially financial records or customer **personal data**, may be a violation of data protection laws and other legal requirements

**(c) ImageMaps needs to store a large quantity of data that will not be frequently accessed. State how they can reduce costs while doing so. [2]**

> [!Answer]
> Data not frequently accessed can be archived
>
> * by moving it to cheaper storage

**(d) State two actions the company must take regarding the collection and use of personal user data to comply with prevailing personal data protection laws. [4]**

> [!Answer]
> Notification: ImageMaps must inform customers of the purposes of data use (e.g. through a privacy policy)
> Consent: ImageMaps must obtain customers' informed consent (e.g. through app permissions or webapp dialog box)
> Purpose Limitation: ImageMaps must ensure employees do not use customer **personal data** for purposes other than the stated (e.g. by using access control measures)
> Access and Correction: ImageMaps must allow customers to see their stored **personal data**, and correct it if necessary (e.g. through a web portal)
> (other appropriate obligations relating to collection and use, with appropriate action specified)

**(e) State whether a native or web application is more suitable for ImageMaps’s application. Explain your answer. [3]**

> [!Answer]
> Native application
>
> * The application needs to access device storage
>
> * Web apps do not have the same capabilities as native apps, such as the capability to access device storage / run offline

---

##### 2025 TJC Prelim P1 Q5)

**5A company, ImageMaps, wishes to develop an application that scans a user's device for photographs, detect the associated location, and display the images on a map using the associated locations.**

(a) State two actions the company must take regarding the collection and use of personal user data to comply with prevailing personal data protection laws. [4]

> [!Answer]
>
> * Notification: ImageMaps must inform customers of the purposes of data use through a privacy policy
>
> * Consent: ImageMaps must obtain customers' informed consent (e.g. through app permissions or webapp dialog box)
>
> * Purpose Limitation: ImageMaps must ensure employees do not use customer **personal data** for purposes other than the stated (e.g. cannot be used to train AI)
>
> * Access and Correction: ImageMaps must allow customers to see their stored **personal data**, and correct it if necessary.(other appropriate obligations relating to collection and use, with appropriate action specified)

**(b) ImageMaps needs to store a large quantity of data that will not be frequently accessed. State how they can reduce costs while doing so. [2]**

> [!Answer]
> Data not frequently accessed can be archived by moving it to cheaper storage

**(c) State whether a native or web application is more suitable for ImageMaps’s application. Explain your answer. [3]**

> [!Answer]
> Native applicationThe application needs to access device storage to scan for photographs Web apps do not have the same capabilities as native apps, such as the capability to access device storage

**(d) When data is transmitted between a user’s device and ImageMaps’ server, it is divided into packets that travel through the network. Describe how networking protocols address the following problems:**

(i) Data packets may arrive out of order and require reassembly [2]

(ii) Data packets may be corrupted in transit. [2]

> [!Answer]
> (d)When data is transmitted between user’s device and ImageMaps’ server, it is divided into **packets** that travel through the network. Describe how networking protocols address the following problems:
>
> Each **packet** is tagged with a sequence number The sequence number is included in the header to allow sequential reassembly(ii) The **packet** data is hashed to produce a checksumThe recipient verifies the checksum against its hashed data

---

##### 2025 VJC Prelim P1 Q4)

**A company, ImageMaps, wishes to develop an application that scans a user's device for photographs, detect the associated location, and display the images on a map using the associated locations.**

State the actions ImageMaps must take to secure critical business data such as user data against catastrophic hardware failure.[4]

> [!Answer]
>
> * Backups of critical data must be made
>
> * Backups should be made regularly
>
> * Multiple copies should be made and stored offsite / in different locations, to minimise risk of complete data loss
>
> * The backups should be tested to ensure that data recovery can succeed
>
> * Any other sensible answers related to **backup**.

State the consequences, should ImageMaps suffer such a hardware failure.[2]

> [!Answer]
>
> * Catastrophic failure resulting in data loss can mean loss of business continuity (business is unable to operate), loss of revenue, loss of customer / stakeholder trust, etc
>
> * Failure to protect critical data, especially financial records or customer **personal data**, may be a violation of data protection laws and other legal requirements

**ImageMaps needs to store a large quantity of data that will not be frequently accessed.**

State how they can reduce costs while doing so.[2]

> [!Answer]
> Data not frequently accessed can be archived [1]by moving it to cheaper storage

State two actions the company must take regarding the collection and use of personal user data to comply with Singapore’s Personal Data Protection Act (PDPA).[4]

> [!Answer]
>
> * Proper explanation of **PDPA** obligation
>
> * Description of a concrete action to fulfill the obligation
>
> * Notification: ImageMaps must inform customers of the purposes of data use through a privacy policy
>
> * Consent: ImageMaps must obtain customers' informed consent (e.g. through app permissions or webapp dialog box)
>
> * Purpose Limitation: ImageMaps must ensure employees do not use customer **personal data** for purposes other than the stated (e.g. cannot be used to train AI)
>
> * Access and Correction: ImageMaps must allow customers to see their stored **personal data**, and correct it if necessary. (other appropriate obligations relating to collection and use, with appropriate action specified)

**State whether a native or web application is more suitable for ImageMaps’s application. Explain your answer. [3]**

> [!Answer]
>
> * Native application
>
> * The application needs to access device storage
>
> * Web apps do not have the same capabilities as native apps, such as the capability to access device storage
>
> * Native app is more suitable due to deeper OS integration, better performance for image processing, and more reliable file system access across all devices.

---

<a id="toc-relational-databases"></a>

# Relational Databases

<a id="toc-relational-databases-sql-queries"></a>

### SQL Queries

##### 2025 ASRJC Prelim P1 Q7)

**7 A university has several departments. Each department has multiple lecturers, and each lecturer belongs to exactly one department. A record of courses taught by each lecturer has been set up using a relational database. Each course is only taught by one lecturer. Students can enrol in multiple courses. They may also re-enrol in the same course in another semester, particularly when they need to repeat the course due to unsatisfactory performance. The following tables hold the data. STUDENT (StudentID, StudentName, StudentEmail, StudentPhone)DEPARTMENT (DeptID, DeptName, DeptAddress)COURSE (CourseID, CourseName, LecturerID, MaxCapacity)LECTURER (LecturerID, LecturerName, DeptID)ENROLMENT (StudentID, CourseID, EnrolmentDate, Grade, Status)**

(a) Copy the above table definitions, notating all primary keys and foreign keys. [4]

(b) Draw an Entity-Relationship (E-R) diagram to represent the database design. [3]

> [!Answer]
> E-R diagram:
>
> ```mermaid
> erDiagram
>   DEPARTMENT ||--|{ LECTURER : has
>   LECTURER ||--|{ COURSE : teaches
>   STUDENT ||--o{ ENROLMENT : has
>   COURSE ||--o{ ENROLMENT : has
>
> ```

**(c) There is an address field in this database. Explain why storing the address as a single field is not good database design. [1]**

> [!Answer]
> It violates the principle of atomicity required in **1NF**. Address contains multiple separate components (e.g. block number, street, etc.) that should be stored in individual fields to allow for efficient searching and manipulation.

**A report is to be generated showing the courses taken by a student and the corresponding grades. Student: Michael TanCourse IDCourse NameGradeCS1231Discrete StructuresA-DSA5101Introduction to Big Data for IndustryB+DSA5102Foundations of Machine LearningADSA5105Principles of Machine LearningA-DSA5204Deep Learning and ApplicationsBDSA5206Advanced Topics in Data ScienceB+**

(d) Write an SQL query that would enable us to extract the required information above for the student Michael Tan, sequenced in ascending order by course ID. [3]

> [!Answer]
> SQL query:
>
> ```sql
> SELECT COURSE.CourseID, COURSE.CourseName, ENROLMENT.GradeFROM STUDENTINNER JOIN ENROLMENT ON STUDENT.StudentID = ENROLMENT.StudentIDINNER JOIN COURSE ON ENROLMENT.CourseID = COURSE.CourseIDWHERE STUDENT.StudentName = 'Michael Tan'ORDER BY COURSE.CourseID;
>
> ```
>
> Alternatively:SELECT COURSE.CourseID, COURSE.CourseName, ENROLMENT.Grade FROM STUDENT, ENROLMENT, COURSE WHERE STUDENT.StudentID = ENROLMENT.StudentID    AND ENROLMENT.CourseID = COURSE.CourseID    AND STUDENT.StudentName = 'Michael Tan' ORDER BY COURSE.CourseID;

**The university has decided to distribute individual student grade reports via email as digitally signed PDF documents.**

(e) (i) Explain the purpose of a digital signature. [2]

> [!Answer]
> It ensures:
> **Authentication** (confirming identity of the sender)
> **Data integrity** (verifies the document has not been tampered with)
> Non-repudiation (prevents the sender from denying that he signed the document)

(ii) Describe the process of digitally signing a PDF document by the sender, and the process performed by the receiver. [4]

> [!Answer]
> Sender:
> The PDF document is passed through a cryptographic hash function to create a unique hash value.
> The hash is encrypted using the sender’s **private key** to create the **digital signature**, which is attached to the PDF document.
> Receiver:
> The receiver extracts the **digital signature** and decrypts it using the sender’s **public key** to obtain the original hash.
> He also generates a hash of the received document using the same hash function and compares it with the decrypted hash. If they match, the **digital signature** is valid.

---

<a id="toc-relational-databases-er-entity-relationship-diagram"></a>

### ER (Entity Relationship) Diagram

##### 2025 JPJC Prelim P1 Q1)

**1 JPCAR operates a car-sharing network across Singapore. Users can rent cars from docking stations using a mobile app. The company maintains two types of data storage:**

**Relational Database (RDBMS): Stores structured data like user accounts, cars, stations, and rentals.**

**NoSQL Database (Document Store): Stores unstructured data like real-time Global Positioning System (GPS) coordinates of bicycles and usage logs from Internet of Things (IoT) devices.**

**Anyone who wishes to use the car-sharing network needs to sign up to be a user of the JPCAR. The company wants to store data in a relational database with the following requirements:**

* **Each user has a unique userID that corresponds to a name, email, and**
  **phoneNo.**

* **Each car has a carID that is linked to a stationID (where it is parked), and**
  **status (Available or In Use).**

* **Each station has a stationID that corresponds to a stationName, and**
  **location.**

**It is given that whenever a user rents an available car parked at the station, the car’s status will be set to “In Use” immediately, and the rental date and rental start time will be recorded by the system. Upon returning, the returned car’s status will be changed to “Available”. Rental end time, total rental cost, and information on the station the car was returned to will also be determined and recorded.**

**(a) JPCAR wants to use a relational database to store and manage the data for the system.**

**(i) A database requires several tables to store the data. Draw an entity-relationship (ER) diagram to show the tables in third normal form (3NF) and the relationship(s) between them. [2]**

4

> [!Answer]
> USER RENTAL CAR
> STATION
>
> ```mermaid
> erDiagram
>   USER ||--o{ RENTAL : makes
>   CAR ||--o{ RENTAL : has
>   STATION ||--o{ CAR : parks
>
> ```

**(ii) A table description can be expressed as: TableName (Attribute1, Attribute2, Attribute3, …) The primary key is indicated by underlining one or more attributes. Foreign keys are indicated by using an asterisk (*). Write table descriptions for the tables identified in part (a)(i), using the information given. [4]**

> [!Answer]
> User(userID, name, email, phoneNo)
> Station(stationID, stationName, location)
> Cars(carID, stationID*, status)
> Rentals(rentalID, userID*, carID*, startTime, endTime,
> totalCost)
> Note: * denotes a **foreign key**.
> Car.stationID is a FK that references to the PK stationID in Station table.

**(b) Using tables created, write SQL statements for the following queries:**

**(i) display all the available cars parked at the location “Desker Road”. [2]**

> [!Answer]
>
> ```sql
> SELECT Car.carID
> FROM Car, Station
> JOIN Stations ON Car.stationID = Station.stationID
> WHERE Car.status = 'Available' AND Station.stationName = 'Desker Road'
>
> ```

**(ii) display every userID, and the total number of car rentals the user has made. [2]**

> [!Answer]
>
> ```sql
> SELECT User.userID, COUNT(Rental.rentalID) AS Total_Car_Rentals
> FROM User, Rental
> LEFT JOIN Rental ON Rental.userID = User.userID
> GROUP BY User.userID
>
> ```

**(iii) display the top three users who spent the highest total cost on car rentals, sorted from highest to lowest. [2]**

> [!Answer]
>
> ```sql
> SELECT User.userID, User.Name, SUM(Rental.totalCost) AS Total_Amount_Spent
> FROM Rental, User
> JOIN Users ON User.userID = Rental.userID
> WHERE Rental.totalCost IS NOT NULL
> GROUP BY User.userID, User.name
> ORDER BY Total_Amount_Spent DESC
> LIMIT 3;
>
> ```

**(c) Explain how double-booking conflicts on a particular car between two or more users can be prevented. [2]**

> [!Answer]
> Either one:
>
> * Enforcing One Active Rental per Car at any one time:
>
>   * Each rental record should link a carID to a userID with startDate and
>     startTime recorded immediately when the booking is made.
>
>   * The system must check that the same carID does not already appear in
>     another rental record with a NULL endTime (i.e., still in use).
> * Using database constraints and transactions:
>
>   * When inserting a new rental row, the database checks availability
>     (status='Available').
>
>   * If the car’s status is already 'In Use', the transaction fails and rolls back,
>     blocking a double booking.
> * Use Status Update Logic:
>
>   * When a booking is confirmed, the system immediately updates Car.status
>     to 'In Use'.
>
>   * This real-time update ensures that subsequent booking attempts for the same
>     car will be rejected until the rental is completed and the status is reset to
>     'Available'.

**(d) Explain two key differences between a backup file and an archive file. [2]**

> [!Answer]
> **Backup** file: Created to provide a recent copy of data that can be restored quickly in
> case of data loss, corruption, or system failure.
> **Archive** file: Created to store data long-term that is no longer actively used but must
> be retained for historical, compliance, or legal reasons.
>
> Either one:
>
> * **Backup** files are accessed regularly (often daily or weekly) to ensure recovery
>   readiness, while **archive** filed are accessed rarely, usually only when reviewing
>   old records
>
> * **Backup** files are usually temporary, and may be overwritten by newer backups
>   while archive files are retained permanently or long-term, often until
>   legal/organisational policies permit deletion.
>
> * **Backup** files are often stored locally (disk, tape, or cloud **backup** service) for quick
>   retrieval, while **archive** files are stored on lower-cost, long-term media (e.g.,
>   magnetic tape, cloud cold storage).

**(e) The real-time locations of cars are stored in a NoSQL document database (e.g., MongoDB) using the following document structure:**
**{**
**"carID": "C1001",**
**"location": { "lat": 1.283, "lon": 103.860 },**
**"battery%": 85,**
**"lastUpdate": "2025-07-15T13:45:00Z"**
**}**

**(i) Write a MongoDB query to find all bicycles with battery < 20% [2]**

> [!Answer]
>
> ```javascript
> db.cars.find(
>     { "battery": { $lt: 20 } }
> )
>
> ```

**(ii) Explain one advantage of using NoSQL over SQL for storing GPS tracking data. [2]**

> [!Answer]
> **NoSQL**’s flexibility and scalability with unstructured / semi-structured data. GPS
> tracking generates large volumes of real-time data with variable fields (e.g.,
> location, battery, timestamp, sensor metadata). **NoSQL** (e.g., **MongoDB**) stores
> data as JSON-like documents, allowing the schema to evolve easily without
> altering rigid table definitions. This makes it highly efficient for storing and
> retrieving location updates in real time, and supports horizontal scaling across
> multiple servers for high throughput.

**(iii) Describe one scenario where the relational database design is still preferable for JPCAR. [2]**

5

> [!Answer]
> A relational database ensures this through referential integrity and transactions,
> preventing data anomalies like double-booking or incorrect billing. When a user
> rents a car, the system must ensure that:
> a. the car ’s status changes from Available → In Use,
> b. the rental record is created, and
> c. the billing information is consistent.

**2 A start-up company is developing a ride-hailing application called JRide. The system will have different types of vehicles, such as car and motorbike, that share common attributes and behaviours but also have some unique features. The company wants to use Object-Oriented Programming (OOP) to model this situation.**

**The system needs to:**

* **Store details of the driver’s name, vehicle registration number, and maximum**
  **passenger capacity.**

* **Motorbike can only carry one passenger while Car can carry up to seven**
  **passengers.**

* **The fare is calculated differently depending on the type of vehicle. For example,**
  **Car calculates fare based on distance and a base fee, while Motorbike calculates fare based only on distance with a lower rate.**

(a) Draw a class diagram for the described situation, showing:

* any derived classes and inheritance from the base class
* the properties needed in the base and any derived classes
* suitable methods, in each class, to support the system.

[6]

**(b) The company has decided to introduce a Driver class to store details of the driver’s name, license number, and years of experience. Describe how you would update the class diagram to include this new class. [3]**

**It is common for the properties of a class to be private.**

**(c) Explain what encapsulation means in OOP. [2]**

**(d) Describe how it could be applied to this situation. [2]**

6

**3 A college is launching an online e-Assessment portal. Teachers record the marks in spreadsheets and upload them to the portal. The spreadsheets must be verified for both authenticity and integrity. Additionally, the portal must be protected from the public Internet.**

**(a) Explain how a digital signature works in this situation. [5]**

**(b) State one key difference between encrypting a file and digitally signing a file. [1]**

**(c) Propose a firewall policy to protect the e-Assessment server that is reachable over HTTPS from the Internet but administered only from the IT office. [2]**

**4 A school maintains a Binary Search Tree (BST) of locker IDs to support quick allocation, deallocation and look-ups. Each node stores a unique integer key (the locker ID), and pointers left and right.**

**Unless stated otherwise, assume no duplicate keys and that the BST property holds: all keys in the left subtree < key, all keys in the right subtree > key.**

**(a) The following locker IDs are inserted into an initially empty BST in the following order: 42, 18, 60, 12, 35, 50, 70, 63, 72**

(i) Draw the resulting BST.

**(ii) Write the in-order traversal output of your tree as a comma-separated list. [2]**

[1]

**Assume each node has fields: key, left, right.**

(b) Write a recursive pseudocode for InOrder(root) that displays the keys in ascending order.

**(c) Describe an iterative algorithm for BST_Search(root, k) that returns TRUE if found or FALSE if not found. [4]**

[5]

**7**

**(d) State and justify the worst-case time complexity of searching in a BST using an iterative algorithm. [2]**

**(e) Explain why you would store the ordered locker IDs in a BST rather than an ordered array. [2]**

**The school’s allocation service buffers locker assignment requests in a fixed-capacity circular queue before processing them against the BST. The queue is implemented as an array that stores up to 50 integers.**

**(f) Write the pseudocode for DEQUEUE()which returns the integer stored at the front of queue or -1 if the queue is empty. [6]**

**(g) Explain one advantage of a circular queue over a linear queue in this situation. [2]**

8

**5 A smart thermostat stores the current temperature setpoint and shows a short history of recent changes on its display.**

**The following describes the implementation:**

**Variables**

* **SETPOINT an integer temperature**
* **HISTORY a list of change records kept in memory that expands as needed**
* **DISPLAY_BUFFER text that is used to draw the screen**

**On start-up**
**1. Set SETPOINT to 24**
**2. Create an empty HISTORY list**

**Main loop (every 200 milliseconds)**
**3. If the dial is turned, update SETPOINT to the dial value 4. Add a new change record (containing the current SETPOINT and time) to HISTORY. 5. Initialise a 32-character DISPLAY_BUFFER, format the current setpoint and a few historical items, display it on screen. 6. Repeat from step 3.**

**After several months in service, many units begin to reset and eventually refuse to start, showing “out of memory”.**

**(a) Explain how mistakes in the algorithm caused this recurring problem. [2]**

**(b) Explain how the algorithm should be changed to prevent the problem from recurring. [2]**

**(c) State one advantage and one disadvantage of using dynamic memory allocation (compared with static allocation) in embedded devices like this thermostat. [2]**

9

**6 A college hosts a web application on a web server at the domain portal.jpjc.edu.sg. Students access it from home and on campus.**

**(a) Explain how a client obtains the IP address for portal.jpjc.edu.sg using a Domain Name Server (DNS). [3]**

**(b) Data transmitted across the Internet is divided into sequentially numbered packets.**

(i) State two reasons why data is split into packets for transmission across the Internet.

(ii) State two reasons why the packets are numbered.

**(iii) State two items, other than the packet number, that are stored in the packet header. [2]**

[2]

[2]

**(c) State the key difference between a static IP address and a dynamic IP address. [1]**

**(d) For the 300 student laptops connecting to the campus Wi-Fi, recommend either static or dynamic addressing and justify your choice. [3]**

**7 A junior college is rolling out an online admissions portal that asks applicants for their full name, email, mobile, NRIC, CCA, medical condition (optional), emergency contact, bank account (for bursary), and uploads of a passport-style photo.**

**(a) Define the term “personal data” and give one example from this situation. [2]**

**(b) State a possible threat of losing the applicants’ data and suggest a method to prevent it. [2]**

**(c) Recommend two Personal Data Protection Act (PDPA) controls the college should implement for the portal. [2]**

10

**8 A media server scans a nested folder structure to list all files. Each folder may contain files and subfolders. The following is a recursive procedure:**

```text
PROCEDURE ListAll(f: FOLDER)
IF f <> NULL AND f.isEmpty() <> TRUE THEN
FOR EACH item IN f.items DO
IF item.type = "FILE" THEN
OUTPUT item.name
ELSE // item is a FOLDER

```

**ListAll(item) // recursive call**

```text
ENDIF

```

**ENDFOR**

```text
ENDIF
ENDPROCEDURE

```

**(a) Describe the base case. [2]**

**(b) The call ListAll(Root) is performed on the following structure:**

(i) List the recursive calls made for the call ListAll(Root) in the exact order they occur.

(ii) Write the exact sequence of file names displayed by the procedure.

**(iii) State the number of times ListAll called itself. [2]**

[1]

[1]

(c) Explain when and why a memory stack overflow could occur with ListAll. [2]

Root
FOLDER_A
X.txt
FOLDER_B
FOLDER_C
Z.ppt
FOLDER_D
W.jpg
Y.txt
FOLDER_E
File X.txt and folder
FOLDER_B are in FOLDER_A.
Files Z.ppt, Y.txt and
folder FOLDER_D are in
FOLDER_C.
File W.jpg is in FOLDER_D.

FOLDER_A, FOLDER_C and
FOLDER_E are in Root .

11

---

##### 2025 RI Prelim P1 Q1)

**1 A company operates a ride-hailing platform that allows passengers to book rides via a mobile app. A relational database is being designed to manage rides, drivers, passengers, and payments.**

**Each ride includes:**

* **a unique RideID**
* **PickupLocation**
* **DropoffLocation**
* **RideDateTime**
* **Status (e.g., completed, cancelled, ongoing)**
* **DriverID**
* **PassengerID**

**Each driver includes:**

* **a unique DriverID**
* **FullName**
* **VehicleNumber**
* **LicenseExpiryDate**
* **ContactNumber**

**Each passenger includes:**

* **a unique PassengerID**
* **FullName**
* **PhoneNumber**
* **EmailAddress**

**Each payment includes:**

* **a unique PaymentID**
* **RideID**
* **PaymentMethod (e.g., credit card, e-wallet)**
* **FareAmount**
* **PaymentStatus (e.g., paid, pending)**

**(a) Draw an entity -relationship (ER) diagram showing the four entities and the relationships between them. [3]**

> [!Answer]
> 1
>
> * All four entities shown
>
> * Correct 1:1 relationship shown (Ride -  Payment)
>
> * Correct 1:M relationships (e.g., one Driver has many Rides, One Passenger
>
> has many Rides)
>
> Passenger Driver Ride
> Payment
>
> ```mermaid
> erDiagram
>   PASSENGER ||--o{ RIDE : books
>   DRIVER ||--o{ RIDE : operates
>   RIDE ||--|| PAYMENT : has
>
> ```

(b) Write table definitions for each of the tables so that they are in third normal form, using this format: TableName (Attribute1, Attribute2, Attribute3, …)

(i) Ride [2]

> [!Answer]
> Ride (RideID, PickupLocation, DropoffLocation, RideDateTime,
> Status, DriverID, PassengerID)

(ii) Driver [2]

> [!Answer]
> Driver (DriverID, FullName, VehicleNumber, LicenseExpiryDate,
> ContactNumber)

(iii) Passenger [2]

> [!Answer]
> Passenger (PassengerID, FullName, PhoneNumber, EmailAddress)

(iv) Payment [2]

> [!Answer]
> Payment (PaymentID, RideID, PaymentMethod, FareAmount,
> PaymentStatus)

**(c) (i) The company wants to know which drivers earned the most. Write an SQL query to calculate the total fare amount collected by each DriverID, and sort the results in descending order of total fare. [4]**

> [!Answer]
>
> ```sql
> SELECT DriverID, SUM(FareAmount) AS TotalEarnings
> FROM Ride
> JOIN Payment ON Ride.RideID = Payment.RideID
> WHERE PaymentStatus = 'paid'
> GROUP BY DriverID
> ORDER BY TotalEarnings DESC;
>
> ```

(ii) Write an SQL query to update the PaymentStatus of a ride with

```text
RideID = 'R7645' to 'paid'. [2]

```

> [!Answer]
>
> ```sql
> UPDATE Payment
> SET PaymentStatus = 'paid'
> WHERE RideID = 'R7645';
>
> ```

**(d) The company is planning to collect customer reviews and use them to improve driver performance. Justify three reasons why a NoSQL database might be more suitable than a relational database for storing customer reviews for the ride-hailing platform. [3]**

> [!Answer]
> Reasons why **NoSQL** is suitable for storing customer reviews:
>
> 1. Unstructured/semi-structured data – Reviews may contain ratings, free text,
>    emojis, images, etc., which **NoSQL** can store more naturally than SQL.
>
> 2. Schema flexibility – Different reviews can have different fields (e.g. some with
>    upvotes, some without) without needing database redesign, supporting future feature
>    expansion.
>
> 3. Horizontal scalability – **NoSQL** can distribute data across multiple servers, handling
>    thousands/millions of reviews efficiently as the platform grows.
>
> 4. Fault tolerance – Reviews can be replicated across multiple servers; if one server
>    fails, data is still accessible. This ensures reliability and availability for both
>    passengers and drivers.
>
> 5. Hierarchical data storage – **NoSQL** supports nested structures. For example, a
>    single review record could include:
>
> * Review text and rating
>
> * Driver replies
>
> * User upvotes
>
> * Timestamps
>   This avoids the need to split into multiple relational tables and makes
>   retrieving full review threads faster.
>
> 6. Performance on queries – Fetching a review document is faster (no complex joins
>    across multiple tables as in SQL), which improves the app’s responsiveness.

**During the booking process, the following personal data is collected and stored:**

* **From the passenger: full name, mobile number, pickup and drop -off location,**
  **and ride history.**

* **From the driver: full name, contact number, vehicle number, driving license**
  **number, and real-time location when online.**
  **The system also stores in-app messages between drivers and passengers.**

**(e) From the perspective of a passenger, explain two concerns you may have about how your personal data is used or shared. [2]**

> [!Answer]
> (Any 2 of the following, or any other reasonable answers):
>
> 1. Location data misuse:
>    Concern that real-time or historical pickup/drop-off locations might be shared with
>    third parties or used to track personal habits.
> 2. Unconsented data sharing:
>    Worry that personal information (e.g., name or contact number) may be shared
>    with external advertisers or third-party apps without consent.
> 3. Data retention:
>    Concern about how long the company keeps ride history and whether old data is
>    securely deleted.

**(f) From the perspective of a driver, explain two responsibilities you have under PDPA when handling passenger data. [2]**

> [!Answer]
> (Any 2 of the following, or any other reasonable answers):
>
> 1. Do not misuse passenger contact details:
>    A driver must not use the passenger’s phone number (e.g., for personal
>    messages or marketing) after the ride is completed.
>
> 2. Keep information confidential:
>    A driver must not disclose passenger details (e.g., drop-off location, name) to
>    others or post them online.
>
> 3. Report data breaches:
>    If a driver’s device is lost or compromised, they must report it to the platform if
>    passenger data is affected.

**(g) To prevent misuse of passenger information, the company plans to work with a third-party fraud analysis firm. What actions should the company take before sharing personal data with this vendor? [2]**

> [!Answer]
> Actions the company should take:
>
> 1. Anonymise or pseudonymise data before sharing (e.g., remove names,
>    mask phone numbers)
> 2. Obtain informed consent from passengers OR ensure a data sharing
>    agreement is in place that complies with data protection laws (e.g., **PDPA**,
>    GDPR)
> 3. Limit Data to the Minimum Necessary: e.g., transaction IDs, device
>    fingerprints) — not unnecessary details like full names or contact numbers.

---

<a id="toc-relational-databases-database-normalisation"></a>

### Database Normalisation

##### 2025 ACJC Prelim P1 Q7)

**7An art company engages a number of artists to produce artworks. These artworks are displayed for sale at various studios which are run by the company. Each artwork has a unique title. Part of the data in the database is shown in the table below.**

| ArtworkTitle | Medium      | Price ($) | ArtistName | ArtistContact                     | Studio Name | StudioAddress  |
| ------------ | ----------- | --------- | ---------- | --------------------------------- | ----------- | -------------- |
| Lion Head    | Stone       | 3 000     | Fariz      | [fariz@b.com](mailto:fariz@b.com) | La Galleria | 123 King Road  |
| Tiger Head   | Stone       | 3 000     | Fariz      | [fariz@b.com](mailto:fariz@b.com) | New Studio  | 456 Jalan Kayu |
| Fire Star    | Watercolour | 1 500     | Sue Tan    | [sue@tan.com](mailto:sue@tan.com) | La Galleria | 123 King Road  |
| Thunder Bird | Oil paint   | 4 500     | Sue Tan    | [sue@tan.com](mailto:sue@tan.com) | New Studio  | 456 Jalan Kayu |
| Banana       | Plastic     | 5 000     | Surya      | [surya@k.co](mailto:surya@k.co)   | New Studio  | 456 Jalan Kayu |
| Guava        | Steel       | 4 000     | Surya      | [surya@k.co](mailto:surya@k.co)   | La Galleria | 123 King Road  |

(a) Explain why the table is not in third normal form (3NF). [1]

> [!Answer]
> There exist transitive dependencies in the table (e.g. studio address depends on studio name which depends on artwork title)

**(b) A table description can be expressed as: TableName(Attribute1, Attribute2, Attribute3, …) The primary key is indicated by underlining one or more attributes. Foreign keys are indicated by using a dashed underline. Write table descriptions for all the required tables in the database so that they are in third normal form (3NF). [4]**

> [!Answer]
> Artworks(Title, Medium, Price, ArtistName, StudioName)Artists(Name, Contact)Studios(Name, Address)

(c) Draw the entity-relationship (ER) diagram of the above database. [3]

> [!Answer]
> ArtistArtworkStudioArtistArtworkStudio
>
> ```mermaid
> erDiagram
>   Artists ||--o{ Artworks : produces
>   Studios ||--o{ Artworks : displays
>
> ```

(d) Explain why it is recommended to maintain multiple tables in 3NF instead of storing all the data in one table as shown above. [2]

> [!Answer]
> Remove redundancies in the data, so that when data is updated, only one entry needs to be changed. It also lowers the risk of errors and inconsistencies in the data.

(e) Write an SQL query to output all the names of the artists who have at least one artwork displayed in La Galleria that costs at most $3500. [4]

> [!Answer]
>
> ```sql
> SELECT ArtistName
> FROM Artworks
> WHERE StudioName = 'La Galeria'AND Price <= 3500
>
> ```

(f) State any two ways the privacy of the artists’ data should be provided for under the Personal Data Protection Act (PDPA). [2]

> [!Answer]
> **Personal data** such as contact details should be stored with reasonable security.Use of artists’ data should be carried out with consent of the artists.**Personal data** should be deleted if no longer in use, e.g. artist is no longer working with the companyEtc.

---

##### 2025 DHS Prelim P1 Q7)

**7. A university wishes to store its data using a relational database.**

**The university records the following data for each student:**

* **student identification number**
* **name**
* **email**

**The university records the following data for each lecturer:**

* **lecturer reference number**
* **name**
* **department**
* **email**

**The university records the following data for each course it is offering:**

* **course reference code**
* **course name**
* **department**
* **number of credits**

**Students enrol in up to 5 courses in each semester which is taught by different lecturers. The university records the following details for each enrolment:**

* **the course**
* **the student taking the course**
* **the lecturer teaching the course**
* **the student’s score achieved in the course**
* **the semester**

**(a) Draw an entity-relationship (ER) diagram to show the tables in third normal form (3NF) and the relationship(s) between them. [3]**

> [!Answer]
> Enrolment Student
> Lecturer
> Course
>
> ```mermaid
> erDiagram
>   STUDENT ||--o{ ENROLMENT : has
>   LECTURER ||--o{ ENROLMENT : teaches
>   COURSE ||--o{ ENROLMENT : contains
>
> ```

**(b) Write table definitions, indicating the primary key with underline and foreign key with *, for each of the tables you identified in (a). [4]**

Use the format: TableName(Attribute1, Attribute2, Attribute3*, etc.)

> [!Answer]
> Write table definitions, indicating the **primary key** with underline and **foreign key** with *, for each of the
> tables you identified in (a).
> Student(StudentID, Name, Email)
> Lecturer(LecturerID, Name, Department, Email)
> Course(CourseID, CourseName, Department, Credits)
> Enrolment(StudentID*, LecturerID*, CourseID*, Semester, Score)

**(c) Three lecturers teach the course CS202 in Semester 2025Sem1. After moderation, they decided to add 5 marks to all the students taking the course that semester. Write an SQL query to update the scores. [3]**

> [!Answer]
> Three lecturers teach the course CS202 in Semester 2025Sem
>
> add 5 marks to all the students taking the course that semester. Write an SQL query to update the
> scores.
>
> ```sql
> UPDATE Enrolment SET Score = Score + 5 WHERE CourseID = "CS202" AND Semester
>
> ```
>
> = "2025Sem1
> Adding 5 marks to Score field – 1 mark

**(d) A student requires at least 100 accumulated credits to graduate. At the end of each semester, the university will generate a report to calculate the total number of credits each student has completed ( you can assume that all students pass all of their courses). Write an SQL query that will output all the students who have completed at least 100 credits. [4]**

> [!Answer]
> A student requires at least 100 accumulated credits to graduate. At the end of each semester, the
> university will generate a report to calculate the total number of credits each student has completed (you
> can assume that all students pass all of their courses).
> Write an SQL query that will output all the students who have completed at least 100 credits.
>
> ```sql
> SELECT Student.StudentID, SUM(Credits) FROM Student
> INNER JOIN Enrolment ON Student.StudentID = Enrolment.StudentID
> INNER JOIN Course ON Enrollment.CourseID = Course.CourseID
> GROUP BY Student.StudentID
> HAVING SUM(Credits) >= 100;
>
> ```
>
> Correct fields: Student.StudentID & SUM(Credits)
>
> * INNER JOINS with correct tables
>
> * GROUP BY
>
> * HAVING

(e) State the two aims of normalisation. [2]

> [!Answer]
> State the two aims of **normalisation**.
>
> 1. Reduces redundant data so as to optimise storage space.
> 2. Prevent data inconsistency due to insert, update or delete anomalies.

**(f) The university is considering whether to move its data to a NoSQL database.**

(i) State two key differences between the two types of databases. [2]

(ii) State and explain which database system the university should choose. [2]

> [!Answer]
> The university is considering whether to move its data to a **NoSQL** database.
>
> **Possible answer in SQL’s favour:**
>
> * Since the data stored has a fixed schema and flexibility afforded by **NOSQL** is unnecessary,
>
> * Complex queries involving join operations are required to retrieve data across multiple
>
> tables
>
> * ACID compliance is important
>
> * There is possibly a high number of simultaneous transactions performed during mark entry
>
> period
> **Possible answer in**NOSQL**’s favour:**
>
> * **NoSQL** databases can take advantage of multiple servers, ensuring the application
>
> functions even if one server fails
>
> * **NoSQL** provides flexibility in adding/removing data fields should the requirements of the
>
> application change with time
>
> * Horizontally scalable, hence the university might find it easier to add an additional low cost
>
> server if the need arises, as compared to replacing existing server with a better one

---

##### 2025 RVHS Prelim P1 Q9)

**9. A new badminton complex was just built in Fernvale town. The management is planning to implement a new system for residents to book its courts. At present, residents must physically go down to the office in the complex to book the courts with the person in charge. Resident details are recorded in a spreadsheet on a shared laptop for their bookings with the following instructions:**

* **There are 4 courts for booking. The bookings for each court are recorded**
  **in each row.**

* **For each booking, NRIC number, name, date and time of usage are**
  **recorded; name and NRIC number will be recorded in a single cell.**

* **Bookings can be for multiple courts and for different dates and times at**
  **each time.**

* **Should the payment be made at the time of booking, status will be ‘Paid’**
  **else it will be left empty. Payment will then be made on the day of use.**

**Below shows a part of the spreadsheet.**

**a) Identify 1 possible social issue and 1 economic issue because of using the shared spreadsheet for booking management. [2]**

> [!Answer]
> Social issue – NRIC number is revealed; sensitive information may be
> accessible by others that may be detrimental to the resident; No privacy and
> **personal data** protection.
> Financial issue – admin may missed out keying in status and result payment
> issues.
> 1
>
> 1

**b) The spreadsheet is not in 1st Normal Form and thus is not suitable to use in a relational database. Identify all issues in the spreadsheet which does not make it to 1st Normal Form. [2]**

> [!Answer]
> i) repeated booking grouping for each court;
>
> ii) fields are not atomic
>
> iii) fields value are not consistent ‘Paid’ and ‘’ for Unpaid
> 1
> 1

**c) Is data redundancy present in the spreadsheet? Explain your answer. [2]**

9

> [!Answer]
> **Data redundancy** is present. The NRIC information for a resident is repeated
> for each of the booking.
> 2

**An attempt to normalise the spreadsheet for a relational database turn up with the following 3 tables.**

**Booking_Schedule**
**booking_id resident_id court date time**
**2025001 001 1 23/10/2025 0900**
**2025001 001 1 23/10/2025 1000**
**2025001 001 1 23/10/2025 1100**
**2025001 001 1 24/10/2025 0900**
**2025001 001 1 24/10/2025 1000**
**2025001 001 1 24/10/2025 1100**
**2025002 002 2 22/10/2025 1900**
**2025002 002 3 22/10/2025 1900**
**2025003 003 3 23/10/2025 1000**
**2025003 003 3 23/10/2025 1100**
**2025003 003 3 23/10/2025 1200**
**… … … … …**

**Resident table keeps the data of residents who made the booking. The attribute resident_id was generated for quick reference in the database; attribute name for addressing the resident; and attribute nric_last_4 for quick verification on the day of usage.**

**Booking table keeps the data of bookings made. The attribute booking_id was generated for bookings made; Attribute payment is to keep track if payment has been made.**

**Booking_Schedule keeps the data of booking details for a booking_id**

which include attribute resident_id who made the booking, the date of usage, court and time. Time is recorded in an hour block with the starting time reflected in the table. Example time entry of 0900 means the court is booked for an hour from 0900 to 1000.

Resident
resident_id name nric_last_4
001 Tan Ai Ling 831K
002 Koh Chee Keng 567H
003 Sim Toh Long 234I
… … …
**Booking booking_id payment 2025001 Paid 2025002 Unpaid 2025003 Paid … … 10 d) Explain the 2 aims of normalization in relational database. [2]**

> [!Answer]
> **Normalisation** is to reduce redundancy and improve
> readability/management of data
> 2

**e) The above database that is made up of the 3 tables above is not normalized to 3NF. Identify which table is not normalized to 3NF. Explain your answer. [2]**

> [!Answer]
> The database is not in 3rd **normal form** as resident_id will not be directly
> dependent on the Primary Keys. resident_id is directly dependent on
> booking_id which cannot be the PK by itself in this table
> 2

**f) A table description can be expressed as**

**Tablename (Attribute1, Attribute2, Attribute3, …)**

**The primary key is indicated by underlining one or more attributes. Foreign keys are indicated using a dashed underline.**

**Write table descriptions with normalised tables in the database. Provide suitable Primary Key and indicate the Foreign Key for each table. [9]**

> [!Answer]
> Resident (resident_id, name, nric_last_4)
> Booking (booking_id, resident_id, payment)
> Booking_Schedule (booking_id, date, court, time)
> 2
> 3
> 4

**g) Draw out the entity-relationship (ER) diagram for the normalised tables in the database. [4]**

> [!Answer]
> Resident >-- Booking --< Booking_Schedule 4
>
> ```mermaid
> erDiagram
>   RESIDENT ||--o{ BOOKING : has
>   BOOKING ||--o{ BOOKING_SCHEDULE : has
>
> ```

---

##### 2025 VJC Prelim P1 Q7)

**A software company is writing a program for a vehicle hire business. Both cars and vans are available for hire. For all vehicles, the data that will be stored include: Vehicle Registration Number (VRN) Total distance travelled (km) Date hired Date of return Cost per day Available for hire For cars, the additional data stored include: Fuel type (petrol, diesel, electric, hybrid) For vans, the additional data stored include: Maximum load (kg) The odometer in the vehicle displays the total distance the vehicle has travelled since manufacture. When a vehicle is hired: total distance travelled is set to the odometer's value date hired is set to the current date return date is set to the date the vehicle is expected to be returned available for hire is set to FALSE. When a vehicle is returned: hire cost is returned as the cost per day multiplied by the number of days the vehicle was hired total distance travelled is set to the odometer value date returned is set to the current date available for hire is set to TRUE. The programmer uses a database to store vehicle hire data. Each row in the table represents a vehicle hire record. A vehicle must be hired for a minimum of one day. Vehicle hire data is stored in the following table: VRN TotalDistance DateHired DateReturned CostPerDay Available FuelType MaxLoad**

Identify a suitable primary key for the above table.[1]

> [!Answer]
> VRN AND DateHired

**Identify suitable SQL data types for the following columns: DateHired [1]**

> [!Answer]
> DATE / TEXT

Available[1]

> [!Answer]
> BOOLEAN / INTEGER

**State whether the above table is in Third Normal Form (3NF). Explain your answer. [4]**

> [!Answer]
>
> * Not in **3NF**
>
> * **3NF** require **2NF** [1]non-key attributes CostPerDay, FuelType, MaxLoad depend only on VRN (name at least one appropriate non-key attribute) [1]and not on the entire PK (partial dependence)

**A database consultant rewrites the above table into the following table descriptions: Vehicle (VRN, Type, TotalDistance, CostPerDay, Available) Hire (VRN, DateHired, DateReturned) Car (VRN, FuelType) Van (VRN, MaxLoad) The vehicle type is stored as either 'Car' or 'Van'.**

Draw an entity-relationship (ER) diagram representing the four tables.[4]

> [!Answer]
>
> * All entities represented: Vehicle, Hire, Car, Van
>
> * Vehicle <--1--1--> Car
>
> * Vehicle <--1--1--> Van
>
> * Vehicle <--1--n--> Hire
>
> ```mermaid
> erDiagram
>   Vehicle ||--|| Car : has
>   Vehicle ||--|| Van : has
>   Vehicle ||--o{ Hire : has
>
> ```

Write an SQL query to retrieve from the above tables the VRNs of hybrid cars and their latest date of hire.[6]

> [!Answer]
>
> ```sql
> SELECT Vehicle.VRN, MAX(DateHired)
> FROM Vehicle
> INNER JOIN Hire ON Vehicle.VRN = Hire.VRN
> INNER JOIN Car ON Vehicle.VRN = Car.VRN
> WHERE Type = 'Car' AND FuelType = 'hybrid'
> GROUP BY Vehicle.VRN
>
> OR
>
> SELECT Car.VRN, MAX(Hire.DateHired)
> FROM Car
> INNER JOIN Hire ON Car.VRN = Hire.VRN
> WHERE Car.FuelType = 'hybrid'
> GROUP BY Car.VRN
>
> ```

---

##### 2025 YIJC Prelim P1 Q7)

**A small company uses a flat file to keep track of the courses attended by the employees. The following are some records found in the file:**

| EmpID | Name  | Dept | CourseID | CourseName        | CourseType  | Fee | Date  |
| ----- | ----- | ---- | -------- | ----------------- | ----------- | --- | ----- |
| E001  | Sarah | FX   | C101     | Excel Basics      | Skills      | 150 | 01-10 |
| E001  | Sarah | FX   | C102     | PowerPoint Pro    | Skills      | 200 | 01-15 |
| E001  | Sarah | FX   | C103     | Strategic Writing | Comms       | 550 | 01-20 |
| E002  | James | CS   | C101     | Excel Basics      | Skills      | 150 | 01-12 |
| E002  | James | CS   | C103     | Strategic Writing | Comms       | 550 | 01-22 |
| E003  | Priya | HR   | C102     | PowerPoint Pro    | Skills      | 200 | 01-18 |
| E004  | John  | FX   | C104     | Leadership 101    | Soft Skills | 400 | 01-08 |

Describe with a specific example how an update anomaly may occur in the above table. [2]

> [!Answer]
> If the fee for the 'Excel Basics' course (C101) increases from $150 to $175, a user must update the Fee value in every row where CourseID is C101 (i.e., for both Sarah and James). If the update is performed on James's record but forgotten on Sarah's record, the data becomes inconsistent, as the same course now has two different fees in the database.

Explain the deletion anomaly present in the above table by giving a specific example and state the unintended consequence.[2]

> [!Answer]
> If John (E004) is the only employee registered for the 'Leadership 101' course (C104) and his registration record is deleted, all information about the 'Leadership 101' course (its ID, name, type, and fee) is also permanently erased from the database. The unintended consequence is the loss of course catalog data simply because an employee's registration was removed.

Identify two specific examples of data redundancy found in this table. [2]

> [!Answer]
> The employee details for Sarah (EmpID E001, Name Sarah, Dept FX) are repeated three times, once for each course she takes.""The course details for 'Excel Basics' (CourseID C101, CourseName Excel Basics, CourseType Skills, Fee 150) are repeated twice, once for each employee (Sarah and James) who takes the course.

Explain why the table is in first normal form (1NF).[2]

> [!Answer]
> The table is in **1NF** because every cell contains a single, atomic value (e.g., each cell has one name, one course ID, one date). Furthermore, there are no repeating groups of columns; each attribute is defined only once.

Explain by giving a specific example why the table is not in second normal form (2NF).[2]

> [!Answer]
> The table is not in **2NF** because it contains partial dependencies. The composite **primary key** is (EmpID, CourseID). However, the employee's Name and Dept are dependent only on EmpID (part of the key), not the full key. For example, knowing EmpID E002 is enough to determine the Name is James and the Dept is CS, without needing to know the CourseID.

State a specific transitive dependency example found in the table.[1]

> [!Answer]
>
> * CourseID determines CourseName, and CourseName determines CourseType. Therefore, CourseID transitively determines CourseType via CourseName."

Construct all the table(s) for a normalised database and populate them with the data given in the flat file table.[5]

> [!Answer]
> Construct all the table(s) for a normalised database and populate them with the data given in the flat file table.
>
> * Employees (EmpID, Name, Dept)EmpID | Name | DeptE001 | Sarah | FXE002 | James | CSE003 | Priya | HRE004 | John | FXCourses (CourseID, CourseName, CourseType, Fee)CourseID | CourseName | CourseType | FeeC101 | Excel Basics | Skills | 150C102 | PowerPoint Pro | Skills | 200C103 | Strategic Writing| Comms | 550C104 | Leadership 101 | Soft Skills| 400Registrations (EmpID, CourseID, Date)EmpID | CourseID | DateE001 | C101 | 01-10E001 | C102 | 01-15E001 | C103 | 01-20E002 | C101 | 01-12E002 | C103 | 01-22E003 | C102 | 01-18E004 | C104 | 01-08

---

<a id="toc-non-relational-databases"></a>

# Non-relational Databases

<a id="toc-non-relational-databases-syntax"></a>

### Syntax

##### 2025 YIJC Prelim P1 Q6)

**A software developer uses MongoDB to store the data of video games from various publishers on their online platform.**

Explain two key advantages of using a NoSQL database like MongoDB over a relational (SQL) database for the platform. [2]

> [!Answer]
>
> * Schema Flexibility / Dynamic Schema: **NoSQL** databases do not require a fixed, pre-defined schema. Each document can have a different structure, which is ideal for storing game data that may have varying attributes (e.g., some games have DLC, others have multiplayer modes). This allows for easier and faster adaptation to changing data requirements.
>
> * Scalability / Horizontal Scaling: **NoSQL** databases are designed to scale out horizontally across many commodity servers, which is more efficient and cost-effective for handling large amounts of data and high user traffic (like a public gaming platform) than the vertical scaling (upgrading a single server) typical of SQL databases.

**A database named gameverse has already been created. Inside it, a collection named games exists to store individual game documents. The fields for the documents in this collection are title, publisher, metacritic_score, and platforms which uses an array.**

**Write a command to insert a new document with the following details into the games collection: title: "Eclipse of Destiny" publisher: "Nexus Studios" metacritic_score: 87 platforms: ["PC", "PlayStation 5", "Xbox Series X"] [3]**

> [!Answer]
>
> * Write a command to insert a new document...
>
> ```text
> db.games.insert_one({ "title": "Eclipse of Destiny", "publisher": "Nexus Studios", "metacritic_score": 87, "platforms": ["PC", "PlayStation 5", "Xbox Series X"]})
>
> ```

**Using the find_one() or find_many() methods, write commands to perform the following queries on the games collection:**

Find one game that is published by "Nexus Studios". [2]

> [!Answer]
>
> * Find one game that was published by "Nexus Studios".
>
> ```text
> db.games.find_one({"publisher": "Nexus Studios"})
>
> ```

Find all games with a Metacritic Score greater than or equal to 90. [2]

> [!Answer]
>
> ```text
> db.games.find_many({"metacritic_score": {$gte: 90}})
>
> ```

Find all game titles that are available on the "PlayStation 5" platform. [3]

> [!Answer]
>
> ```text
> db.games.find_many({"platforms": "PlayStation 5"}, {"title": 1, "_id": 0})or db.games.find_many({"platforms": {‘$in’: ["PlayStation 5"]}}, {"title": 1, "_id": 0})
>
> ```

---

<a id="toc-computer-networks"></a>

# Computer Networks

<a id="toc-computer-networks-lan-local-area-network"></a>

### LAN (Local Area Network)

##### 2025 ASRJC Prelim P1 Q6)

**6 Yee Kee Yah Ltd operates 3 furniture outlets in Singapore. The company has decided to implement a computerised inventory management system with a web app interface.**

**(a) The IT team has recommended using client-server architecture for each outlet’s inventory system.**

(i) Explain what is meant by a client-server model in this context. [2]

> [!Answer]
> A client-server model is a network architecture where the server stores and manages the inventory database, while clients (individual computers at workstations) request data and services from the server. The server processes client requests and sends back the requested data.

(ii) Identify three types of software required to implement this client-server system. [3]

> [!Answer]
> Database management system (DBMS) software – to manage the inventory database
> Web server software – to serve the web app and handle client requests
> Web browser software – for clients to access the inventory system

(iii) Write down one advantage of adopting a client-server system in this context. [1]

> [!Answer]
> Centralised data storage ensures all staff access the same up-to-date inventory information.

**(b) Currently, each outlet operates independently. To improve coordination, the furniture company wants to connect all three outlets to its headquarters so they can share inventory data and coordinate stock transfers.**

(i) Explain how LAN and WAN technologies would work together to support the company’s inventory management operations and describe the role of routers in this network setup. [3]

> [!Answer]
> Each outlet and the headquarters uses a **LAN** to connect devices within that location. A **WAN** connects all four LANs (three outlets plus HQ) together across these distant locations. Routers connect each location's **LAN** to the **WAN** and direct data **packets** between different networks, enabling efficient inventory data sharing and stock transfer coordination between all outlets and headquarters.

(ii) Explain how an intranet would benefit the operations. [2]

> [!Answer]
> An **intranet** provides a private internal network accessible only to company staff across all locations, allowing secure sharing of inventory data and internal communications. External parties cannot access the **intranet**, which helps protect sensitive company information and inventory data from external threats while enabling coordinated operations.

(iii) State two methods for ensuring the security of access to the inventory management application. [2]

> [!Answer]
> Implement user **authentication** (through usernames and passwords, 2FA) to ensure only staff can access the application.
> Use role-based access control (setting different permission levels for different staff roles), reducing the risk of unauthorised data access and changes.

(iv) Suggest two methods to secure the network infrastructure. [2]

> [!Answer]
> Deploy **firewall** to monitor and filter incoming and outgoing network traffic.
> Use data **encryption** (such as using VPN) to secure data transmitted across the **WAN**, preventing interception.

**(c) The company also keeps track of customer purchase history, delivery addresses and payment information.**

(i) Explain the difference between data backup and data archiving of the customer and sales data. [2]

> [!Answer]
> Data **backup** is the process of making a copy of the current, active customer and sales data so it can be quickly restored in case the original data is lost or corrupted. It is used for disaster recovery.
> Data archiving involves moving older, inactive data to a separate storage location for long-term retention and compliance purposes. It is meant for future reference.

(ii) Describe two specific PDPA compliance measures Yee Kee Yah Ltd must implement when handling customer data. [2]

> [!Answer]
> Any two reasonable answers with explanations. For example:
> Consent obligation: The company must inform customers about the purpose of collecting their **personal data** and obtain their consent before collecting, using or disclosing it.
> Data protection obligation: The company must secure customer data by using safeguards such as **encryption** and regular security audits
> Access and correction obligation: The company should provide customers with the right to access their **personal data** and request corrections if the data is inaccurate.

---

<a id="toc-computer-networks-internet"></a>

### Internet

##### 2025 DHS Prelim P1 Q2)

**2 A company has a website. Users use the internet and the world wide web to access the website.**

(a) Describe the difference between the internet and the world wide web. [1]

> [!Answer]
> (1)
>
> * The **internet** is the infrastructure
>
> * The world wide web is a collection of web pages

**(b) Data packets are transmitted across a network from one computer to another computer. Describe the structure of a data packet. [1]**

> [!Answer]
> All three from:      (1)
>
> * A **packet** is split into three different sections
>
> * … the header
>
> * … the payload
>
> * … the trailer

**(c) Explain what is meant by the term router and describe the function of a router in a computer network. [2]**

> [!Answer]
> network.
> A **router** is a device in a network which holds information about the addresses of computers in the
> network (or other networks) …      (1)
> Any one of the function of a **router**     (1)
> … and can direct data to the correct computer
> … and can direct data around network in (most) efficient way
> … and act as a gateway connecting to a larger network.

**(d) Explain what is meant by circuit switching and packet switching in a computer network and give two advantages of packet switching over circuit switching. [4]**

> [!Answer]
> Explain what is meant by **circuit switching** and **packet switching** in a computer network and give
> two advantages of **packet switching** over **circuit switching**.
>
> **Circuit switching**:       (1)
> Path is set up between the sender and receiver
> All data follows the same path, in order
> Path cannot be used by any other data
>
> **Packet switching**:
> Data split into **packets**
> Each **packet** may be transmitted by different routes
> **Packets** may arrive out of order and are re-assembled
>
> **Packet** switch preferred:
> Better security as it is very difficult to intercept
> Makes more efficient use of data lines as there is no waiting during gaps
> Less likely to be affected by network failure because multiple paths used

**(e) A website of a company may collect information of the customers,**

(i) State the meaning of privacy of data. [1]

> [!Answer]
> A website of a company may collect information of the customers.
>
> * Ensuring data can only be accessed by / disclosed to authorised persons Or
>
> * Ensuring data cannot be accessed by / disclosed to unauthorised persons

(ii) State the meaning of integrity of data. [1]

> [!Answer]
>
> * Ensuring the accuracy / completeness / consistency of data (during / after processing)
>
> * Ensuring the data is up to date

(iii) Describe the following threats to a computer system. [4]

Spyware
Phishing email

> [!Answer]
> **Phishing** email (max 2)
>
> * The email pretends to be from an official body
>
> * ... persuading individuals to disclose private information // by example such as bank details
>
> * ... or requesting **authentication** by redirecting to an unofficial/unauthorised website // inviting a user to
>
> click a link
>
> **Spyware** (max 2)
>
> * **Malware** downloaded without the user’s knowledge
>
> * ... which secretly records the user’s actions / keystrokes on the computer
>
> * ... and sends logs of the actions to a third party

---

<a id="toc-computer-networks-packets"></a>

### Packets

##### 2025 NYJC Prelim P1 Q6)

6 (a) Describe how networking protocols address the following problems:

(i) Data packets may arrive out of order and require reassembly [2]

> [!Answer]
> 6.0	Networking, Data Structures, Testing
>
> Each **packet** is tagged with a sequence number
>
> * The sequence number is included in the header to allow sequential reassembly

(ii) Data packets may be corrupted in transit [2]

> [!Answer]
> The **packet** data is hashed to produce a checksum
>
> * The recipient verifies the checksum against its hashed data

(b) State the time complexity of the following operations:

(i) adding an item to an array [1]

> [!Answer]
> $O(n)$

(ii) adding an item to a BST. [1]

> [!Answer]
> $O(\log n)$

**(c) A data structure is used to hold data packets that are being reassembled. Describe one advantage and one disadvantage of each data structure for packet reassembly.**

(i) Statically allocated array [3]

(ii) Dynamically allocated BST. [3]

> [!Answer]
> 6ci,ii	array: $O(1)$ random read or write
>
> * Enables incoming data **packets** to be written in sequence quickly / in constant time regardless of message size
>
> * array: number of **packets** must be known beforehand
>
> BST: number of **packets** need not be known upfront
>
> * array: lower memory allocation overhead for reassembly of data **packets** (since all required memory is allocated upfront)
>
> BST: maintains **packets** in sorted order
> BST: **packets** arriving mostly in sequence might result in worst case performance due to unbalanced tree
> BST: requires $O(n)$ **in-order** traversal to retrieve data **packets**
>
> * if router has limited memory / handles large number of connections:
>
> * BST might cause memory fragmentation
>
> * array might use memory inefficiently (for data **packets** taking a long time to arrive)

**Not all data packets require reassembly; only data packets that are too large to be sent in a single packet will need to be split into multiple packets , which are then reassembled by the recipient. A network router uses the following algorithm to process incoming data packets: 1. Allocate sufficient memory to hold data for the incoming packet. 2. If the data packet does not require reassembly, free the allocated memory and pass the data to the appropriate program. 3. If the data packet requires reassembly, instantiate an array with sufficient slots in the allocated memory to store data fragments as they arrive. 4. When all data fragments have been received, pass the data to the appropriate program. The program passed initial user testing and ran successfully for a few weeks before the router suddenly crashes.**

(d) State the type of error that occurred. [1]

> [!Answer]
> Runtime error

(e) Explain why the error was not caught in initial user testing. [2]

> [!Answer]
> Suitable highlight of test inadequacy, e.g.:
>
> * The initial testing was not carried out over a sufficiently long period of time ...
>
> * Testing did not cover conditions that crashed **router** ...
>
> * Elaboration / evidence / explanation:
>
> * ... as the program ran for multiple weeks before reaching a crash condition
>
> * ... such as high traffic levels
>
> * ... because the **router** had sufficiently high memory

(f) Describe the change(s) required in the algorithm to resolve the error. [1]

-- END OF PAPER –

> [!Answer]
> Allocated memory should be freed after either branch terminates / the branch that requires reassembly should free allocated memory before end

---

##### 2025 RI Prelim P1 Q7)

**7 A food delivery company operates a fleet of riders who rely on a mobile app to receive orders and navigate to customers. The app communicates with a central server located in the company’s data center. Riders connect to the internet using either public Wi-Fi or mobile networks as they move through different locations.**

**(a) When a rider logs into the app, the device sends a request to http://api.foodtrack.sg. Explain the role of the Domain Name System (DNS) in this process. [2]**

> [!Answer]
> 7
>
> The Domain Name System (**DNS**) translates the human-readable web address
> api.foodtrack.sg into its corresponding **IP address** (e.g. 203.0.113.15) so the rider’s
> device can locate and communicate with the server.
>
> * identifying that **DNS** performs a translation/lookup
>
> * specifying the result is an **IP address**

**(b) Each rider’s device has both a MAC address and an IP address.**

(i) State the purpose of each type of address. [2]

> [!Answer]
> MAC: A unique identifier hard-coded into the network interface card (NIC) of a
> device. Used for communication within the local network segment (e.g., Wi-Fi or
> **LAN**).
> IP: A logical address assigned to a device that identifies its location in a larger
> network (**Internet**). Used for routing data between networks.

(ii) Explain why both are necessary in network communication. [2]

> [!Answer]
> Both are needed because data travels across different networks using IP addresses
> for global delivery, but once the data reaches the destination network, the MAC
> address is used for final delivery to the correct device.

**(c) Describe the structure of a data packet that may be transmitted between the rider’s device and the central server. Your answer should include three components commonly found in a packet, and explain clearly the purpose of each component. [6]**

> [!Answer]
> (Any three, correct component and brief explanation of purpose)
>
> 1. Destination Address
>
> * Identifies the **IP address** of the receiving device (e.g. the central server)
>
> * Used by routers to ensure the **packet** reaches the correct destination
>
> 2. Sequence Number
>
> * Indicates the position of the **packet** in a sequence of **packets** from a
>
> larger message
>
> * Helps the recipient reassemble data in the correct order
>
> 3. Checksum (Error-checking field)
>
> * A calculated value based on the data in the **packet**
>
> * Used by the receiver to verify integrity and detect any transmission
>
> errors
> 4. Source Address – IP of the sender (rider’s device); allows reply to be sent back
> 5. Payload – The actual data, e.g. GPS coordinates, delivery status
> 6. **Protocol** field – Identifies the type of data or how it should be processed
> 7. Time to Live (TTL) – Prevents **packets** from circulating endlessly by limiting hops

**The company is exploring ways to improve the system’s resilience and efficiency, especially in areas with weak or unstable internet connectivity. One proposal is to allow rider devices to share updates with each other using a Peer -to-Peer (P2P) model.**

**(d) Explain one advantage and one disadvantage of using a Peer-to-Peer model in this food delivery scenario. Your answer should be based on how the model helps or hinders delivery operations in real-world conditions. [4]**

> [!Answer]
> Advantage 1: Riders can share updates (e.g., delivery status, traffic alerts) directly
> with nearby peers without **internet**, which is helpful in areas with weak connectivity.
>
> Advantage 2: Reduces reliance on the central server, potentially decreasing latency
> and improving resilience if the server is temporarily unreachable.
>
> Disadvantage: P2P requires devices to be physically near each other for
> communication and can lead to inconsistent or delayed updates if devices don’t sync
> promptly.
>
> Security - Difficult to monitor the flow of data and ensure security, especially as more
> devices are added. Raises risk of malicious attacks, which could hinder delivery
> operations as riders may be unable to communicate with one another.
>
> **2m** per advantage (1 for idea, 1 for clear explanation)
>
> **2m** for disadvantage (1 for idea, 1 for clear explanation)

---

##### 2025 VJC Prelim P1 Q6)

**A packet switching network breaks data into packets, which are sent independently across the network and reassembled at the destination.**

**Describe how networking protocols address the following problems: Data packets may arrive out of order and require reassembly [2]**

> [!Answer]
>
> * Each **packet** is tagged with a sequence number
>
> * The sequence number is included in the header to allow sequential reassembly
>
> * A sequence number is assigned for each **packet** to ensure correct ordering and eventual reassembly of the original message.#No need to differentiate between **TCP** and **UDP**.

Data packets may be corrupted in transit.[2]

> [!Answer]
>
> * The **packet** data is hashed to produce a checksum
>
> * The recipient verifies the checksum against its hashed data
>
> * ORThe receiver checks the **packets** as it reassembles
>
> * If any are corrupted in transit, they are retransmitted
>
> * Each **packet** has a sequence number. The receiver checks the **packets**, and if any are corrupted in transit, they are retransmitted; this supports correct reassembly of the original message. #No need to differentiate between **TCP** and **UDP**.

**State and explain the time complexity of the following operations: Adding an item to a sorted array [2]**

> [!Answer]
>
> * $O(n)$
>
> * Need to traverse the whole array if the item is to be inserted at the end

Adding an item to a balanced binary search tree (BST).[2]

> [!Answer]
>
> * $O(\log n)$
>
> * At every level, traverse to either left sub tree or right sub tree. If need to traverse to the leaf node, we would have traversed log n of the tree

**A data structure is used to hold data packets that are being reassembled.**

**Describe one advantage and one disadvantage of each of the following data structures for packet reassembly. Statically allocated array [2]**

> [!Answer]
>
> * Advantage: Any one of the following
>
> * $O(1)$ random read or write. Enables incoming data **packets** to be written in sequence quickly Avoids memory fragmentation because memory blocks are contiguous and aligned.Enables faster reassembly because memory blocks are contiguous and aligned.Disadvantage:  Any one of the following
>
> * Number of **packets** must be known beforehandInflexible/fixed size **Static** allocation is used for arrays, which are not easily resized.*Can accept memory wastage.

Dynamically allocated BST.[2]

> [!Answer]
>
> * Advantage: Any one of the following
>
> * Number of **packets** need not be known upfront.$O(\log n)$ addition of data **packets** in order Can grow as **packets** arrive BST supports insert operations, allowing scalable reassembly for varying **packet** counts *Can accept minimise memory wastage.Disadvantage:  Any one of the following
>
> * **Packets** arriving mostly in sequence might result in worst case performance due to unbalanced tree More complex implementation **Dynamic memory** brings overhead (slower and more complex memory management)Can cause memory fragmentation.

---

<a id="toc-computer-networks-tcp-ip-model"></a>

### TCP/IP Model

##### 2025 RVHS Prelim P1 Q7)

**7. Answer all the questions.**

**a) You are the network engineer of a company. For each of the following scenarios:**

* **Identify which layer of the TCP/IP model is most directly involved.**
* **Suggest what you would check to troubleshoot the issue.**

**Scenarios:**

i. Users can connect to the Internet but cannot load the company’s website in their browser.

> [!Answer]
> Application layer
> The engineer checks:
>
> * whether the web server application (HTTP/HTTPS) is running
>
> * whether the **DNS** resolution works correctly
>
> * if the application itself has crashed or configuration is wrong.
>
> 2

ii. A computer cannot even reach other machines on the same LAN, and pinging local devices fails.

> [!Answer]
> Network Access layer
> The engineer checks:
>
> * Faulty Ethernet cable
>
> * Wi-Fi not associated
>
> * ARP resolution failure
>
> 2

iii. The database server is running. Its IP address is reachable. However, client sessions to the database cannot be established and often time out, so applications cannot connect.

> [!Answer]
> Transport layer
> The engineer checks:
>
> * Correct port number used
>
> * **Firewall** rules
>
> * Session setup process
>
> 2

**iv. A user can connect to the local network but cannot reach external networks. [8]**

> [!Answer]
> **Internet** layer
> The engineer checks:
>
> * **IP address**
>
> * subnet mask,
>
> * default gateway,
>
> * routing configuration
>
> 2

b) State two differences between TCP and UDP. [2]

> [!Answer]
> **TCP** is connection-oriented, **UDP** is connectionless
> **TCP** provides reliable delivery through knowledgements, retransmissions,
> and error checking ensure data arrives in order and without los t. **UDP**
> provides best-effort delivery.
> 2

**Company Z, a healthcare provider, has a central database storing patient**
**records. One employee, John, receives an email with an attachment claiming to be an urgent invoice from a medical supplier. The attachment is actually malicious software that exploits outdated software on John’s computer. When John opens the file, the malware quickly spreads through the network and encrypts the company’s database, making patient records inaccessible.**

**c) Identify the human mistake that allowed the attacker to carry out the attack. [1]**

> [!Answer]
> opened a **phishing** email attachment without verifying its authenticity 1

d) Name the type of malware that encrypted the company’s database. [1]

> [!Answer]
> **ransomware** 1

**e) State one recovery measure that Company Z should implement to reduce the impact in the future. [1]**

> [!Answer]
> Recovery measure: Maintain regular backups of critical data so it can be
> restored if encrypted.
> 1

**f) State one preventive measure that Company Z should implement to prevent such incidents in the future. [1]**

> [!Answer]
> Preventive measure: Keep systems patched and updated, and use
> email filtering and user awareness training to reduce **phishing** risk.
> 1

---

<a id="toc-network-security"></a>

# Network Security

<a id="toc-network-security-malware-attacks"></a>

### Malware Attacks

##### 2025 TJC Prelim P1 Q6)

**6A commercial bank is strengthening its cybersecurity framework after experiencing multiple security breaches.**

(a)(i) Explain how a Trojan horse differs from a worm in terms of propagation and payload delivery. [2]

> [!Answer]
> **Trojan**: Masquerades as legitimate software and tricks users to execute it, does not replicate itselfWorm: Self-replicating, spreads autonomously through networks

(ii) Describe two characteristics that make ransomware particularly dangerous to financial institutions. [2]

> [!Answer]
> Encrypts critical financial dataCauses operational disruption during attacksHigh ransom demands target valuable data(Any 2 points)

**(b) The bank has deployed a firewall and Intrusion Prevention System (IPS). Explain why implementing both a firewall and IPS provides better security than using either system alone. [2]**

> [!Answer]
>
> * **Firewall** filters basic malicious traffic
>
> * IPS detects sophisticated attacks in payloads
>
> * Defense-in-depth approach(Any 2 points)

**(c) The bank must choose between biometric authentication and security tokens for employee access to sensitive systems. Evaluate which method would provide better security, giving two reasons for your choice. [3]**

> [!Answer]
>
> * Biometric **Authentication** Preferred Because:1.Unique physiological traits2.Cannot be lost/stolen like tokens3.Harder to replicate than token codesOR
>
> * Security Tokens Preferred Because:1.Not affected by physical changes2.Easier to revoke/reissue3.No biometric data storage risks(Accept either position with valid reasoning)

(d) Describe the complete process of generating and verifying a digital signature for an electronic funds transfer request. [4]

> [!Answer]
> Hash document using a hashing algorithm to produce a hash digestEncrypt hash digest with sender's **private key** and send message with cipher to recipientRecipient decrypts cipher using sender's **public key** to obtain hash digest and verify the sender’s identityRecipient hashes document using the same hashing algorithm, compares it with the hash digest to ensure that the original document has not been tampered with.

**(e) A bank employee wishes to email a contract document to a customer. To prevent tampering with the contract document, he attaches his digital certificate to the email alongside with the document. Explain why this is insufficient to ensure the integrity of the document. [2]**

* End of Paper -

> [!Answer]
> A digital is a method of ensuring that an encrypted message is from a trusted source as they have a certificate from a Certification Authority that confirms that the individual is who they claim to be in an online communication.However, it is unable to verify the authenticity of message content and whether the message has been tampered with.

---

<a id="toc-network-security-secure-access-method"></a>

### Secure access method

##### 2025 ACJC Prelim P1 Q6)

**6A user on a website has to fill out a form to register for an account. The user needs to create a username and a password. The password needs to be at least 8 characters long and contain at least one uppercase letter, one lowercase letter, one digit, and one punctuation symbol.**

(a) State the difference between data validation and data verification. [2]

> [!Answer]
> **Data validation**: Ensuring that data fits a particular format suitable for the algorithmData verification: Ensuring that the data inputted / transmitted is the same as what was intended

(b) In this context, describe how data validation can be carried out. [2]

> [!Answer]
> **Data validation** can be carried out via length check (8 characters) and format check (contains required characters)

(c) In this context, describe how data verification can be carried out. [2]

> [!Answer]
> **Data verification** can be carried out by asking user to enter password twice, and comparing to make sure both entered password strings are identical

**The data on the form is sent from the user’s computer to the website’s server over the internet. The password is sent via a public key cryptography system.**

(d) Describe how public key cryptography prevents a third party from being able to see the password. [2]

> [!Answer]
> The data is encrypted using the server’s **public key**. It can only be decrypted and read using the server’s **private key**, which is unknown to a third party.

(e) Describe how the three-way handshake in the TCP protocol ensures that the data is sent completely and accurately. [3]

> [!Answer]
>
> * The three-way handshake takes place before the data transfer to ensure that the connection is reliable.(1) The user first sends a synchronization **packet** to the server to check that the server is ready to receive.(2) The server sends an acknowledgement back to the user and sends its own synchronization **packet** to the user.(3) The user acknowledges the server’s synchronization **packet**.
>
> * After this, the actual data **packets** are transmitted.

**To prevent passwords from being leaked, the server’s database does not store users’ passwords in raw form, but in a hashed form instead.**

(f) Explain how this prevents passwords from being leaked, and describe what happens when a user tries to log in with an incorrect password. [3]

> [!Answer]
>
> * Since a hash is irreversible, it is impossible to recover the original password from the hashed form. This ensures that even if the server’s database is compromised, it is not possible to recover the list of passwords.
>
> * When a user logs in, the password entered by the user is hashed and this is compared to the hashed password stored under the user’s name in the database. If they do not match, then the user has logged in with an incorrect password and will be prompted to retry.

(g) Describe another security feature the server can use to ensure security of the user passwords. [1]

> [!Answer]
> The server can use 2-factor **authentication** to ensure that the user is who he claims to be.

**When the server sends a message to the user, it uses a digital signature to authenticate the message.**

(h) Describe how the digital signature is generated. [2]

> [!Answer]
> The message is hashed and then encrypted with the sender’s (server’s) **private key** to generate the **digital signature**.

**(i) Suppose the message is intercepted and edited by a malicious third party before it reaches the user. Describe how the user can detect the fact that the message has been intercepted and edited. [3]**

> [!Answer]
> The user hashes the message. The user also decrypts the **digital signature** using the sender’s **public key**. If the decrypted signature matches the hashed message, then the message is authentic. If they do not match, then the message has been edited.

---

<a id="toc-network-security-digital-signature"></a>

### Digital signature

##### 2025 NYJC Prelim P1 Q4)

**4 (a) Describe how a digital certificate is involved in producing a digital signature for a document. [4]**

> [!Answer]
> 4.0	Network Security
>
> message is hashed (using a pre-determined algorithm) to produce a digest
>
> * sender encrypts digest ...
>
> with **private key** to produce a cipher (**digital signature**)
>
> * cipher and message are sent to recipient together with **digital certificate** (**public key**) /
>
> **public key** is used to decrypt the **digital signature**

**A CEO wishes to email a contract document to a customer. To prevent tampering with the contract document, he attaches his digital certificate to the email alongside the document.**

(b) Explain why this is insufficient to ensure the integrity of the document. [2]

> [!Answer]
> a **digital certificate** authenticates a sender('s **public key**, through a certificate authority), but is unable to verify authenticity of the message contents
>
> * does not verify document contents / no way to know if message has been tampered with

---

##### 2025 VJC Prelim P1 Q5)

**A commercial bank is strengthening its cybersecurity framework after experiencing multiple security breaches.**

Compare between a Trojan horse and a worm in terms of how they spread and how they are executed in the targeted network or device.[2]

> [!Answer]
>
> * **Trojan**: Masquerades as legitimate software | **Worm**: Self-replicating
>
> * **Trojan**: requires user execution | **Worm**: spreads autonomously through networks

Describe two characteristics that make ransomware particularly dangerous to financial institutions.[2]

> [!Answer]
>
> * Encrypts critical financial data
>
> * Causes operational disruption during attacks
>
> * High ransom demands target valuable data

**The bank has deployed a firewall and Intruder Protection System (IPS).**

Explain why implementing both a firewall and IPS provides better security than using either system alone.[2]

> [!Answer]
>
> * **Firewall** filters basic malicious traffic
>
> * IPS detects sophisticated attacks in payloads
>
> * Defense-in-depth approach

Describe the complete process of generating and verifying a digital signature for an electronic funds transfer request.[3]

> [!Answer]
>
> * Hash document
>
> * Encrypt hash with sender's **private key**
>
> * Recipient verifies with **public key**

**The bank must choose between biometric authentication and security tokens for employee access to sensitive systems.**

Evaluate which method would provide better security, giving two reasons for your choice.[3]

> [!Answer]
>
> * Biometric **Authentication** Preferred Because:Unique physiological traits
>
> * Cannot be lost/stolen like tokens
>
> * Harder to replicate than token codes
>
> * OR
>
> * Security Tokens Preferred Because:Not affected by physical changes
>
> * Easier to revoke/reissue
>
> * No biometric data storage risks

---

<a id="toc-network-security-authentication"></a>

### Authentication

##### 2025 YIJC Prelim P1 Q5)

**A company is setting up a new office with a Local Area Network (LAN) that is connected to the internet. A web server on the LAN hosts a popular e-commerce website.**

Give two reasons why communication protocols are essential for the smooth operation of the office LAN and for reliable access to the internet. [2]

> [!Answer]
>
> * Explain two reasons why communication protocols are essential...
>
> * To provide a standard set of rules that all devices must follow, ensuring different hardware and software from various vendors can communicate and understand each other (interoperability).
>
> * To define how data is formatted, addressed, transmitted, routed, and received to ensure it arrives correctly and completely at its intended destination.

**The web server's admin portal uses only a username and password for authentication.**

Explain why this approach is considered a security weakness. [1]

> [!Answer]
>
> * Explain why single-factor **authentication** is a security weakness.
>
> * It relies on only one type of evidence ("something you know"), which is a single point of failure. This makes it vulnerable to being compromised through weak passwords, **phishing** attacks, keylogging **malware**, or database breaches.

Describe how the process of authentication can be improved.[2]

> [!Answer]
>
> * Describe how the **authentication** system can be improved.
>
> * Implement Multi-Factor **Authentication** (MFA), which requires a user to provide two or more distinct verification factors.
>
> * Description of a second factor: Adding a requirement for:"Something you have" (e.g., a code from a smartphone authenticator app like Google Authenticator, or a hardware security key),or "Something you are" (e.g., a biometric scan like a fingerprint or facial recognition).

State and describe three network security and data protection measures the company should implement to protect the web server and ensure the availability and integrity of the website. [3]

> [!Answer]
>
> * Describe three network security... measures... (1 mark per measure (any 3 measures)**Implement a Firewall: To filter incoming and outgoing network traffic based on security rules, blocking unauthorized access and helping to mitigate Denial-of-Service (DoS) attacks that threaten availability.
>
> * Utilize an Intrusion Detection or Prevention System (IDS or IPS): To actively monitor network traffic and block detected threats and attack patterns in real-time.
>
> * Enforce Regular Software Updates/Patching: To promptly fix known vulnerabilities in the server's operating system and software.

**All devices on the LAN use private IP addresses, but the web server is accessible from the public internet.**

Explain the difference between a private IP address and a public IP address. [2]

> [!Answer]
>
> * Explain the difference between a private and a public **IP address**.
>
> * Public IP addresses are globally unique addresses assigned by an ISP that are used to identify devices on the public **internet**. They are directly routable and accessible from anywhere online.
>
> * Private IP addresses are from reserved ranges (e.g., 192.168.x.x) used to identify devices within a local network. They are not routable on the public **internet** and cannot be used for direct communication online.

Describe how a client from the public internet is able to communicate with the web server located within the LAN that uses a private IP address. Your answer should identify the relevant network technology used.[4]

> [!Answer]
>
> * Describe the process...
>
> * The relevant technology is Network Address Translation (NAT), performed by the **router**.
>
> * The web server is assigned a **static** private **IP address** (e.g., 192.168.1.100).
>
> * The company's **router** has a single public **IP address** assigned by its ISP.
>
> * The **router** is configured with port forwarding. A rule is created that tells the **router** to automatically forward any incoming traffic on specific ports (e.g., port 80/HTTP, 443/HTTPS) to the web server's private **IP address**.

---
