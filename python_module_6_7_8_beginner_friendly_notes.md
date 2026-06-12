# Python Module 6, 7, and 8 - Beginner Friendly Complete Notes

Lists, Tuples, Dictionaries, Sets, Functions, Lambda Functions, and To-Do List Manager Project

These notes are written for beginners. Language is simple English with light Hinglish so that you can read, understand, and explain the topics to learners.

---

## How to Study These Notes

Do not try to memorize everything in one time. Follow this order:

1. First understand the real-life example.
2. Then read the Python concept.
3. Then type the code yourself.
4. Then compare your output.
5. Then read the line-by-line explanation.

Programming ka best rule: pehle samjho, phir type karo, phir output observe karo.

---

## Chapter Index

| Module | Topic | You Will Learn |
|---|---|---|
| Module 6 | Lists | Multiple values ko ek variable mein store karna |
| Module 6 | List operations | Add, update, delete, search, sort |
| Module 6 | Nested lists | List ke andar list |
| Module 6 | Tuples | Fixed values ka collection |
| Module 6 | Project | CLI To-Do List Manager |
| Module 7 | Dictionaries | Key-value pair data |
| Module 7 | Dictionary operations | Add, update, delete, loop |
| Module 7 | Sets | Unique values store karna |
| Module 8 | Functions | Reusable code blocks |
| Module 8 | Arguments and return values | Function ko input dena and output lena |
| Module 8 | Default and keyword arguments | Flexible function calls |
| Module 8 | Lambda functions | Small one-line functions |

---

# Module 6 - Lists and Tuples

## Big Idea of Module 6

Socho aapke paas ek shopping bag hai. Us bag mein multiple items ho sakte hain:

```text
milk, bread, rice, sugar
```

Python mein aise multiple items ko store karne ke liye list use hoti hai.

Ab socho aapke paas fixed data hai jo change nahi hona chahiye, jaise week days:

```text
Monday, Tuesday, Wednesday...
```

Is type ke fixed data ke liye tuple useful hota hai.

Simple difference:

| Data Type | Real-Life Meaning | Change Possible? |
|---|---|---|
| List | Shopping bag, cart, task list | Yes |
| Tuple | Fixed record, location, color code | No |

---

## Chapter 1 - Lists

### What Is a List?

A list is a collection of multiple values stored in one variable.

Hinglish:

List ek box ya bag ki tarah hai jisme multiple values ek saath rakh sakte hain.

### Real-World Example

Suppose you are building a shopping cart.

Cart mein ek item nahi, multiple items ho sakte hain:

```text
milk
bread
rice
tea
```

Python list:

```python
cart = ["milk", "bread", "rice", "tea"]
```

### Basic Code

```python
cart = ["milk", "bread", "rice", "tea"]

print(cart)
```

### Output

```text
['milk', 'bread', 'rice', 'tea']
```

### Line-by-Line Explanation

| Line | Code | Meaning |
|---|---|---|
| 1 | `cart = [...]` | `cart` naam ki list banayi. |
| 1 | `"milk", "bread"` | List ke items hain. |
| 1 | `[]` | Square brackets list banate hain. |
| 3 | `print(cart)` | Complete list screen par print hoti hai. |

### Teacher Explanation

Learners ko aise samjhao:

“Agar hume 4 items store karne hain, to 4 variables banane ki zaroorat nahi. Ek list bana do.”

Without list:

```python
item1 = "milk"
item2 = "bread"
item3 = "rice"
item4 = "tea"
```

With list:

```python
cart = ["milk", "bread", "rice", "tea"]
```

List code ko clean and manageable banati hai.

---

## Chapter 2 - List Indexing

### What Is Indexing?

Indexing means list ke kisi specific item ko access karna.

Python indexing always 0 se start hoti hai.

Example:

```python
fruits = ["apple", "banana", "mango"]
```

Index map:

