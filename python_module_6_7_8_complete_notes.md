# Python Module 6, 7, and 8 - Complete Notes

Lists, Tuples, Dictionaries, Sets, Functions, Lambda Functions, and To-Do List Manager Project

Language style: Simple English with light Hinglish explanation.

Goal: Is document ko padhkar beginner easily samajh sake, aur teacher/student kisi ko bhi step-by-step explain kar sake. Har topic ke saath code, output, and detailed explanation diya gaya hai.

---

## Chapter Index - What You Will Learn

| Module | Topic | Main Idea |
|---|---|---|
| Module 6 | Lists | Multiple values ko ek variable mein store karna |
| Module 6 | List Operations | Add, update, delete, search, sort |
| Module 6 | Nested Lists | List ke andar list |
| Module 6 | Tuples | Fixed/unchangeable sequence |
| Module 6 | Mini Project | CLI-based To-Do List Manager |
| Module 7 | Dictionaries | Key-value data handling |
| Module 7 | Dictionary Operations | Add, update, delete, access |
| Module 7 | Key-Value Manipulation | Data ko keys ke through manage karna |
| Module 7 | Sets | Unique values ka collection |
| Module 7 | Set Operations | Union, intersection, difference |
| Module 8 | Functions | Reusable code blocks |
| Module 8 | Arguments and Return Values | Function ko input dena and output lena |
| Module 8 | Default Arguments | Agar value na mile to default use karna |
| Module 8 | Keyword Arguments | Argument ko naam ke saath pass karna |
| Module 8 | Lambda Functions | Small one-line functions |

---

# Module 6 - Lists and Tuples

Module 6 ka main focus hai multiple values ko store and manage karna. Python mein lists and tuples dono sequence data types hain.

Simple difference:

| Type | Changeable? | Syntax | Example |
|---|---|---|---|
| List | Yes, mutable | `[]` | `["apple", "banana"]` |
| Tuple | No, immutable | `()` | `("red", "green")` |

---

## Chapter 1 - What is a List?

List Python ka data type hai jisme multiple values ek hi variable mein store kar sakte hain.

Example:

```python
fruits = ["apple", "banana", "mango"]
```

Simple meaning:

Ek list ek container ki tarah hoti hai. Is container mein multiple items store ho sakte hain.

## Real-World Use Case

List ka use tab hota hai jab ek hi type ke multiple items ko ek saath manage karna ho.

Real examples:

| Situation | List Example | Why List is Useful |
|---|---|---|
| Shopping app | `cart_items = ["milk", "bread", "rice"]` | User ke cart ke saare items ek jagah store kar sakte hain |
| School marks | `marks = [85, 90, 78, 92]` | Student ke multiple subject marks store kar sakte hain |
| To-do app | `tasks = ["study", "practice", "revise"]` | Daily tasks ko add/remove/update kar sakte hain |
| Website menu | `menu = ["Home", "About", "Contact"]` | Navigation options ko sequence mein store kar sakte hain |
| Employee names | `employees = ["Aman", "Priya", "Rahul"]` | Company ke employees ki list maintain kar sakte hain |

Simple Hinglish explanation:

Agar aapke paas ek se zyada values hain aur aap un par loop chalana, search karna, add karna, ya remove karna chahte ho, to list best choice hoti hai.

## List Syntax

```python
list_name = [item1, item2, item3]
```

Syntax explanation:

| Part | Meaning |
|---|---|
| `list_name` | Variable name |
| `=` | Assignment operator |
| `[]` | Square brackets list banate hain |
| `item1, item2` | List ke values/items |
| `,` | Items ko separate karta hai |

---

## Example 1 - Create and Print a List

```python
fruits = ["apple", "banana", "mango", "orange"]

print(fruits)
print(type(fruits))
```

## Output

```text
['apple', 'banana', 'mango', 'orange']
<class 'list'>
```

## Detailed Code Explanation

| Line | Code | Explanation |
|---|---|---|
| 1 | `fruits = [...]` | `fruits` naam ka variable banaya. Isme 4 string values store hain. |
| 3 | `print(fruits)` | Complete list print karta hai. |
| 4 | `type(fruits)` | Variable ka data type check karta hai. Output `list` aata hai. |

Important:

List ke andar different data types bhi store ho sakte hain:

```python
student = ["Rahul", 20, 85.5, True]
```

But clean code ke liye usually same type ka data list mein rakhna better hota hai.

---

## Chapter 2 - List Indexing

List indexing string indexing jaisi hoti hai. Python index 0 se start karta hai.

Example:

```text
fruits = ["apple", "banana", "mango", "orange"]
Index      0        1         2        3
Negative  -4       -3        -2       -1
```

## Example

```python
fruits = ["apple", "banana", "mango", "orange"]

print(fruits[0])
print(fruits[1])
print(fruits[-1])
print(fruits[-2])
```

## Output

```text
apple
banana
orange
mango
```

## Detailed Code Explanation

| Line | Code | Explanation |
|---|---|---|
| 1 | `fruits = [...]` | 4 items wali list create ki. |
| 3 | `fruits[0]` | First item access karta hai: `apple`. |
| 4 | `fruits[1]` | Second item access karta hai: `banana`. |
| 5 | `fruits[-1]` | Last item access karta hai: `orange`. |
| 6 | `fruits[-2]` | End se second item access karta hai: `mango`. |

Common mistake:

```python
print(fruits[4])
```

This gives error because valid indexes are 0, 1, 2, 3.

## Real-World Use Case

Indexing ka use tab hota hai jab hume list ka specific item chahiye hota hai.

Example situations:

| Situation | Code Idea | Meaning |
|---|---|---|
| First rank student | `students[0]` | List ka first student |
| Latest message | `messages[-1]` | Last received message |
| First product in cart | `cart[0]` | Cart ka first item |
| Last transaction | `transactions[-1]` | Most recent transaction |

Example:

```python
messages = ["Hi", "How are you?", "See you tomorrow"]

print("Latest message:", messages[-1])
```

Output:

```text
Latest message: See you tomorrow
```

Explanation:

Chat application mein latest message usually list ke end mein hota hai. Isliye `messages[-1]` se last message easily mil jata hai.

---

