# Python Module 6, 7, and 8 - Proper Hinglish Complete Notes

Lists, Tuples, Dictionaries, Sets, Functions, Lambda Functions, aur To-Do List Manager Project

Yeh notes beginner learners ke liye banaye gaye hain. Language proper Hinglish mein rakhi gayi hai taaki aap khud padhkar samajh sako aur kisi learner ko easily explain bhi kar sako.

---

## Kaise Padhna Hai

Har topic ko is order mein samjho:

1. Pehle real-life example samjho.
2. Phir Python concept samjho.
3. Phir code dekho.
4. Phir output samjho.
5. Phir line-by-line explanation read karo.

Important baat:

Programming ratne wali cheez nahi hai. Programming samajhne, type karne, error dekhne, aur practice karne wali skill hai.

---

## Chapter Index - Kya Kya Seekhoge

| Module | Topic | Simple Meaning |
|---|---|---|
| Module 6 | Lists | Multiple values ko ek variable mein store karna |
| Module 6 | List Operations | Add, update, delete, search, sort |
| Module 6 | Nested Lists | List ke andar list |
| Module 6 | Tuples | Fixed values ka collection |
| Module 6 | Mini Project | CLI To-Do List Manager |
| Module 7 | Dictionaries | Key-value pair data |
| Module 7 | Dictionary Operations | Add, update, delete, loop |
| Module 7 | Sets | Unique values store karna |
| Module 8 | Functions | Reusable code block |
| Module 8 | Arguments and Return | Function ko input dena aur output lena |
| Module 8 | Default Arguments | Agar value na do to default value use hona |
| Module 8 | Keyword Arguments | Naam ke saath value pass karna |
| Module 8 | Lambda Functions | Small one-line function |

---

# Module 6 - Lists and Tuples

## Module 6 Ka Main Idea

Socho aap shopping karne gaye ho. Aapke bag mein ek item nahi, multiple items ho sakte hain:

```text
milk, bread, rice, tea
```

Python mein agar hume multiple values ko ek saath store karna ho, to hum **list** use karte hain.

Ab socho kuch values fixed hain, jaise:

```text
Monday, Tuesday, Wednesday
```

Week days normally change nahi hote. Aise fixed data ke liye hum **tuple** use kar sakte hain.

Simple difference:

| Data Type | Real-Life Example | Change Kar Sakte Hain? |
|---|---|---|
| List | Shopping cart, task list, marks list | Haan |
| Tuple | Week days, GPS location, RGB color | Nahi |

---

## Chapter 1 - List Kya Hoti Hai?

List Python ka ek data type hai jisme hum multiple values ek hi variable mein store kar sakte hain.

Simple Hinglish:

List ek bag/box ki tarah hoti hai. Jaise bag mein multiple items rakh sakte ho, waise list mein multiple values rakh sakte ho.

### Real-Life Example

Shopping cart:

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

### Code

```python
cart = ["milk", "bread", "rice", "tea"]

print(cart)
print(type(cart))
```

### Output

```text
['milk', 'bread', 'rice', 'tea']
<class 'list'>
```

### Line-by-Line Explanation

| Line | Code | Hinglish Explanation |
|---|---|---|
| 1 | `cart = [...]` | `cart` naam ka variable banaya aur usme list store ki. |
| 1 | `[]` | Square brackets batate hain ki yeh list hai. |
| 1 | `"milk"` | Yeh list ka first item hai. Quotes ka matlab text/string. |
| 1 | `,` | Comma items ko separate karta hai. |
| 3 | `print(cart)` | Complete list screen par print hoti hai. |
| 4 | `type(cart)` | Data type check karta hai. Output list aata hai. |

### Teacher Style Explanation

Learner ko aise samjhao:

“Agar hume 4 items store karne hain, to 4 alag variables banane ki zaroorat nahi. Ek list bana do.”

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

List code ko clean, short, aur manageable banati hai.

---

## Chapter 2 - List Indexing

Indexing ka matlab hai list ke kisi specific item ko uski position ke through access karna.

Python mein counting 0 se start hoti hai.

Example:

```python
students = ["Rahul", "Priya", "Aman"]
```

Index map:

```text
Value:   Rahul   Priya   Aman
Index:     0       1      2
Negative: -3      -2     -1
```

### Real-Life Example

Attendance register mein first student chahiye:

```python
students[0]
```

Last student chahiye:

