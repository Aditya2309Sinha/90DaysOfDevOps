
<img width="1656" height="934" alt="image" src="https://github.com/user-attachments/assets/0710145e-fc55-41cc-a395-f4db02998417" />

<img width="1204" height="597" alt="image" src="https://github.com/user-attachments/assets/58c87d89-871c-414e-9074-dc070cb211fe" />

# Linux Troubleshooting Mini Runbook 🐧

**Target service / process:** `ssh` (`sshd`)  
**Environment:** Ubuntu 24.04.1 LTS on WSL2  
**Objective:** Capture a quick, repeatable troubleshooting snapshot and next actions.

---

## 1. Environment Basics

### uname
uname -a
Observed

Linux ADITYA 6.6.87.2-microsoft-standard-WSL2 x86_64 GNU/Linux
Note: Running Linux kernel under WSL2.

OS Release
lsb_release -a
Observed

Distributor ID: Ubuntu
Description: Ubuntu 24.04.1 LTS
Release: 24.04
Codename: noble
Note: Stable LTS release suitable for production-style practice.

2. Filesystem Sanity
Create test directory and file
mkdir /tmp/runbook-demo
cp /etc/hosts /tmp/runbook-demo/hosts-copy
ls -l /tmp/runbook-demo
Observed

-rw-r--r-- 1 root root hosts-copy
Note: Filesystem is writable and functioning normally.
Initial typo in directory name caused a “No such file” error, corrected successfully.

Disk usage
df -h
Observed

/dev/sdd  1007G  1.6G  955G  1% /
Note: Disk space is healthy, no pressure.

3. CPU & Memory Snapshot
Memory
free -h
Observed

Mem: 7.7Gi total, ~466Mi used
Swap: 2.0Gi total, 0 used
Note: No memory pressure, swap unused.

SSH process
ps -o pid,pcpu,pmem,comm -C sshd
Observed

PID   %CPU %MEM COMMAND
315   0.0  0.0  sshd
Note: SSH daemon running and idle.

4. Disk & IO
Log directory size
du -sh /var/log
Observed

Permission denied: /var/log/private
Re-run with privileges:

sudo du -sh /var/log
148M /var/log
Note: Log size is reasonable.

IO / CPU activity
vmstat 1 3
Observed

No swap usage, CPU mostly idle
Note: No IO wait or CPU contention.

5. Quick Findings
System resources (CPU, memory, disk) are healthy

sshd process is running and stable

Observed issues were user-level (typos, permissions), not system faults

No signs of service degradation

6. If This Worsens (Next Steps)
Service Recovery

sudo systemctl restart ssh
sudo systemctl status ssh
Log Inspection

journalctl -u ssh -n 100 --no-pager
Increase SSH verbosity temporarily if needed.

Deeper Diagnostics

ss -tulpn | grep ssh
sudo strace -p <sshd_pid>
Final Assessment
Status: Healthy
Confidence Level: High
Conclusion: System is stable; encountered errors were due to command mistakes or permission boundaries, not infrastructure issues.
