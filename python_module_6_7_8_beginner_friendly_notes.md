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

This project looks small, but isme real app ka complete basic flow hai:

```text
Data store karo -> Menu show karo -> User input lo -> Action perform karo -> Repeat karo
```

---

## Part 1 - Empty Task List

### Code

```python
tasks = []
```

### Meaning

`tasks` ek empty list hai. Is list ke andar saare tasks store honge.

Start mein list empty hai because user ne abhi koi task add nahi kiya.

### Why We Use List Here

Hume ek task nahi, multiple tasks store karne hain.

Example:

```python
tasks = [
    {"title": "Study Python", "done": False},
    {"title": "Practice lists", "done": True}
]
```

List multiple task dictionaries ko ek saath store kar sakti hai.

Real-world:

To-do app mein saare tasks ek task list mein dikhte hain.

---

## Part 2 - `while True` Menu Loop

### Code

```python
while True:
```

### Meaning

`while True` ek infinite loop hai. Program baar-baar chalega jab tak `break` nahi milta.

### Why We Use It

Menu-based program mein user multiple actions kar sakta hai:

- Add task
- View tasks
- Mark task completed
- Delete task
- Exit

Agar loop nahi hoga, program ek choice ke baad close ho jayega.

Real-world:

ATM machine ya mobile app ka menu bhi user ko multiple actions karne deta hai.

---

## Part 3 - Menu Print Lines

### Code

```python
print("\n===== To-Do List Manager =====")
print("1. Add Task")
print("2. View Tasks")
print("3. Mark Task as Completed")
print("4. Delete Task")
print("5. Exit")
```

### Meaning

Ye lines user ko available options show karti hain.

### Line Meaning

| Code | Meaning |
|---|---|
| `\n` | New line add karta hai, output clean dikhta hai. |
| `1. Add Task` | User task add kar sakta hai. |
| `2. View Tasks` | User existing tasks dekh sakta hai. |
| `3. Mark Task as Completed` | User task complete mark kar sakta hai. |
| `4. Delete Task` | User task delete kar sakta hai. |
| `5. Exit` | User program close kar sakta hai. |

---

## Part 4 - User Choice Input

### Code

```python
choice = input("Enter your choice (1-5): ")
```

### Meaning

`input()` user se choice leta hai and `choice` variable mein store karta hai.

Important:

`input()` hamesha string return karta hai.

If user types:

```text
1
```

Python stores:

```python
"1"
```

That is why we compare with `"1"`, `"2"`, `"3"` as strings.

---

## Part 5 - Add Task Option

### Code

```python
if choice == "1":
    title = input("Enter task title: ").strip()
```

### Meaning

If user enters `"1"`, Add Task block run hota hai.

`input()` task title leta hai.

`.strip()` extra spaces remove karta hai.

Example:

```text
"   Study Python   "
```

After `.strip()`:

```text
"Study Python"
```

### Why `.strip()` Is Important

User galti se spaces type kar sakta hai. Clean data store karne ke liye `.strip()` useful hai.

---

## Part 6 - Empty Task Validation

### Code

```python
if title == "":
    print("Task title cannot be empty.")
```

### Meaning

Ye check karta hai ki title blank hai ya nahi.

If user only presses Enter, title empty ho jayega.

### Why We Need This

Blank task ka koi meaning nahi hota.

Bad data:

```python
{"title": "", "done": False}
```

Real-world apps bhi required fields blank hone par error show karti hain.

---

## Part 7 - Task Dictionary

### Code

```python
task = {"title": title, "done": False}
```

### Meaning

Ye line ek task dictionary create karti hai.

| Key | Meaning |
|---|---|
| `"title"` | Task ka naam |
| `"done"` | Task complete hai ya pending |
| `False` | New task pending hai |

Example:

If user enters:

```text
Study Python
```

Task becomes:

```python
{"title": "Study Python", "done": False}
```

### Why Dictionary Is Used

Task ke paas multiple details hain. Sirf title nahi, status bhi hai. Isliye dictionary better hai.

---

## Part 8 - Add Task to List

### Code

```python
tasks.append(task)
print("Task added successfully.")
```

### Meaning

`append()` new task ko tasks list ke end mein add karta hai.

Before:

```python
tasks = []
```

After:

```python
tasks = [
    {"title": "Study Python", "done": False}
]
```

Success message user ko confirmation deta hai.

---

## Part 9 - View Tasks Option

### Code

```python
elif choice == "2":
```

### Meaning

If user enters `"2"`, View Tasks block run hota hai.

### Empty List Check

