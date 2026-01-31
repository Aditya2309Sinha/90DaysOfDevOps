# Linux Commands Cheat Sheet 🐧

A practical, quick-scan Linux command reference focused on **process management**,  
**file system operations**, and **network troubleshooting**.

This is a toolkit you’ll reuse for years.

---

## 🗂️ File System Commands

| Command | Usage |
|------|------|
| `pwd` | Show current working directory |
| `ls` | List files and directories |
| `ls -la` | List all files with permissions |
| `cd <dir>` | Change directory |
| `mkdir <dir>` | Create a directory |
| `rmdir <dir>` | Remove empty directory |
| `touch <file>` | Create an empty file |
| `cp src dest` | Copy files or directories |
| `mv src dest` | Move or rename files |
| `rm <file>` | Delete a file |
| `rm -r <dir>` | Delete directory recursively |
| `find /path -name file` | Search files by name |
| `df -h` | Show disk space usage |
| `du -sh <dir>` | Show directory size |
| `mount` | Show mounted file systems |

---

## ⚙️ Process Management Commands

| Command | Usage |
|------|------|
| `ps` | Show running processes |
| `ps aux` | Detailed process list |
| `top` | Real-time process monitoring |
| `htop` | Enhanced interactive process viewer |
| `pidof <process>` | Get PID of a process |
| `kill <pid>` | Terminate a process |
| `kill -9 <pid>` | Force kill a process |
| `bg` | Resume process in background |
| `fg` | Resume process in foreground |
| `jobs` | List background jobs |
| `uptime` | Show system running time |
| `free -h` | Display memory usage |
| `watch <cmd>` | Run command repeatedly |

---

## 🌐 Networking & Troubleshooting Commands

| Command | Usage |
|------|------|
| `ping <host>` | Check network connectivity |
| `ip addr` | Show IP addresses |
| `ip route` | Display routing table |
| `ss -tuln` | Show listening ports |
| `netstat -tuln` | List open ports (legacy) |
| `curl <url>` | Test HTTP endpoints |
| `wget <url>` | Download files |
| `dig <domain>` | DNS lookup |
| `traceroute <host>` | Trace network path |

---

## 📦 System & Utility Commands

| Command | Usage |
|------|------|
| `uname -a` | Show system information |
| `whoami` | Show current user |
| `id` | Show user/group IDs |
| `history` | Show command history |
| `clear` | Clear terminal |
| `exit` | Close terminal session |

---

## 🔑 Key Troubleshooting Flow

1. **Check connectivity** → `ping`, `ip addr`
2. **Check service/process** → `ps`, `top`, `systemctl`
3. **Check disk/memory** → `df -h`, `free -h`
4. **Check ports** → `ss -tuln`, `netstat`

---

## 📌 Tip

> Linux mastery isn’t about memorizing commands.  
> It’s about knowing **which command to reach for under pressure**.

---

Happy hacking 🧠🐧  
Feel free to fork, star ⭐, or customize.
