Files & Directories Created
Files

devops-file.txt

team-notes.txt

project-config.yaml

heist-project/vault/gold.txt

heist-project/plans/strategy.conf

bank-heist/access-codes.txt

bank-heist/blueprints.pdf

bank-heist/escape-plan.txt

Directories

app-logs/

heist-project/

heist-project/vault/

heist-project/plans/

bank-heist/

Ownership Changes
1️⃣ devops-file.txt

Before: aditya:aditya

After: berlin:aditya

2️⃣ team-notes.txt

Before: aditya:aditya

After: aditya:heist-team

3️⃣ project-config.yaml

Before: aditya:aditya

After: professor:heist-team

4️⃣ app-logs/

Before: aditya:aditya

After: berlin:heist-team

5️⃣ heist-project/ (Recursive)

Before:

aditya:aditya (all files and subdirectories)

After:

professor:planners (applied using -R flag)

6️⃣ bank-heist Files

access-codes.txt: aditya:aditya → tokyo:vault-team

blueprints.pdf: aditya:aditya → berlin:tech-team

escape-plan.txt: aditya:aditya → nairobi:vault-team

Commands Used
# View ownership
ls -l
ls -lR heist-project/

# Create files
touch devops-file.txt
touch team-notes.txt
touch project-config.yaml

# Create directories
mkdir app-logs
mkdir -p heist-project/vault
mkdir -p heist-project/plans
mkdir bank-heist

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

# Change owner
sudo chown tokyo devops-file.txt
sudo chown berlin devops-file.txt

# Change group
sudo chgrp heist-team team-notes.txt

# Change owner and group together
sudo chown professor:heist-team project-config.yaml
sudo chown berlin:heist-team app-logs

# Recursive ownership change
sudo chown -R professor:planners heist-project/

# Set specific ownership for practice challenge
sudo chown tokyo:vault-team bank-heist/access-codes.txt
sudo chown berlin:tech-team bank-heist/blueprints.pdf
sudo chown nairobi:vault-team bank-heist/escape-plan.txt