```python
students[-1]
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

| Line | Code | Hinglish Explanation |
|---|---|---|
| 1 | `students = [...]` | Students ki list banayi. |
| 3 | `students[0]` | Index 0 ka item access kiya. Python mein first item index 0 hota hai. |
| 4 | `students[1]` | Index 1 ka item, yani second student access hua. |
| 5 | `students[-1]` | Negative index `-1` last item ko access karta hai. |

### Output Kyu Aaya?

- `students[0]` = Rahul
- `students[1]` = Priya
- `students[-1]` = Aman

### Common Mistake

```python
print(students[3])
```

Error:

```text
IndexError: list index out of range
```

Reason:

List mein 3 items hain, valid indexes 0, 1, 2 hain. Index 3 exist hi nahi karta.

---

## Chapter 3 - List Slicing

Slicing ka matlab hai list ka ek part nikalna.

Syntax:

```python
list_name[start:stop]
```

Important:

`stop` index include nahi hota.

### Real-Life Example

Top 3 students nikalne hain:

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

### Detailed Explanation

| Code | Hinglish Explanation |
|---|---|
| `students[0:3]` | Index 0 se start, index 3 se pehle stop. Isliye Rahul, Priya, Aman. |
| `students[:2]` | Start blank hai, so Python 0 se start karega. Index 2 se pehle rukega. |
| `students[2:]` | Index 2 se start karke end tak jayega. |
| `students[-2:]` | Last 2 items lega. |

### Real-World Use

| Situation | Slicing Use |
|---|---|
| Top 3 students | `students[:3]` |
| Latest 5 orders | `orders[-5:]` |
| First 10 products | `products[:10]` |
| Last 2 messages | `messages[-2:]` |

---

## Chapter 4 - List Operations

List operations ka matlab hai list ke andar changes karna:

- Item add karna
- Item update karna
- Item remove karna
- Item search karna
- Items sort karna

Shopping cart example:

| Action | Python Method |
|---|---|
| Cart mein item add | `append()` |
| Beech mein item add | `insert()` |
| Item edit | Index update |
| Item remove by value | `remove()` |
| Item remove by index | `pop()` |
| Item available hai ya nahi | `in` |
| Items arrange karna | `sort()` |

---

## 4.1 `append()` - End Mein Item Add Karna

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

| Line | Code | Hinglish Explanation |
|---|---|---|
| 1 | `cart = ["milk", "bread"]` | Cart mein starting ke 2 items hain. |
| 3 | `cart.append("rice")` | `append()` rice ko list ke end mein add karta hai. |
| 5 | `print(cart)` | Updated cart print hota hai. |

Real-world:

User ne “Add to Cart” click kiya, product cart list ke end mein add ho gaya.

---

## 4.2 `insert()` - Specific Position Par Item Add Karna

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

| Code | Meaning |
|---|---|
| `insert(1, "Song B")` | Index 1 par Song B add karo. |

Song C right side shift ho gaya.

Real-world:

Music app mein playlist ke beech mein song add karna ho to `insert()` use kar sakte hain.

---

## 4.3 List Item Update Karna

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

| Code | Hinglish Explanation |
|---|---|
| `tasks[1]` | Second item select hua. |
| `= "revise"` | Old value `sleep` replace hoke `revise` ho gayi. |

Real-world:

To-do app mein user old task edit karke new task text set karta hai.

---

## 4.4 `remove()` - Value Se Item Remove Karna

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

`remove("bread")` list ke andar `bread` find karta hai aur usko remove karta hai.

Important:

`remove()` value ke basis par remove karta hai, index ke basis par nahi.

Safe code:

```python
if "bread" in cart:
    cart.remove("bread")
else:
    print("Bread cart mein nahi hai")
```

---

## 4.5 `pop()` - Index Se Item Remove Karna

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

| Code | Hinglish Explanation |
|---|---|
| `notifications.pop()` | Index nahi diya, so last item remove hoga. |
| `latest = ...` | Removed item `latest` variable mein store hoga. |

Real-world:

Notification system mein latest notification ko remove/read karna ho to `pop()` useful hai.

---

## 4.6 `in` - Item Search Karna

### Code

```python
courses = ["Python", "Linux", "AWS"]

if "Python" in courses:
    print("Python course available hai")
else:
    print("Python course available nahi hai")