```python
if len(tasks) == 0:
    print("No tasks found.")
```

`len(tasks)` list ke total tasks count karta hai.

If count 0 hai, message show hota hai:

```text
No tasks found.
```

### Why This Check Is Needed

If no tasks exist, user ko clear message milna chahiye. Empty output confusing hota hai.

---

## Part 10 - Show Tasks with Numbering

### Code

```python
for index, task in enumerate(tasks, start=1):
    status = "Completed" if task["done"] else "Pending"
    print(f"{index}. {task['title']} - {status}")
```

### Meaning

This code tasks ko numbering ke saath print karta hai.

### `enumerate()` Explanation

`enumerate(tasks, start=1)` list ke har task ke saath number deta hai.

`start=1` ka matlab numbering 1 se start hogi.

Why?

Users usually 1, 2, 3 numbering samajhte hain. Python index 0 se start hota hai, but user ko 0 se numbering dikhana confusing ho sakta hai.

### Status Line Explanation

```python
status = "Completed" if task["done"] else "Pending"
```

Meaning:

If `task["done"]` True hai, status Completed hoga. Otherwise Pending hoga.

### Print Line Explanation

```python
print(f"{index}. {task['title']} - {status}")
```

This prints:

```text
1. Study Python - Pending
```

---

## Part 11 - Mark Task as Completed

### Code

```python
elif choice == "3":
```

If user enters `"3"`, complete task block run hota hai.

### Task Number Input

```python
task_number = int(input("Enter task number: "))
```

`input()` user se task number leta hai.

`int()` string input ko number mein convert karta hai.

Why?

Range check number ke saath easy hota hai.

### Valid Number Check

```python
if 1 <= task_number <= len(tasks):
```

Meaning:

Task number 1 se kam nahi hona chahiye and total tasks se zyada nahi hona chahiye.

If 3 tasks exist, valid numbers:

```text
1, 2, 3
```

Invalid:

```text
0, 4, 5, -1
```

### Mark Completed

```python
tasks[task_number - 1]["done"] = True
```

Why `task_number - 1`?

User numbering starts from 1.

Python list index starts from 0.

Example:

User enters task number 1.

Python index:

```text
1 - 1 = 0
```

So first task update hota hai.

Before:

```python
{"title": "Study Python", "done": False}
```

After:

```python
{"title": "Study Python", "done": True}
```

---

## Part 12 - Delete Task

### Code

```python
elif choice == "4":
```

If user enters `"4"`, delete task block run hota hai.

### Empty Check

```python
if len(tasks) == 0:
    print("No tasks available to delete.")
```

If task list empty hai, delete karne ke liye kuch nahi hai.

### Delete Logic

```python
removed_task = tasks.pop(task_number - 1)
print(f"Deleted task: {removed_task['title']}")
```

`pop(index)` selected task remove karta hai.

Removed task `removed_task` variable mein store hota hai.

Then deleted task ka title print hota hai.

Example output:

```text
Deleted task: Study Python
```

---

## Part 13 - Exit Program

### Code

```python
elif choice == "5":
    print("Thank you for using To-Do List Manager.")
    break
```

### Meaning

If user enters `"5"`, thank you message print hota hai and `break` loop stop kar deta hai.

Why `break`?

Because `while True` loop automatically stop nahi hota. Usko stop karne ke liye `break` zaroori hai.

---

## Part 14 - Invalid Choice

### Code

```python
else:
    print("Invalid choice. Please enter 1 to 5.")
```

### Meaning

If user enters anything other than 1 to 5, this block runs.

Example:

```text
Enter your choice: 9
Invalid choice. Please enter 1 to 5.
```

Why?

User mistakes handle karna real apps ka important part hai.

---

## Project Concepts Summary

| Concept | Project Mein Use |
|---|---|
| List | Multiple tasks store karne ke liye |
| Dictionary | Task title and status store karne ke liye |
| `while True` | Menu baar-baar chalane ke liye |
| `input()` | User se data lene ke liye |
| `if-elif-else` | Choice ke according action run karne ke liye |
| `.strip()` | Extra spaces clean karne ke liye |
| `append()` | New task add karne ke liye |
| `len()` | Empty list check karne ke liye |
| `enumerate()` | Numbering ke saath tasks show karne ke liye |
| f-string | Clean output ke liye |
| `int()` | Task number ko number mein convert karne ke liye |
| `pop()` | Task delete karne ke liye |
| `break` | Program exit karne ke liye |

## Simple Teacher Explanation

Is project ko class mein aise explain kar sakte ho:

