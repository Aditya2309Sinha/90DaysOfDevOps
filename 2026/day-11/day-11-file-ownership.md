🐧 Day 11 – File Ownership Challenge

Mastering chown, chgrp, and recursive ownership management in Linux.

📁 Files & Directories Created
📄 Files

devops-file.txt

team-notes.txt

project-config.yaml

heist-project/vault/gold.txt

heist-project/plans/strategy.conf

bank-heist/access-codes.txt

bank-heist/blueprints.pdf

bank-heist/escape-plan.txt

📂 Directories

app-logs/

heist-project/

heist-project/vault/

heist-project/plans/

bank-heist/

🔄 Ownership Changes
1️⃣ devops-file.txt
Before	After
aditya:aditya	tokyo:aditya
tokyo:aditya	berlin:aditya
2️⃣ team-notes.txt
Before	After
aditya:aditya	aditya:heist-team
3️⃣ project-config.yaml
Before	After
aditya:aditya	professor:heist-team
4️⃣ app-logs/
Before	After
aditya:aditya	berlin:heist-team
5️⃣ heist-project/ (Recursive Change)

All files and subdirectories changed using -R flag.

Before	After
aditya:aditya	professor:planners

Includes:

vault/

vault/gold.txt

plans/

plans/strategy.conf

6️⃣ bank-heist Directory Files
File	Before	After
access-codes.txt	aditya:aditya	tokyo:vault-team
blueprints.pdf	aditya:aditya	berlin:tech-team
escape-plan.txt	aditya:aditya	nairobi:vault-team
💻 Commands Used
# View ownership
ls -l
ls -l filename
ls -lR directory/

# Create files
touch filename

# Create directories
mkdir directory
mkdir -p parent/child

# Create users
sudo useradd tokyo
sudo useradd berlin
sudo useradd nairobi
sudo useradd professor

# Create groups
sudo groupadd heist-team
sudo groupadd planners
sudo groupadd vault-team
sudo groupadd tech-team

# Change owner only
sudo chown tokyo devops-file.txt
sudo chown berlin devops-file.txt

# Change group only
sudo chgrp heist-team team-notes.txt

# Change owner and group together
sudo chown professor:heist-team project-config.yaml
sudo chown berlin:heist-team app-logs

# Recursive ownership change
sudo chown -R professor:planners heist-project/

# Practice challenge ownership
sudo chown tokyo:vault-team bank-heist/access-codes.txt
sudo chown berlin:tech-team bank-heist/blueprints.pdf
sudo chown nairobi:vault-team bank-heist/escape-plan.txt