## Chapter 3 - List Slicing

Slicing ka use list ka part nikalne ke liye hota hai.

Syntax:

```python
list_name[start:stop:step]
```

Important: `stop` index include nahi hota.

## Example

```python
numbers = [10, 20, 30, 40, 50, 60]

print(numbers[0:3])
print(numbers[2:5])
print(numbers[:4])
print(numbers[3:])
print(numbers[::-1])
```

## Output

```text
[10, 20, 30]
[30, 40, 50]
[10, 20, 30, 40]
[40, 50, 60]
[60, 50, 40, 30, 20, 10]
```

## Detailed Code Explanation

| Code | Explanation |
|---|---|
| `numbers[0:3]` | Index 0, 1, 2 values leta hai. Index 3 include nahi hota. |
| `numbers[2:5]` | Index 2 se 4 tak values. |
| `numbers[:4]` | Start default 0 hai. Index 0 to 3. |
| `numbers[3:]` | Index 3 se end tak. |
| `numbers[::-1]` | List reverse order mein return karta hai. |

## Real-World Use Case

Slicing ka use tab hota hai jab hume complete list nahi, sirf ek part chahiye.

Real examples:

| Situation | Code Idea | Meaning |
|---|---|---|
| Top 3 students | `students[:3]` | First 3 students |
| Latest 5 orders | `orders[-5:]` | Last 5 orders |
| Skip first 2 records | `records[2:]` | First 2 records ignore |
| Reverse history | `history[::-1]` | Latest item first dikhana |

Example:

```python
orders = ["order1", "order2", "order3", "order4", "order5"]

latest_orders = orders[-2:]

print(latest_orders)
```

Output:

```text
['order4', 'order5']
```

Explanation:

E-commerce app mein latest orders list ke end mein add hote hain. `orders[-2:]` last 2 orders nikalta hai.

---

## Chapter 4 - List Operations

List operations ka matlab list mein items add, update, remove, search, sort, etc. karna.

## Real-World Use Case

List operations real apps mein daily use hote hain.

| Operation | Real Example |
|---|---|
| `append()` | Shopping cart mein new product add karna |
| `insert()` | Playlist mein song ko specific position par add karna |
| `extend()` | Two batches ke students ko combine karna |
| Update by index | To-do task ka text change karna |
| `remove()` | Cart se product remove karna |
| `pop()` | Last notification read/remove karna |
| `sort()` | Marks ko low-to-high ya high-to-low arrange karna |
| `in` | Check karna ki product available hai ya nahi |

Is chapter ko practical thinking se samjho: list ek dynamic collection hai. Matlab items time ke saath change ho sakte hain.

---

## 1. Add Item with `append()`

`append()` list ke end mein new item add karta hai.

```python
tasks = ["study", "practice"]

tasks.append("revise")

print(tasks)
```

## Output

```text
['study', 'practice', 'revise']
```

## Explanation

| Line | Code | Explanation |
|---|---|---|
| 1 | `tasks = [...]` | 2 tasks wali list create ki. |
| 3 | `tasks.append("revise")` | End mein `"revise"` add kiya. |
| 5 | `print(tasks)` | Updated list print hui. |

Important:

`append()` only one item add karta hai.

---

## 2. Add Item at Specific Position with `insert()`

```python
fruits = ["apple", "mango"]

fruits.insert(1, "banana")

print(fruits)
```

## Output

```text
['apple', 'banana', 'mango']
```

## Explanation

`insert(1, "banana")` index 1 par `"banana"` insert karta hai. Existing items right side shift ho jaate hain.

---

## 3. Add Multiple Items with `extend()`

```python
numbers = [1, 2, 3]

numbers.extend([4, 5, 6])

print(numbers)
```

## Output

```text
[1, 2, 3, 4, 5, 6]
```

## Explanation

`extend()` ek list ke items ko doosri list ke end mein add karta hai.

Important difference:

```python
a = [1, 2]
a.append([3, 4])
print(a)
```

Output:

```text
[1, 2, [3, 4]]
```

But:

```python
a = [1, 2]
a.extend([3, 4])
print(a)
```

Output:

```text
[1, 2, 3, 4]
```

Meaning:

| Method | Result |
|---|---|
| `append([3, 4])` | Complete list ko single item bana deta hai |
| `extend([3, 4])` | Items ko separately add karta hai |

---

## 4. Update List Item

Lists mutable hoti hain, meaning list ke items change kar sakte hain.

```python
fruits = ["apple", "banana", "mango"]

fruits[1] = "orange"

print(fruits)
```

## Output

```text
['apple', 'orange', 'mango']
```

## Explanation

`fruits[1]` originally `"banana"` tha. Humne uski value `"orange"` se replace kar di.

---

## 5. Remove Item with `remove()`

```python
fruits = ["apple", "banana", "mango"]

fruits.remove("banana")

print(fruits)
```

## Output

```text
['apple', 'mango']
```

## Explanation

`remove("banana")` list se first matching item remove karta hai.

Important:

If item does not exist, error aata hai.

```python
fruits.remove("grapes")
```

Error:

```text
ValueError: list.remove(x): x not in list
```

Safe way:

```python
if "grapes" in fruits:
    fruits.remove("grapes")
else:
    print("Item not found")
```

---

## 6. Remove Item with `pop()`

`pop()` index ke basis par item remove karta hai and removed item return bhi karta hai.

```python
fruits = ["apple", "banana", "mango"]

removed_item = fruits.pop(1)

print("Removed:", removed_item)
print("List:", fruits)
```

## Output

```text
Removed: banana
List: ['apple', 'mango']
```

## Explanation

| Code | Meaning |
|---|---|
| `fruits.pop(1)` | Index 1 ka item remove karta hai |
| `removed_item` | Removed value store karta hai |

If no index is given:

```python
fruits.pop()
```

Last item remove hota hai.

---

## 7. Delete Item with `del`

```python
numbers = [10, 20, 30, 40]

del numbers[2]

print(numbers)
```

## Output

```text
[10, 20, 40]
```

## Explanation

`del numbers[2]` index 2 ka item delete karta hai. Index 2 par `30` tha.

---

## 8. Find Length with `len()`

