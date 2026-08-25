# 🐝 BeeWatch

### Smart Beehive Monitoring & IoT Management Platform

BeeWatch is a complete IoT platform designed for modern beekeepers
to monitor and manage their beehives remotely.

The platform combines a mobile application, web administration
dashboard, IoT sensor infrastructure, real-time monitoring,
alerts, farm management, and subscription-based services.

---

## 🚀 Product Overview

BeeWatch provides beekeepers with real-time visibility into their
hives through connected IoT sensors.

The platform allows users to monitor:

- ⚖️ Hive Weight
- 🌡️ Internal Temperature
- 🌡️ External Temperature
- 💧 Humidity
- 🔊 Sound Levels
- 🔋 Device Battery
- 🚨 Hive Alerts
- 🐝 Multiple Hives
- 🚜 Multiple Farms

---

## 📱 Mobile Application

The BeeWatch mobile application provides beekeepers with a simple
interface for monitoring their farms and connected hives.

### Features

- Secure authentication
- Farm management
- Hive monitoring
- Live sensor readings
- Historical monitoring
- Hive alerts
- Battery monitoring
- User profile
- Multiple farms and hives

### Screenshots

<p align="center">
  <img src="screenshots/beewatch-loginPage.png" width="250">
  <img src="screenshots/mobile-hive-monitor.png" width="250">
</p>

---

## 🖥️ Admin Dashboard

BeeWatch includes a web-based administration dashboard for managing
the entire platform.

### Administration Features

- Dashboard analytics
- User management
- Farm management
- Hive management
- Subscription management
- Billing
- Revenue monitoring
- Alert monitoring
- Platform statistics

### Dashboard

<p align="center">
  <img src="screenshots/admin-dashboard.png" width="900">
</p>

---

## 🌐 Platform Architecture

BeeWatch is designed as a complete IoT SaaS ecosystem consisting of:


                    ┌────────────────────┐
                    │   IoT Hive Sensors │
                    └─────────┬──────────┘
                              │
                              ▼
                    ┌────────────────────┐
                    │   IoT / Backend    │
                    │     Platform       │
                    └─────────┬──────────┘
                              │
              ┌───────────────┴───────────────┐
              │                               │
              ▼                               ▼
      ┌───────────────┐               ┌───────────────┐
      │ Mobile App    │               │ Admin Panel   │
      │   Beekeepers  │               │   Web         │
      └───────────────┘               └───────────────┘
