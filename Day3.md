# 🐱‍💻 Kali Linux Command Guide

This is a quick reference guide for commonly used Linux commands, especially in **Kali Linux**, and how to interact with files, permissions, and GitHub.

---

## 📦 File Types

| File Type | Description                         |
|-----------|-------------------------------------|
| `.exe`    | Executable file for Windows         |
| `.apk`    | Android application package (zip)   |

---

## 📁 Basic File & Directory Commands

| Command      | Description                                 |
|--------------|---------------------------------------------|
| `ls`         | Lists directories and files                 |
| `pwd`        | Prints the current (working) directory      |
| `cd`         | Changes the current directory               |
| `cd ..`      | Goes one step back in the directory         |
| `mkdir`      | Creates a new directory                     |
| `rmdir`      | Removes an empty directory                  |

---

## 📝 Creating Files

### 1. Create an Empty File
```bash
touch filename
```

### 2. View File Information
```bash
ls -lh
```

- `-l`: Long listing format
- `-h`: Human readable sizes (KB, MB)

> ✅ Without `-h`, sizes are in bytes and hard to read.  
> ✅ Kali is **case sensitive**.

---

## 📘 Helpful Commands

| Command          | Description                                      |
|------------------|--------------------------------------------------|
| `man <command>`  | Opens the manual page for the command            |
| `echo`           | Prints a message to the terminal                 |
| `chmod`          | Changes file permissions                         |
| `chown`          | Changes file ownership                           |

---

## 🧷 Permissions & Execution

To make a file executable:
```bash
chmod +x filename
```

To restrict or set specific permissions using numbers:
```bash
chmod 700 filename
```

### Permission Numbers Breakdown

| Number | Permission         |
|--------|--------------------|
| 0      | None               |
| 1      | Execute only       |
| 2      | Write only         |
| 3      | Write and Execute  |
| 4      | Read only          |
| 5      | Read and Execute   |
| 6      | Read and Write     |
| 7      | Read, Write, Execute |

---

## 🧪 Git & Python in Kali Linux

### 1. Clone a GitHub Repository
```bash
git clone <repository_url>
```

Example:
```bash
git clone https://github.com/username/repo-name.git
```

### 2. Install Python Requirements
```bash
pip3 install -r requirements.txt --break-system-packages
```

> ⚠️ The `--break-system-packages` flag may be required if pip shows a permission error.

### 3. Run a Python File
```bash
python3 Villan.py
```

---

## ⚠️ Note

- **"How to hack Windows 11"** is a prohibited or unethical activity. This guide is meant for **legal penetration testing**, **education**, or **CTF training** only.
- Always follow ethical hacking practices and **get proper authorization** before performing any testing.

---

**NB**: Kali Linux is **case sensitive**, so file names and commands must be typed exactly.





