```text
Pehle empty task list banti hai.
Phir menu repeatedly show hota hai.
User choice deta hai.
Choice ke hisaab se task add, view, complete, delete ya exit hota hai.
List saare tasks store karti hai.
Dictionary har task ki details store karti hai.
```

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

# Complete Code Explanation in Simple Hinglish

This section is for teaching and revision. Yahan par document ke important code examples ko aur detail mein explain kiya gaya hai, taaki aap learners ko easily samjha sako.

## How to Explain Any Code to Learners

Jab bhi aap code explain karo, is order ko follow karo:

1. Code ka purpose kya hai?
2. Kaunsa data store ho raha hai?
3. Code line-by-line kya kar raha hai?
4. Output kyu aaya?
5. Real-world mein iska use kaha hota hai?

Example teaching line:

```text
Pehle hum data store kar rahe hain, phir us data par operation kar rahe hain, phir final result print kar rahe hain.
```

---

## Code Explanation 1 - List Creation

### Code

```python
cart = ["milk", "bread", "rice", "tea"]

print(cart)
```

### What This Code Does

Ye code ek shopping cart create karta hai. Cart ke andar 4 items store hain.

### Line-by-Line Explanation

| Line | Code | Simple Hinglish Explanation |
|---|---|---|
| 1 | `cart = [...]` | `cart` naam ka variable ban raha hai. Is variable mein ek list store ho rahi hai. |
| 1 | `[` and `]` | Square brackets ka matlab hai ye list hai. |
| 1 | `"milk"` | List ka first item hai. Quotes ka matlab hai ye string/text hai. |
| 1 | `,` | Comma items ko alag-alag karta hai. |
| 3 | `print(cart)` | Complete cart list screen par show karega. |

### Output Reason

Output list ke format mein aata hai:

```text
['milk', 'bread', 'rice', 'tea']
```

Python list ko square brackets ke saath print karta hai, so learner ko clear dikhta hai ki ye list hai.

### Real-World Use

Shopping cart, playlist, attendance list, marks list, and task list mein list ka use hota hai.

---

## Code Explanation 2 - List Indexing

### Code

```python
students = ["Rahul", "Priya", "Aman"]

print(students[0])
print(students[1])
print(students[-1])
```

### What This Code Does

Ye code list ke specific students ko index number se access karta hai.

### Index Map

```text
Value:   Rahul   Priya   Aman
Index:     0       1      2
Neg:      -3      -2     -1
```

### Line-by-Line Explanation

| Line | Code | Simple Hinglish Explanation |
|---|---|---|
| 1 | `students = [...]` | Students ki list create hui. |
| 3 | `students[0]` | Index 0 ka item access ho raha hai. Python mein first item ka index 0 hota hai. |
| 4 | `students[1]` | Index 1 ka item access ho raha hai, yani second item. |
| 5 | `students[-1]` | Negative index `-1` last item ko access karta hai. |

### Output Reason

```text
Rahul
Priya
Aman
```

Because:

- `students[0]` = Rahul
- `students[1]` = Priya
- `students[-1]` = Aman

### Common Mistake

```python
print(students[3])
```

This gives error because list mein index 3 exist nahi karta. Valid indexes are 0, 1, 2.

---

## Code Explanation 3 - List Slicing

### Code

```python
students = ["Rahul", "Priya", "Aman", "Neha", "Vikas"]

print(students[0:3])
print(students[:2])
print(students[2:])
print(students[-2:])
```

### What This Code Does

Ye code list ke parts nikalta hai. Isko slicing bolte hain.

### Line-by-Line Explanation

| Code | Simple Hinglish Explanation |
|---|---|
| `students[0:3]` | Index 0 se start karo, index 3 se pehle ruk jao. Output first 3 students. |
| `students[:2]` | Start blank hai, so Python 0 se start karega. Index 2 se pehle rukega. |
| `students[2:]` | Index 2 se start karke end tak jayega. |
| `students[-2:]` | End se last 2 values lega. |

### Output Reason

```text
['Rahul', 'Priya', 'Aman']
['Rahul', 'Priya']
['Aman', 'Neha', 'Vikas']
['Neha', 'Vikas']
```

Important rule:

```text
Stop index include nahi hota.
```

### Real-World Use

- Top 3 students nikalna
- Last 5 orders show karna
- First 10 products display karna
- Recent messages show karna

---

## Code Explanation 4 - `append()`

### Code

```python
cart = ["milk", "bread"]

cart.append("rice")

print(cart)
```

### What This Code Does

Ye code cart ke end mein new item add karta hai.

### Line-by-Line Explanation

