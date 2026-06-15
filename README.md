# EV Vehicle Control Unit (VCU) – STM32F407

## Overview

This project is a prototype **Vehicle Control Unit (VCU)** designed for a 48V electric vehicle platform using the STM32F407 microcontroller.
The VCU acts as the central controller that reads vehicle inputs, monitors system parameters, and manages outputs and communication.

This project is developed as a learning and portfolio build based on real EV system architecture principles.

---

## Key Features

* Dual-channel throttle position sensing (safety redundancy)
* Brake input detection
* Battery voltage monitoring (ADC-based sensing)
* Battery and motor temperature monitoring using NTC sensors
* CAN communication interface for vehicle network integration
* Cooling fan control
* Main contactor control logic
* Ready and Fault status indication via LEDs

---

## Hardware Overview

* MCU: STM32F407VGT6
* Communication: CAN bus (via external CAN transceiver)
* Input Voltage: 48V EV battery system
* Internal Rails: 12V / 5V / 3.3V regulated supply system
* Analog Inputs: ADC-based sensor acquisition

---

## System Scope

The VCU is responsible for:

* Reading driver inputs (throttle, brake, ignition)
* Monitoring vehicle electrical and thermal parameters
* Executing basic safety logic (fault detection, plausibility checks)
* Communicating status over CAN bus
* Controlling auxiliary outputs (fan, contactor, indicators)

The VCU does not control the motor directly; it communicates with the motor controller.

---

## Project Status

* Requirements definition: In progress
* Hardware design: Not started
* Firmware: Not started
* PCB: Not started

---

## Purpose

This project is built to understand real-world EV electronic architecture, embedded system design, and automotive-style control logic using STM32.