```python
tasks = ["study", "practice", "revise"]

print(len(tasks))
```

## Output

```text
3
```

## Explanation

`len(tasks)` list ke total items count karta hai.

---

## 9. Search Item with `in`

```python
fruits = ["apple", "banana", "mango"]

if "mango" in fruits:
    print("Mango is available")
else:
    print("Mango is not available")
```

## Output

```text
Mango is available
```

## Explanation

`in` membership operator hai. Ye check karta hai item list mein present hai ya nahi.

---

## 10. Sort a List

```python
marks = [80, 45, 90, 60]

marks.sort()

print(marks)
```

## Output

```text
[45, 60, 80, 90]
```

## Descending Sort

```python
marks.sort(reverse=True)
print(marks)
```

## Output

```text
[90, 80, 60, 45]
```

## Explanation

| Code | Meaning |
|---|---|
| `sort()` | Ascending order |
| `sort(reverse=True)` | Descending order |

Important:

`sort()` original list ko change karta hai.

If you want a new sorted list:

```python
new_list = sorted(marks)
```

---

## Chapter 5 - Loop Through a List

List ke har item par kaam karne ke liye `for` loop use karte hain.

```python
fruits = ["apple", "banana", "mango"]

for fruit in fruits:
    print("Fruit:", fruit)
```

## Output

```text
Fruit: apple
Fruit: banana
Fruit: mango
```

## Detailed Code Explanation

| Line | Code | Explanation |
|---|---|---|
| 1 | `fruits = [...]` | Fruits list create ki. |
| 3 | `for fruit in fruits:` | Har item one by one `fruit` variable mein aata hai. |
| 4 | `print(...)` | Current fruit print hota hai. |

## Real-World Use Case

Loop through list tab use hota hai jab same action multiple items par perform karna ho.

Examples:

| Situation | What Loop Does |
|---|---|
| Send emails | Har email address par email send karo |
| Print invoice | Har product ka price print karo |
| Student result | Har student ke marks check karo |
| File processing | Har file ko read/process karo |

Example:

```python
prices = [100, 200, 150]

for price in prices:
    final_price = price + 20
    print("Final price:", final_price)
```

Output:

```text
Final price: 120
Final price: 220
Final price: 170
```

Explanation:

Suppose delivery charge 20 rupees hai. Loop har price par same delivery charge add kar raha hai.

---

## Chapter 6 - Nested Lists

Nested list means list ke andar list.

Example:

```python
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
```

Ye ek 3x3 table jaisa structure hai.

## Access Nested List Items

```python
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

print(matrix[0])
print(matrix[1][2])
print(matrix[2][0])
```

## Output

```text
[1, 2, 3]
6
7
```

## Detailed Explanation

| Code | Meaning |
|---|---|
| `matrix[0]` | First inner list: `[1, 2, 3]` |
| `matrix[1][2]` | Second row, third item: `6` |
| `matrix[2][0]` | Third row, first item: `7` |

Think like this:

```text
matrix[row][column]
```

## Real-World Use Case

Nested lists tab useful hoti hain jab data rows and columns mein ho.

Examples:

| Situation | Nested List Structure |
|---|---|
| Classroom marks | Har student ke multiple subject marks |
| Game board | Tic-tac-toe board or chess board |
| Excel-like data | Rows and columns |
| Seating arrangement | Rows of seats in theatre |

Example:

```python
marks = [
    ["Rahul", 85, 90],
    ["Priya", 92, 88],
    ["Aman", 78, 84]
]

print(marks[1][0])
print(marks[1][2])
```

Output:

```text
Priya
88
```

Explanation:

`marks[1]` second student ka row hai. `marks[1][0]` name hai, and `marks[1][2]` second subject ke marks hain.

---

## Loop Through Nested List

```python
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

for row in matrix:
    for number in row:
        print(number, end=" ")
    print()
```

## Output

```text
1 2 3
4 5 6
7 8 9
```

## Detailed Code Explanation

| Line | Code | Explanation |
|---|---|---|
| 1-5 | `matrix = [...]` | Nested list create ki. |
| 7 | `for row in matrix:` | Har inner list ko `row` mein store karta hai. |
| 8 | `for number in row:` | Row ke har number par loop chalta hai. |
| 9 | `print(number, end=" ")` | Same line mein number print karta hai. |
| 10 | `print()` | Har row ke baad new line print karta hai. |

---

## Chapter 7 - Tuple Basics

Tuple list jaisa hota hai, but tuple immutable hota hai. Immutable means create hone ke baad change nahi kar sakte.

Syntax:

```python
colors = ("red", "green", "blue")
```

## Example

```python
colors = ("red", "green", "blue")

print(colors)
print(colors[0])
print(type(colors))
```

## Output

```text
('red', 'green', 'blue')
red
<class 'tuple'>
```

## Explanation

| Line | Code | Explanation |
|---|---|---|
| 1 | `colors = (...)` | Tuple create kiya. |
| 3 | `print(colors)` | Complete tuple print karta hai. |
| 4 | `colors[0]` | First item access karta hai. |
| 5 | `type(colors)` | Data type tuple show karta hai. |

---

## Tuple Cannot Be Changed

```python
colors = ("red", "green", "blue")

colors[1] = "yellow"
```

## Output

```text
TypeError: 'tuple' object does not support item assignment
```

## Explanation

Tuple immutable hota hai. Isliye index value update nahi kar sakte.

## Why Use Tuple?

Tuples use karte hain jab data fixed ho.

Examples:

```python
days = ("Monday", "Tuesday", "Wednesday")
coordinates = (10, 20)
rgb_color = (255, 0, 0)
```

## Single Item Tuple

```python
a = ("apple")
b = ("apple",)

print(type(a))
print(type(b))
```

## Output

```text
<class 'str'>
<class 'tuple'>
```

Important:

Single item tuple ke liye comma zaroori hai.

## Real-World Use Case

Tuple ka use fixed data ke liye hota hai, jise program ke beech mein change nahi karna chahiye.

Examples:

| Situation | Tuple Example | Why Tuple |
|---|---|---|
| GPS location | `(28.6139, 77.2090)` | Latitude/longitude fixed pair hota hai |
| RGB color | `(255, 0, 0)` | Red color ka fixed value |
| Week days | `("Mon", "Tue", "Wed")` | Week days normally change nahi hote |
| Database row | `(101, "Rahul", 85)` | Record ko fixed form mein read kar sakte hain |

Simple explanation:

Agar data ko accidental change se protect karna hai, tuple use karna better hota hai. List flexible hai; tuple safer hai for fixed data.

---

# Mini Project - To-Do List Manager CLI Based

This project uses lists, loops, conditions, functions basics, and user input. CLI means Command Line Interface.

## Project Goal

Program user ko options dega:

1. Add task
2. View tasks
3. Mark task as completed
4. Delete task
5. Exit

We will store tasks in a list. Each task will be a dictionary:

```python
{"title": "Study Python", "done": False}
```

This structure helps us store task name and completion status together.

## Real-World Use Case

To-Do List Manager ek simple project hai, but iska logic bahut real applications mein use hota hai.

Examples:

| Real Application | Similar Logic |
|---|---|
| Notes app | Notes add, view, delete |
| Task management app | Task create, complete, remove |
| Shopping cart | Product add, view, remove |
| Ticket system | Tickets create and mark resolved |
| Student assignment tracker | Assignment add and mark submitted |

Is project mein list tasks ko store karti hai, aur dictionary har task ka detail store karti hai. Real apps mein bhi same idea use hota hai: collection ke liye list, structured item ke liye dictionary.

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
            task_number = int(input("Enter task number to mark completed: "))

            if 1 <= task_number <= len(tasks):
                tasks[task_number - 1]["done"] = True
                print("Task marked as completed.")
            else:
                print("Invalid task number.")

    elif choice == "4":
        if len(tasks) == 0:
            print("No tasks available to delete.")
        else:
            task_number = int(input("Enter task number to delete: "))

            if 1 <= task_number <= len(tasks):
                removed_task = tasks.pop(task_number - 1)
                print(f"Deleted task: {removed_task['title']}")
            else:
                print("Invalid task number.")

    elif choice == "5":
        print("Thank you for using To-Do List Manager.")
        break

    else:
        print("Invalid choice. Please enter a number from 1 to 5.")
```

## Sample Output

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

===== To-Do List Manager =====
Enter your choice (1-5): 2

Your Tasks:
1. Study lists - Pending
```

## Detailed Code Explanation

| Code | Explanation |
|---|---|
| `tasks = []` | Empty list create ki. Saare tasks isi list mein store honge. |
| `while True:` | Program continuously run karega jab tak user exit na kare. |
| `print(...)` menu lines | User ko options show karte hain. |
| `choice = input(...)` | User ka selected option string ke form mein store hota hai. |
| `if choice == "1":` | Add task option handle karta hai. |
| `title.strip()` | Extra spaces remove karta hai. |
| `if title == "":` | Empty task check karta hai. |
| `task = {"title": title, "done": False}` | Task ko dictionary ke form mein store karta hai. |
| `tasks.append(task)` | New task list ke end mein add hota hai. |
| `elif choice == "2":` | View tasks option. |
| `len(tasks) == 0` | Check karta hai list empty hai ya nahi. |
| `enumerate(tasks, start=1)` | Tasks ko numbering ke saath loop karta hai. |
| `status = "Completed" if ... else ...` | One-line conditional expression. |
| `task["done"]` | Dictionary se done status read karta hai. |
| `elif choice == "3":` | Task complete mark karne ka option. |
| `tasks[task_number - 1]` | User numbering 1 se start hoti hai, list index 0 se. Isliye `-1`. |
| `["done"] = True` | Selected task ka status completed banata hai. |
| `elif choice == "4":` | Delete task option. |
| `tasks.pop(task_number - 1)` | Selected task remove karta hai and removed task return karta hai. |
| `elif choice == "5":` | Exit option. |
| `break` | Loop stop karta hai. |
| `else:` | Invalid choice handle karta hai. |

## Important Learning from Project

| Concept | Use |
|---|---|
| List | Multiple tasks store karna |
| Dictionary | Task title and status together store karna |
| while loop | Program repeatedly run karna |
| if-elif-else | Menu choices handle karna |
| append | Task add karna |
| pop | Task delete karna |
| enumerate | Numbering ke saath tasks show karna |
| f-string | Clean output print karna |

---

# Module 7 - Dictionaries and Sets

Module 7 ka main focus key-value data and unique data handling hai.

---

## Chapter 8 - What is a Dictionary?

Dictionary key-value pairs ka collection hota hai.

Example:

```python
student = {
    "name": "Rahul",
    "age": 20,
    "course": "Python"
}
```

Simple meaning:

Dictionary real-life form jaisa hota hai:

```text
name: Rahul
age: 20
course: Python
```

## Real-World Use Case

Dictionary tab use hoti hai jab data ko label ke saath store karna ho.

Real examples:

| Situation | Dictionary Example |
|---|---|
| Student profile | `{"name": "Rahul", "age": 20, "course": "Python"}` |
| Product details | `{"name": "Laptop", "price": 55000, "stock": 10}` |
| Login user | `{"username": "admin", "role": "manager"}` |
| API response | `{"status": "success", "data": [...]}` |
| Contact book | `{"name": "Aman", "phone": "9876543210"}` |

Simple Hinglish explanation:

List mein value index se milti hai, but dictionary mein value key se milti hai. Agar data ka meaning important hai, dictionary better hoti hai.

## Dictionary Syntax

```python
dict_name = {
    key1: value1,
    key2: value2
}
```

| Part | Meaning |
|---|---|
| `{}` | Dictionary create karta hai |
| `key` | Data ka name/label |
| `value` | Actual data |
| `:` | Key and value ko separate karta hai |
| `,` | Pairs ko separate karta hai |

---

## Example 1 - Create and Access Dictionary

```python
student = {
    "name": "Rahul",
    "age": 20,
    "course": "Python"
}

print(student)
print(student["name"])
print(student["age"])
```

## Output

```text
{'name': 'Rahul', 'age': 20, 'course': 'Python'}
Rahul
20
```

## Detailed Code Explanation

