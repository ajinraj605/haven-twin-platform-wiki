
# Platform Requirements and Scope

## 1. Overview

The Smart Device Management Platform is designed to provide a centralized solution for controlling, configuring and managing connected electrical devices through a mobile application and cloud infrastructure.

The platform aims to support general-purpose device control rather than being limited to a specific application or use case.

The initial V1 implementation will use the **Sonoff RE5V1C module** as its target hardware platform. The existing firmware will be replaced with custom-developed firmware to enable integration with the platform's cloud infrastructure and mobile application.

The core V1 functionalities will include basic ON/OFF control, scheduled operations and inching functionality.

These capabilities can support various applications, including electrical load switching, appliance control and gate automation.

This document defines the platform objectives, target hardware, functional requirements and scope of the initial V1 release.

## 2. Platform Goals

1. Develop a centralized platform for managing connected electrical devices.
2. Replace the existing firmware on supported hardware with custom-developed firmware.
3. Enable remote ON/OFF control through a mobile application.
4. Support scheduled device operations.
5. Provide configurable inching functionality for momentary switching applications.
6. Enable secure communication between devices and cloud infrastructure.
7. Provide device provisioning, registration and management.
8. Establish an extensible architecture for supporting additional device types and hardware capabilities.

## 3. Target Hardware

### 3.1 Sonoff RE5V1C

The Sonoff RE5V1C module is the selected hardware platform for the initial V1 implementation.

The existing firmware will be replaced with custom-developed firmware.

The module will act as a remotely controllable switching device integrated with the platform.

### 3.2 Firmware Replacement

The custom firmware will be responsible for:

- Device initialization and configuration.
- Network connectivity and provisioning.
- Secure cloud communication.
- Relay control.
- ON/OFF operations.
- Inching functionality.
- Scheduled operations.
- Device state reporting and synchronization.

## 4. Core Platform Functionalities

### 4.1 ON/OFF Control

Enable users to remotely control the connected relay through the mobile application.

- Turn the relay ON.
- Turn the relay OFF.
- View the reported relay state.

### 4.2 Scheduling

Allow users to configure scheduled device operations.

- Create schedules.
- Configure scheduled ON/OFF operations.
- Enable or disable schedules.
- Manage existing schedules.

### 4.3 Inching

Provide momentary relay activation for applications requiring a temporary switching operation.

- Activate the relay for a configured duration.
- Automatically deactivate the relay after the configured duration.
- Allow configuration of the inching duration.

### 4.4 Device Management

- Device provisioning and onboarding.
- Device registration and claiming.
- Device identification.
- Device configuration.
- Device connectivity monitoring.

## 5. Application Use Cases

The platform's core functionalities can be applied across multiple scenarios.

| Use Case | Applicable Functionality |
|---|---|
| General Electrical Load Control | ON/OFF |
| Appliance Control | ON/OFF, Scheduling |
| Gate Automation | Inching |
| Scheduled Equipment Operation | Scheduling, ON/OFF |
| Momentary Switching Applications | Inching |

The above are example applications and are not intended to restrict the platform to these use cases.

## 6. Platform Architecture Components

| Component | Responsibility |
|---|---|
| Device Hardware | Physical switching and electrical interfacing |
| Firmware | Device logic, relay control and connectivity |
| AWS IoT Core | Device connectivity and MQTT communication |
| Cloud Backend | Business logic, request processing and orchestration |
| Database | Persistent storage of user, device and configuration information |
| Mobile Application | Device onboarding, control and management |

## 7. V1 Scope

V1 will focus on integrating the Sonoff RE5V1C module with the platform using custom-developed firmware.

| Feature | Description | Scope |
|---|---|---|
| Target Hardware | Sonoff RE5V1C | Included |
| Firmware Replacement | Custom firmware development | Included |
| Device Provisioning | Device connectivity configuration | Included |
| Device Registration | Device association with user accounts | Included |
| ON/OFF Control | Basic relay control | Included |
| Scheduling | Scheduled device operations | Included |
| Inching | Configurable momentary relay activation | Included |
| Cloud Connectivity | AWS IoT Core integration | Included |
| MQTT Communication | Device-cloud messaging | Included |
| Device Shadow | Device state synchronization | Included |
| Mobile Application | Device onboarding and operation | Included |

## 8. Future Scope

Future versions may introduce additional hardware capabilities and device categories.

One potential extension is the development of custom hardware with input interfaces for connecting external sensors.

Possible future capabilities include:

- Digital input monitoring.
- Sensor integration.
- Physical equipment state monitoring.
- Gate open/closed position detection.
- Reporting external sensor states to the cloud.
- Supporting additional hardware modules and device categories.

These capabilities are future possibilities and are not included in the current V1 implementation.

## 9. Assumptions and Dependencies

- Sonoff RE5V1C is the selected hardware for V1.
- Existing firmware will be replaced with custom firmware.
- Hardware compatibility and firmware flashing procedures will be validated.
- AWS IoT Core will be used for device connectivity.
- The mobile application will communicate with the backend through defined APIs.
- Device control and scheduling behaviour will be finalized during architecture design.
- Future hardware extensions will be evaluated independently.

## 10. Open Decisions

| Item | Decision Required | Status |
|---|---|---|
| Firmware Architecture | Finalize firmware structure | Pending |
| Provisioning | Finalize provisioning mechanism | Pending |
| Relay Behaviour | Define relay operation and default state | Pending |
| Inching Duration | Define configurable timing range | Pending |
| Scheduling | Define scheduling and recurrence behaviour | Pending |
| Offline Behaviour | Define operation during connectivity loss | Pending |
| Device Shadow | Finalize desired and reported state structure | Pending |
| Firmware Updates | Determine firmware update mechanism | Pending |

## 11. Document Status

This document establishes the proposed requirements and scope of the initial platform release.

V1 focuses on integrating the Sonoff RE5V1C module with custom firmware, cloud infrastructure and a mobile application.

The platform architecture should remain extensible to accommodate additional hardware capabilities, device categories and application use cases in future releases.