```text
Item:   apple   banana   mango
Index:    0        1       2
```

### Real-World Example

Suppose classroom attendance list hai:

```python
students = ["Rahul", "Priya", "Aman"]
```

If teacher wants first student name:

```python
students[0]
```

### Code

```python
students = ["Rahul", "Priya", "Aman"]

print(students[0])
print(students[1])
print(students[-1])
```

### Output

```text
Rahul
Priya
Aman
```

### Line-by-Line Explanation

| Line | Code | Meaning |
|---|---|---|
| 1 | `students = [...]` | 3 students ki list banayi. |
| 3 | `students[0]` | First item access kiya. Output `Rahul`. |
| 4 | `students[1]` | Second item access kiya. Output `Priya`. |
| 5 | `students[-1]` | Last item access kiya. Output `Aman`. |

### Common Mistake

```python
print(students[3])
```

This gives error:

```text
IndexError: list index out of range
```

Why?

List mein only 3 items hain, valid indexes are 0, 1, 2. Index 3 exist nahi karta.

---

## Chapter 3 - List Slicing

### What Is Slicing?

Slicing means list ka ek part nikalna.

Syntax:

```python
list_name[start:stop]
```

Important rule:

`stop` index include nahi hota.

### Real-World Example

Suppose aapko top 3 students chahiye:

```python
students = ["Rahul", "Priya", "Aman", "Neha", "Vikas"]
```

Top 3:

```python
students[0:3]
```

### Code

```python
students = ["Rahul", "Priya", "Aman", "Neha", "Vikas"]

print(students[0:3])
print(students[:2])
print(students[2:])
print(students[-2:])
```

### Output

```text
['Rahul', 'Priya', 'Aman']
['Rahul', 'Priya']
['Aman', 'Neha', 'Vikas']
['Neha', 'Vikas']
```

### Explanation

| Code | Meaning |
|---|---|
| `students[0:3]` | Index 0, 1, 2 values. Index 3 include nahi hota. |
| `students[:2]` | Start default 0. First 2 students. |
| `students[2:]` | Index 2 se end tak. |
| `students[-2:]` | Last 2 students. |

### Easy Memory Trick

`[start:stop]` means:

```text
start se chalu karo, stop se pehle ruk jao
```

---

## Chapter 4 - List Operations

List operations means list mein changes karna.

Real-world comparison:

Shopping cart mein:

- New item add karna
- Wrong item remove karna
- Quantity update karna
- Cart check karna
- Items sort karna

Python list operations exactly isi type ke kaam karte hain.

---

## 4.1 Add Item with `append()`

`append()` list ke end mein item add karta hai.

### Code

```python
cart = ["milk", "bread"]

cart.append("rice")

print(cart)
```

### Output

```text
['milk', 'bread', 'rice']
```

### Explanation

| Line | Code | Meaning |
|---|---|---|
| 1 | `cart = ["milk", "bread"]` | Cart mein 2 items hain. |
| 3 | `cart.append("rice")` | Cart ke end mein rice add hua. |
| 5 | `print(cart)` | Updated cart print hua. |

### Real-World Meaning

Shopping app mein user “Add to Cart” button click karta hai. Behind the scenes item list mein append hota hai.

---

## 4.2 Add Item at Position with `insert()`

`insert()` item ko specific index par add karta hai.

### Code

```python
playlist = ["Song A", "Song C"]

playlist.insert(1, "Song B")

print(playlist)
```

### Output

```text
['Song A', 'Song B', 'Song C']
```

### Explanation

`insert(1, "Song B")` means index 1 par Song B add karo.

Real-world:

Music playlist mein song ko beech mein add karna ho to `insert()` useful hai.

---

## 4.3 Update Item

List mutable hoti hai, so item change kar sakte hain.

### Code

```python
tasks = ["study", "sleep", "practice"]

tasks[1] = "revise"

print(tasks)
```

### Output

