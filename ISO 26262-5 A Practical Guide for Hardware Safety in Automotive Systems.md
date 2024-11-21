# ISO 26262-5: A Practical Guide for Hardware Safety in Automotive Systems

**Version:** 1.0  
**Date:** November 2024  
**Author:** Mathijs Stam  

---

## 1. Introduction

This document serves as an accessible guide to the ISO 26262-5 standard. While the ISO standard itself is dense and technical, this guide distills the essential points, making the information more accessible and easier to understand. Key concepts, definitions, and processes have been extracted and clarified, allowing readers to grasp the foundational elements of ISO 26262-5 without needing to dive into the full standard. By combining theoretical explanations with practical examples, this document enables users to gain a clear and comprehensive understanding of the hardware safety requirements for electrical and electronic systems in automotive applications.

---

## 2. Scope

This document focuses on ISO 26262-5, which addresses hardware safety requirements for automotive systems. It highlights the necessary safety assessments, design considerations, and validation steps essential for ensuring the reliability of critical components. Unlike the original ISO standard, this version distills the content into key topics and provides practical examples, aiming to simplify the understanding and implementation of hardware safety in modern vehicles.

---

## 3. Structure

This document begins with a general overview of ISO 26262, providing context on the standard’s purpose and importance in ensuring the functional safety of electrical and electronic systems in the automotive industry. Following this, it introduces Automotive Safety Integrity Levels (ASILs), which are essential for classifying and managing risks within these systems.

Next, the document covers ISO 26262-5, detailing its specific scope and objectives focused on hardware-level safety. It then delves into key aspects of hardware development, beginning with hardware design requirements, which outline how to ensure that hardware components meet the necessary safety standards.

The following section addresses the evaluation of hardware architectural metrics. Afterward, the document explores methods for hardware verification and validation, essential for confirming that all safety requirements are met through severe testing.

To provide practical insight, the structure concludes with a step-by-step example illustrating how to develop a radar sensor according to ISO 26262-5. This example demonstrates the application of safety goals, hardware specifications, fault detection mechanisms, and validation testing, helping readers understand how ISO 26262-5 requirements translate into real-world tasks, ultimately supporting the creation of safer automotive systems.

---

## 4. Knowledge-Base

To improve accessibility and usability, the content from this document will be integrated into an internal WIKI-database for RDW currently under development. This will include further information on sensors for autonomous vehicles that contribute to safety, along with other relevant standards.

---

## 5. ISO 26262

### 5.1 Overview of ISO 26262

ISO 26262 is an international standard specifically developed for the automotive industry to guarantee the safety of all electronic systems in a vehicle. The standard provides a structured approach to identifying and managing risks, ensuring the safety of the driver and other road users.

The standard consists of 12 parts:

#### 5.2 ISO 26262 Classification

| **Part**    | **Description**                                                                                                                                                  |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Part 1**  | Vocabulary: Glossary of terms used in the standard.                                                                                                              |
| **Part 2**  | Functional Safety Management: Structural approach to safety planning and risk management.                                                                        |
| **Part 3**  | Concept Phase: Hazard Analysis and Risk Assessment (HARA) with ASIL classification.                                                                              |
| **Part 4**  | System-Level Product Development: Defines safety requirements and mechanisms for both software and hardware systems.                                             |
| **Part 5**  | Hardware-Level Product Development: Focuses on hardware safety requirements, risk assessments, and design considerations.                                         |
| **Part 6**  | Software-Level Product Development: Addresses safe and reliable software design through rigorous validation and verification.                                     |
| **Part 7**  | Production, Operation, Maintenance, and Dismantling: Covers safety during production and the system's lifecycle.                                                 |
| **Part 8**  | Supporting Processes: Addresses verification, validation, and risk management for unexpected situations.                                                         |
| **Part 9**  | ASIL-Oriented and Safety-Oriented Analyses: Safety analysis techniques to recognize and address potential failures.                                               |
| **Part 10** | Guidelines for the Use of the Standard: Overview of the processes discussed earlier, with guidelines for applying the standard.                                  |
| **Part 11** | Application to Semiconductors: Guidelines for semiconductor-specific safety requirements.                                                                        |
| **Part 12** | Specific Requirements for Motorcycles: Tailored safety requirements for motorcycles.                                                                             |

---

## 6. Automotive Safety Integrity Level (ASIL)

### 6.1 Determining an ASIL

ASIL is based on three factors:

| **Factor**          | **Description**                                                                                                                       | **Categories**                                                                                                                                     |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| **Severity (S)**    | Assesses the impact of injuries or damages.                                                                                          | S0 (No injuries) to S3 (Life-threatening or fatal injuries).                                                                                       |
| **Exposure (E)**    | Evaluates how often the hazard could occur.                                                                                          | E0 (Very unlikely) to E4 (High probability).                                                                                                       |
| **Controllability (C)** | Measures the ability to avoid the hazard.                                                                                          | C0 (Generally controllable) to C3 (Difficult or uncontrollable).                                                                                   |

### 6.2 ASIL Levels

| **ASIL Level** | **Description**                                                                                      |
|----------------|------------------------------------------------------------------------------------------------------|
| **QM**         | Quality Management: No formal safety measures required.                                             |
| **ASIL A**     | Lowest safety integrity level, moderate risk.                                                       |
| **ASIL D**     | Highest safety integrity level, where strict measures are required.                                  |

---

## 7. ISO 26262-5: Hardware-Level Product Development

### 7.1 Scope  

Focuses on hardware safety for electrical/electronic systems, excluding mopeds. Provides guidelines for safety requirements, hardware design, and reliability testing.

---

### 7.2 Figures

#### V-Model Development Process
![V-Model Development Process](relative/path/to/v-model.png)

#### ASIL Classification Table
![ASIL Table](relative/path/to/asil-table.png)

---

## 8. Safety-Oriented Design and Validation of a Radar Sensor

### Example Steps  
1. **Determine Safety Goals**  
   Example: Detect objects within 200 meters with a minimal margin of error.  
2. **Define Hardware Design Specifications**  
   Example: Ensure the microcontroller can withstand temperatures from -40°C to 85°C.  
3. **Implement Error Detection**  
   Example: Include self-diagnosis and fail-safe modes.  
4. **Verification and Validation**  
   Example: Conduct fault injection testing and environmental simulations.

---

## Bibliography

1. **ISO Standards**:  
   - International Organization for Standardization. (2018). ISO 26262: Road vehicles – Functional safety.  
2. **Academic References**:  
   - Kochanthara, S., et al. (2021). A functional safety assessment method. [Journal Link](https://doi.org/10.1016/j.jss.2021.110991)  
3. **Diagrams & Images**:  
   - Mao, L. (2022). Functional Safety Decomposition. [Lei Mao’s Log Book](https://leimao.github.io/blog/Functional-Safety-Decomposition/)
