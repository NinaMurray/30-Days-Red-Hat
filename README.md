# 30-Days-Red-Hat
Absolutely — here is a **clean, professional, GitHub‑ready `README.md`** containing your full **30‑Day RHCSA Study Plan**, formatted to look polished in a portfolio and aligned with your structured, visually organized style.

You can drop this directly into a repo as `README.md`.

---

# 📘 **30‑Day RHCSA Study Plan**
A structured, hands‑on, exam‑aligned roadmap for mastering Red Hat Enterprise Linux administration and preparing for the **RHCSA (EX200)** certification.  
Designed for daily 1–2 hour sessions with deeper weekend practice.

---

## 🧭 **Overview**
This study plan focuses on:
- Real‑world RHEL administration skills  
- Hands‑on labs using Rocky/AlmaLinux or browser‑based environments  
- Mastery of RHCSA exam objectives  
- Repetition, documentation, and scenario‑based practice  

---

# 📅 **WEEK 1 — Core Linux Foundations (Days 1–7)**  
**Focus:** Essential tools, navigation, file management, users, permissions.

---

## **Day 1 — Lab Setup**
- Install Rocky Linux or AlmaLinux in VirtualBox  
- Configure hostname, users, networking (NAT + Host‑Only)  
- Practice:  
  - `ip a`  
  - `nmcli`  
  - `hostnamectl`

---

## **Day 2 — Essential Tools**
- Commands: `ls`, `cp`, `mv`, `rm`, `touch`, `mkdir`, `grep`, `find`, `tar`  
- Practice:  
  - Archive/extract files  
  - Search logs  

---

## **Day 3 — Vim + Bash Basics**
- Vim: insert, save, quit, search  
- Bash: variables, pipes, redirection, history  

---

## **Day 4 — Users & Groups**
- Commands: `useradd`, `passwd`, `groupadd`  
- Files: `/etc/passwd`, `/etc/shadow`, `/etc/group`  
- Practice:  
  - Create users with custom shells  
  - Manage group membership  

---

## **Day 5 — Permissions & ACLs**
- `chmod`, `chown`, `umask`  
- ACLs: `setfacl`, `getfacl`  
- Practice:  
  - Default ACLs  
  - Inheritance  

---

## **Day 6 — System Documentation**
- `man`, `info`, `/usr/share/doc`  
- Practice:  
  - Solve tasks using only documentation  

---

## **Day 7 — Weekly Review**
- Create 5 users  
- Set ACLs  
- Compress logs  
- Search files  
- Validate with RHCSA objective list  

---

# 📅 **WEEK 2 — Storage, Boot Process, System Services (Days 8–14)**  
**Focus:** LVM, partitions, systemd, scheduling, boot targets.

---

## **Day 8 — Partitions**
- Tools: `lsblk`, `fdisk`, `parted`, `mkfs`  
- Practice:  
  - Create partitions  
  - Mount persistently  

---

## **Day 9 — LVM**
- Create PV → VG → LV  
- Resize LV (extend + shrink with XFS constraints)  

---

## **Day 10 — Auto‑Mounting & FSTAB**
- Edit `/etc/fstab`  
- Test boot failures (critical exam skill)  

---

## **Day 11 — Systemd Services**
- `systemctl enable/disable/start/stop`  
- Create a custom service file  

---

## **Day 12 — Scheduling Tasks**
- `cron`, `at`, systemd timers  

---

## **Day 13 — Boot Targets & GRUB**
- Switch system targets  
- Reset root password  

---

## **Day 14 — Weekly Review**
- Full LVM workflow  
- FSTAB entries  
- Service management  

---

# 📅 **WEEK 3 — Networking, Security, SELinux, Firewalld (Days 15–21)**  
**Focus:** Networking, firewall rules, SELinux troubleshooting.

---

## **Day 15 — Networking Basics**
- `nmcli`, `nmtui`  
- Configure static IPs, DNS, hostnames  

---

## **Day 16 — Firewalld**
- Zones, services, ports  
- Permanent vs runtime rules  

---

## **Day 17 — SELinux**
- Modes: enforcing, permissive  
- Tools: `semanage`, `restorecon`, `chcon`  
- Practice:  
  - Break SELinux contexts  
  - Fix them  

---

## **Day 18 — SSH & Key Management**
- Configure SSHD  
- Create key pairs  
- Disable password authentication  

---

## **Day 19 — System Logging**
- `journalctl`  
- Filter logs by service, time, priority  

---

## **Day 20 — Networking Services**
- Configure chrony (NTP)  
- Basic web service setup  

---

## **Day 21 — Weekly Review**
- SELinux troubleshooting  
- Firewall rules  
- Static networking  

---

# 📅 **WEEK 4 — Containers, Scripting, Exam Simulation (Days 22–30)**  
**Focus:** Podman, shell scripting, full exam‑style scenarios.

---

## **Day 22 — Podman Basics**
- Pull images  
- Run containers  
- Persistent storage  

---

## **Day 23 — Podman Advanced**
- Systemd‑managed containers  
- Build custom images  

---

## **Day 24 — Shell Scripting**
- Variables, loops, conditionals  
- Make scripts executable  
- Create systemd timers  

---

## **Day 25 — Archiving & Transfer**
- `scp`, `rsync`, `tar`, `gzip`, `xz`  

---

## **Day 26 — Objective Review**
- Cross‑check each RHCSA domain  
- Identify weak areas  

---

## **Day 27 — Practice Exam #1**
- Simulate 2.5 hours  
- No internet  
- Use only man pages  

---

## **Day 28 — Fix Weak Areas**
- Re‑practice LVM, SELinux, networking  

---

## **Day 29 — Practice Exam #2**
- Repeat simulation  
- Aim for 80%+ task completion  

---

## **Day 30 — Final Review**
- Re‑read RHCSA objectives  
- Validate all commands from memory  
- Prepare exam environment  

---

