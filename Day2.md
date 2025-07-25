# 🐱‍💻 Installation Guide: VirtualBox and Kali Linux

This guide will help you install **VirtualBox** and set up **Kali Linux** as a virtual machine (VM) step by step.

---

## 📦 1. Install VirtualBox

### 🔗 Download:
- Go to: [https://www.virtualbox.org](https://www.virtualbox.org)
- Click **Downloads**
- Choose your OS:
  - Windows hosts
  - macOS hosts
  - Linux distributions

### 🛠️ Installation Steps (Windows Example):
1. Run the downloaded `.exe` file.
2. Click **Next** through the setup wizard.
3. Keep default options.
4. Click **Install**.
5. Allow administrator permission if prompted.
6. Click **Finish** and launch VirtualBox.

---

## 🧪 2. Download Kali Linux ISO

### 🔗 Download:
- Go to: [https://www.kali.org/get-kali](https://www.kali.org/get-kali)
- Choose: **Installer ISO** (64-bit recommended)
- Save the `.iso` file.

---

## 💻 3. Create Kali Linux VM in VirtualBox

### ➕ Create New VM:
1. Open **VirtualBox**
2. Click **New**
3. Name: `Kali Linux`
4. Type: `Linux`
5. Version: `Debian (64-bit)`
6. Click **Next**

### 💾 Memory (RAM):
- Allocate **2 GB (2048 MB)** or more
- Recommended: 4 GB or higher if your system allows

### 🗃️ Create Virtual Hard Disk:
- Choose: **Create a virtual hard disk now**
- File type: `VDI`
- Storage: `Dynamically allocated`
- Size: Minimum **20 GB**

Click **Create**

---

## 🛠️ 4. Attach Kali Linux ISO

1. Select your VM → Click **Settings**
2. Go to **Storage**
3. Click on **Empty** under the Controller: IDE
4. Click the **CD icon** → Choose a disk file
5. Select the downloaded Kali `.iso` file
6. Click **OK**

---

## 🚀 5. Start and Install Kali Linux

1. Click **Start** in VirtualBox
2. Kali boot menu will appear → Choose **Graphical install**
3. Follow on-screen steps:
   - Language, Location, Keyboard layout
   - Set **Hostname** and **Domain name**
   - Create a user and password
   - Configure time zone
   - Disk partitioning: Use entire disk → Guided

4. Wait for the installation to finish
5. When prompted, remove ISO (Settings → Storage → Remove ISO)
6. Reboot the VM

---

## 🔐 6. Login to Kali Linux

- Use the username and password you set during installation
- You now have Kali Linux running in a virtual environment!

---

## 🧰 Optional: Install Guest Additions

To enable fullscreen, shared clipboard, and folder sharing:
1. Start the Kali VM
2. In VirtualBox menu → Devices → Insert Guest Additions CD
3. Mount and install it inside Kali (you may need `sudo`)

---

## ✅ Done!

You now have Kali Linux running inside VirtualBox. You're ready for ethical hacking, penetration testing, or cybersecurity learning.

---

## 💡 Tips

- Update Kali: `sudo apt update && sudo apt upgrade`
- Use snapshot feature before experimenting
- Install essential tools with: `sudo apt install kali-linux-top10`