| Line | Code | Simple Hinglish Explanation |
|---|---|---|
| 1 | `cart = ["milk", "bread"]` | Cart list mein starting ke 2 items hain. |
| 3 | `cart.append("rice")` | `append()` cart ke end mein `"rice"` add karta hai. |
| 5 | `print(cart)` | Updated list print hoti hai. |

### Output Reason

```text
['milk', 'bread', 'rice']
```

Rice end mein add hua because `append()` always end par add karta hai.

### Real-World Use

User ne shopping website par “Add to Cart” click kiya. Product cart list ke end mein add ho gaya.

---

## Code Explanation 5 - `insert()`

### Code

```python
playlist = ["Song A", "Song C"]

playlist.insert(1, "Song B")

print(playlist)
```

### What This Code Does

Ye code playlist ke beech mein new song add karta hai.

### Line-by-Line Explanation

| Line | Code | Simple Hinglish Explanation |
|---|---|---|
| 1 | `playlist = ["Song A", "Song C"]` | Playlist mein two songs hain. |
| 3 | `playlist.insert(1, "Song B")` | Index 1 par Song B add karo. |
| 5 | `print(playlist)` | Updated playlist print karo. |

### Output Reason

```text
['Song A', 'Song B', 'Song C']
```

Song B index 1 par add hua. Song C right side shift ho gaya.

### Real-World Use

Music app mein user song ko playlist ke beech mein add kar sakta hai.

---

## Code Explanation 6 - Update List Item

### Code

```python
tasks = ["study", "sleep", "practice"]

tasks[1] = "revise"

print(tasks)
```

### What This Code Does

Ye code list ke second item ko update karta hai.

### Line-by-Line Explanation

| Line | Code | Simple Hinglish Explanation |
|---|---|---|
| 1 | `tasks = [...]` | Tasks ki list create hui. |
| 3 | `tasks[1]` | Index 1 ka item select hua. Index 1 means second item. |
| 3 | `= "revise"` | Old value `"sleep"` replace hoke `"revise"` ho gayi. |
| 5 | `print(tasks)` | Updated list print hui. |

### Output Reason

```text
['study', 'revise', 'practice']
```

Because index 1 par pehle `sleep` tha. Ab `revise` ho gaya.

### Real-World Use

To-do app mein user existing task edit karta hai.

---

## Code Explanation 7 - `remove()`

### Code

```python
cart = ["milk", "bread", "rice"]

cart.remove("bread")

print(cart)
```

### What This Code Does

Ye code cart se bread remove karta hai.

### Line-by-Line Explanation

| Line | Code | Simple Hinglish Explanation |
|---|---|---|
| 1 | `cart = [...]` | Cart mein 3 items hain. |
| 3 | `cart.remove("bread")` | Python list mein `"bread"` find karega and remove karega. |
| 5 | `print(cart)` | Updated cart print hoga. |

### Output Reason

```text
['milk', 'rice']
```

Bread remove ho gaya, baaki items list mein reh gaye.

### Important Point

`remove()` value ke basis par remove karta hai, index ke basis par nahi.

Wrong item remove karne se bachne ke liye pehle check kar sakte hain:

```python
if "bread" in cart:
    cart.remove("bread")
```

---

## Code Explanation 8 - `pop()`

### Code

```python
notifications = ["msg1", "msg2", "msg3"]

latest = notifications.pop()

print("Removed:", latest)
print("Remaining:", notifications)
```

### What This Code Does

Ye code last notification remove karta hai and usko `latest` variable mein store karta hai.

### Line-by-Line Explanation

| Line | Code | Simple Hinglish Explanation |
|---|---|---|
| 1 | `notifications = [...]` | Notifications ki list create hui. |
| 3 | `notifications.pop()` | Last item remove hota hai because index nahi diya. |
| 3 | `latest = ...` | Removed value `latest` mein store hoti hai. |
| 5 | `print("Removed:", latest)` | Jo item remove hua, wo print hota hai. |
| 6 | `print("Remaining:", notifications)` | List mein jo items bache hain wo print hote hain. |

### Output Reason

```text
Removed: msg3
Remaining: ['msg1', 'msg2']
```

`msg3` last item tha, so pop ne usko remove kiya.

---

## Code Explanation 9 - Loop Through List

### Code

```python
students = ["Rahul", "Priya", "Aman"]

for student in students:
    print("Attendance:", student)
```

### What This Code Does

Ye code students list ke har student ko one by one print karta hai.

### Line-by-Line Explanation

