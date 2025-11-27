# Conveyor-Belt-Dual-Motor-Control-System-PLC-Siemens-TIA-Portal

This project demonstrates a **PLC-controlled dual-motor conveyor system** using one start push button, one stop push button, and two sensors for box counting.
The system is designed to automatically switch between two conveyor motors based on sensor counts.

---

## 📌 Project Description

The system includes:

* **Motor 1 (Conveyor 1)**
* **Motor 2 (Conveyor 2)**
* **Start Push Button**
* **Stop Push Button**
* **Sensor 1** (counts boxes on Conveyor 1)
* **Sensor 2** (counts boxes on Conveyor 2)

---

## 🔧 Operating Logic

### 1. System Start

* When the **Start Button** is pressed:

  * **Motor 1** (Conveyor 1) starts running.

### 2. Box Counting on Conveyor 1

* **Sensor 1** counts boxes as they pass.
* When **Sensor 1 counts 7 boxes**:

  * **Motor 1 turns OFF**.
  * **Motor 2 turns ON immediately**.

### 3. Conveyor 2 Operation

* Conveyor 2 moves the boxes toward the storage area.
* **Sensor 2** counts these boxes as they arrive.

### 4. Return to Conveyor 1

* When Sensor 2 finishes counting the boxes sent from Conveyor 1:

  * **Motor 2 turns OFF**.
  * **Motor 1 turns ON again**.
* The cycle repeats, continuously transferring boxes to storage.

