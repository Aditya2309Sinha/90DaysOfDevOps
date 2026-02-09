# Day 10 Challenge – File Permissions

## Files Created
- devops.txt
- notes.txt
- script.sh
- project/

## Permission Changes
- script.sh: rw-r--r-- → rwxr-xr-x
- devops.txt: rw-r--r-- → r--r--r--
- notes.txt: rw-r--r-- → rw-r-----
- project/: rwxr-xr-x

## Commands Used
- touch devops.txt
- echo > notes.txt
- vim script.sh
- ls -l
- cat, head, tail
- chmod +x, chmod 640, chmod 755
- mkdir project

## What I Learned
1. Linux permissions control access for owner, group, and others
2. Execute permission is required to run scripts
3. chmod can use both symbolic and numeric modes
