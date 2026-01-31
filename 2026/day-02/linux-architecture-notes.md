# Linux Basics – Short Notes 🐧

Concise notes covering fundamental Linux concepts, commands, and boot process.  
Useful for beginners, interviews, and quick revision.

---

## 1. Core Linux Philosophy

- **Everything in Linux is a file**
  - Files, directories, devices, sockets, and pipes.
- **Everything starts with a process**
  - Each running program is a process with a unique **PID**.

---

## 2. Linux File System Hierarchy

- **`/` (root)**
  - Top-level directory of the Linux file system.
- **`/bin`**
  - Essential binary executables (basic shell commands).
- **`/mnt`**
  - Temporary mount point for external file systems.
- **Current Directory**
  - Displayed using `pwd`.
- **Directory Navigation**
  - `cd` → Change directory.

---

## 3. Shell Basics

- **Shell**
  - Acts as an interface between the user and the OS.
  - Interprets and executes commands.
- **Built-in Commands**
  - Some commands (e.g., `cd`) are built into the shell itself.

---

## 4. Common Linux Commands

### File & Directory Creation
mkdir folder_name     # Create a directory
touch file.txt        # Create an empty file
cp source dest        # Copy file or directory
mv source dest        # Move or rename
rm file_name          # Remove file

### Networking
ping google.com       # Check network connectivity
ip addr               # Show IP address details