```

### Output

```text
Python course available hai
```

### Explanation

`in` check karta hai ki value list mein present hai ya nahi.

Real-world:

Website search mein check kar sakte hain ki course available hai ya nahi.

---

## 4.7 `sort()` - List Ko Arrange Karna

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

## Chapter 5 - List Par Loop Chalana

Loop ka use tab hota hai jab same kaam list ke har item par karna ho.

### Real-Life Example

Teacher ko attendance print karni hai:

```python
students = ["Rahul", "Priya", "Aman"]
```

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

### Explanation

| Line | Code | Hinglish Explanation |
|---|---|---|
| 1 | `students = [...]` | Students ki list create hui. |
| 3 | `for student in students:` | Har item one by one `student` variable mein aayega. |
| 4 | `print(...)` | Current student print hoga. |

Loop flow:

| Round | `student` Value | Output |
|---|---|---|
| 1 | Rahul | Attendance: Rahul |
| 2 | Priya | Attendance: Priya |
| 3 | Aman | Attendance: Aman |

---

## Chapter 6 - Nested Lists

Nested list ka matlab hai list ke andar list.

### Real-Life Example

Marks table:

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

| Code | Hinglish Explanation |
|---|---|
| `marks[0]` | First row, yani Rahul ka full data. |
| `marks[1][0]` | Row 1 ka column 0, yani Priya. |
| `marks[1][2]` | Row 1 ka column 2, yani 88. |

Formula:

```python
list[row][column]
```

Real-world:

Nested list table-like data ke liye useful hai, jaise marks table, seating chart, game board.

---

## Chapter 7 - Tuple

Tuple list jaisa hota hai, but tuple ko change nahi kar sakte.

### Real-Life Example

GPS location:

```python
delhi = (28.6139, 77.2090)
```

RGB color:

```python
red = (255, 0, 0)
```

Yeh values accidentally change nahi honi chahiye, isliye tuple useful hai.

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

| Line | Code | Hinglish Explanation |
|---|---|---|
| 1 | `colors = (...)` | Parentheses se tuple create hota hai. |
| 3 | `print(colors)` | Complete tuple print hota hai. |
| 4 | `colors[0]` | First item access hota hai. |
| 5 | `type(colors)` | Data type tuple show hota hai. |

### Tuple Update Nahi Hota

```python
colors[0] = "yellow"
```

Error:

```text
TypeError: 'tuple' object does not support item assignment
```

Meaning:

Tuple immutable hai. Isliye value change nahi kar sakte.

---

# Mini Project - To-Do List Manager

## Project Ka Idea

Hum ek CLI based To-Do List Manager banayenge.

CLI ka matlab:

```text
Command Line Interface
```

Yani program terminal mein chalega.

## Real-World Connection

Ye project same logic use karta hai jo real apps mein hota hai:

| Real App | Similar Feature |
|---|---|
| Notes app | Note add, view, delete |
| To-do app | Task add, complete, delete |
| Shopping cart | Item add, view, remove |
| Ticket system | Ticket open, resolved, delete |

## Data Ka Structure

Ek task:

```python
{"title": "Study Python", "done": False}
```

Multiple tasks:

```python
tasks = [
    {"title": "Study Python", "done": False},
    {"title": "Practice lists", "done": True}
]
```

Explanation:

| Part | Meaning |
|---|---|
| `tasks = []` | Saare tasks list mein store honge. |
| `{}` | Har task dictionary hai. |
| `"title"` | Task ka naam. |
| `"done"` | Task complete hai ya pending. |
| `False` | Pending. |
| `True` | Completed. |

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

## Project Code Ka Full Detailed Explanation

Ab hum project ke code ko chhote-chhote parts mein samjhenge. Har part mein yeh clear hoga:

- Yeh line kya kar rahi hai
- Yeh line kyu use ki gayi hai
- Iska real-world meaning kya hai
- Output par iska effect kya hota hai

---

## Part 1 - Empty Task List

### Code

```python
tasks = []
```

### Explanation

`tasks` ek empty list hai. Is list ke andar saare tasks store honge.

Start mein list empty hai because user ne abhi koi task add nahi kiya.

Real-world example:

Jab aap new to-do app open karte ho aur koi task add nahi hota, to task list blank hoti hai. Waise hi yahan `tasks = []` blank list hai.

### Kyu List Use Ki?

Kyuki hume multiple tasks store karne hain.

Example:

```python
tasks = [
    {"title": "Study Python", "done": False},
    {"title": "Practice lists", "done": True}
]
```

List multiple task dictionaries ko ek saath hold karegi.

---

## Part 2 - Infinite Menu Loop

### Code

```python
while True:
```

### Explanation

`while True` ka matlab hai program continuously chalega.

Yeh loop tab tak stop nahi hoga jab tak hum manually `break` use nahi karte.

### Kyu Use Kiya?

To-Do app mein user sirf ek kaam nahi karta. User:

1. Task add kar sakta hai
2. Task view kar sakta hai
3. Task complete mark kar sakta hai
4. Task delete kar sakta hai
5. Exit kar sakta hai

Isliye menu baar-baar dikhna chahiye. Agar loop nahi hota, program ek operation ke baad band ho jata.

Real-world example:

ATM machine bhi transaction ke baad poochti hai:

```text
Do you want another transaction?
```

Menu based programs mein loop important hota hai.

---

## Part 3 - Menu Print Karna

### Code

```python
print("\n===== To-Do List Manager =====")
print("1. Add Task")
print("2. View Tasks")
print("3. Mark Task as Completed")
print("4. Delete Task")
print("5. Exit")
```

### Explanation

Yeh lines user ko menu options show karti hain.

| Line | Kya Show Hota Hai |
|---|---|
| `print("\n===== To-Do List Manager =====")` | Heading show hoti hai |
| `print("1. Add Task")` | Option 1 task add karne ke liye |
| `print("2. View Tasks")` | Option 2 tasks dekhne ke liye |
| `print("3. Mark Task as Completed")` | Option 3 task complete karne ke liye |
| `print("4. Delete Task")` | Option 4 task delete karne ke liye |
| `print("5. Exit")` | Option 5 program close karne ke liye |

### `\n` Kyu Use Kiya?

`\n` new line add karta hai. Isse har baar menu clean spacing ke saath dikhta hai.

Without `\n`, output crowded lag sakta hai.

---

## Part 4 - User Choice Lena

### Code

```python
choice = input("Enter your choice (1-5): ")
```

### Explanation

`input()` user se value leta hai.

User jo option type karega, wo `choice` variable mein store hoga.

Important:

`input()` hamesha string return karta hai.

So agar user `1` type kare, Python usko `"1"` string ke form mein store karta hai, number `1` ke form mein nahi.

Isliye code mein compare karte hain:

```python
if choice == "1":
```

Not:

```python
if choice == 1:
```

---

## Part 5 - Add Task Option

### Code

```python
if choice == "1":
    title = input("Enter task title: ").strip()
