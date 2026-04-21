# 🔒 Android Sandboxing

Android uses sandboxing to isolate applications and protect user data.

---

## 🧠 Core Concept

- Each app runs in its own isolated environment  
- Apps cannot access each other's data directly  
- Isolation is enforced by the Linux kernel  

---

## 🔐 How Sandboxing Works

Android implements sandboxing using:

- Unique User ID (UID) for each app  
- File system permissions  
- Process isolation  

---

## 👤 Unique UID

- Every app is assigned a unique Linux user ID  
- This UID controls access to files and resources  

Example:
- App A → UID 10101  
- App B → UID 10102  

App A cannot access App B data  

---

## 📁 Private App Storage

Each app has its own private directory:

/data/data/com.example.app/

Permissions:

drwx------

- Only the app (owner) can access  
- No access for other apps  

---

## 🌍 External Storage (Shared)

/storage/emulated/0/

- Accessible by multiple apps  
- Not secure for sensitive data  

---

## 🔁 Process Isolation

- Each app runs in a separate process  
- Memory is isolated  
- One app cannot directly access another app’s memory  

---

## ⚠️ When Sandboxing Can Be Weak

Sandboxing can be bypassed or weakened due to:

- Storing sensitive data in external storage  
- Misconfigured file permissions  
- Exported components without proper security  
- Debuggable applications  
- Backup misconfigurations  

---

## 💥 Security Risks

Weak sandboxing can lead to:

- Data leakage  
- Unauthorized access  
- Privacy violations  

---

## 🎯 Example Scenario

### Secure Case

/data/data/com.bank.app/  
drwx------

- Only the banking app can access its data  

---

### Insecure Case

/storage/emulated/0/app_data.txt  
-rw-r--r--

- Any app can read the file  
- Sensitive data may be exposed  

---

## 🧠 Summary

- Sandboxing isolates apps from each other  
- Each app has a unique UID and private storage  
- External storage is not secure  
- Misconfigurations can break isolation  
