# 🏗️ Android Architecture Layers

Android is built using a layered architecture. Each layer has a specific role and works together to run applications securely and efficiently.

---

## 🧠 Core Concept

- Android uses multiple layers  
- Each layer provides specific functionality  
- Higher layers depend on lower layers  

---

## 🔻 Layers Overview (Bottom to Top)

1. Linux Kernel  
2. Hardware Abstraction Layer (HAL)  
3. Native Libraries + Android Runtime (ART)  
4. Java API Framework  
5. System Applications  

---

## 🐧 1. Linux Kernel

- Base layer of Android  
- Manages:
  - Hardware drivers  
  - Memory  
  - Processes  
  - Security (UID, permissions)  

---

## 🔌 2. Hardware Abstraction Layer (HAL)

- Acts as a bridge between hardware and software  
- Allows Android to interact with hardware components  

### Example:
- Camera access  
- Bluetooth communication  

---

## ⚙️ 3. Native Libraries + Android Runtime (ART)

### Native Libraries
- Written in C/C++  
- Provide core functionalities:
  - Graphics (OpenGL)  
  - Media playback  
  - Database (SQLite)  

### Android Runtime (ART)
- Executes application code  
- Each app runs in its own runtime environment  

---

## 🧩 4. Java API Framework

- Provides APIs for developers  
- Includes system services such as:
  - Activity Manager  
  - Notification Manager  
  - Location Manager  

---

## 📱 5. System Applications

- Top layer  
- Includes:
  - Built-in apps (Dialer, Camera)  
  - Third-party apps  

---

## 🔁 Execution Flow Example

Opening the camera:

1. App requests camera access  
2. Framework processes the request  
3. Runtime executes code  
4. HAL communicates with hardware  
5. Kernel controls the hardware  

---

## 🔐 Security Across Layers

- Kernel → Permissions and process isolation  
- Runtime → App sandboxing  
- Framework → Access control  
- Apps → Permission enforcement  

---

## 💥 Security Insight

- Most vulnerabilities are found in:
  - Application layer  
  - Framework misuse  
- Lower layers are harder to exploit  

---

## 🧠 Summary

- Android uses a layered architecture  
- Each layer has a specific role  
- Security is enforced at multiple levels  
- Understanding layers helps in pentesting  
