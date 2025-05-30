# Windows-online-script
An Online Script Based Github Tools Installer +:
# **Guide: How to Download and Run the Script in PowerShell**

This guide explains how to:  
1️⃣ **Download the script** (`Install-ChocoAndEssentials.ps1`) from GitHub Releases.  
2️⃣ **Run it in PowerShell** (recommended for better compatibility).  

---

## **Method 1: Direct Download & Run (Recommended)**
### **Step 1: Open PowerShell as Admin**
- search for `PowerShell`, right-click, and choose **"Run as administrator"**.  

### **Step 2: Download the Script**
Run this command to download the script directly:  
```powershell
cd "$env:USERPROFILE\Downloads"; Invoke-WebRequest "https://github.com/ahmadrezawiki/Windows-online-script/releases/download/V1.0/Install-ChocoAndEssentials.ps1" -OutFile "Install-ChocoAndEssentials.ps1" -UseBasicParsing -ErrorAction SilentlyContinue
```
*(This saves the file to your **Downloads** folder.)*  

### **Step 3: Run the Script**
```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force
& "$env:USERPROFILE\Downloads\Install-ChocoAndEssentials.ps1"
```
- `Set-ExecutionPolicy Bypass` allows script execution (temporarily).  
- `&` runs the script.  

---

## **Method 2: Manual Download & Run (Alternative)**
### **Step 1: Download from GitHub Releases**
1. Go to the **GitHub Releases** page:  
   → [https://github.com/ahmadrezawiki/Windows-online-script/releases](https://github.com/ahmadrezawiki/Windows-online-script/releases)  
2. Under **"Assets"**, click **`Install-ChocoAndEssentials.ps1`** to download it.  

### **Step 2: Open PowerShell as Admin**
(Run as Administrator, as shown in **Method 1**.)  

### **Step 3: Navigate to the Downloads Folder**
```powershell
cd "$env:USERPROFILE\Downloads"
```

### **Step 4: Run the Script**
```powershell
.\Install-ChocoAndEssentials.ps1
```
*(If blocked, first run `Set-ExecutionPolicy Bypass -Scope Process -Force`.)*  

---

## **Troubleshooting**
❌ **"Script execution disabled"** → Run `Set-ExecutionPolicy Bypass -Scope Process -Force`.  
❌ **File not found** → Check path with `ls` or `Test-Path Install-ChocoAndEssentials.pst`.  
---

### **Need Help?**
- Report issues on the **GitHub repository**.  
- For security, verify scripts from trusted sources.
- 🚀 **Done!** The script should now run in PowerShell. 