| Line | Code | Simple Hinglish Explanation |
|---|---|---|
| 1 | `students = [...]` | Students list create hui. |
| 3 | `for student in students:` | List ka har item one by one `student` variable mein aayega. |
| 4 | `print(...)` | Current student ka attendance print hoga. |

### Loop Flow

| Round | `student` Value | Printed Output |
|---|---|---|
| 1 | Rahul | Attendance: Rahul |
| 2 | Priya | Attendance: Priya |
| 3 | Aman | Attendance: Aman |

### Real-World Use

Attendance system, email sending, invoice printing, and file processing mein loop use hota hai.

---

## Code Explanation 10 - Nested List

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

### What This Code Does

Ye code students ke marks table ko nested list ke form mein store karta hai.

### Structure

```text
Row 0: Rahul, 85, 90
Row 1: Priya, 92, 88
Row 2: Aman, 78, 84
```

### Line-by-Line Explanation

| Code | Simple Hinglish Explanation |
|---|---|
| `marks[0]` | First row print hoti hai: Rahul ka data. |
| `marks[1][0]` | Row 1 ka column 0. Priya ka name. |
| `marks[1][2]` | Row 1 ka column 2. Priya ka second marks value. |

### Output Reason

```text
['Rahul', 85, 90]
Priya
88
```

Formula:

```python
list[row][column]
```

### Real-World Use

Nested lists table-like data ke liye useful hoti hain: marks table, seating chart, game board, spreadsheet rows.

---

## Code Explanation 11 - Tuple

### Code

```python
colors = ("red", "green", "blue")

print(colors)
print(colors[0])
print(type(colors))
```

### What This Code Does

Ye code fixed color values ko tuple mein store karta hai.

### Line-by-Line Explanation

| Line | Code | Simple Hinglish Explanation |
|---|---|---|
| 1 | `colors = (...)` | Parentheses tuple create karte hain. |
| 3 | `print(colors)` | Complete tuple print hota hai. |
| 4 | `colors[0]` | First item access hota hai. |
| 5 | `type(colors)` | Data type check hota hai. |

### Output Reason

```text
('red', 'green', 'blue')
red
<class 'tuple'>
```

Tuple list jaisa access hota hai, but update nahi hota.

### Real-World Use

Tuple fixed data ke liye: GPS location, RGB color, date parts, fixed settings.

---

## Code Explanation 12 - To-Do Project Data Structure

### Code

```python
tasks = [
    {"title": "Study Python", "done": False},
    {"title": "Practice lists", "done": True}
]
```

### What This Code Does

Ye code multiple tasks store karta hai. Har task dictionary hai, aur saare tasks ek list mein store hain.

### Structure Explanation

| Part | Meaning |
|---|---|
| `tasks = [...]` | Tasks ka collection list mein hai. |
| `{...}` | Har task ek dictionary hai. |
| `"title"` | Task ka naam store karta hai. |
| `"done"` | Task complete hai ya pending, ye store karta hai. |
| `False` | Task abhi pending hai. |
| `True` | Task complete ho chuka hai. |

### Real-World Meaning

Real to-do app mein har task ke saath title, status, date, priority, etc. store ho sakte hain. Yahan beginner version mein sirf title and done status rakha gaya hai.

---

## Code Explanation 13 - To-Do Project Menu Loop

### Code

```python
while True:
    print("\n===== To-Do List Manager =====")
    print("1. Add Task")
    print("2. View Tasks")
    print("3. Mark Task as Completed")
    print("4. Delete Task")
    print("5. Exit")

    choice = input("Enter your choice (1-5): ")
```

### What This Code Does

Ye code menu ko repeatedly show karta hai jab tak user exit na kare.

### Line-by-Line Explanation

| Line | Code | Simple Hinglish Explanation |
|---|---|---|
| 1 | `while True:` | Infinite loop start. Program baar-baar menu show karega. |
| 2 | `\n` | New line add karta hai, output clean dikhata hai. |
| 2-7 | `print(...)` | Menu options show karte hain. |
| 9 | `input(...)` | User se choice leta hai. |
| 9 | `choice = ...` | User ki choice variable mein store hoti hai. |

### Why `while True`?

Menu-based programs mein user multiple actions kar sakta hai. Agar user exit choose kare, tab `break` se loop stop hota hai.

---

## Code Explanation 14 - Add Task Logic

### Code

```python
if choice == "1":
    title = input("Enter task title: ").strip()

    if title == "":
        print("Task title cannot be empty.")
    else:
        task = {"title": title, "done": False}
        tasks.append(task)
        print("Task added successfully.")
```

### What This Code Does

Ye code user se task title leta hai and task list mein add karta hai.

