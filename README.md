# 🐧 Linux Systems Programming & Process Control

An academic project demonstrating advanced proficiency in Unix/Linux command-line utilities, Bash scripting, and Python-based multi-processing (Inter-Process Communication & Process Trees). 

Developed for the **"Software Development Tools & Systems Programming"** course at the Technical University of Crete (TUC).

**Authors:** 
* Georgios Argyris (AM: 2020030138)
* Stamatios Alexiou (AM: 2020030158)

---

## 🚀 Project Overview

This repository is divided into 5 distinct core topics, moving from basic terminal text processing to advanced OS-level process manipulation:

### 1. 🛠️ Advanced Linux Commands
Complex, single-line chained Linux commands used to parse, filter, and manipulate a text dataset (`tweetsmall.txt`). 
* **Concepts used:** Output redirection (`>`, `>>`), command chaining (`|`, `;`, `&&`).
* **Tools used:** `head`, `tail`, `grep`, `cut`, `paste`, `sort`, `wc`. *(Note: `awk` and `sed` were strictly restricted to encourage creative combinations of basic tools).*

### 2. 🐦 Bash Twitter Viewer & Editor
An interactive, CLI-based CRUD (Create, Read, Update, Delete) application written entirely in **Bash Script**.
* Loads data into arrays and memory.
* Provides a continuous navigation menu to read, edit, delete, and append tweets.
* Saves states persistently back to the disk.

### 3. 📊 Bash Sentiment Analyser
A script that parses the `tweetsmall.txt` file line-by-line and calculates the sentiment of each tweet.
* Compares words against loaded `positive.txt` and `negative.txt` dictionaries.
* Determines whether a tweet has a **Positive**, **Negative**, or **Neutral** sentiment.
* Outputs the processed results into a new `sentimentpertweet.txt` file.

### 4. ⚡ Python Zig-Zag Process Generator
A Python script (`zigzaggen.py`) that utilizes OS-level process creation to build a specific "zig-zag" process tree.
* Uses `os.fork()`, `os.wait()`, and `os._exit()`.
* The parent process creates a left and right child. Depending on whether the tree depth level is odd or even, only one specific child is allowed to continue forking, creating an alternating zig-zag hierarchy up to 10 levels deep.

### 5. 🔀 Python Three-Way IPC Pipe
Implementation of Inter-Process Communication (IPC) using Python's `os.pipe()`.
* Creates a parent process and two child processes using `os.fork()`.
* The parent process acts as the "Writer", pushing string messages into the pipe.
* The two child processes act as the "Readers", concurrently reading and printing the exact same messages passed by the parent.
* Features proper handling and closing of file descriptors.

---

## 💻 Tech Stack
* **OS Environment:** Unix / Linux
* **Scripting Languages:** Bash, Shell
* **Programming Languages:** Python 3 (specifically utilizing the `os` and `sys` modules)
* **Notebook Environment:** Jupyter Notebook / Google Colab
