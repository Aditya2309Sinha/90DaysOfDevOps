# Day 09 Challenge – User & Group Management 🐧

**Goal:** Practice Linux user and group management with hands-on tasks  
**Environment:** Linux (WSL / VM / Server)

---

## Users & Groups Created

### Users
- tokyo
- berlin
- professor
- nairobi

### Groups
- developers
- admins
- project-team

---

## Task 1: Create Users
Commands Used:

sudo useradd -m tokyo
sudo passwd tokyo

sudo useradd -m berlin
sudo passwd berlin

sudo useradd -m professor
sudo passwd professor

cat /etc/passwd | grep -E "tokyo|berlin|professor"
ls -l /home

Observation:
-All users exist in /etc/passwd
-Home directories created under /home

### Task 2: Create Groups
Commands Used
sudo groupadd developers
sudo groupadd admins
Verification
cat /etc/group | grep -E "developers|admins"
Observation:

Both groups successfully created

### Task 3: Assign Users to Groups
Commands Used
sudo usermod -aG developers tokyo
sudo usermod -aG developers,admins berlin
sudo usermod -aG admins professor
Verification
groups tokyo
groups berlin
groups professor
Group Assignments

tokyo → developers

berlin → developers, admins

professor → admins

### Task 4: Shared Directory (Developers)
Commands Used
sudo mkdir /opt/dev-project
sudo chgrp developers /opt/dev-project
sudo chmod 775 /opt/dev-project
Verification
ls -ld /opt/dev-project
Testing Access
sudo -u tokyo touch /opt/dev-project/tokyo.txt
sudo -u berlin touch /opt/dev-project/berlin.txt
Observation:

Both users could create files successfully

Group permissions working as expected

### Task 5: Team Workspace

Commands Used:
sudo useradd -m nairobi
sudo passwd nairobi

sudo groupadd project-team
sudo usermod -aG project-team nairobi
sudo usermod -aG project-team tokyo

sudo mkdir /opt/team-workspace
sudo chgrp project-team /opt/team-workspace
sudo chmod 775 /opt/team-workspace

groups nairobi
groups tokyo
ls -ld /opt/team-workspace

sudo -u nairobi touch /opt/team-workspace/nairobi.txt

Observation:
-Team workspace accessible to project-team members
-Permissions correctly enforced

### Commands Used (Summary)
-useradd, passwd, usermod
-groupadd, groups
- mkdir, chgrp, chmod
- ls, cat
- sudo -u

### What I Learned: 
- Users must be explicitly added to groups using usermod -aG
- Group ownership + permissions enable controlled collaboration
- Testing with sudo -u is essential to verify real access
sudo useradd -m professor
sudo passwd professor