### Line-by-Line Explanation

| Line | Code | Simple Hinglish Explanation |
|---|---|---|
| 1 | `if choice == "1":` | Check karta hai user ne Add Task option choose kiya ya nahi. |
| 2 | `input(...)` | User se task ka title leta hai. |
| 2 | `.strip()` | Extra spaces remove karta hai. |
| 4 | `if title == "":` | Empty title check karta hai. |
| 5 | `print(...)` | Agar title empty hai, error message show hota hai. |
| 7 | `task = {...}` | New task dictionary create hoti hai. |
| 7 | `"done": False` | New task by default pending hota hai. |
| 8 | `tasks.append(task)` | New task tasks list mein add hota hai. |
| 9 | `print(...)` | Success message show hota hai. |

### Real-World Use

Task management app mein jab user new task create karta hai, task by default pending hota hai.

---

## Code Explanation 15 - View Tasks Logic

### Code

```python
elif choice == "2":
    if len(tasks) == 0:
        print("No tasks found.")
    else:
        print("\nYour Tasks:")
        for index, task in enumerate(tasks, start=1):
            status = "Completed" if task["done"] else "Pending"
            print(f"{index}. {task['title']} - {status}")
```

### What This Code Does

Ye code all tasks ko numbering ke saath show karta hai.

### Line-by-Line Explanation

| Line | Code | Simple Hinglish Explanation |
|---|---|---|
| 1 | `elif choice == "2":` | Check karta hai user ne View Tasks option choose kiya. |
| 2 | `len(tasks) == 0` | Check karta hai tasks list empty hai ya nahi. |
| 3 | `print("No tasks found.")` | Agar list empty hai, message show hota hai. |
| 5 | `print("\nYour Tasks:")` | Heading print hoti hai. |
| 6 | `enumerate(tasks, start=1)` | Har task ko numbering ke saath loop karta hai. Number 1 se start hota hai. |
| 7 | `task["done"]` | Check karta hai task complete hai ya pending. |
| 7 | `"Completed" if ... else "Pending"` | One-line condition. True ho to Completed, warna Pending. |
| 8 | `print(f"...")` | Task number, title, and status print karta hai. |

### Why `enumerate()`?

Learner ko list index 0 se confuse na ho, isliye numbering 1 se start karte hain.

Example:

```text
1. Study Python - Pending
2. Practice lists - Completed
```

---

## Code Explanation 16 - Mark Task Completed

### Code

```python
task_number = int(input("Enter task number: "))

if 1 <= task_number <= len(tasks):
    tasks[task_number - 1]["done"] = True
    print("Task marked as completed.")
else:
    print("Invalid task number.")
```

### What This Code Does

Ye selected task ko completed mark karta hai.

### Line-by-Line Explanation

| Line | Code | Simple Hinglish Explanation |
|---|---|---|
| 1 | `input(...)` | User se task number leta hai. |
| 1 | `int(...)` | Input string ko integer number mein convert karta hai. |
| 3 | `1 <= task_number <= len(tasks)` | Check karta hai task number valid range mein hai ya nahi. |
| 4 | `task_number - 1` | User number 1 se start karta hai, but list index 0 se. Isliye minus 1. |
| 4 | `["done"] = True` | Selected task ka status completed ho jata hai. |
| 5 | `print(...)` | Success message. |
| 7 | `print(...)` | Invalid number ke liye error message. |

### Example

If user enters `1`, list index should be `0`.

```text
task_number - 1 = 1 - 1 = 0
```

---

## Code Explanation 17 - Dictionary Access

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

### What This Code Does

Ye code student dictionary se name and course access karta hai.

### Line-by-Line Explanation

| Line | Code | Simple Hinglish Explanation |
|---|---|---|
| 1 | `student = {...}` | Student data dictionary mein store hua. |
| 2 | `"name": "Rahul"` | Key `name`, value `Rahul`. |
| 3 | `"age": 20` | Key `age`, value `20`. |
| 4 | `"course": "Python"` | Key `course`, value `Python`. |
| 7 | `student["name"]` | Name key ki value access hoti hai. |
| 8 | `student["course"]` | Course key ki value access hoti hai. |

### Why Dictionary?

Dictionary mein data readable hota hai. `student["name"]` dekhte hi samajh aa raha hai ki name access ho raha hai.

---

## Code Explanation 18 - `get()` Method

### Code

```python
profile = {
    "name": "Priya",
    "email": "priya@example.com"
}

phone = profile.get("phone", "Phone number not available")

print(phone)
```

### What This Code Does