```

### Explanation

`if choice == "1"` check karta hai ki user ne Add Task option choose kiya hai ya nahi.

Agar user ne `1` type kiya, tab program task title maangega.

`.strip()` extra spaces remove karta hai.

Example:

```text
"   Study Python   "
```

`.strip()` ke baad:

```text
"Study Python"
```

### `.strip()` Kyu Use Kiya?

User galti se spaces type kar sakta hai. Hume clean task title chahiye.

Real-world:

Forms mein user extra spaces type kar deta hai. Apps usually input clean karte hain.

---

## Part 6 - Empty Task Check

### Code

```python
if title == "":
    print("Task title cannot be empty.")
```

### Explanation

Yeh check karta hai ki task title blank hai ya nahi.

Agar user sirf Enter press kare ya spaces type kare, `.strip()` ke baad title empty string ban jayega.

Example:

```python
title = ""
```

Tab message print hoga:

```text
Task title cannot be empty.
```

### Kyu Zaroori Hai?

Blank task add karna useful nahi hota.

Bad data:

```python
{"title": "", "done": False}
```

Isliye validation lagaya gaya.

Real-world:

Apps mein required fields blank chhodne par error aata hai, jaise:

```text
Name is required
Email is required
Task title cannot be empty
```

---

## Part 7 - Task Dictionary Banana

### Code

```python
task = {"title": title, "done": False}
```

### Explanation

Yeh line ek task dictionary create karti hai.

Dictionary mein 2 keys hain:

| Key | Meaning |
|---|---|
| `"title"` | Task ka naam |
| `"done"` | Task complete hai ya pending |

`"title": title` ka matlab:

User ne jo title input diya, wo task ka title banega.

`"done": False` ka matlab:

New task initially pending hota hai, completed nahi.

### Example

Agar user title deta hai:

```text
Study Python
```

Task dictionary banegi:

```python
{"title": "Study Python", "done": False}
```

### Kyu Dictionary Use Ki?

Kyuki ek task ke multiple details hain:

- title
- status

List mein sirf title store karte to status manage karna difficult hota.

---

## Part 8 - Task List Mein Add Karna

### Code

```python
tasks.append(task)
print("Task added successfully.")
```

### Explanation

`tasks.append(task)` new task ko `tasks` list ke end mein add karta hai.

Then success message print hota hai.

### Example Flow

Before adding:

```python
tasks = []
```

After adding:

```python
tasks = [
    {"title": "Study Python", "done": False}
]
```

Real-world:

User app mein task create karta hai, task list mein new task add ho jata hai.

---

## Part 9 - View Tasks Option

### Code

```python
elif choice == "2":
```

### Explanation

`elif` ka matlab hai: agar pehla `if` false tha, to ye condition check karo.

Yahan check ho raha hai ki user ne option 2 choose kiya ya nahi.

Option 2 ka kaam hai tasks ko view/show karna.

---

## Part 10 - Empty List Check Before View

### Code

```python
if len(tasks) == 0:
    print("No tasks found.")
