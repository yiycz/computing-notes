---
tags:
  - theory
  - data-representation
---
# Data Validation

### Definition 

Data validation is a process of **ensuring** that the input data supplied to a system **satisfies a set
of rules such that it is **sensible, complete, and within acceptable boundaries.** 

Its purpose is to **avoid data errors**. It does not guarantee that data is accurate.

### Errors

- **Transcription errors**: a single incorrect character being entered For eg, a correct postal code $449035$ could be wrongly entered as $449036$.
- **Transposition error:** two digits are accidentally swapped.

| Validation Check | Description                                                                                                                                                             | Example                                                                                                                                             |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| Range Check      | Checks that a value falls within the specified range.                                                                                                                   | The marks of the A level H2 Computing Paper 1 must fall within the specified range of 0 to 100 and not anything less than 0 or more than 100 marks. |
| Format Check     | Checks the data is in the right format.                                                                                                                                 | A date has to be dd/mm/yyyy.                                                                                                                        |
| Length Check     | Checks the data isn't too short or too long.                                                                                                                            | A telephone number must have a length of 8 numbers.                                                                                                 |
| Presence Check   | Checks that data has been entered into a field.                                                                                                                         | Ensure that an entry field is not left blank.                                                                                                       |
| Check Digit      | An extra digit added to the end of a code number, which has been calculated from the digits of the code number. This ensures the code number has been entered properly. | —                                                                                                                                                   |
An error where changes to multiple bits or bytes cancel each other out, resulting in the same checksum being calculated.

### Workflow for data validation

- having a prompt to get user input 
- apply appropriate data validation techniques on user input 
- output relevant error message for invalid data and allow re-entry until user input valid data

# Data Verification

### Definition

Verification is the process of **getting the user to confirm** that the data entered was what was
**intended to be entered.** 

Essentially, it is a way of preventing errors when data is copied from one medium to another. It does not check if the data makes sense or is within acceptable boundaries. It only checks that the data entered is identical to the original source.

- Double entry is one method of verification.
  - The process of entering data twice, with the second entry being compared with the first is to ensure that it is accurate. It is common in batch processing for a second data entry operator to key in a batch of data to verify it. Another example is when setting a password, a user would be asked to key in the password a second time to ensure that the passwords match up.

- Proofreading data is another method that **involves someone checking the data entered against** the original source to ensure that the data match.

# Difference between data validation and verification

- Verification only checks the data is **copied correctly**
- Validation checks are **carries out automatically by the computer**
- Verification does not check if data is **reasonable / sensible**


# Program Errors

| Type of Error | Description | Example |
|---|---|---|
| **Syntax errors** | An error that occurs when a command **does not follow the expected syntax of a language.** | `IF` without `THEN` |
| **Runtime errors** | An error that only occurs when the programme is running and is **difficult to foresee** before a programme is compiled and run. | Divide by zero |
| **Logical errors** | An error that causes the programme to **output** an **incorrect answer** when the programmer makes **a mistake in their logic for some parts** of the programme. | `count = count - 1` should be `count = count + 1` |


# Test Data

| Type                               | Description                                                           |
| ---------------------------------- | --------------------------------------------------------------------- |
| **Normal / valid**                 | Typical data values that are valid and will be accepted by the system |
| **Abnormal / invalid / erroneous** | Data values that the system should not accept or should be rejected   |
| **Extreme / boundary**             | Data values that are at the extreme ends of the valid range           |
