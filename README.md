# Uyuni Automation Integration via MQTT

## 📌 Overview

This project explores how to integrate Uyuni with modern automation platforms using an event-driven architecture based on MQTT.

Uyuni is powerful for configuration and infrastructure management, but it lacks a flexible, native automation engine.
This repository demonstrates how to decouple automation logic from Uyuni and connect it with external tools like Node-RED.

---

## 🧠 Motivation

Instead of embedding automation directly into Uyuni, this project aims to:

* Keep Uyuni focused on system management
* Expose real-time events (e.g. updates, registrations, status changes)
* Enable external automation engines to react to those events

---

## 🏗️ Architecture

```
Uyuni → MQTT Broker → Node-RED → Automation Actions
```

* Uyuni publishes system events to MQTT
* Node-RED subscribes and executes automation workflows
* The system remains modular and extensible

---

## ⚙️ Features

* Publish Uyuni events to MQTT:

  * Package updates
  * System registration
  * Status changes

* Integrate with Node-RED for automation

* No modification of Uyuni core required

* Flexible and extensible event-driven design

---

## 🚀 Getting Started

### Prerequisites

* Docker
* Docker Compose

### Run the demo

```bash
docker-compose up -d
```

This will start:

* MQTT broker
* Node-RED instance

---

## 📦 Example Use Cases

1. New system registered → automatically assign tags
2. Package update completed → send notification
3. System issue detected → trigger remediation workflow

---

## 📁 Project Structure

```
.
├── docker-compose.yml
├── node-red/
│   └── flows.json
├── mqtt/
│   └── config.md
├── uyuni/
│   └── event-publisher.md
└── examples/
    └── use-cases.md
```

---

## 🎯 Goals

* Make Uyuni a first-class citizen in automation ecosystems
* Decouple automation logic from infrastructure management
* Provide a reusable event-driven integration pattern

---

## 🔧 Current Status

This project is an early prototype that demonstrates:

* MQTT-based event publishing
* Integration with Node-RED
* Basic automation workflows

---

## 🤝 Why This Matters

This approach enables:

* Low-code automation (via Node-RED)
* Integration with multiple tools (not limited to one platform)
* Scalable and maintainable automation architecture

---

## 🙋 About Me

I am currently exploring event-driven automation around Uyuni and have built this prototype to demonstrate the concept.

I am interested in contributing to projects related to:

* Uyuni
* Automation platforms
* Event-driven systems

I would love to collaborate and further develop this into a production-ready solution.

---

## 📬 Feedback & Contributions

Feedback, ideas, and contributions are welcome!
Feel free to open an issue or start a discussion.