```text
['study', 'revise', 'practice']
```

### Explanation

| Code | Meaning |
|---|---|
| `tasks[1]` | Second item select kiya |
| `= "revise"` | Old value ko new value se replace kiya |

Real-world:

To-do app mein user task edit karta hai. Old task text replace hota hai.

---

## 4.4 Remove Item with `remove()`

`remove()` value ke naam se item remove karta hai.

### Code

```python
cart = ["milk", "bread", "rice"]

cart.remove("bread")

print(cart)
```

### Output

```text
['milk', 'rice']
```

### Explanation

`remove("bread")` list mein bread find karta hai and remove karta hai.

Common mistake:

```python
cart.remove("tea")
```

If tea list mein nahi hai, error aayega.

Safe way:

```python
if "tea" in cart:
    cart.remove("tea")
else:
    print("Tea is not in cart")
```

---

## 4.5 Remove Item with `pop()`

`pop()` index ke basis par item remove karta hai. Removed item ko return bhi karta hai.

### Code

```python
notifications = ["msg1", "msg2", "msg3"]

latest = notifications.pop()

print("Removed:", latest)
print("Remaining:", notifications)
```

### Output

```text
Removed: msg3
Remaining: ['msg1', 'msg2']
```

### Explanation

No index diya, so `pop()` last item remove karta hai.

Real-world:

Notification system mein latest notification read/remove karne ke liye last item pop kar sakte hain.

---

## 4.6 Search Item with `in`

### Code

```python
available_courses = ["Python", "Linux", "AWS"]

if "Python" in available_courses:
    print("Python course is available")
else:
    print("Python course is not available")
```

### Output

```text
Python course is available
```

### Explanation

`in` check karta hai ki value list mein present hai ya nahi.

Real-world:

Website check kar sakti hai ki searched course available hai ya nahi.

---

## 4.7 Sort List

### Code

```python
marks = [80, 45, 90, 60]

marks.sort()

print(marks)
```

### Output

```text
[45, 60, 80, 90]
```

### Explanation

`sort()` list ko ascending order mein arrange karta hai.

Descending:

```python
marks.sort(reverse=True)
print(marks)
```

Output:

```text
[90, 80, 60, 45]
```

Real-world:

Result system mein marks high-to-low sort karke toppers nikal sakte hain.

---

## Chapter 5 - Loop Through a List

### Why Loop?

Agar list mein 100 items hain, kya hum 100 baar `print()` likhenge? Nahi.

Loop use karenge.

### Real-World Example

Teacher ke paas students list hai. Har student ko attendance mein print karna hai.

### Code

```python
students = ["Rahul", "Priya", "Aman"]

for student in students:
    print("Attendance:", student)
```

### Output

```text
Attendance: Rahul
Attendance: Priya
Attendance: Aman
```

### Line-by-Line Explanation

| Line | Code | Meaning |
|---|---|---|
| 1 | `students = [...]` | Students list create hui. |
| 3 | `for student in students:` | Har student one by one `student` variable mein aayega. |
| 4 | `print(...)` | Current student print hoga. |

### Teacher Explanation

Loop ka meaning:

```text
Har item ke liye same kaam repeat karo
```

---

## Chapter 6 - Nested Lists

### What Is a Nested List?

Nested list means list ke andar list.

Real-world:

Classroom marks table:

```text
Rahul: 85, 90
Priya: 92, 88
Aman: 78, 84
```

Python:

```python
marks = [
    ["Rahul", 85, 90],
    ["Priya", 92, 88],
    ["Aman", 78, 84]
]
```

### Code

```python
marks = [
    ["Rahul", 85, 90],
    ["Priya", 92, 88],
    ["Aman", 78, 84]
]

print(marks[0])
print(marks[1][0])
print(marks[1][2])
```

### Output

```text
['Rahul', 85, 90]
Priya
88
```

### Explanation

