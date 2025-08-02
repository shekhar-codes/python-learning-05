# Python Advanced Programming Tutorial - Complete Deep Theory Guide 🐍

Aaj hum seekhenge Python ke sabse important advanced topics ka **complete deep theory** with **practical examples**! Maine ye tutorial bilkul detail mein banaya hai taaki even a beginner bhi easily samajh sake. Chaliye start karte hain! 💪

## Block 4: Functions (Code Reusability) - Deep Theory & Practice

### Functions ka Deep Theory - Kya hai aur Kyun Important hai? 🤔

**Function** matlab ek code ka block jo **specific task** perform karta hai. Think of it like this - jaise aapke ghar mein different rooms hain (kitchen, bedroom, bathroom), waise hi programming mein different functions hain jo different kaam karte hain.

**Why Functions? Kyun zaroori hain?**
- **Code Reusability**: Ek baar likho, baar baar use karo
- **Modularity**: Big problem ko small pieces mein divide karo
- **Maintainability**: Code maintain karna easy ho jata hai
- **Readability**: Code padhna aur samajhna easy hota hai

### Defining Functions - def Keyword 📝

Python mein function banane ke liye **`def`** keyword use karte hain. Ye keyword Python ko batata hai ki "yahan se function start ho raha hai".

**Basic Syntax:**
```python
def function_name(parameters):
    """Optional docstring"""
    # Function body
    return value  # Optional
```

**Example - Simple Function:**
```python
def greet():
    print("Hello World!")

# Function call
greet()  # Output: Hello World!
```

**Real-life analogy**: Imagine karo aap coffee machine bana rahe ho. Machine ka naam hai `make_coffee()`, aur jab aap ise call karte ho, to coffee ban jati hai!

### Parameters and Return Values - Deep Dive 🔄

#### Parameters vs Arguments - Confusion Clear Karte Hain!

**Parameter**: Function define karte time jo variables likhte hain  
**Argument**: Function call karte time jo actual values pass karte hain

```python
def add_numbers(x, y):  # x, y are PARAMETERS
    return x + y

result = add_numbers(5, 3)  # 5, 3 are ARGUMENTS
```

#### Return Values - Function se Data wapas kaise laayein?

`return` statement function ka output deta hai. Think of it like ATM machine - aap card daalte ho (input), machine process karti hai, aur paise deti hai (return value).

```python
def calculate_area(length, width):
    area = length * width
    return area  # This value goes back to caller

result = calculate_area(10, 5)  # result = 50
print(result)  # 50
```

**Multiple Return Values:**
```python
def get_name_age():
    name = "Rahul"
    age = 25
    return name, age  # Returns tuple

name, age = get_name_age()  # Unpacking
print(f"{name} is {age} years old")
```

### Default Arguments - Smart Programming 🧠

Default arguments se aap parameters ko default values de sakte ho. Agar caller koi value nahin deta, to default value use hoti hai.

```python
def greet_user(name="Guest", message="Hello"):
    return f"{message}, {name}!"

print(greet_user())                    # Hello, Guest!
print(greet_user("Priya"))            # Hello, Priya!
print(greet_user("Amit", "Namaste"))  # Namaste, Amit!
```

**⚠️ Important Rule**: Default arguments hamesha non-default arguments ke baad aate hain!

```python
# ❌ Wrong way
def wrong_func(name="John", age):  # Error!
    pass

# ✅ Correct way
def correct_func(age, name="John"):
    pass
```

### *args and **kwargs - Variable Arguments ka Magic ✨

Ye sabse powerful feature hai functions mein! Jab aapko nahin pata kitne arguments aayenge.

#### *args - Variable Positional Arguments

```python
def sum_all(*args):
    """Sum any number of arguments"""
    return sum(args)

print(sum_all(1, 2, 3))        # 6
print(sum_all(1, 2, 3, 4, 5))  # 15
print(sum_all(10))             # 10
```

**Real Example - Pizza Order:**
```python
def order_pizza(*toppings):
    print("Pizza ordered with:")
    for topping in toppings:
        print(f"- {topping}")

order_pizza("cheese", "tomato")
order_pizza("cheese", "tomato", "mushroom", "olives")
```

#### **kwargs - Variable Keyword Arguments

```python
def create_profile(**kwargs):
    """Create user profile with any number of details"""
    print("User Profile:")
    for key, value in kwargs.items():
        print(f"{key}: {value}")

create_profile(name="Rahul", age=25, city="Delhi")
create_profile(name="Priya", age=22, city="Mumbai", profession="Engineer")
```

#### Combination - *args aur **kwargs Together

```python
def flexible_function(required_arg, *args, **kwargs):
    print(f"Required: {required_arg}")
    print(f"Additional args: {args}")
    print(f"Keyword args: {kwargs}")

flexible_function("Must have", 1, 2, 3, name="John", age=30)
```

### Lambda Functions - One-Line Functions 🚀

Lambda functions chhote, anonymous functions hote hain. Perfect hain quick operations ke liye.

**Syntax:**
```python
lambda arguments: expression
```

**Basic Examples:**
```python
# Regular function
def square(x):
    return x * x

# Lambda equivalent
square = lambda x: x * x

print(square(5))  # 25
```

**Real-world Usage - with map(), filter():**
```python
numbers = [1, 2, 3, 4, 5]

# Square all numbers
squared = list(map(lambda x: x**2, numbers))
print(squared)  # [1, 4, 9, 16, 25]

# Filter even numbers
evens = list(filter(lambda x: x % 2 == 0, numbers))
print(evens)  # [2, 4]
```

**Lambda with Multiple Arguments:**
```python
# Addition lambda
add = lambda x, y: x + y
print(add(10, 20))  # 30

# Lambda with conditional
max_val = lambda a, b: a if a > b else b
print(max_val(10, 20))  # 20
```

### Recursion - Function Calling Itself 🔄

Recursion tab hota hai jab function khud ko call karta hai. It's like **Russian dolls** - ek ke andar doosra, doosre ke andar teesra!

**Key Components of Recursion:**
1. **Base Case**: Kab rukna hai  
2. **Recursive Case**: Function khud ko kaise call kare

#### Classic Example - Factorial

```python
def factorial(n):
    # Base case
    if n <= 1:
        return 1
    # Recursive case
    return n * factorial(n - 1)

print(factorial(5))  # 120
```

#### Fibonacci Sequence - Advanced Recursion

```python
def fibonacci(n):
    if n <= 1:
        return n
    return fibonacci(n-1) + fibonacci(n-2)

for i in range(10):
    print(fibonacci(i), end=" ")
```

*... (Full tutorial continues covering OOP, File Handling, Modules, Error Handling, Intermediate Topics, Summary)*

---

*याद रखें: Programming सीखना ek journey hai, destination nahin. Hamesha practice karte rahen aur nai cheezein explore karte rahen!*