| Line | Code | Explanation |
|---|---|---|
| 1-5 | `student = {...}` | Dictionary create ki with 3 key-value pairs. |
| 7 | `print(student)` | Complete dictionary print karta hai. |
| 8 | `student["name"]` | `name` key ki value access karta hai. |
| 9 | `student["age"]` | `age` key ki value access karta hai. |

---

## Chapter 9 - Access Value Safely with `get()`

Direct key access wrong key par error de sakta hai.

```python
student = {"name": "Rahul", "age": 20}

print(student["city"])
```

Output:

```text
KeyError: 'city'
```

Safe way:

```python
student = {"name": "Rahul", "age": 20}

print(student.get("city"))
print(student.get("city", "Not available"))
```

## Output

```text
None
Not available
```

## Explanation

| Code | Meaning |
|---|---|
| `student.get("city")` | Key missing hai, so `None` return karta hai. |
| `student.get("city", "Not available")` | Key missing hai, default value return karta hai. |

## Real-World Use Case

`get()` tab useful hota hai jab data incomplete ho sakta hai.

Example:

```python
profile = {
    "name": "Rahul",
    "email": "rahul@example.com"
}

phone = profile.get("phone", "Phone number not added")

print(phone)
```

Output:

```text
Phone number not added
```

Explanation:

Real apps mein user profile incomplete ho sakti hai. Kisi user ne phone number add nahi kiya ho, to direct `profile["phone"]` error dega. `get()` app ko crash hone se bachata hai.

---

## Chapter 10 - Add and Update Dictionary Values

```python
student = {
    "name": "Rahul",
    "age": 20
}

student["course"] = "Python"
student["age"] = 21

print(student)
```

## Output

```text
{'name': 'Rahul', 'age': 21, 'course': 'Python'}
```

## Explanation

| Code | Explanation |
|---|---|
| `student["course"] = "Python"` | New key-value pair add karta hai. |
| `student["age"] = 21` | Existing key ki value update karta hai. |

Important:

If key already exists, value update hoti hai. If key does not exist, new pair add hota hai.

## Real-World Use Case

Dictionary update ka use user profile, product stock, scoreboards, and settings mein hota hai.

Example:

```python
product = {
    "name": "Keyboard",
    "price": 1200,
    "stock": 5
}

product["stock"] = product["stock"] - 1
product["status"] = "Available"

print(product)
```

Output:

```text
{'name': 'Keyboard', 'price': 1200, 'stock': 4, 'status': 'Available'}
```

Explanation:

Customer ne ek keyboard buy kiya, so stock 5 se 4 ho gaya. `status` new key add hui. Real e-commerce systems mein stock update exactly isi type ke logic se hota hai.

---

## Chapter 11 - Delete Dictionary Values

## Using `pop()`

```python
student = {"name": "Rahul", "age": 20, "course": "Python"}

removed_value = student.pop("age")

print("Removed:", removed_value)
print(student)
```

## Output

```text
Removed: 20
{'name': 'Rahul', 'course': 'Python'}
```

## Using `del`

```python
student = {"name": "Rahul", "age": 20}

del student["age"]

print(student)
```

## Output

```text
{'name': 'Rahul'}
```

## Explanation

| Method | Meaning |
|---|---|
| `pop("age")` | Key remove karta hai and value return karta hai |
| `del student["age"]` | Key-value pair delete karta hai |

---

## Chapter 12 - Dictionary Methods

```python
student = {
    "name": "Rahul",
    "age": 20,
    "course": "Python"
}

print(student.keys())
print(student.values())
print(student.items())
```

## Output

```text
dict_keys(['name', 'age', 'course'])
dict_values(['Rahul', 20, 'Python'])
dict_items([('name', 'Rahul'), ('age', 20), ('course', 'Python')])
```

## Explanation

| Method | Meaning |
|---|---|
| `keys()` | All keys return karta hai |
| `values()` | All values return karta hai |
| `items()` | Key-value pairs return karta hai |

---

## Chapter 13 - Loop Through Dictionary

```python
student = {
    "name": "Rahul",
    "age": 20,
    "course": "Python"
}

for key, value in student.items():
    print(key, ":", value)
```

## Output

```text
name : Rahul
age : 20
course : Python
```

## Detailed Explanation

| Code | Explanation |
|---|---|
| `student.items()` | Key-value pairs return karta hai. |
| `for key, value in ...` | Har pair ko key and value variables mein unpack karta hai. |
| `print(key, ":", value)` | Clean format mein output print karta hai. |

## Real-World Use Case

Dictionary loop tab use hota hai jab hume complete data readable format mein show karna ho.

Example:

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

Output:

```text
Product: Mouse
Price: 500
Quantity: 2
Total: 1000
```

Explanation:

Invoice, report, profile page, and settings page mein key-value data ko display karna common task hai.

---

## Chapter 14 - Nested Dictionary

Nested dictionary means dictionary ke andar dictionary.

```python
students = {
    "s1": {"name": "Rahul", "marks": 85},
    "s2": {"name": "Priya", "marks": 92},
    "s3": {"name": "Aman", "marks": 78}
}

print(students["s1"]["name"])
print(students["s2"]["marks"])
```

## Output

```text
Rahul
92
```

## Explanation

| Code | Meaning |
|---|---|
| `students["s1"]` | First student ka dictionary |
| `students["s1"]["name"]` | First student ka name |
| `students["s2"]["marks"]` | Second student ke marks |

Nested dictionaries real projects mein common hote hain.

## Real-World Use Case

Nested dictionary tab useful hoti hai jab ek main record ke andar aur detailed records store karne ho.

Example:

```python
company = {
    "emp101": {
        "name": "Rahul",
        "department": "IT",
        "salary": 35000
    },
    "emp102": {
        "name": "Priya",
        "department": "HR",
        "salary": 40000
    }
}

print(company["emp102"]["department"])
```

Output:

```text
HR
```

Explanation:

Company system mein employee ID key ho sakti hai, aur uske andar employee details dictionary ke form mein store ho sakte hain.

---

## Chapter 15 - What is a Set?

Set unique values ka unordered collection hota hai.

Syntax:

```python
numbers = {1, 2, 3, 4}
```

Important features:

- Set duplicate values store nahi karta.
- Set unordered hota hai.
- Set index support nahi karta.

