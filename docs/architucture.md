# BeeWatch — System Architecture

BeeWatch is a smart hive monitoring platform designed to connect IoT-enabled beehives with a centralized cloud backend, mobile application, and administrative dashboard.

The platform collects environmental and hive telemetry, processes the data through a backend service, provides real-time monitoring and alerts, and supports subscription-based billing.

---

## 1. Architecture Overview

BeeWatch follows a layered cloud architecture designed to separate the presentation, application, data, IoT, and billing concerns.

### High-Level Architecture


                         ┌──────────────────────┐
                         │    BeeWatch Mobile   │
                         │      Flutter App     │
                         └──────────┬───────────┘
                                    │
                                  HTTPS
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │     NestJS API       │
                         │    Backend Service   │
                         └───────┬──────┬───────┘
                                 │      │
                    ┌────────────┘      └──────────────┐
                    ▼                                  ▼
          ┌──────────────────┐              ┌──────────────────┐
          │    PostgreSQL    │              │      Stripe      │
          │   Data Storage   │              │     Billing      │
          └──────────────────┘              └──────────────────┘
                    ▲
                    │
                    │ MQTT / IoT
                    │
          ┌─────────┴─────────┐
          │   IoT Devices     │
          │                   │
          │ Temperature       │
          │ Humidity          │
          │ Weight            │
          │ Sound             │
          │ Battery           │
          └───────────────────┘

                         ┌──────────────────────┐
                         │    Admin Dashboard   │
                         │    Web Application   │
                         └──────────┬───────────┘
                                    │
                                  HTTPS
                                    │
                                    ▼
                              NestJS API
