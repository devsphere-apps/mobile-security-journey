# ⬆️ Privilege Escalation

This phase comes after exploitation.

👉 Goal: **Gain higher access than originally (allowed)**

---

## 🧠 What is Privilege Escalation?

Privilege escalation means:
- Increasing your access level  
- Moving from a low-privileged user to a higher-privileged user  

> 👉 Example: Normal user → Admin access

---

## 🎯 Objective

- Bypass access controls  
- Access restricted resources  
- Demonstrate impact of broken authorization  

---

## 🔍 Types of Privilege Escalation

### 🔹 Vertical Privilege Escalation
- Low-level user → High-level user  

**Example:**
- User becomes admin  

---

### 🔹 Horizontal Privilege Escalation
- Same level access, but different user  

**Example:**
- Access another user’s account/data  

---

## 📱 Mobile App Context

In mobile applications, privilege escalation often occurs due to:

- Missing server-side authorization  
- Trusting client-side data  
- Improper role validation  
- Weak API security  

---

## ⚙️ Common Techniques

- Modifying user roles in requests  
- Changing user IDs (IDOR)  
- Accessing hidden/admin endpoints  
- Reusing tokens across accounts  

---

## 🛠️ Tools Commonly Used

- :contentReference[oaicite:0]{index=0}  
- :contentReference[oaicite:1]{index=1}  

👉 Used to intercept and modify requests  

---

## ⚠️ Important Rules

- Stay within testing scope  
- Do not modify or delete real user data  
- Only prove access, avoid damage  
- Maintain ethical testing practices  

---

## 🎯 Example Flow

1. Login as normal user  
2. Intercept request  
3. Modify role or user ID  
4. Send request  
5. Gain higher or unauthorized access  

---

## 🧠 Summary

- Privilege Escalation = **Access control failure**  
- Vertical = Higher role access  
- Horizontal = Access other users’ data  

---

💡 **Pro Tip:**  
If the backend trusts the client, privilege escalation is often possible  