```

### Explanation

`len(tasks)` tasks list ke total items count karta hai.

Agar count 0 hai, iska matlab koi task add nahi hua.

Then output:

```text
No tasks found.
```

### Kyu Use Kiya?

Agar list empty hai aur hum tasks print karne ki koshish karein, user ko kuch samajh nahi aayega. Better hai clear message show karna.

Real-world:

Apps mein agar data nahi hota, to message aata hai:

```text
No records found
No tasks found
No messages yet
```

---

## Part 11 - Tasks Ko Numbering Ke Saath Show Karna

### Code

```python
for index, task in enumerate(tasks, start=1):
    status = "Completed" if task["done"] else "Pending"
    print(f"{index}. {task['title']} - {status}")
```

### Explanation

`enumerate()` list ke items ke saath numbering deta hai.

`start=1` ka matlab numbering 1 se start hogi.

### Kyu `start=1` Use Kiya?

Python list index 0 se start hota hai, but normal users numbering 1 se samajhte hain.

User ke liye:

```text
1. Study Python
2. Practice lists
```

Better hai compared to:

```text
0. Study Python
1. Practice lists
```

### Status Line Explanation

```python
status = "Completed" if task["done"] else "Pending"
```

Yeh one-line if-else hai.

Meaning:

```text
Agar task["done"] True hai, status Completed hoga.
Warna status Pending hoga.
```

### Print Line Explanation

```python
print(f"{index}. {task['title']} - {status}")
```

Yeh f-string use karta hai.

Output example:

```text
1. Study Python - Pending
```

---

## Part 12 - Mark Task as Completed

### Code

```python
elif choice == "3":
```

### Explanation

Yeh check karta hai ki user ne option 3 choose kiya hai ya nahi.

Option 3 ka kaam hai selected task ko completed mark karna.

---

## Part 13 - Task Number Input

### Code

```python
task_number = int(input("Enter task number: "))
```

### Explanation

`input()` user se task number leta hai.

`int()` us input ko number mein convert karta hai.

### Kyu `int()` Use Kiya?

`input()` string return karta hai.

Example:

```python
"1"
```

But range check ke liye hume number chahiye:

```python
1
```

Isliye `int()` use kiya.

Note:

Agar user number ki jagah text type kare, error aa sakta hai. Advanced version mein `try-except` use karke handle kar sakte hain.

---

## Part 14 - Valid Task Number Check

### Code

```python
if 1 <= task_number <= len(tasks):
```

### Explanation

Yeh check karta hai ki task number valid range mein hai ya nahi.

Example:

Agar 3 tasks hain:

```text
Valid numbers: 1, 2, 3
Invalid numbers: 0, 4, 5, -1
```

Condition:

```python
1 <= task_number <= len(tasks)
```

Meaning:

Task number 1 se chhota nahi hona chahiye aur total tasks se bada nahi hona chahiye.

---

## Part 15 - Task Complete Mark Karna

### Code

```python
tasks[task_number - 1]["done"] = True
```

### Explanation

Yeh line selected task ka `done` status True kar deti hai.

### `task_number - 1` Kyu?

User numbering 1 se dekhta hai:

```text
1. Study Python
2. Practice lists
```

But Python list index 0 se start hota hai:

```text
Index 0 = Study Python
Index 1 = Practice lists
```

So agar user task number 1 enter kare:

```python
task_number - 1
1 - 1 = 0
```

Correct list index mil gaya.

### Example

Before:

```python
{"title": "Study Python", "done": False}
```

After:

```python
{"title": "Study Python", "done": True}
```

---

## Part 16 - Delete Task Option

### Code

```python
elif choice == "4":
```

### Explanation

Yeh check karta hai ki user ne Delete Task option choose kiya hai ya nahi.

Delete ke liye bhi pehle check karte hain:

```python
if len(tasks) == 0:
    print("No tasks available to delete.")