## Example

```python
numbers = {1, 2, 2, 3, 3, 4}

print(numbers)
```

## Output

```text
{1, 2, 3, 4}
```

## Explanation

Duplicate `2` and `3` automatically remove ho gaye. Set sirf unique values rakhta hai.

## Real-World Use Case

Set ka use tab hota hai jab duplicate data remove karna ho ya unique values manage karni ho.

Examples:

| Situation | Why Set |
|---|---|
| Unique visitors | Same user ko baar-baar count nahi karna |
| Unique skills | Resume mein duplicate skills remove karna |
| Unique email IDs | Mailing list clean karna |
| Common students | Two batches ke common students find karna |
| Tags system | Duplicate tags avoid karna |

Example:

```python
emails = ["a@gmail.com", "b@gmail.com", "a@gmail.com"]

unique_emails = set(emails)

print(unique_emails)
```

Output:

```text
{'a@gmail.com', 'b@gmail.com'}
```

Explanation:

Email campaign mein same email ko multiple times message bhejna wrong hai. Set duplicate emails remove kar deta hai.

---

## Chapter 16 - Add and Remove Set Items

```python
skills = {"python", "linux"}

skills.add("git")
print(skills)

skills.remove("linux")
print(skills)
```

## Output

```text
{'python', 'linux', 'git'}
{'python', 'git'}
```

Note:

Output order different ho sakta hai because set unordered hota hai.

## Safe Remove with `discard()`

```python
skills = {"python", "linux"}

skills.discard("docker")

print(skills)
```

## Output

```text
{'python', 'linux'}
```

Explanation:

| Method | Behavior |
|---|---|
| `remove()` | Item missing ho to error |
| `discard()` | Item missing ho to error nahi |

---

## Chapter 17 - Set Operations

```python
a = {"python", "linux", "git"}
b = {"linux", "docker", "aws"}

print(a.union(b))
print(a.intersection(b))
print(a.difference(b))
```

## Output

```text
{'python', 'linux', 'git', 'docker', 'aws'}
{'linux'}
{'python', 'git'}
```

Output order change ho sakta hai.

## Explanation

| Operation | Meaning |
|---|---|
| `union()` | Dono sets ke all unique items |
| `intersection()` | Dono sets mein common items |
| `difference()` | Pehle set ke items jo second set mein nahi hain |

## Real Use Case - Remove Duplicates from List

```python
names = ["Rahul", "Aman", "Rahul", "Priya", "Aman"]

unique_names = set(names)

print(unique_names)
```

## Output

```text
{'Rahul', 'Aman', 'Priya'}
```

Explanation:

List mein duplicate names the. `set()` ne duplicate remove kar diye.

## Real-World Use Case

Set operations comparison ke liye bahut useful hain.

Example:

```python
python_students = {"Rahul", "Priya", "Aman"}
linux_students = {"Aman", "Neha", "Priya"}

all_students = python_students.union(linux_students)
common_students = python_students.intersection(linux_students)
only_python = python_students.difference(linux_students)

print("All:", all_students)
print("Common:", common_students)
print("Only Python:", only_python)
```

Output:

```text
All: {'Rahul', 'Priya', 'Aman', 'Neha'}
Common: {'Priya', 'Aman'}
Only Python: {'Rahul'}
```

Explanation:

Training institute mein Python and Linux batches ke students compare karne ke liye set operations useful hain:

- `union()` se all unique students milte hain.
- `intersection()` se dono batches mein common students milte hain.
- `difference()` se sirf Python wale students milte hain.

---

# Module 8 - Functions

Functions reusable code blocks hote hain. Agar ek kaam baar-baar karna ho, to function bana do.

---

## Chapter 18 - What is a Function?

Function ek named block of code hota hai jo specific task perform karta hai.

Simple example:

```python
def greet():
    print("Hello, welcome to Python!")

greet()
```

## Output

```text
Hello, welcome to Python!
```

## Syntax Explanation

| Code | Explanation |
|---|---|
| `def` | Function define karne ka keyword |
| `greet` | Function ka name |
| `()` | Parameters ke liye parentheses |
| `:` | Function block start |
| Indented code | Function body |
| `greet()` | Function call |

Important:

Function define karne se code run nahi hota. Function call karna zaroori hota hai.

## Real-World Use Case

Functions ka use repeated code avoid karne ke liye hota hai.

Examples:

| Situation | Function Idea |
|---|---|
| Login system | `check_password()` |
| Billing app | `calculate_total()` |
| Student result | `calculate_grade()` |
| Email app | `send_email()` |
| Banking app | `withdraw_money()` |

Simple explanation:

Agar same logic program mein multiple places par chahiye, usko function bana do. Isse code clean, reusable, and easy to maintain hota hai.

Example:

```python
def calculate_gst(price):
    gst = price * 0.18
    return gst

print(calculate_gst(1000))
print(calculate_gst(2500))
```

Output:

```text
180.0
450.0
```

Explanation:

Billing software mein GST calculation baar-baar hoti hai. Function se calculation ek jagah define ho gaya, phir jitni baar chaho use kar sakte ho.

---

## Chapter 19 - Function with Arguments

Argument means function ko input dena.

```python
def greet(name):
    print(f"Hello {name}, welcome to Python!")

greet("Rahul")
greet("Priya")
```

## Output

```text
Hello Rahul, welcome to Python!
Hello Priya, welcome to Python!
```

## Detailed Explanation

| Line | Code | Explanation |
|---|---|---|
| 1 | `def greet(name):` | Function define kiya with one parameter `name`. |
| 2 | `print(...)` | `name` value ko message mein use kiya. |
| 4 | `greet("Rahul")` | `"Rahul"` argument function ko diya. |
| 5 | `greet("Priya")` | `"Priya"` argument diya. |

Parameter vs Argument:

| Term | Meaning |
|---|---|
| Parameter | Function definition mein variable name |
| Argument | Function call ke time actual value |

In `def greet(name)`, `name` parameter hai.
In `greet("Rahul")`, `"Rahul"` argument hai.

## Real-World Use Case

Arguments tab use hote hain jab same function ko different values ke saath run karna ho.

Example:

```python
def calculate_discount(price, discount_percent):
    discount = price * discount_percent / 100
    final_price = price - discount
    return final_price

print(calculate_discount(1000, 10))
print(calculate_discount(2000, 15))
```

Output:

```text
900.0
1700.0
```

Explanation:

Shopping app mein different products par different discount apply hota hai. Same function alag price and discount ke saath reuse ho sakta hai.

---

## Chapter 20 - Function with Return Value

`return` function se result wapas bhejta hai.

```python
def add(a, b):
    total = a + b
    return total

result = add(10, 20)
print(result)
```

## Output

```text
30
```

## Detailed Explanation

| Line | Code | Explanation |
|---|---|---|
| 1 | `def add(a, b):` | Function two inputs leta hai. |
| 2 | `total = a + b` | Dono numbers add karta hai. |
| 3 | `return total` | Result function ke bahar bhejta hai. |
| 5 | `result = add(10, 20)` | Function call result variable mein store hota hai. |
| 6 | `print(result)` | Result print hota hai. |

Important:

`print()` sirf screen par show karta hai. `return` value ko function ke bahar use karne ke liye deta hai.

## Real-World Use Case

`return` tab important hota hai jab function ka result aage calculation mein use karna ho.

Example:

```python
def get_total(price, quantity):
    return price * quantity

total = get_total(500, 3)
delivery_charge = 50
final_bill = total + delivery_charge

print("Final bill:", final_bill)
```

Output:

```text
Final bill: 1550
```

Explanation:

`get_total()` sirf total calculate karke return karta hai. Us result ko baad mein delivery charge ke saath add kiya gaya. Real billing systems mein return values bahut important hoti hain.

---

## Chapter 21 - Multiple Return Values

```python
def calculate(a, b):
    add = a + b
    subtract = a - b
    multiply = a * b
    return add, subtract, multiply

x, y, z = calculate(10, 5)

print("Add:", x)
print("Subtract:", y)
print("Multiply:", z)
```

## Output

```text
Add: 15
Subtract: 5
Multiply: 50
```

## Explanation

Python function multiple values return kar sakta hai. Actually Python tuple return karta hai, then hum values unpack kar sakte hain.

---

## Chapter 22 - Default Arguments

Default argument ka matlab agar user value na de, to default value use ho.

```python
def greet(name="Guest"):
    print(f"Hello {name}")

greet()
greet("Rahul")
```

## Output

```text
Hello Guest
Hello Rahul
```

## Explanation

| Code | Meaning |
|---|---|
| `name="Guest"` | Default value Guest set ki |
| `greet()` | No argument, so Guest use hua |
| `greet("Rahul")` | Argument diya, so Rahul use hua |

## Real-World Use Case

Default arguments tab useful hote hain jab mostly same value use hoti hai, but kabhi-kabhi custom value chahiye hoti hai.

Example:

```python
def create_user(username, role="student"):
    print(f"User: {username}, Role: {role}")

create_user("rahul")
create_user("admin_user", "admin")
```

Output:

```text
User: rahul, Role: student
User: admin_user, Role: admin
```

Explanation:

Training portal mein most users students hote hain. Isliye default role `student` rakha. Agar admin banana ho, custom role pass kar sakte hain.

---

## Chapter 23 - Keyword Arguments

Keyword arguments mein value ko parameter name ke saath pass karte hain.

```python
def student_info(name, age, course):
    print(f"Name: {name}")
    print(f"Age: {age}")
    print(f"Course: {course}")

student_info(course="Python", name="Rahul", age=20)
```

## Output

```text
Name: Rahul
Age: 20
Course: Python
```

## Explanation

Keyword arguments ka advantage hai order matter nahi karta, because Python parameter name ke basis par value assign karta hai.

## Real-World Use Case

Keyword arguments code ko readable banate hain, especially jab function mein multiple values ho.

Example:

```python
def book_ticket(name, source, destination, seat_type):
    print(f"{name} booked {seat_type} ticket from {source} to {destination}.")

book_ticket(
    destination="Mumbai",
    source="Delhi",
    seat_type="AC",
    name="Rahul"
)
```

Output:

```text
Rahul booked AC ticket from Delhi to Mumbai.
```

Explanation:

Ticket booking function mein multiple values hain. Keyword arguments se code easy to read hota hai and order mistake ka chance kam hota hai.

---

## Chapter 24 - Positional vs Keyword Arguments

```python
def introduce(name, city):
    print(f"My name is {name} and I live in {city}.")

introduce("Rahul", "Delhi")
introduce(city="Mumbai", name="Priya")
```

## Output

```text
My name is Rahul and I live in Delhi.
My name is Priya and I live in Mumbai.
```

Explanation:

| Call | Type |
|---|---|
| `introduce("Rahul", "Delhi")` | Positional arguments |
| `introduce(city="Mumbai", name="Priya")` | Keyword arguments |

---

## Chapter 25 - Lambda Functions

Lambda function small one-line anonymous function hota hai. Anonymous means function ka normal name nahi hota.

Syntax:

```python
lambda arguments: expression
```

## Example

```python
square = lambda x: x * x

print(square(5))
```

## Output

```text
25
```

## Explanation

| Code | Meaning |
|---|---|
| `lambda x: x * x` | Input `x` lo and `x * x` return karo |
| `square = ...` | Lambda function ko variable mein store kiya |
| `square(5)` | 5 ka square return karta hai |

Normal function version:

```python
def square(x):
    return x * x
```

Both do same work.

## Real-World Use Case

Lambda functions short temporary logic ke liye useful hote hain. Jab function ka kaam chhota ho and only one expression ho, lambda clean option ho sakta hai.

Examples:

| Situation | Lambda Use |
|---|---|
| Sort products by price | `key=lambda product: product["price"]` |
| Filter adult users | `lambda age: age >= 18` |
| Square numbers | `lambda x: x * x` |
| Convert names to uppercase | `lambda name: name.upper()` |

Example:

```python
products = [
    {"name": "Keyboard", "price": 1200},
    {"name": "Mouse", "price": 500},
    {"name": "Monitor", "price": 9000}
]

products.sort(key=lambda product: product["price"])

print(products)
```

Output:

```text
[{'name': 'Mouse', 'price': 500}, {'name': 'Keyboard', 'price': 1200}, {'name': 'Monitor', 'price': 9000}]
```

Explanation:

E-commerce app mein products ko price ke basis par sort karna common feature hai. `lambda product: product["price"]` Python ko batata hai ki sorting price value ke basis par karni hai.

---

## Lambda with `map()`

```python
numbers = [1, 2, 3, 4]

squares = list(map(lambda x: x * x, numbers))

print(squares)
```

## Output

```text
[1, 4, 9, 16]
```

## Explanation

| Code | Explanation |
|---|---|
| `numbers` | Original list |
| `lambda x: x * x` | Har number ka square calculate karta hai |
| `map(...)` | Function ko list ke har item par apply karta hai |
| `list(...)` | Result ko list mein convert karta hai |

---

## Lambda with `filter()`

```python
numbers = [1, 2, 3, 4, 5, 6]

even_numbers = list(filter(lambda x: x % 2 == 0, numbers))

print(even_numbers)
```

## Output

```text
[2, 4, 6]
```

## Explanation

`filter()` only un values ko keep karta hai jinke liye condition True hoti hai.

Condition:

```python
x % 2 == 0
```

Means number even hai.

---

# Practice Questions

Try these questions after completing the notes.

## Question 1 - Create a Fruit List

Create a list of 5 fruits. Print the first fruit, last fruit, and total number of fruits.

Concepts used: list, indexing, negative indexing, `len()`.

## Question 2 - Marks Analyzer

Create a list of marks. Print total marks, highest marks, lowest marks, and average marks.

Hint:

```python
sum(marks)
max(marks)
min(marks)
```

Concepts used: list, built-in functions, arithmetic.

## Question 3 - Remove Duplicate Names

Create a list with duplicate names. Convert it into a set and print unique names.

Concepts used: list, set, uniqueness.

## Question 4 - Student Dictionary

Create a dictionary with keys: `name`, `age`, `course`, and `marks`. Print each value separately.

Concepts used: dictionary, key-value access.

## Question 5 - Update Student Marks

Create a student dictionary and update the marks value. Then print the updated dictionary.

Concepts used: dictionary update.

## Question 6 - Nested List Matrix

Create a 3x3 nested list and print all values row by row.

Concepts used: nested list, nested loop.

## Question 7 - Function for Addition

Create a function `add_numbers(a, b)` that returns the sum of two numbers.

Concepts used: function, arguments, return.

## Question 8 - Function with Default Argument

Create a function `welcome(name="Student")` that prints a welcome message.

Concepts used: default argument.

## Question 9 - Keyword Argument Practice

Create a function `profile(name, city, course)` and call it using keyword arguments in different order.

Concepts used: keyword arguments.

## Question 10 - Lambda Practice

Create a lambda function to find cube of a number.

Example:

```python
cube = lambda x: x * x * x
```

Concepts used: lambda function.

---

# Quick Reference Cheatsheet

## Lists

| Task | Code |
|---|---|
| Create list | `items = [1, 2, 3]` |
| Access item | `items[0]` |
| Last item | `items[-1]` |
| Add item | `items.append(4)` |
| Insert item | `items.insert(1, 10)` |
| Extend list | `items.extend([5, 6])` |
| Remove by value | `items.remove(2)` |
| Remove by index | `items.pop(0)` |
| Length | `len(items)` |
| Sort | `items.sort()` |

## Tuples

| Task | Code |
|---|---|
| Create tuple | `t = (1, 2, 3)` |
| Access item | `t[0]` |
| Single tuple | `t = (1,)` |
| Count item | `t.count(1)` |
| Find index | `t.index(2)` |

## Dictionaries

| Task | Code |
|---|---|
| Create dictionary | `d = {"name": "Rahul"}` |
| Access value | `d["name"]` |
| Safe access | `d.get("city", "NA")` |
| Add/update | `d["age"] = 20` |
| Delete | `d.pop("age")` |
| Keys | `d.keys()` |
| Values | `d.values()` |
| Items | `d.items()` |

## Sets

| Task | Code |
|---|---|
| Create set | `s = {1, 2, 3}` |
| Add item | `s.add(4)` |
| Remove item | `s.remove(2)` |
| Safe remove | `s.discard(5)` |
| Union | `a.union(b)` |
| Intersection | `a.intersection(b)` |
| Difference | `a.difference(b)` |

## Functions

| Task | Code |
|---|---|
| Define function | `def hello():` |
| Call function | `hello()` |
| Argument | `def greet(name):` |
| Return | `return value` |
| Default argument | `def greet(name="Guest"):` |
| Keyword argument | `greet(name="Rahul")` |
| Lambda | `lambda x: x * x` |

---

# Final Summary

## Module 6 Key Takeaways

- List multiple values store karta hai.
- List mutable hoti hai, so items add/update/delete kar sakte hain.
- Indexing 0 se start hoti hai.
- Negative indexing end se start hoti hai.
- Slicing list ka part return karta hai.
- Nested list means list ke andar list.
- Tuple list jaisa hota hai, but immutable hota hai.
- Tuple fixed data ke liye useful hota hai.
- To-Do List Manager project lists and dictionaries ka practical use dikhata hai.

## Module 7 Key Takeaways

- Dictionary key-value pairs store karta hai.
- Key ke through value access kar sakte hain.
- `get()` safe access ke liye useful hai.
- Dictionary mutable hoti hai.
- Nested dictionary real-world structured data ke liye useful hai.
- Set unique values store karta hai.
- Set duplicates automatically remove karta hai.
- Set operations like union, intersection, difference data comparison mein useful hain.

## Module 8 Key Takeaways

- Function reusable code block hota hai.
- Function define karne ke liye `def` use hota hai.
- Function call karne par hi code run hota hai.
- Arguments function ko input dete hain.
- `return` function se output deta hai.
- Default arguments optional values ke liye useful hain.
- Keyword arguments readable function calls ke liye useful hain.
- Lambda one-line small function hota hai.

## Best Practice

Har concept ko khud type karke run karo. Sirf copy-paste mat karo. Values change karo, output observe karo, and errors ko samjho. Programming practice se strong hoti hai.

Happy Coding.