| Code | Meaning |
|---|---|
| `marks[0]` | First row: Rahul ka data |
| `marks[1][0]` | Second row ka first item: Priya |
| `marks[1][2]` | Second row ka third item: 88 |

### Easy Formula

```python
nested_list[row][column]
```

### Print All Rows

```python
for student in marks:
    print(student)
```

Output:

```text
['Rahul', 85, 90]
['Priya', 92, 88]
['Aman', 78, 84]
```

---

## Chapter 7 - Tuples

### What Is a Tuple?

Tuple list jaisa hota hai, but tuple change nahi hota.

List:

```python
fruits = ["apple", "banana"]
```

Tuple:

```python
days = ("Monday", "Tuesday")
```

### Real-World Example

RGB color code:

```python
red = (255, 0, 0)
```

Latitude and longitude:

```python
delhi_location = (28.6139, 77.2090)
```

Ye values accidentally change nahi honi chahiye, so tuple useful hai.

### Code

```python
colors = ("red", "green", "blue")

print(colors)
print(colors[0])
print(type(colors))
```

### Output

```text
('red', 'green', 'blue')
red
<class 'tuple'>
```

### Explanation

| Line | Code | Meaning |
|---|---|---|
| 1 | `colors = (...)` | Tuple create hua. |
| 3 | `print(colors)` | Complete tuple print hua. |
| 4 | `colors[0]` | First item access hua. |
| 5 | `type(colors)` | Data type tuple hai. |

### Tuple Cannot Be Updated

```python
colors[0] = "yellow"
```

Error:

```text
TypeError: 'tuple' object does not support item assignment
```

Meaning:

Tuple immutable hai. Isliye update nahi kar sakte.

---

# Mini Project - To-Do List Manager

## Project Idea

Hum ek simple CLI based To-Do List Manager banayenge.

CLI means Command Line Interface. Program terminal mein chalega.

## Real-World Connection

Ye project same idea use karta hai jo apps mein hota hai:

| App | Similar Feature |
|---|---|
| Google Keep | Notes add/view/delete |
| Todoist | Task add/complete/delete |
| Shopping cart | Item add/view/remove |
| Support system | Ticket open/close/delete |

## What We Need

Each task should have:

| Data | Example |
|---|---|
| Task title | `Study Python` |
| Status | `Pending` or `Completed` |

We will store one task like this:

```python
{"title": "Study Python", "done": False}
```

And many tasks like this:

```python
tasks = [
    {"title": "Study Python", "done": False},
    {"title": "Practice lists", "done": True}
]
```

## Full Code

```python
tasks = []

while True:
    print("\n===== To-Do List Manager =====")
    print("1. Add Task")
    print("2. View Tasks")
    print("3. Mark Task as Completed")
    print("4. Delete Task")
    print("5. Exit")

    choice = input("Enter your choice (1-5): ")

    if choice == "1":
        title = input("Enter task title: ").strip()

        if title == "":
            print("Task title cannot be empty.")
        else:
            task = {"title": title, "done": False}
            tasks.append(task)
            print("Task added successfully.")

    elif choice == "2":
        if len(tasks) == 0:
            print("No tasks found.")
        else:
            print("\nYour Tasks:")
            for index, task in enumerate(tasks, start=1):
                status = "Completed" if task["done"] else "Pending"
                print(f"{index}. {task['title']} - {status}")

    elif choice == "3":
        if len(tasks) == 0:
            print("No tasks available to mark.")
        else:
            task_number = int(input("Enter task number: "))

            if 1 <= task_number <= len(tasks):
                tasks[task_number - 1]["done"] = True
                print("Task marked as completed.")
            else:
                print("Invalid task number.")

    elif choice == "4":
        if len(tasks) == 0:
            print("No tasks available to delete.")
        else:
            task_number = int(input("Enter task number: "))

            if 1 <= task_number <= len(tasks):
                removed_task = tasks.pop(task_number - 1)
                print(f"Deleted task: {removed_task['title']}")
            else:
                print("Invalid task number.")

    elif choice == "5":
        print("Thank you for using To-Do List Manager.")
        break

    else:
        print("Invalid choice. Please enter 1 to 5.")
```

