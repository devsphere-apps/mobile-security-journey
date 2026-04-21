# 🔎 Scanning & Enumeration

This phase comes after reconnaissance.

👉 Goal: **Identify vulnerabilities and explore the target in depth**

---

## ⚙️ 2. Scanning

Scanning is used to **automatically detect potential vulnerabilities** in the application.

👉 Tools are commonly used in this step.

---

### 🔍 What to Check

- Open ports (if backend involved)  
- Known vulnerabilities  
- Misconfigurations  
- Insecure components  

---

### 📱 Mobile App Scanning

In mobile application testing, scanning includes:

- Static analysis (analyzing APK/IPA without running it)  
- Detecting hardcoded secrets  
- Finding insecure permissions  
- Checking for exposed components  

---

### 🛠️ Common Tools

- :contentReference[oaicite:0]{index=0}  
- :contentReference[oaicite:1]{index=1}  

👉 These tools help automate initial testing

---

## 🧾 3. Enumeration

Enumeration is a **manual and detailed process**.

👉 Here, you actively investigate and confirm findings.

---

### 🔍 What to Enumerate

- API endpoints  
- Parameters in requests  
- User roles and permissions  
- Hidden functionalities  

---

### 📱 Mobile App Enumeration

- Intercept API calls  
- Modify requests and responses  
- Analyze authentication flow  
- Extract endpoints from app code  

---

### ⚡ Key Difference

| Scanning | Enumeration |
|----------|------------|
| Automated | Manual |
| Finds potential issues | Confirms and explores deeply |
| Fast | Detailed |

---

## 🎯 Example Flow

1. Run scan using tools  
2. Identify possible vulnerabilities  
3. Manually test each finding  
4. Explore APIs and app logic  

---

## 🧠 Summary

- Scanning = **Find possible issues (automated)**  
- Enumeration = **Deep analysis and confirmation (manual)**  

---

💡 **Pro Tip:**  
Scanning gives direction, but **Enumeration finds real vulnerabilities**
