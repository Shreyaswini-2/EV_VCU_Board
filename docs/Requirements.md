# Requirements – EV Vehicle Control Unit (VCU)

## 1. System Overview

The Vehicle Control Unit (VCU) is the central controller for a 48V electric vehicle system.
It reads driver inputs and vehicle sensor data, executes basic control logic, and communicates with other vehicle modules via CAN.

---

## 2. Functional Requirements

### Driver Inputs

- The VCU shall read two throttle position sensor channels (TPS1 and TPS2).
- The VCU shall read a brake switch input.
- The VCU shall read an ignition/key input signal.

---

### Vehicle Monitoring

- The VCU shall measure battery pack voltage using an ADC channel.
- The VCU shall measure battery temperature using an NTC sensor.
- The VCU shall measure motor temperature using an NTC sensor.

---

### Control Outputs

- The VCU shall control a cooling fan based on temperature thresholds.
- The VCU shall control a main contactor for power enable/disable.
- The VCU shall provide Ready status indication.
- The VCU shall provide Fault status indication.

---

### Communication

- The VCU shall transmit vehicle status over CAN bus.
- The VCU shall support receiving basic control messages over CAN.

---

## 3. Safety Requirements

- The VCU shall detect throttle sensor mismatch (TPS1 vs TPS2).
- The VCU shall enter a fault state if sensor values exceed valid range.
- The VCU shall disable the contactor output during a fault state.
- The VCU shall default outputs to a safe state on reset.

---

## 4. Electrical Requirements

- The system shall operate from a 48V nominal input supply.
- The MCU shall operate at 3.3V regulated supply.
- Analog sensor inputs shall be read using STM32 ADC channels.
- CAN communication shall operate at 500 kbps.

---

## 5. Design Constraints

- The design shall use STM32F407VGT6 microcontroller.
- The system shall use external CAN transceiver.
- All external inputs shall include basic protection (filtering and voltage limiting).

---

## 6. System Scope

The VCU does not control the motor directly.
Motor control is handled by a separate motor controller via CAN communication.

---

## 7. Project Status

* Requirements: Defined
* Architecture: Pending
* Schematic Design: Pending
* PCB Layout: Pending
* Firmware: Pending