## How to Run

Save file as:

```text
todo.py
```

Run:

```bash
python todo.py
```

or:

```bash
python3 todo.py
```

## Sample Run

```text
===== To-Do List Manager =====
1. Add Task
2. View Tasks
3. Mark Task as Completed
4. Delete Task
5. Exit
Enter your choice (1-5): 1
Enter task title: Study lists
Task added successfully.
```

Then view:

```text
Enter your choice (1-5): 2

Your Tasks:
1. Study lists - Pending
```

## Detailed Code Explanation

| Code | Meaning |
|---|---|
| `tasks = []` | Empty task list. All tasks will be stored here. |
| `while True:` | Program repeatedly runs until `break`. |
| Menu `print()` lines | User ko options show karte hain. |
| `choice = input(...)` | User ka selected option leta hai. |
| `if choice == "1":` | Add task option. |
| `title.strip()` | Extra spaces remove karta hai. |
| `if title == "":` | Empty task block karta hai. |
| `task = {"title": title, "done": False}` | One task dictionary create karta hai. |
| `tasks.append(task)` | Task list mein add karta hai. |
| `elif choice == "2":` | View tasks option. |
| `len(tasks) == 0` | Check karta hai list empty hai ya nahi. |
| `enumerate(tasks, start=1)` | Tasks ko numbering ke saath show karta hai. |
| `task["done"]` | Task completed hai ya pending, ye check karta hai. |
| `task_number - 1` | User numbering 1 se, list index 0 se. Isliye minus 1. |
| `tasks.pop(...)` | Selected task delete karta hai. |
| `break` | Program stop karta hai. |

## Why This Project Is Important

This project combines:

- List
- Dictionary
- Loop
- Condition
- Input
- f-string
- Data update
- Data delete

Learner ko yahan samajhna hai ki real programs mein concepts alag-alag nahi hote. Sab concepts milkar app banate hain.

---

# Module 7 - Dictionaries and Sets

## Big Idea of Module 7

List values ko index se access karti hai.

Dictionary values ko key se access karti hai.

Example:

```python
student = ["Rahul", 20, "Python"]
```

Problem:

`student[0]` kya hai? Name? Course? City? Hume yaad rakhna padega.

Better:

```python
student = {
    "name": "Rahul",
    "age": 20,
    "course": "Python"
}
```

Now data clearly readable hai.

---

## Chapter 8 - Dictionaries

### What Is a Dictionary?

Dictionary key-value pairs ka collection hota hai.

Real-life form:

```text
Name: Rahul
Age: 20
Course: Python
```

Python:

```python
student = {
    "name": "Rahul",
    "age": 20,
    "course": "Python"
}
```

### Real-World Use

Dictionaries are used in:

| Real App | Dictionary Use |
|---|---|
| Student portal | Student profile |
| Shopping app | Product details |
| Banking app | Account information |
| Login system | Username, role, status |
| API response | Structured data |

### Code

```python
student = {
    "name": "Rahul",
    "age": 20,
    "course": "Python"
}

print(student["name"])
print(student["course"])
```

### Output

```text
Rahul
Python
```

### Explanation

| Code | Meaning |
|---|---|
| `student["name"]` | `name` key ki value return karta hai. |
| `student["course"]` | `course` key ki value return karta hai. |

Teacher line:

“Dictionary mein data ko key ke naam se access karte hain. Isliye code readable hota hai.”

---

## Chapter 9 - `get()` Method

### Why `get()`?

If key missing hai, direct access error deta hai.

```python
student = {"name": "Rahul"}

print(student["city"])
```

Error:

```text
KeyError: 'city'
```