```

Kyu?

Agar task list empty hai, delete karne ke liye kuch hai hi nahi.

---

## Part 17 - Task Delete Karna

### Code

```python
removed_task = tasks.pop(task_number - 1)
print(f"Deleted task: {removed_task['title']}")
```

### Explanation

`pop(index)` selected index ka item remove karta hai.

`removed_task` variable removed task ko store karta hai.

Phir hum removed task ka title print karte hain:

```python
removed_task["title"]
```

### Example

Before:

```python
tasks = [
    {"title": "Study Python", "done": False},
    {"title": "Practice lists", "done": False}
]
```

User deletes task 1.

After:

```python
tasks = [
    {"title": "Practice lists", "done": False}
]
```

Output:

```text
Deleted task: Study Python
```

---

## Part 18 - Exit Option

### Code

```python
elif choice == "5":
    print("Thank you for using To-Do List Manager.")
    break
```

### Explanation

Yeh check karta hai ki user ne Exit option choose kiya hai.

`break` loop ko stop karta hai.

Without `break`, `while True` loop hamesha chalta rahega.

Real-world:

App mein logout/exit button program ko close karne ke liye hota hai.

---

## Part 19 - Invalid Choice Handle Karna

### Code

```python
else:
    print("Invalid choice. Please enter 1 to 5.")
```

### Explanation

Agar user 1, 2, 3, 4, 5 ke alawa kuch bhi type kare, ye block chalega.

Example:

```text
Enter your choice: 9
Invalid choice. Please enter 1 to 5.
```

### Kyu Zaroori Hai?

User galti kar sakta hai. Program ko crash ya silent nahi hona chahiye. Clear message dena chahiye.

---

## Project Mein Kaun-Kaun Se Concepts Use Hue?

| Concept | Project Mein Use |
|---|---|
| List | Saare tasks store karne ke liye |
| Dictionary | Har task ka title and status store karne ke liye |
| `while True` | Menu baar-baar show karne ke liye |
| `input()` | User se choice and task title lene ke liye |
| `if-elif-else` | Menu options handle karne ke liye |
| `.strip()` | Extra spaces remove karne ke liye |
| `append()` | New task add karne ke liye |
| `len()` | Check karne ke liye ki list empty hai ya nahi |
| `enumerate()` | Tasks ko numbering ke saath show karne ke liye |
| f-string | Clean output print karne ke liye |
| `int()` | Task number ko number mein convert karne ke liye |
| `pop()` | Task delete karne ke liye |
| `break` | Program exit karne ke liye |

## Project Ko Class Mein Kaise Explain Karein

Simple flow:

```text
1. Empty list banti hai.
2. Menu baar-baar show hota hai.
3. User choice deta hai.
4. Choice ke according if/elif block run hota hai.
5. Task add, view, complete, ya delete hota hai.
6. User 5 choose karta hai to loop break hota hai.
```

Ek line explanation:

```text
Yeh project ek real task app ka small version hai jisme list data store karti hai, dictionary task details store karti hai, aur loop menu ko baar-baar chalata hai.
```

---

# Module 7 - Dictionaries and Sets

## Module 7 Ka Main Idea

List index se data access karti hai.

Dictionary key se data access karti hai.

List example:

```python
student = ["Rahul", 20, "Python"]
```

Problem:

`student[0]` dekhkar immediately clear nahi hota ki yeh name hai ya kuch aur.

Dictionary better:

```python
student = {
    "name": "Rahul",
    "age": 20,
    "course": "Python"
}
```

Ab code readable hai:

```python
student["name"]
```

---

## Chapter 8 - Dictionary

Dictionary key-value pairs ka collection hota hai.

### Real-Life Example

Student form:

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

| Code | Hinglish Explanation |
|---|---|
| `"name": "Rahul"` | `name` key hai, `Rahul` value hai. |
| `student["name"]` | Name key ki value access hoti hai. |
| `student["course"]` | Course key ki value access hoti hai. |

Real-world:

Profile, product details, bank account, login data, API response mein dictionary use hoti hai.

---

## Chapter 9 - `get()` Method

`get()` safe tarike se value access karta hai.

### Problem

```python
student = {"name": "Rahul"}

