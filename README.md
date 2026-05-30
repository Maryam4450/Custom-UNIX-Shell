


# 🐚 Custom UNIX Shell (myshell)

A fully functional UNIX-like command-line shell built in C as part of an Operating Systems programming assignment.  
This project demonstrates deep understanding of process management, system calls, file descriptors, parsing, and shell internals.

---

## 🚀 Features

### 🔹 Core Shell Functionality
- Executes external system commands using `fork()`, `exec()`, and `wait()`
- Command-line parsing and tokenization
- Interactive prompt-based interface

---

### 🔹 Built-in Commands
- `cd <directory>` → Change directory using `chdir()`
- `exit` → Exit the shell safely
- `help` → Show available built-in commands
- `jobs` → Display background processes

---

### 🔹 Command History
- Stores last 20+ commands
- `history` command to display previous commands
- `!n` feature to re-execute a specific command

---

### 🔹 GNU Readline Integration
- Arrow key navigation (up/down history)
- Tab auto-completion support
- Improved interactive command-line editing

---

### 🔹 I/O Redirection
- Output redirection: `>`
- Input redirection: `<`

```bash
ls -l > output.txt
sort < input.txt
````

---

### 🔹 Pipes

* Supports pipeline execution using `|`

```bash
cat file.txt | grep "error"
```

---

### 🔹 Command Chaining

* Sequential execution using `;`

```bash
echo Hello ; ls ; pwd
```

---

### 🔹 Background Execution & Job Control

* Run processes in background using `&`

```bash
sleep 10 &
```

* Tracks background jobs
* Prevents zombie processes using `waitpid(..., WNOHANG)`

---

### 🔹 Conditional Execution

* Supports `if-then-else-fi` scripting structure

```bash
if grep "user" /etc/passwd > /dev/null
then
  echo "User exists"
else
  echo "User not found"
fi
```

---

### 🔹 Shell Variables

* Variable assignment:

```bash
NAME=Vesper
```

* Variable expansion:

```bash
echo $NAME
```

* `set` command to list all variables

---

## 🧠 Concepts Used

* Process lifecycle (`fork`, `exec`, `wait`)
* File descriptors (`dup2`, `open`, `close`)
* Pipes and inter-process communication
* Signal and zombie process handling
* Parsing and lexical analysis
* Data structures (arrays / linked lists)
* Memory management in C
* Git workflow (branches, tags, releases)

---

## 📁 Project Structure

```
Custom-UNIX-Shell/
├── src/
│   ├── main.c
│   ├── shell.c
│   ├── execute.c
│   └── parser.c
├── include/
│   └── shell.h
├── Makefile
└── README.md
```

---

## ⚙️ Build Instructions

### Compile the project

```bash
make
```

### Run the shell

```bash
./bin/myshell
```

---

## 🧪 Example Usage

```bash
myshell> ls -l
myshell> cd Documents
myshell> echo "Hello World"
myshell> cat file.txt | grep "data"
myshell> sleep 5 &
myshell> history
myshell> !3
```

---

## 📌 Learning Outcomes

* Understanding how UNIX shells work internally
* Hands-on experience with system programming in C
* Practical implementation of OS concepts
* Building a mini scripting language
* Strengthened debugging and memory handling skills

---

## 🏷️ Versioning (Git Tags)

* `v1.0-base` → Base shell
* `v2` → Built-in commands
* `v3` → Command history
* `v4` → Readline integration
* `v5` → I/O redirection & pipes
* `v6` → Multitasking & background jobs
* `v7` → if-then-else-fi
* `v8` → Shell variables

---