Safe method:

```python
student = {"name": "Rahul"}

print(student.get("city", "City not added"))
```

Output:

```text
City not added
```

### Real-World Use

User profile mein phone number optional ho sakta hai.

```python
profile = {
    "name": "Priya",
    "email": "priya@example.com"
}

phone = profile.get("phone", "Phone number not available")

print(phone)
```

Output:

```text
Phone number not available
```

Explanation:

App crash nahi hua. Missing data ko default message se handle kar liya.

---

## Chapter 10 - Add and Update Dictionary

### Code

```python
product = {
    "name": "Keyboard",
    "price": 1200
}

product["stock"] = 10
product["price"] = 999

print(product)
```

### Output

```text
{'name': 'Keyboard', 'price': 999, 'stock': 10}
```

### Explanation

| Code | Meaning |
|---|---|
| `product["stock"] = 10` | New key-value pair add hua. |
| `product["price"] = 999` | Existing price update hua. |

### Real-World Use

E-commerce website mein price and stock frequently update hote hain.

---

## Chapter 11 - Delete Dictionary Data

### Code

```python
student = {
    "name": "Rahul",
    "age": 20,
    "course": "Python"
}

removed = student.pop("age")

print("Removed:", removed)
print(student)
```

### Output

```text
Removed: 20
{'name': 'Rahul', 'course': 'Python'}
```

### Explanation

`pop("age")` age key remove karta hai and removed value return karta hai.

Real-world:

If user deletes optional profile information, dictionary se key remove ho sakti hai.

---

## Chapter 12 - Loop Through Dictionary

### Code

```python
invoice = {
    "Product": "Mouse",
    "Price": 500,
    "Quantity": 2,
    "Total": 1000
}

for key, value in invoice.items():
    print(f"{key}: {value}")
```

### Output

```text
Product: Mouse
Price: 500
Quantity: 2
Total: 1000
```

### Explanation

| Code | Meaning |
|---|---|
| `invoice.items()` | All key-value pairs deta hai. |
| `for key, value in ...` | Har pair ko key and value mein divide karta hai. |
| `print(f"{key}: {value}")` | Clean invoice format print karta hai. |

Real-world:

Invoice, user profile, report card, and settings page display karne mein dictionary loop useful hai.

---

## Chapter 13 - Nested Dictionary

Nested dictionary means dictionary ke andar dictionary.

### Real-World Example

Company employee data:

```python
employees = {
    "emp101": {
        "name": "Rahul",
        "department": "IT"
    },
    "emp102": {
        "name": "Priya",
        "department": "HR"
    }
}
```

### Code

```python
print(employees["emp101"]["name"])
print(employees["emp102"]["department"])
```

### Output

```text
Rahul
HR
```

### Explanation

| Code | Meaning |
|---|---|
| `employees["emp101"]` | Employee 101 ka full data |
| `employees["emp101"]["name"]` | Employee 101 ka name |
| `employees["emp102"]["department"]` | Employee 102 ka department |

---

## Chapter 14 - Sets

### What Is a Set?

Set unique values ka collection hota hai.

Duplicate values automatically remove ho jaati hain.

### Real-World Example

Suppose website visitors:

```text
Rahul, Priya, Rahul, Aman, Priya
```

Unique visitors:

```text
Rahul, Priya, Aman
```

### Code

```python
visitors = {"Rahul", "Priya", "Rahul", "Aman", "Priya"}

print(visitors)
```

### Output

```text
{'Rahul', 'Priya', 'Aman'}
```

Output order different ho sakta hai because set unordered hota hai.

### Explanation

Set duplicate names keep nahi karta. Isliye only unique visitors print hue.

---

## Chapter 15 - Set Operations

### Real-World Example

Two courses ke students compare karne hain:

```python
python_students = {"Rahul", "Priya", "Aman"}
linux_students = {"Aman", "Neha", "Priya"}
```