print(student["city"])
```

Error:

```text
KeyError: 'city'
```

Reason:

Dictionary mein `city` key exist nahi karti.

### Safe Code

```python
profile = {
    "name": "Priya",
    "email": "priya@example.com"
}

phone = profile.get("phone", "Phone number not available")

print(phone)
```

### Output

```text
Phone number not available
```

### Explanation

| Code | Hinglish Explanation |
|---|---|
| `profile.get("phone", "...")` | Phone key find karo. Agar missing hai to default message return karo. |

Real-world:

User profile mein phone number optional ho sakta hai. App crash nahi hona chahiye, isliye `get()` useful hai.

---

## Chapter 10 - Dictionary Add and Update

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

| Code | Hinglish Explanation |
|---|---|
| `product["stock"] = 10` | New key stock add hui. |
| `product["price"] = 999` | Existing price update hua. |

Rule:

Agar key exist karti hai, value update hoti hai.

Agar key exist nahi karti, new key-value pair add hota hai.

---

## Chapter 11 - Dictionary Loop

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

| Code | Hinglish Explanation |
|---|---|
| `invoice.items()` | Dictionary ke saare key-value pairs deta hai. |
| `for key, value in ...` | Har pair ko key aur value mein divide karta hai. |
| `print(f"{key}: {value}")` | Clean format mein print karta hai. |

Real-world:

Invoice, student report card, profile page, settings page display karne mein dictionary loop useful hai.

---

## Chapter 12 - Nested Dictionary

Nested dictionary ka matlab dictionary ke andar dictionary.

### Code

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

print(employees["emp101"]["name"])
print(employees["emp102"]["department"])
```

### Output

```text
Rahul
HR
```

### Explanation

| Code | Hinglish Explanation |
|---|---|
| `employees["emp101"]` | Employee 101 ka full data. |
| `employees["emp101"]["name"]` | Employee 101 ka name. |
| `employees["emp102"]["department"]` | Employee 102 ka department. |

Real-world:

Company employee database, student database, product catalog, JSON API response mein nested dictionaries use hoti hain.

---

## Chapter 13 - Set

Set unique values ka collection hota hai.

Duplicate values automatically remove ho jaati hain.

### Real-Life Example

Website visitors:

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

Note:

Set unordered hota hai, so output order change ho sakta hai.

### Explanation

Set duplicate values store nahi karta. Isliye Rahul aur Priya repeat hone ke baad bhi ek hi baar aaye.

---

## Chapter 14 - Set Operations

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

| Operation | Hinglish Explanation |
|---|---|
| `union()` | Dono sets ke saare unique students. |
| `intersection()` | Jo students dono sets mein common hain. |
| `difference()` | Jo first set mein hain but second set mein nahi. |

Real-world:

Institute compare kar sakta hai:

- Total unique students
- Common students
- Sirf Python wale students

---

# Module 8 - Functions

## Module 8 Ka Main Idea

Function ka simple meaning:

```text
Ek kaam ko ek naam de do, phir baar-baar use karo.
```

Example:

Tea machine ka button press karo, tea milti hai. Har baar process manually nahi karna padta.

Function bhi aisa hi hota hai. Ek baar logic define karo, phir function call karo.

---

## Chapter 15 - Basic Function

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

| Code | Hinglish Explanation |
|---|---|
| `def` | Function define karne ka keyword. |
| `greet` | Function ka naam. |
| `()` | Parameters ke liye place. |
| `:` | Function block start hota hai. |
| `print(...)` | Function ka kaam. |
| `greet()` | Function call. Is line par function run hota hai. |

Important:

Function define karne se code run nahi hota. Function ko call karna padta hai.

---

## Chapter 16 - Function with Arguments

Arguments ka matlab function ko input dena.

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

| Part | Meaning |
|---|---|
| `name` | Parameter. Function definition mein variable. |
| `"Rahul"` | Argument. Function call ke time actual value. |
| `f"Welcome {name}"` | f-string. Name ki value message mein insert hoti hai. |

Real-world:

Website login ke baad different users ke liye welcome message show kar sakti hai.

---

## Chapter 17 - Function with Return

`return` function se result bahar bhejta hai.

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

