# Linux Directory Structure – Essential Notes 🐧

This document explains important Linux directories, what they contain,  
and when they are used during real troubleshooting and DevOps work.

---

## Core Directories (Must Know)

### `/` (root)
- The top-level directory of the Linux filesystem.
- All other directories branch from here.

### bash
ls -l /
Observed: bin, etc, home, var, usr

I would use this when navigating the filesystem or understanding disk layout.

/home
Contains home directories for normal users.

Each user stores personal files, configs, and projects here.

ls -l /home
Observed: adi/

I would use this when managing user files or checking user-specific issues.

/root
Home directory of the root (administrator) user.

Separate from /home for security reasons.

ls -l /root
Observed: shell config files and admin scripts

I would use this when logged in as root for administrative tasks.

/etc
Stores system-wide configuration files.

Most services read their settings from here.

ls -l /etc
Observed: hostname, hosts, ssh/

I would use this when configuring services or debugging startup issues.

/var/log
Contains system and application log files.

Critical for debugging and monitoring.

ls -l /var/log
Observed: syslog, auth.log, journal/

I would use this when investigating errors, crashes, or security events.

/tmp
Stores temporary files.

Files here may be deleted automatically on reboot.

ls -l /tmp
Observed: temporary runtime files

I would use this when testing scripts or creating short-lived files.

Additional Directories (Good to Know)
/bin
Essential command binaries required for basic system operation.

Available even in recovery mode.

ls -l /bin
Observed: ls, cp, mv, bash

I would use this when running core commands during system recovery.

/usr/bin
User-level command binaries.

Most commonly used commands live here.

ls -l /usr/bin | head
Observed: grep, awk, sed

I would use this when executing standard Linux utilities.

/opt
Optional or third-party software installations.

Often used by vendor applications.

ls -l /opt
Observed: (empty or custom app folders)

I would use this when managing external or manually installed software.

### Hands-On Tasks
Find the Largest Log Files
du -sh /var/log/* 2>/dev/null | sort -h | tail -5
Observation: Identifies log files consuming the most disk space.

### View a Configuration File
cat /etc/hostname
Observation: Displays system hostname.

Inspect Home Directory
ls -la ~
Observation: Shows hidden config files like .bashrc and .profile.

Key Takeaway
Understanding Linux directories makes troubleshooting faster
because you know where to look before guessing.
