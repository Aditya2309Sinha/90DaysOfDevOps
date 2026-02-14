Here’s your clean, structured, GitHub-ready revision file.
Save as: day-12-revision.md

🔁 Day 12 – Fundamentals Revision

One-day pause to consolidate Days 01–11
Focus: retention, clarity, confidence.

🧠 1️⃣ Mindset & Plan Check
🔍 Revisited Day 01 Learning Plan

My goal: Build strong Linux + DevOps fundamentals.

Progress so far: Comfortable with navigation, processes, services, permissions, users, ownership.

Weak spots:

chmod numeric permissions need faster recall.

Remembering useful journalctl flags.

Adjustment:

Next 3 days: Improve speed + real-world thinking (troubleshooting mindset).

✅ Plan still aligned with DevOps + Cloud goals.

⚙️ 2️⃣ Processes & Services Review
Commands Re-run
ps aux | head
systemctl status ssh
journalctl -u ssh --since "10 minutes ago"

Observations

ps aux shows running processes with user, PID, CPU, memory usage.

systemctl status ssh clearly shows:

Active (running)

PID

Recent logs

journalctl -u ssh gives detailed service logs for debugging.

📝 Insight:
systemctl status gives quick health.
journalctl gives deep troubleshooting data.

📂 3️⃣ File Skills Practice
Practiced Commands
echo "Revision practice" >> notes.txt
chmod 755 notes.txt
ls -l notes.txt
cp notes.txt backup-notes.txt
mkdir revision-test

What I Reinforced

>> appends without deleting content.

chmod 755 → Owner full, others read & execute.

ls -l is essential for verifying changes.

Always verify after modifying permissions.

📜 4️⃣ Incident Cheat Sheet – Top 5 Commands

If something breaks, I reach for:

ls -l → Check permissions immediately

ps aux → Check if process is running

systemctl status <service> → Check service health

journalctl -xe → Read error logs

id username → Verify user and group membership

These commands quickly answer:
Is it running?
Does it have permission?
Who owns it?
What error occurred?

👥 5️⃣ User & Group Sanity Check
Mini Scenario Recreated
sudo useradd testuser
sudo groupadd testgroup
sudo chown testuser:testgroup notes.txt
id testuser
ls -l notes.txt

Verified

id testuser shows UID, GID, and group membership.

ls -l confirms ownership change.

📝 Ownership only works if:

User exists

Group exists

You use sudo

🧪 Mini Self-Check
1️⃣ Which 3 commands save you the most time right now, and why?

ls -l → Immediate visibility into permissions and ownership.

systemctl status → Quick service health check.

ps aux → Confirms whether a process is running or consuming resources.

2️⃣ How do you check if a service is healthy?

First commands I run:

systemctl status nginx
ps aux | grep nginx
journalctl -u nginx --since "10 minutes ago"


This checks:

Service state

Running process

Recent logs

3️⃣ How do you safely change ownership and permissions?

Steps:

sudo chown aditya:devops project/
sudo chmod 755 project/

Always confirm with ls -l after change.

🎯 Key Takeaways

Fundamentals feel stronger after repetition.

Verification (ls -l, id, systemctl status) is critical.

Small daily practice prevents forgetting.

Troubleshooting mindset is forming
