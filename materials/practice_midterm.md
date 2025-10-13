# CMPSC 100 Practice Midterm Exam
**Computational Expression - Fall 2025**

## Midterm Exam Structure

**Note:** This is a practice exam that is similar to the actual midterm exam but may not cover all concepts that will appear on the actual exam. Use this to familiarize yourself with the format and types of questions. Review all slides, labs, and activities to study a comprehensive list of topics.

Midterm exam is closed notes, closed devices (no computer, no phone, etc.).

**Time Limit:** 50 minutes  
**Total Points:** 10 points

---

## Part I: Multiple Choice (5 points)
*Choose the best answer for each question. 0.5 point each.*

### Question 1
Which of the following is a valid Python variable name following proper naming conventions?
- A) `2cats`
- B) `my age`
- C) `student_count`
- D) `if`

### Question 2
What will this code output?
```python
score = 5
score = score + 3
print(score)
```
- A) 5
- B) 8
- C) 53
- D) Error

### Question 3
Which function performs explicit type conversion from string to integer?
- A) `str()`
- B) `int()`
- C) `float()`
- D) `input()`

### Question 4
What will this code output?
```python
student_name = "maya"
print(student_name.upper())
```
- A) maya
- B) MAYA
- C) Maya
- D) Error

### Question 5
What will this conditional statement output?
```python
temperature = 16
if temperature >= 75:
    print("Hot")
elif temperature >= 60:
    print("Warm")
else:
    print("Cold")
```
- A) Hot
- B) Warm
- C) Cold
- D) Error

### Question 6
What does `range(3)` create for use in a for loop?
- A) [1, 2, 3]
- B) [0, 1, 2]
- C) [0, 1, 2, 3]
- D) [3]

### Question 7
Which statement about Python error types is MOST accurate?
- A) Syntax errors occur when code runs but produces wrong results
- B) Runtime errors happen when Python can't understand the code structure
- C) Logic errors cause the program to crash with an error message
- D) Syntax errors prevent the program from running at all

### Question 8
Given this directory structure, if you are currently in the `lab01` directory, what command would take you to the `lab03` directory?
```
home/
├── student/
│   ├── cmpsc100/
│   │   ├── lab01/          ← You are here
│   │   ├── lab02/
│   │   └── lab03/          ← You want to go here
│   └── documents/
└── shared/
```
- A) `cd lab03`
- B) `cd ../lab03`
- C) `cd /lab03`
- D) `cd cmpsc100/lab03`

### Question 9
What does `len([10, 20, 30, 40])` return?
- A) 3
- B) 4
- C) [10, 20, 30, 40]
- D) Error

### Question 10
How many times will "Hello" be printed by this nested loop?
```python
for i in range(2):
    for j in range(3):
        print("Hello")
```
- A) 2
- B) 3
- C) 5
- D) 6

---

## Part II: Code Analysis (3 points)

### Question 11 (1.5 points)
**Trace through this conditional code and determine what gets printed:**

```python
age = 17
has_license = True
has_car = False

if age >= 16 and has_license:
    print("Can drive")
    if age >= 18 or has_car:
        print("Can drive independently")
    else:
        print("Needs supervision")
        if has_car:
            print("Has own vehicle")
        else:
            print("Needs to borrow vehicle")
else:
    print("Cannot drive")
```

**Analysis:**
- First condition (age >= 16 and has_license): _______ (True/False)
- If true, second condition (age >= 18 or has_car): _______ (True/False)
- What gets printed? (write each line of output in order)
  - Line 1: ____________________________________________________________
  - Line 2: ____________________________________________________________
  - Line 3: ____________________________________________________________

### Question 12 (1.5 points)
**Show each iteration and predict the output:**

```python
numbers = [5, 10, 15, 5]
total = 0
for num in numbers:
    total += num
    if num >= 10:
        print(f"Large number: {num}, total: {total}")
    else:
        print(f"Small number: {num}, total: {total}")
```

**Iteration Analysis:**
- **Iteration 1** (num=5): 
  - total = ______
  - Condition (num >= 10): _______ (True/False)
  - Terminal output: _______________________________________________
- **Iteration 2** (num=10):
  - total = ______
  - Condition (num >= 10): _______ (True/False)  
  - Terminal output: _______________________________________________
- **Iteration 3** (num=15):
  - total = ______
  - Condition (num >= 10): _______ (True/False)
  - Terminal output: _______________________________________________
- **Iteration 4** (num=5):
  - total = ______
  - Condition (num >= 10): _______ (True/False)
  - Terminal output: _______________________________________________

---

## Part III: Code Writing (2 points)

### Question 13 (2 points)
**Write the Python statements (NOT a complete program!) needed to:**
- Declare and initialize a string variable named `device_name` (initialize it to any device name you wish, like "Kitchen Sensor")
- Declare a string variable named `device_code` and set it equal to the first 3 characters of `device_name` plus the string "_001"

**Your Python statements:**
```python
# Write your 2 statements here:




```