Ye code safely phone number access karta hai. Agar phone key nahi hai, default message show hota hai.

### Line-by-Line Explanation

| Line | Code | Simple Hinglish Explanation |
|---|---|---|
| 1-4 | `profile = {...}` | User profile dictionary create hui. |
| 6 | `profile.get("phone", "...")` | Phone key find karta hai. |
| 6 | `"Phone number not available"` | Agar phone key missing hai, ye default value return hoti hai. |
| 8 | `print(phone)` | Final value print hoti hai. |

### Output Reason

```text
Phone number not available
```

Because profile dictionary mein `phone` key present nahi hai.

---

## Code Explanation 19 - Dictionary Update

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

### What This Code Does

Ye code product mein stock add karta hai and price update karta hai.

### Line-by-Line Explanation

| Line | Code | Simple Hinglish Explanation |
|---|---|---|
| 1-4 | `product = {...}` | Product dictionary create hui. |
| 6 | `product["stock"] = 10` | New key `stock` add hui. |
| 7 | `product["price"] = 999` | Existing key `price` ki value update hui. |
| 9 | `print(product)` | Updated product print hua. |

### Important Rule

If key exists, value update hoti hai.

If key does not exist, new key add hoti hai.

---

## Code Explanation 20 - Loop Through Dictionary

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

### What This Code Does

Ye code invoice dictionary ke all key-value pairs print karta hai.

### Line-by-Line Explanation

| Line | Code | Simple Hinglish Explanation |
|---|---|---|
| 1-6 | `invoice = {...}` | Invoice data dictionary mein store hua. |
| 8 | `invoice.items()` | Dictionary ke key-value pairs return karta hai. |
| 8 | `for key, value in ...` | Har pair ko key and value variable mein store karta hai. |
| 9 | `print(f"{key}: {value}")` | Key and value clean format mein print hota hai. |

### Real-World Use

Invoice, profile, report card, and settings page mein dictionary loop use hota hai.

---

## Code Explanation 21 - Set and Unique Values

### Code

```python
visitors = {"Rahul", "Priya", "Rahul", "Aman", "Priya"}

print(visitors)
```

### What This Code Does

Ye code duplicate visitor names ko automatically remove karta hai.

### Explanation

Set duplicate values store nahi karta.

Input values:

```text
Rahul, Priya, Rahul, Aman, Priya
```

Unique output:

```text
Rahul, Priya, Aman
```

### Real-World Use

Website analytics mein unique visitors count karne ke liye set useful hai.

---

## Code Explanation 22 - Set Operations

### Code

```python
python_students = {"Rahul", "Priya", "Aman"}
linux_students = {"Aman", "Neha", "Priya"}

print("All students:", python_students.union(linux_students))
print("Common students:", python_students.intersection(linux_students))
print("Only Python:", python_students.difference(linux_students))
```

### What This Code Does

Ye code two course batches compare karta hai.

### Explanation Table

| Code | Simple Hinglish Explanation |
|---|---|
| `union()` | Dono sets ke all unique students. |
| `intersection()` | Jo students dono courses mein common hain. |
| `difference()` | Jo Python mein hain but Linux mein nahi. |

### Real-World Use

Institute ko pata chal sakta hai:

- Total unique students kitne hain
- Dono courses mein common students kaun hain
- Sirf Python wale students kaun hain

---

## Code Explanation 23 - Basic Function

### Code

```python
def greet():
    print("Hello, welcome to Python!")

greet()
```

### What This Code Does

Ye code ek function define karta hai and then usko call karta hai.

### Line-by-Line Explanation

| Line | Code | Simple Hinglish Explanation |
|---|---|---|
| 1 | `def greet():` | `greet` naam ka function define hua. |
| 2 | `print(...)` | Function ke andar ka kaam. |
| 4 | `greet()` | Function call hua, tab print statement run hua. |

### Important Point

Function define karne se code run nahi hota. Function call karna zaroori hai.

---

## Code Explanation 24 - Function with Arguments

### Code

```python
def welcome(name):
    print(f"Welcome {name}")

welcome("Rahul")
welcome("Priya")
```

### What This Code Does

Ye function different users ke liye welcome message print karta hai.

### Line-by-Line Explanation

| Line | Code | Simple Hinglish Explanation |
|---|---|---|
| 1 | `def welcome(name):` | Function ek input leta hai called `name`. |
| 2 | `print(f"Welcome {name}")` | Name ko message ke andar place karta hai. |
| 4 | `welcome("Rahul")` | Function ko Rahul value di gayi. |
| 5 | `welcome("Priya")` | Function ko Priya value di gayi. |

