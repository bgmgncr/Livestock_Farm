# Livestock Farm Monitoring System

**İzmir University of Economics**
**SE311 – Software Design Patterns**
**2024–2025 Spring**

## 👥 Group Members

* Begüm Gençer
* Cemile Dilvin Ağaçhanlı
* Sinem Yeşil
* Tuana Kara

---

## 📌 Project Overview

The **Livestock Farm** project is a simulation system for monitoring cattle on a farm using electronic tracking devices. Most cattle communicate via **Zigbee**, while some use **Bluetooth**. The system tracks cattle locations, alerts the farmer when cattle leave farm boundaries, manages different feeding plans, and supports veterinary and governmental inspections.

The main goal of the project is to demonstrate the practical use of **software design patterns** in a realistic scenario.

---

## 🧩 Design Patterns Used

* **Adapter Pattern** – Converts Bluetooth signals to Zigbee so all devices can communicate with the server.
* **Observer Pattern** – Notifies the farmer when a cattle leaves the farm boundaries.
* **Singleton Pattern** – Ensures a single shared `LocationDatabase` for all cattle.
* **Abstract Factory Pattern** – Creates appropriate feed types for dairy and beef cattle.
* **Visitor Pattern** – Allows veterinarians and ministry inspectors to perform checks without modifying cattle classes.

---

## 🏗 Key Components

* **Cattle (Abstract Class):** Stores ID and location information and accepts visitors.
* **DairyCattle / BeefCattle:** Subclasses with different feeding requirements.
* **FeedFactory:** Produces carbohydrate and protein feeds based on cattle type.
* **BluetoothToZigbeeAdapter:** Provides compatibility between Bluetooth devices and the Zigbee-based server.
* **Farmer:** Observer that receives boundary violation alerts.
* **Veterinarian / MinistryInspector:** Visitors that perform vaccination and ear tag checks.
* **LocationDatabase:** Singleton class that stores cattle and location data.

---

## 🧾 UML Diagrams

UML diagrams are included to illustrate class relationships and applied design patterns.

---

## ✅ Conclusion

This project combines **Observer**, **Adapter**, **Singleton**, **Abstract Factory**, and **Visitor** patterns into a clear and extensible system. The design makes the project easy to understand, maintain, and extend for future features.
