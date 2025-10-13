# CMPSC 100 Practice Midterm Exam - Answer Key
**Computational Expression - Fall 2025**

---

## Part I: Multiple Choice (5 points)
*0.5 point each*

### Question 1: **C) `student_count`**
**Explanation:** 
- A) `2cats` - Invalid: Cannot start with a number
- B) `my age` - Invalid: Cannot contain spaces
- C) `student_count` - **CORRECT**: Valid variable name using snake_case convention
- D) `if` - Invalid: Reserved Python keyword

### Question 2: **B) 8**
**Explanation:**
```python
score = 5        # score is now 5
score = score + 3  # score = 5 + 3 = 8
print(score)     # prints 8
```

### Question 3: **B) `int()`**
**Explanation:**
- A) `str()` - Converts to string
- B) `int()` - **CORRECT**: Converts string to integer
- C) `float()` - Converts to floating-point number
- D) `input()` - Gets user input (always returns string)

### Question 4: **B) MAYA**
**Explanation:**
```python
student_name = "maya"    # lowercase string
print(student_name.upper())  # .upper() converts to uppercase: "MAYA"
```

### Question 5: **C) Cold**
**Explanation:**
```python
temperature = 16
# 16 >= 75? False
# 16 >= 60? False
# Goes to else: prints "Cold"
```

### Question 6: **B) [0, 1, 2]**
**Explanation:** `range(3)` creates a sequence starting at 0, ending before 3: [0, 1, 2]

### Question 7: **D) Syntax errors prevent the program from running at all**
**Explanation:**
- A) False - Logic errors produce wrong results
- B) False - Syntax errors prevent understanding code structure
- C) False - Runtime errors cause crashes with error messages
- D) **CORRECT**: Syntax errors stop the program from executing

### Question 8: **B) `cd ../lab03`**
**Explanation:**
- Current location: `home/student/cmpsc100/lab01/`
- Target: `home/student/cmpsc100/lab03/`
- `..` goes up to parent directory (`cmpsc100`), then `lab03` goes into target directory

### Question 9: **B) 4**
**Explanation:** `len([10, 20, 30, 40])` returns the number of items in the list, which is 4.

### Question 10: **D) 6**
**Explanation:**
- Outer loop runs 2 times (i = 0, 1)
- Inner loop runs 3 times for each outer iteration (j = 0, 1, 2)
- Total: 2 × 3 = 6 times

---

## Part II: Code Analysis (3 points)

### Question 11 (1.5 points)
**Analysis:**
- First condition (age >= 16 and has_license): **True**
  - `17 >= 16` = True, `has_license` = True
  - `True and True` = **True**
- If true, second condition (age >= 18 or has_car): **False**
  - `17 >= 18` = False, `has_car` = False
  - `False or False` = **False**

**What gets printed:**
- Line 1: **Can drive**
- Line 2: **Needs supervision**
- Line 3: **Needs to borrow vehicle**

**Execution Flow:**
1. First `if` is True → prints "Can drive"
2. Second `if` is False → goes to `else` → prints "Needs supervision"
3. `has_car` is False → goes to inner `else` → prints "Needs to borrow vehicle"

### Question 12 (1.5 points)
**Iteration Analysis:**

- **Iteration 1** (num=5):
  - total = **5** (0 + 5)
  - Condition (num >= 10): **False** (5 >= 10 is False)
  - Terminal output: **Small number: 5, total: 5**

- **Iteration 2** (num=10):
  - total = **15** (5 + 10)
  - Condition (num >= 10): **True** (10 >= 10 is True)
  - Terminal output: **Large number: 10, total: 15**

- **Iteration 3** (num=15):
  - total = **30** (15 + 15)
  - Condition (num >= 10): **True** (15 >= 10 is True)
  - Terminal output: **Large number: 15, total: 30**

- **Iteration 4** (num=5):
  - total = **35** (30 + 5)
  - Condition (num >= 10): **False** (5 >= 10 is False)
  - Terminal output: **Small number: 5, total: 35**

**Complete Terminal Output:**
```
Small number: 5, total: 5
Large number: 10, total: 15
Large number: 15, total: 30
Small number: 5, total: 35
```

---

## Part III: Code Writing (2 points)

### Question 13 (2 points)
**Sample Correct Answer:**
```python
device_name = "Kitchen Sensor"
device_code = device_name[:3] + "_001"
```

**Alternative Answers Using Different String Methods:**
```python
device_name = "Kitchen Sensor"
device_code = f"{device_name[:3]}_001"
```

```python
device_name = "Kitchen Sensor"  
device_code = "{}_001".format(device_name[:3])
```