### Code

```python
python_students = {"Rahul", "Priya", "Aman"}
linux_students = {"Aman", "Neha", "Priya"}

print("All students:", python_students.union(linux_students))
print("Common students:", python_students.intersection(linux_students))
print("Only Python:", python_students.difference(linux_students))
```

### Output

```text
All students: {'Rahul', 'Priya', 'Aman', 'Neha'}
Common students: {'Priya', 'Aman'}
Only Python: {'Rahul'}
```

### Explanation

| Operation | Meaning |
|---|---|
| `union()` | Dono sets ke all unique values |
| `intersection()` | Dono sets mein common values |
| `difference()` | First set ke values jo second mein nahi hain |

Real-world:

Training institute mein course enrollment compare karne ke liye set operations useful hain.

---

# Module 8 - Functions

## Big Idea of Module 8

Function ka main purpose:

```text
Write once, use many times
```

Without function:

```python
print("Welcome Rahul")
print("Welcome Priya")
print("Welcome Aman")
```

With function:

```python
def welcome(name):
    print(f"Welcome {name}")
```

Now same function many names ke saath use kar sakte hain.

---

## Chapter 16 - Basic Function

### Code

```python
def greet():
    print("Hello, welcome to Python!")

greet()
```

### Output

```text
Hello, welcome to Python!
```

### Explanation

| Code | Meaning |
|---|---|
| `def` | Function define karne ka keyword |
| `greet` | Function name |
| `()` | Parameters ke liye place |
| `:` | Function block start |
| `print(...)` | Function body |
| `greet()` | Function call |

Important:

Function define karne se run nahi hota. Function call karna zaroori hai.

---

## Chapter 17 - Function with Arguments

### Real-World Example

Welcome message different users ke liye same format mein print karna hai.

### Code

```python
def welcome(name):
    print(f"Welcome {name}")

welcome("Rahul")
welcome("Priya")
```

### Output

```text
Welcome Rahul
Welcome Priya
```

### Explanation

| Term | Meaning |
|---|---|
| `name` in function definition | Parameter |
| `"Rahul"` in function call | Argument |

Function reusable ho gaya. Same function different names ke saath use hua.

---

## Chapter 18 - Function with Return Value

### Why Return?

`print()` sirf screen par output dikhata hai.

`return` value ko function ke bahar use karne ke liye bhejta hai.

### Real-World Example

Billing app mein total calculate karna hai and us total par delivery charge add karna hai.

### Code

```python
def calculate_total(price, quantity):
    total = price * quantity
    return total

bill = calculate_total(500, 3)
final_bill = bill + 50

print("Final bill:", final_bill)
```

### Output

```text
Final bill: 1550
```

### Explanation

| Line | Code | Meaning |
|---|---|---|
| 1 | `def calculate_total(price, quantity):` | Function two inputs leta hai. |
| 2 | `total = price * quantity` | Total calculate karta hai. |
| 3 | `return total` | Total bahar bhejta hai. |
| 5 | `bill = calculate_total(500, 3)` | Returned value `bill` mein store hui. |
| 6 | `final_bill = bill + 50` | Delivery charge add hua. |
| 8 | `print(...)` | Final amount print hua. |

---

## Chapter 19 - Default Arguments

Default argument means agar value pass na ho, to default value use hogi.

### Code

```python
def create_user(username, role="student"):
    print(f"Username: {username}, Role: {role}")

create_user("rahul")
create_user("admin1", "admin")
```

### Output

```text
Username: rahul, Role: student
Username: admin1, Role: admin
```

### Explanation

| Code | Meaning |
|---|---|
| `role="student"` | Default role student hai. |
| `create_user("rahul")` | Role pass nahi kiya, so student use hua. |
| `create_user("admin1", "admin")` | Role pass kiya, so admin use hua. |

Real-world:

Most users student hote hain, so default role student rakha. Special case mein admin pass kar diya.

