Perfect — here is a **clean, professional, GitHub‑ready Markdown Home Lab Setup Guide** tailored for RHCSA preparation and aligned with the structured, modular documentation style you prefer.

You can drop this directly into a repo as `HOME_LAB_SETUP.md`.

---

# 🖥️ **Red Hat Linux Home Lab Setup Guide (VirtualBox + Rocky/AlmaLinux)**  
A complete, beginner‑friendly, exam‑aligned guide for building a **local RHCSA practice environment** using free, RHEL‑compatible distributions.

---

# 📘 **1. Overview**
This home lab is designed to help you practice every RHCSA objective using:
- **VirtualBox** (free virtualization)
- **Rocky Linux or AlmaLinux** (RHEL‑compatible)
- **Multiple VMs** for networking, storage, SELinux, and service configuration

This guide includes:
- Host system requirements  
- VirtualBox installation  
- VM creation  
- Networking setup  
- Snapshots  
- Optional multi‑VM topology  

---

# 🧩 **2. System Requirements**

| Component | Minimum | Recommended |
|----------|----------|-------------|
| RAM | 8 GB | 16 GB+ |
| CPU | 2 cores | 4+ cores |
| Storage | 40 GB free | 80–120 GB free |
| Virtualization | VT‑x/AMD‑V enabled | Required |

---

# 📦 **3. Required Downloads**

### **1. VirtualBox**
Download from: https://www.virtualbox.org/

### **2. Rocky Linux or AlmaLinux ISO**
Choose one (both are RHEL‑compatible):
- Rocky Linux: https://rockylinux.org/download  
- AlmaLinux: https://almalinux.org/download  

Use the **Minimal ISO** for RHCSA‑style practice.

---

# 🛠️ **4. Create Your First VM**

## **Step 1 — Create a New VM**
1. Open VirtualBox → *New*
2. Name: `rocky-server-01`
3. Type: Linux  
4. Version: Red Hat (64‑bit)
5. Memory: **4096 MB** (or more)
6. Hard Disk:  
   - Create new VDI  
   - Dynamically allocated  
   - Size: **40 GB**

---

## **Step 2 — Attach the ISO**
1. Settings → Storage  
2. Click the empty optical drive  
3. Choose the Rocky/AlmaLinux ISO  

---

## **Step 3 — Configure CPU & Network**
### **CPU**
- Settings → System → Processor  
- Assign **2 CPUs** minimum  

### **Network**
Use **two adapters**:
- Adapter 1: NAT (internet access)
- Adapter 2: Host‑Only (lab networking)

This mirrors RHCSA exam‑style networking tasks.

---

# 🧭 **5. Install Rocky/AlmaLinux**

### **During Installation**
- Set hostname: `server01.localdomain`
- Create a user: `student`
- Set root password
- Choose **Minimal Install**
- Partitioning: automatic (you’ll practice manual LVM later)

---

# 🔧 **6. Post‑Install Configuration**

After first boot:

### **Update system**
```bash
sudo dnf update -y
```

### **Install essential tools**
```bash
sudo dnf install -y vim bash-completion tar wget curl net-tools
```

### **Enable networking**
```bash
nmcli connection show
nmcli device status
```

### **Verify host‑only connectivity**
Your VM should be reachable from your host machine.

---

# 🌐 **7. Configure Networking (RHCSA‑Style)**

### **Set a static IP**
Example for `enp0s8` (host‑only):

```bash
sudo nmcli con mod enp0s8 ipv4.addresses 192.168.56.10/24
sudo nmcli con mod enp0s8 ipv4.method manual
sudo nmcli con up enp0s8
```

### **Set DNS**
```bash
sudo nmcli con mod enp0s8 ipv4.dns "8.8.8.8"
```

---

# 🧱 **8. Create Snapshots (Critical for Practice)**

Snapshots let you break the system and revert instantly.

Recommended snapshots:
1. **Fresh Install**
2. **Post‑Networking**
3. **Before LVM Practice**
4. **Before SELinux Practice**
5. **Before Podman Practice**

---

# 🖧 **9. Optional: Multi‑VM Lab Topology**

For advanced RHCSA/RHCE practice, create:

### **VM 1 — server01**
- Main practice machine  
- Services, SELinux, LVM, containers  

### **VM 2 — server02**
- SSH key management  
- File sharing  
- Networking scenarios  

### **VM 3 — client01**
- Test connectivity  
- Practice firewall rules  
- Validate services  

This mirrors real enterprise environments.

---

# 🧪 **10. Suggested Practice Scenarios**

### **Storage**
- Create partitions  
- Create LVM PV/VG/LV  
- Resize LVs  
- Configure `/etc/fstab`  

### **Networking**
- Static IPs  
- DNS  
- Hostnames  
- Firewalld rules  

### **SELinux**
- Break contexts  
- Fix with `restorecon`  
- Manage booleans  

### **System Services**
- Create custom systemd units  
- Enable/disable services  

### **Containers (Podman)**
- Run containers  
- Persist storage  
- Create systemd‑managed containers  

---

# 📚 **11. Recommended Free Resources**

- **LabEx RHEL Labs** — browser‑based hands‑on  
- **Rocky/AlmaLinux documentation**  
- **Red Hat official docs**  
- **RHCSA community study guides**  

---

# 🏁 **12. Final Notes**
This home lab is designed to:
- Mirror RHCSA exam tasks  
- Build real‑world sysadmin skills  
- Provide a safe environment to break and fix systems  
- Support my 30‑day study plan  


