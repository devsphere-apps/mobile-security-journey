# 🔐 Android Identity and Access Management (IAM)

Android uses a strong identity and access management system to control how applications interact with the system and each other.

---

## 🧠 Core Concept

- Each application is assigned a unique identity  
- Access to resources is controlled using this identity  
- Isolation is enforced using Linux user IDs (UIDs)  

---

## 👤 Unique User ID (UID)

- Every app gets a unique Linux UID at installation  
- This UID defines what the app can access  

### Example:
- App A → UID 10101  
- App B → UID 10102  

➡️ App A cannot access App B data  

---

## 📁 Application Directories

### 📦 App Installation Directory

/data/app/com.example.app/

- Contains APK files  
- Readable by system  

---

### 🔒 Private App Data

/data/data/com.example.app/

- Stores:
  - Databases  
  - Shared Preferences  
  - Files  

- Permissions:
drwx------

👉 Only the app (owner) can access  

---

### 🌍 External Storage

/storage/emulated/0/Android/data/com.example.app/

- Shared storage  
- Accessible by multiple apps  
- Not secure for sensitive data  

---

## 🔐 Access Control Mechanism

Android enforces access using:

- UID-based isolation  
- File permissions  
- Application sandboxing  

---

## 🚫 App-to-App Access

By default:

- Apps cannot directly access other apps' data  
- Interaction is only possible through:
  - Intents  
  - Content Providers  
  - Services (if exposed)  

---

## 👑 Root User

- Root = superuser  
- Has full access to all data  

### Impact:
- Can bypass all restrictions  
- Access any app’s private data  

---

## 📱 Emulator vs Real Device

- Some emulators run with root access  
- Real devices are usually restricted  

---

## 💥 Security Risks

Weak IAM configuration can lead to:

- Unauthorized data access  
- Data leakage  
- Privilege escalation  

---

## 🎯 Example Scenario

### Secure Case

/data/data/com.bank.app/  
drwx------

- Only the app can access its data  

---

### Risk Case

Data stored in shared storage:

/storage/emulated/0/app_data.txt  

- Other apps may access it  

---

## 🧠 Summary

- Each app has a unique UID  
- Access is controlled using permissions and isolation  
- Private storage is secure  
- External storage is shared and risky  