### Parameter vs Argument

| Word | Meaning |
|---|---|
| Parameter | Function definition mein variable, like `name`. |
| Argument | Function call mein actual value, like `"Rahul"`. |

---

## Code Explanation 25 - Function with Return

### Code

```python
def calculate_total(price, quantity):
    total = price * quantity
    return total

bill = calculate_total(500, 3)
final_bill = bill + 50

print("Final bill:", final_bill)
```

### What This Code Does

Ye code product total calculate karta hai, then delivery charge add karta hai.

### Line-by-Line Explanation

| Line | Code | Simple Hinglish Explanation |
|---|---|---|
| 1 | `def calculate_total(price, quantity):` | Function two inputs leta hai: price and quantity. |
| 2 | `total = price * quantity` | Total price calculate hoti hai. |
| 3 | `return total` | Total function ke bahar bheja jata hai. |
| 5 | `bill = calculate_total(500, 3)` | Function call hota hai. Return value `bill` mein store hoti hai. |
| 6 | `final_bill = bill + 50` | Delivery charge 50 add hota hai. |
| 8 | `print(...)` | Final bill print hota hai. |

### Why `return`?

`return` value ko aage use karne ke liye deta hai. Agar sirf `print()` karte, to value variable mein store nahi hoti.

---

## Code Explanation 26 - Default Argument

### Code

```python
def create_user(username, role="student"):
    print(f"Username: {username}, Role: {role}")

create_user("rahul")
create_user("admin1", "admin")
```

### What This Code Does

Ye function user create message print karta hai. Agar role na diya jaye, role automatically student hota hai.

### Line-by-Line Explanation

| Line | Code | Simple Hinglish Explanation |
|---|---|---|
| 1 | `role="student"` | Role ki default value student set hai. |
| 4 | `create_user("rahul")` | Sirf username diya, so role default student use hua. |
| 5 | `create_user("admin1", "admin")` | Username and role dono diye, so admin use hua. |

### Real-World Use

Portal mein mostly users students hote hain. Isliye default role student rakha.

---

## Code Explanation 27 - Keyword Arguments

### Code

```python
def book_ticket(name, source, destination):
    print(f"{name} booked ticket from {source} to {destination}")

book_ticket(destination="Mumbai", name="Rahul", source="Delhi")
```

### What This Code Does

Ye code ticket booking message print karta hai.

### Line-by-Line Explanation

| Code | Simple Hinglish Explanation |
|---|---|
| `destination="Mumbai"` | Destination value directly destination parameter ko milegi. |
| `name="Rahul"` | Name value directly name parameter ko milegi. |
| `source="Delhi"` | Source value directly source parameter ko milegi. |

### Important Point

Keyword arguments mein order matter nahi karta because values parameter names ke saath pass hoti hain.

---

## Code Explanation 28 - Lambda Function

### Code

```python
square = lambda x: x * x

print(square(5))
```

### What This Code Does

Ye one-line function number ka square calculate karta hai.

### Line-by-Line Explanation

| Code | Simple Hinglish Explanation |
|---|---|
| `lambda x:` | Function ek input leta hai called `x`. |
| `x * x` | Input ka square return hota hai. |
| `square = ...` | Lambda function ko square variable mein store kiya. |
| `square(5)` | 5 ka square calculate hota hai. |

### Output Reason

```text
25
```

Because:

```text
5 * 5 = 25
```

---

## Code Explanation 29 - Lambda Sort by Price

### Code

```python
products = [
    {"name": "Keyboard", "price": 1200},
    {"name": "Mouse", "price": 500},
    {"name": "Monitor", "price": 9000}
]

products.sort(key=lambda product: product["price"])

print(products)
```

### What This Code Does

Ye code products ko price ke basis par low to high sort karta hai.

### Line-by-Line Explanation

| Line | Code | Simple Hinglish Explanation |
|---|---|---|
| 1-5 | `products = [...]` | Products ki list hai. Har product dictionary hai. |
| 7 | `products.sort(...)` | Original products list sort hoti hai. |
| 7 | `key=` | Sorting kis basis par hogi, ye batata hai. |
| 7 | `lambda product: product["price"]` | Har product mein se price value lo and uske basis par sort karo. |
| 9 | `print(products)` | Sorted products print hote hain. |

### Output Reason

Products price ke basis par sorted:

```text
Mouse: 500
Keyboard: 1200
Monitor: 9000
```

### Real-World Use

E-commerce website mein “Sort by Price: Low to High” feature same type ke logic se ban sakta hai.

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
