# 🏠 Smart Home Automation System

This project is a **cloud-based smart home automation system** that enables secure, remote control and monitoring of home devices. It features **Role-Based Access Control (RBAC)**, device status management, and supports **nested virtualization** for room-level simulation on cloud platforms like AWS and GCP.

---

## 🧾 Overview

The smart home system models a house as a virtual environment running on a **bare-metal EC2 instance**, with individual rooms simulated as **nested virtual machines (VMs)**. Each room contains devices (e.g., lights, fans, AC, CCTV), and users can interact with these based on their access roles.

---

## 📁 File Structure

| File / Folder | Description |
|---------------|-------------|
| `main_controller.py` | Central control unit for monitoring and managing rooms and devices |
| `firebase_config.py` | Firebase initialization and authentication setup |
| `rbac_manager.py` | RBAC logic to define user roles and permissions |
| `device_controller.py` | Interface to control devices (on/off, status check) |
| `room_vm_manager.py` | Logic for room-level VM deployment and simulation |
| `cloud_setup.md` | Instructions for setting up nested virtualization on AWS/GCP |
| `alerts_notifier.py` | Push notifications and email alerts for critical events |
| `user_interface/` | Front-end (web/mobile) interface for user interactions |
| `dashboard.html` | Web dashboard for manual control and monitoring |
| `mobile_ui.html` | Mobile-friendly UI variant |
| `README.md` | Project overview and documentation (you’re reading it!) |

---

## 🔐 Features

- 🔁 **Nested Virtualization** on AWS and GCP
- 👥 **Role-Based Access Control (RBAC)** with Firebase Auth
- 📲 **Remote device control** via web and mobile interface
- 🔔 **Real-time alerts and notifications**
- 📊 **Live device status and usage analytics**
- 🛡️ **Security system** with access logs and alert triggers
- 🌐 **Cloud-based deployment** with scalable architecture

---

## 🔧 Roles & Access

| Role | Permissions |
|------|-------------|
| Admin | Full access (add/remove devices, users, rooms, etc.) |
| User | Control and monitor assigned rooms only |
| Guest | View-only access to public devices (e.g., CCTV in living room) |

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/smart-home-automation.git
   cd smart-home-automation
   ```

2. Set up Firebase:
   - Create a project in Firebase Console
   - Add config details to `firebase_config.py`

3. Run the system:
   ```bash
   python3 main_controller.py
   ```

4. (Optional) Enable nested virtualization:
   - Follow `cloud_setup.md` for AWS/GCP nested virtualization setup
   - Deploy room-level VMs as per your design

---

## ☁️ Cloud Infrastructure

- **EC2 Bare-Metal Instance**: Base host for the smart home environment
- **Nested VMs**: Each room as a separate VM
- **Firebase**: Auth, real-time database, cloud functions
- **Cloud Functions**: Event triggers for alerts, emails, device state sync

---

## 🧠 Future Enhancements

- 🧠 AI-based user behavior prediction
- 📦 Integration with third-party smart devices (e.g., Alexa, Google Home)
- 🎯 Energy optimization analytics
- 🕸️ MQTT-based communication protocol support
