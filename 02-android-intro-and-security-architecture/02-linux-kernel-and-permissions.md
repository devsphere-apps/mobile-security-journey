# 🐧 Linux Kernel and Permission Model

Android is built on top of the Linux kernel, which provides the foundation for system security, process management, and hardware interaction.

---

## 🧠 Core Concept

- Android uses the Linux kernel for low-level operations  
- Security is enforced using the Linux permission model  
- Every file and process is controlled by permissions  

---

## 🔐 Linux Permission Model

Each file or directory has three types of access control:

Owner | Group | Others

Each of these can have the following permissions:

r (read) | w (write) | x (execute)

---

## 📖 Permission Format

Example:

-rwxr-xr--

### Breakdown:

- `-` → File type  
- `rwx` → Owner permissions  
- `r-x` → Group permissions  
- `r--` → Others permissions  

---

## 📌 Permission Meaning

- `r` → Read (view content)  
- `w` → Write (modify/delete)  
- `x` → Execute (run file)  
- `-` → No permission  

---

## 📁 Directory Permissions

Permissions behave slightly differently for directories:

- `r` → List files in directory  
- `w` → Create/delete files  
- `x` → Enter/access directory  

---

## 📱 Android Mapping

In Android:

- Owner → The application itself (unique UID)  
- Group → System or shared group (rare use)  
- Others → All other applications  

---

## 🔒 Example (Secure App Data)

/data/data/com.example.app/  
drwx------

- Only the app (owner) can access  
- Other apps have no access  

---

## ⚠️ Example (Insecure Configuration)

drwxr-xr-x

- Other apps can access the directory  
- May lead to data exposure  

---

## 🔑 Important Rule

Directory permissions must allow access before file permissions matter.

If a directory is restricted:
- Files inside cannot be accessed by others  

---

## 💥 Security Impact

Incorrect permissions can lead to:

- Sensitive data exposure  
- Unauthorized file access  
- Application data leakage  

---

## 🧠 Summary

- Android security is based on Linux permissions  
- Files and directories use `rwx` model  
- Each app has a unique owner (UID)  
- Proper permissions ensure application isolation  
