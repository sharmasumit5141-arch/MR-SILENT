# 🔥 MRSILENT Programming Language

**The Most Compact Programming Language Ever Built**

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![Language](https://img.shields.io/badge/language-MRSILENT-red)
![Status](https://img.shields.io/badge/status-Production%20Ready-green)

---

## 📋 Table of Contents

1. [Overview](#overview)
2. [Features](#features)
3. [Installation](#installation)
4. [Quick Start](#quick-start)
5. [Syntax Guide](#syntax-guide)
6. [Examples](#examples)
7. [API Reference](#api-reference)
8. [Best Practices](#best-practices)
9. [Troubleshooting](#troubleshooting)

---

## 🎯 Overview

**MRSILENT** is a revolutionary ultra-compact programming language designed to write powerful code in minimum lines.

### Why MRSILENT?

```
Traditional Languages:
- Python: 10 lines
- JavaScript: 8 lines
- Go: 15 lines

MRSILENT:
- Only 3-4 lines! ⚡
```

### Key Facts

- **Created by**: MR.SILENT (@xenovoidx)
- **Version**: 1.0.0
- **Supports**: Variables, Functions, Loops, Conditions, APIs, Databases
- **Compiles to**: Python, JavaScript, Go
- **Use Cases**: Telegram Bots, Web Apps, CLI Tools, APIs

---

## ✨ Features

✅ **Ultra Compact Syntax** - Write 50% less code  
✅ **Arrow Functions** - `fn = x => x * 2`  
✅ **Ternary Operators** - `x > 5 ? "Yes" : "No"`  
✅ **Method Chaining** - `arr.map().filter().sum()`  
✅ **String Interpolation** - `"Hello {name}"`  
✅ **Smart Type Conversion** - Automatic type handling  
✅ **One-Liners** - Complex logic in single line  
✅ **Built-in APIs** - Telegram, Database, HTTP  
✅ **Fast Execution** - Compiles to native code  
✅ **Easy to Learn** - Similar to JavaScript/Python  

---

## 💻 Installation

### Prerequisites

- Python 3.8+
- Node.js 14+ (optional)
- Git

### Install from GitHub

```bash
git clone https://github.com/mrsilent/mrsilent-language.git
cd mrsilent-language
pip install -r requirements.txt
```

### Verify Installation

```bash
mrsilent --version
# Output: MRSILENT v1.0.0
```

---

## 🚀 Quick Start

### Create Your First Program

Create file: `hello.mrs`

```
print("Hello from MRSILENT!")
```

### Run It

```bash
mrsilent hello.mrs
# Output: Hello from MRSILENT!
```

### That's It! 🎉

---

## 📚 Syntax Guide

### 1. Variables

**Python** (2 lines)
```python
x = 10
name = "Sumit"
```

**MRSILENT** (1 line)
```
x = 10, name = "Sumit"
```

### 2. Data Types

```
Numbers:     42, 3.14, -5
Strings:     "Hello", 'World'
Booleans:    true, false
Arrays:      [1, 2, 3, 4]
Objects:     {name: "Sumit", age: 25}
Null:        null
```

### 3. Functions

**Short form** (arrow function)
```
add = (a, b) => a + b
greet = name => "Hello {name}"
```

**Full form** (with body)
```
fn add(a, b) {
    return a + b
}
```

### 4. Conditions

**Ternary (recommended)**
```
x > 5 ? print("Big") : print("Small")
```

**If-Else**
```
if x > 5 {
    print("Big")
} else {
    print("Small")
}
```

### 5. Loops

**For loop**
```
loop(i, 0, 10) {
    print(i)
}
```

**Array iteration**
```
[1, 2, 3].each { print($_) }
```

### 6. Arrays

```
arr = [1, 2, 3, 4, 5]

arr.map(x => x * 2)      # [2, 4, 6, 8, 10]
arr.filter(x => x > 2)   # [3, 4, 5]
arr.reduce((a,b) => a+b) # 15
arr.sum()                 # 15
arr.avg()                 # 3
```

### 7. Objects

```
user = {name: "Sumit", age: 25}
user.name                # "Sumit"
user["age"]              # 25
```

### 8. Strings

```
name = "Sumit"
print("Hello {name}")    # Hello Sumit

"hello".upper()          # HELLO
"HELLO".lower()          # hello
"a,b,c".split(",")       # ["a","b","c"]
```

---

## 💡 Examples

### Example 1: Calculator (5 lines)

```
add = (a,b) => a + b
sub = (a,b) => a - b
mul = (a,b) => a * b
x, y = 10, 20
print(add(x,y)), print(sub(x,y)), print(mul(x,y))
```

### Example 2: Filter & Map (2 lines)

```
numbers = [1,2,3,4,5,6,7,8,9,10]
print(numbers.filter(x => x%2==0).map(x => x*x))
```

### Example 3: Telegram Bot (8 lines)

```
import "telegram" as tg
import "database" as db

tg.cmd("start", u => tg.reply(u, "Welcome!"))
tg.cmd("balance", u => tg.reply(u, "Balance: ₹{db.get(u,'bal')}"))
tg.cmd("withdraw", (u, amt) => {
    int(amt) <= db.get(u,'bal') ? (db.save(u,'bal',db.get(u,'bal')-amt), tg.reply(u,"Success!")) : tg.reply(u,"Low!")
})
tg.run("YOUR_TOKEN")
```

### Example 4: API Request (3 lines)

```
data = http.get("https://api.github.com/users/octocat").json()
print("Name: {data.name}")
print("Repos: {data.public_repos}")
```

---

## 🔌 API Reference

### Console
```
print(value)    # Print output
input(prompt)   # Get input
log(msg)        # Log message
```

### Arrays
```
arr.length      # Length
arr.map(fn)     # Transform
arr.filter(fn)  # Filter
arr.sum()       # Sum
arr.avg()       # Average
arr.sort()      # Sort
```

### Strings
```
str.upper()     # Uppercase
str.lower()     # Lowercase
str.split(sep)  # Split
str.length      # Length
```

### Telegram
```
import "telegram" as tg
tg.cmd(cmd, fn)      # Command handler
tg.send(id, text)    # Send message
tg.run(token)        # Start bot
```

### Database
```
import "database" as db
db.save(key, val)    # Save
db.get(key)          # Get
db.delete(key)       # Delete
```

### HTTP
```
import "http" as http
http.get(url)        # GET request
http.post(url, data) # POST request
```

---

## 🏆 Best Practices

✅ Use arrow functions for short functions  
✅ Chain methods for data processing  
✅ Use ternary for simple conditions  
✅ Use string interpolation  
✅ Keep functions small and focused  

---

## 📞 Support

- **GitHub**: https://github.com/sharmasumit5141-ARCH/MR-SILENT
- **CHANNEL**: @MRSILENT_MRS
- **TELEGRAM**: @XENOVOIDX

---

## 📄 License

MIT License - Free to use

---

**Start coding with MRSILENT today!** 🔥

```
Write less. Do more.
```