| Line | Code | Hinglish Explanation |
|---|---|---|
| 1 | `def calculate_total(price, quantity):` | Function price aur quantity input leta hai. |
| 2 | `total = price * quantity` | Total calculate hota hai. |
| 3 | `return total` | Total function ke bahar bheja jata hai. |
| 5 | `bill = calculate_total(500, 3)` | Function call hota hai, result bill mein store hota hai. |
| 6 | `final_bill = bill + 50` | Delivery charge add hota hai. |
| 8 | `print(...)` | Final bill print hota hai. |

Why return?

`print()` sirf screen par show karta hai. `return` value ko aage use karne deta hai.

---

## Chapter 18 - Default Arguments

Default argument ka matlab: agar user value na de, to default value use ho.

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

| Code | Hinglish Explanation |
|---|---|
| `role="student"` | Role ki default value student hai. |
| `create_user("rahul")` | Role pass nahi hua, so student use hua. |
| `create_user("admin1", "admin")` | Role diya gaya, so admin use hua. |

Real-world:

Training portal mein most users students hote hain, isliye default role student rakha.

---

## Chapter 19 - Keyword Arguments

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

| Keyword | Value |
|---|---|
| `destination` | Mumbai |
| `name` | Rahul |
| `source` | Delhi |

Real-world:

Ticket booking, hotel booking, user registration mein keyword arguments readability improve karte hain.

---

## Chapter 20 - Lambda Functions

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

| Code | Hinglish Explanation |
|---|---|
| `lambda x:` | Function ek input leta hai, jiska naam `x` hai. |
| `x * x` | Input ka square return karta hai. |
| `square = ...` | Lambda function ko variable mein store kiya. |
| `square(5)` | 5 ka square calculate hua. |

Real-world:

Short calculation, filtering, sorting mein lambda useful hota hai.

---

## Chapter 21 - Lambda Sort by Price

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

### Output

```text
[{'name': 'Mouse', 'price': 500}, {'name': 'Keyboard', 'price': 1200}, {'name': 'Monitor', 'price': 9000}]
```

### Explanation

| Code | Hinglish Explanation |
|---|---|
| `products = [...]` | Products ki list hai. Har product dictionary hai. |
| `products.sort(...)` | Products list sort hoti hai. |
| `key=` | Sorting kis basis par hogi, ye batata hai. |
| `lambda product: product["price"]` | Har product mein se price nikalo aur price ke basis par sort karo. |

Real-world:

E-commerce website mein “Sort by price low to high” isi type ke logic se ban sakta hai.

---

# Practice Questions

## Question 1 - Shopping Cart

Ek `cart` list banao. Usme 3 items add karo. Phir `append()` se ek aur item add karo. Final cart print karo.

## Question 2 - Attendance List

5 students ki list banao. First student, last student, aur total students print karo.

## Question 3 - Top 3 Marks

Marks ki list banao. Slicing use karke top 3 marks print karo.

## Question 4 - Update Task

Task list banao. Second task ko update karo.

## Question 5 - Student Dictionary

Student dictionary banao jisme `name`, `age`, `course` ho. Har value key ke through print karo.

## Question 6 - Product Stock

Product dictionary banao. Stock ko 1 se reduce karo and updated product print karo.

## Question 7 - Unique Emails

Duplicate emails wali list banao. Use set mein convert karke unique emails print karo.

## Question 8 - Course Comparison

Python students aur Linux students ke two sets banao. All students and common students print karo.

## Question 9 - Discount Function

Function banao jo price and discount percentage input le aur final price return kare.

## Question 10 - Lambda Cube

Lambda function banao jo number ka cube return kare.

---

# Quick Revision

| Concept | Hinglish Meaning | Real-World Example |
|---|---|---|
| List | Multiple values ka collection | Shopping cart |
| Index | Position number | First student |
| Slicing | List ka part | Top 3 marks |
| Nested List | List ke andar list | Marks table |
| Tuple | Fixed values | GPS location |
| Dictionary | Key-value data | Student profile |
| Set | Unique values | Unique visitors |
| Function | Reusable code | Billing calculation |
| Return | Result bahar bhejna | Final bill |
| Default Argument | Backup value | Default role |
| Keyword Argument | Naam ke saath value | Ticket booking |
| Lambda | One-line function | Sort by price |

---

# Final Advice

Learners ko concepts real life se connect karke samjhao.

Simple examples:

- List means shopping cart.
- Dictionary means form/profile.
- Set means unique collection.
- Function means reusable machine.
- Lambda means short one-line function.

Jab learner real-world meaning samajh leta hai, tab code samajhna easy ho jata hai.

Happy Coding.