---

## Chapter 20 - Keyword Arguments

Keyword arguments mein parameter name ke saath value pass karte hain.

### Code

```python
def book_ticket(name, source, destination):
    print(f"{name} booked ticket from {source} to {destination}")

book_ticket(destination="Mumbai", name="Rahul", source="Delhi")
```

### Output

```text
Rahul booked ticket from Delhi to Mumbai
```

### Explanation

Order matter nahi karta because values names ke saath pass hui hain:

| Argument | Value |
|---|---|
| `destination` | Mumbai |
| `name` | Rahul |
| `source` | Delhi |

Real-world:

Jab function mein multiple values hon, keyword arguments code ko readable banate hain.

---

## Chapter 21 - Lambda Functions

### What Is Lambda?

Lambda ek small one-line function hota hai.

Normal function:

```python
def square(x):
    return x * x
```

Lambda:

```python
square = lambda x: x * x
```

### Code

```python
square = lambda x: x * x

print(square(5))
```

### Output

```text
25
```

### Explanation

| Code | Meaning |
|---|---|
| `lambda x:` | One input `x` |
| `x * x` | Return expression |
| `square(5)` | 5 ka square calculate |

### Real-World Example - Sort Products by Price

```python
products = [
    {"name": "Keyboard", "price": 1200},
    {"name": "Mouse", "price": 500},
    {"name": "Monitor", "price": 9000}
]

products.sort(key=lambda product: product["price"])

print(products)
```

### Output

```text
[{'name': 'Mouse', 'price': 500}, {'name': 'Keyboard', 'price': 1200}, {'name': 'Monitor', 'price': 9000}]
```

### Explanation

`lambda product: product["price"]` Python ko batata hai:

```text
Har product dictionary mein price key dekho, aur uske basis par sort karo.
```

E-commerce website mein “sort by price low to high” feature isi type ke logic se ban sakta hai.

---

# Practice Questions

## Question 1 - Shopping Cart

Create a list called `cart`. Add 3 items. Then add one more item using `append()`. Print the final cart.

## Question 2 - Student Attendance

Create a list of 5 students. Print first student, last student, and total number of students.

## Question 3 - Top 3 Marks

Create a marks list in high-to-low order. Print only top 3 marks using slicing.

## Question 4 - Update To-Do Task

Create a task list. Update the second task with a new task.

## Question 5 - Student Profile

Create a dictionary with `name`, `age`, `course`. Print each value using key.

## Question 6 - Product Stock

Create a product dictionary with `name`, `price`, `stock`. Reduce stock by 1 and print updated product.

## Question 7 - Unique Emails

Create a list with duplicate email IDs. Convert it into a set and print unique emails.

## Question 8 - Course Comparison

Create two sets: Python students and Linux students. Print all students and common students.

## Question 9 - Discount Function

Create a function that takes price and discount percentage, then returns final price.

## Question 10 - Lambda Square

Create a lambda function that returns square of a number.

---

# Quick Revision

| Concept | Simple Meaning | Real-World Example |
|---|---|---|
| List | Multiple values | Shopping cart |
| Index | Position number | First student, last message |
| Slicing | Part of list | Top 3 marks |
| Nested list | List inside list | Marks table |
| Tuple | Fixed values | GPS location |
| Dictionary | Key-value data | Student profile |
| Set | Unique values | Unique visitors |
| Function | Reusable code | Billing calculation |
| Return | Send result back | Final bill |
| Default argument | Backup value | Default user role |
| Keyword argument | Named value | Ticket booking |
| Lambda | Short function | Sort by price |

---

# Final Advice

Learners ko concepts real life se connect karke samjhao.

Example:

- List means cart.
- Dictionary means form/profile.
- Set means unique collection.
- Function means reusable machine.

Jab learner real-world meaning samajh leta hai, code samajhna easy ho jata hai.

Happy Coding.
