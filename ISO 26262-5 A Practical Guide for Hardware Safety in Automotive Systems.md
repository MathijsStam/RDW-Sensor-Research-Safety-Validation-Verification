ISO 26262-5: A Practical Guide for Hardware Safety in Automotive Systems



















































Document Version: 1.0
Date: November 2024
Author: Mathijs Stam

Colophon



Title: ISO 26262-5: An Accessible Guide for Hardware Safety in Automotive Applications

Author: Mathijs Stam
Organization: RDW
Date of Publication: November 14, 2024

Version: 1.0

Copyright: © RDW
All rights reserved. No part of this document may be reproduced, distributed, or transmitted in any form or by any means without the prior written permission of the publisher or author, except for brief excerpts used for educational or review purposes.

Contact Information:
For inquiries or further information, please contact:

Disclaimer:
The information provided in this document is intended for educational and informational purposes only. The author and publisher make no representations or warranties regarding the accuracy or completeness of the content, and are not responsible for any errors, omissions, or damages arising from its use.





List of abbreviations:







Glossary:





# 1. Introduction
This document serves as an accessible guide to the ISO 26262-5 standard. While the ISO standard itself is dense and technical, this guide distills the essential points, making the information more accessible and easier to understand. Key concepts, definitions, and processes have been extracted and clarified, allowing readers to grasp the foundational elements of ISO 26262-5 without needing to dive into the full standard. By combining theoretical explanations with practical examples, this document enables users to gain a clear and comprehensive understanding of the hardware safety requirements for electrical and electronic systems in automotive applications.

## 2.  Scope

This document focuses on ISO 26262-5, which addresses hardware safety requirements for automotive systems. It highlights the necessary safety assessments, design considerations, and validation steps essential for ensuring the reliability of critical components. Unlike the original ISO standard, this version distills the content into key topics and provides practical examples. Aiming to simplify the understanding and implementation of hardware safety in modern vehicles.

### 3. Structure

This document begins with a general overview of ISO 26262, providing context on the standard’s purpose and importance in ensuring the functional safety of electrical and electronic systems in the automotive industry. Following this, it introduces Automotive Safety Integrity Levels (ASILs), which are essential for classifying and managing risks within these systems.

Next, the document covers ISO 26262-5, detailing its specific scope and objectives focused on hardware-level safety. It then delves into key aspects of hardware development, beginning with hardware design requirements, which outline how to ensure that hardware components meet the necessary safety standards.

The following section addresses the evaluation of hardware architectural metrics. Afterward, the document explores methods for hardware verification and validation, essential for confirming that all safety requirements are met through severe testing.

To provide practical insight, the structure concludes with a step-by-step example illustrating how to develop a radar sensor according to ISO 26262-5. This example demonstrates the application of safety goals, hardware specifications, fault detection mechanisms, and validation testing, helping readers understand how ISO 26262-5 requirements translate into real-world tasks, ultimately supporting the creation of safer automotive systems.

5.1 ISO 26262

The ISO 26262 standard is an international standard that has been specially developed for the automotive industry, with the aim of guaranteeing the safety of all electronic systems in a vehicle. The standard was introduced in 2011 by the International Organization for Standardization (ISO), which was necessary due to the increasing complexity of vehicles.

Nowadays, cars are becoming more and more dependent on electronic systems such as driver assistance systems, power brakes, power steering and drive systems. These developments offer a lot of advantages, but they also increase the risk of possible dangerous malfunctions in these electrical systems. ISO 26262 provides a structured approach to identify and manage these risks, better ensuring the safety of the driver and other road users.

The standard arose from the need to improve the reliability and safety of vehicles. In the past, cars were mainly mechanical, nowadays almost everything in a car depends on electronics and software. A malfunction in one of these systems can have major consequences, such as uncontrollable acceleration or failing brakes. It was therefore essential to develop a standard that helps manufacturers design, test, and validate safe electrical systems.

5.2 ISO 26262 Classification 
ISO 26262 is made up of 12 parts, each of which deals with a specific phase or aspect of the development process. Each part helps to ensure the safety of vehicles in a structured way, from initial design to scrapping.

5.2.1 Part 1: Vocabulary
The first part of ISO 26262 provides a comprehensive glossary of definitions of terms used in the standard. The aim is to create a clear language within the automotive industry that everyone, from designers to suppliers, can understand. This improves communication and prevents misunderstandings during the implementation of the standard.

5.2.2 Part 2: Functional Safety Management 
This section focuses on how functional safety is managed within the development process of a system. It mentions how organizations can follow a structural approach to ensure safety, with attention to planning, risk management and the allocation of responsible persons or parties. One of these requirements is the appointment of a functional safety manager, who is responsible for overseeing the safety processes and maintaining the necessary documentation. This documentation must be audited by an independent party to comply with the standard.

5.2.3 Part 3: Concept phase 
Part 3 is about designing and developing vehicles and systems. In this phase of the project, the focus is on determining what exactly needs to be developed. An important part of this is the Hazard Analysis and Risk Assessment (HARA). During this analysis, possible hazards due to system failures are identified and assessed. Based on these findings, safety objectives are formulated, with each objective being assigned an ASIL. This ASIL classification ranges from A (low risk) to D (high risk), depending on how serious the consequences of a failure could be.



5.2.4 Part 4: System-level product development 
This part focuses on designing safe systems by defining safety requirements. It builds on the functional safety goals previously defined in Part 3. Based on these, specific technical requirements are defined. Safety mechanisms are also developed that can detect and resolve errors in the system. This process ensures that both software and hardware meet the stated safety goals, so that the entire system can operate reliably and safely.

5.2.5 Part 5: Hardware-Level Product Development 
Part 5 focuses specifically on hardware system development. It discusses the requirements that hardware components must meet to ensure system safety. This part covers topics such as defining hardware safety requirements, hardware design, and assessing measurable requirements. It also looks at the risk of unexpected hardware failures and how these can affect the functional safety of the system.

5.2.6 Part 6: Software-Level Product Development 
This part covers the development requirements for software. As with hardware in Part 5, the software requirements are developed based on the safety requirements. It focuses on designing reliable and safe software through rigorous testing, validation, and verification. Integrating safety mechanisms to identify and control software errors is also an important part of this part.

5.2.7 Part 7: Production, operation, maintenance and dismantling 
This part discusses how the functional safety of a system is ensured during production and throughout the entire life cycle of the vehicle, from use and maintenance to dismantling. Planning the production process and identifying possible defects is also of great importance. In addition, regular evaluations and checks are necessary to ensure functional safety.

5.2.8 Part 8: Supporting processes 
Part 8 covers various supporting processes that are important for the safe development of a system according to ISO 26262. Topics such as verification and validation, and risk management are covered. This part helps to control unexpected situations during the development process.



5.2.9 Part 9: ASIL-oriented and safety-oriented analyses 
This part discusses the different methods and techniques that can be used to perform safety analyses during the production process. Safety analyses are necessary to gain insight into the possible failures that can occur during the use of the system and the consequences of these failures. Part 9 provides guidelines for performing these analyses alongside the development process, so that safety problems are recognized and solved in a timely manner.

5.2.10 Part 10: Guidelines for the use of the standard 
Part 10 provides an overview of the application of the standard and gives developers an insight into the key processes and procedures. This part provides guidelines for the application of the procedures discussed earlier. It provides information on how the ISO 26262 standard can be applied in the development process of a vehicle.

5.2.11 Part 11: Application of ISO 26262 to semiconductors 
Since semiconductors have different requirements than other systems, this part is intended for the application of ISO 26262 to semiconductors. It focuses on the specific safety requirements relevant to semiconductor components and their function within automotive electrical and electronic systems.

5.2.12 Part 12: Specific requirements for motorcycles 
This last part of ISO 26262 describes the safety requirements for motorcycles, as these differ from the requirements for other vehicles. This part contains guidelines and procedures for developing safe electronic and electrical systems specifically for motorcycles.

Together, these parts cover the entire life cycle of a product, from initial design to production, maintenance and even disassembly.





5.3 ISO 26262 V-model

An important part of ISO 26262 is the V-model, which is widely used in the development of systems that are of great importance for safety. This model offers a structured approach where design and verification go hand in hand.

The V-model gets its name from the shape the process takes. The left part of the V describes the phases in which the system requirements are established. Here the safety goals are set and converted into technical requirements for the different parts of the vehicle, such as system, hardware and software.

The right side of the V focuses on the verification and validation stages. Each step in the design process on the left side has a corresponding test or verification step on the right side. This means that once a part of the system has been designed, it is tested on the other side of the V to ensure that it meets the stated requirements.

For example, once the functional safety requirements for a steering assistance system have been defined (left side of the V), they are tested and validated later in the process through simulations, tests and analyses (right side of the V).

The V-model ensures that every aspect of the system is thoroughly tested and validated, preventing safety issues. This makes it a valuable tool within ISO 26262 for the development of complex electronic and software-controlled vehicle systems.



6. Automotive Safety Integrity Level (ASIL)

ASIL (Automotive Safety Integrity Level) is a classification system within the ISO 26262 standard for safety in the automotive industry. It assesses the risks of defects in electronic systems in vehicles. ASIL determines how strict the safety measures must be based on the severity of possible accidents, how often dangerous situations can occur and how well they can be controlled. As a result, ASIL helps manufacturers to take the right safety measures and thus reduce the risk of accidents.

6.1 Determining an ASIL

To assign an ASIL value to a system, three factors must be taken into account: 

Severity : Severity refers to how severe the injuries or damage would be if a hazardous event occurred. Suppose the braking system of a car fails. If this happens on the highway at high speed, it could be life-threatening for both the occupants and other road users. The severity would therefore be extremely high, because it could lead to serious injuries or fatal accidents. 
There are four categories:

S0: No injuries

S1: Mild to moderate injuries

S2: Serious to life-threatening injuries (survival likely)

S3: Life-threatening (survival uncertain) to fatal injuries

Exposure : Exposure looks at how often a situation occurs in which that hazard could occur. For example, suppose the brake system only fails under certain conditions, such as wet weather or during a specific speed range. If those conditions occur rarely, exposure is low. But if the problem could occur on any ride, exposure is high. 
Again, there are five categories:

E0: Very unlikely

E1: Very low probability

E2: Low probability

E3: Average probability

E4: High probability (injury can occur under most operating conditions)

Controllability : Controllability is about how well the driver or the system itself can react to prevent an accident. For example, if the brakes no longer work, but the driver can still safely stop the car by using the handbrake, for example, controllability is high. But if there is no way to stop the car, controllability is low. 
There are four categories here:

C0: Generally verifiable

C1: Easy to operate

C2: Normally controllable (most drivers can act to avoid injury)

C3: Difficult to control or uncontrollable



(Kochanthara et al., 2021)



6.2 Choosing an ASIL

The table below shows the method for determining the ASIL classification based on the three factors: Severity , Exposure and Controllability .

Each combination of these factors results in a specific ASIL value, which is shown in the color-coded table. The ASIL values range from QM ( Quality Management ), which indicates that no formal safety measures are required according to ISO 26262, to ASIL D , the highest safety level where strict measures are required. The ASIL is chosen based on the worst-case combination of severity, exposure and controllability.

Green boxes represent QM , while the colored boxes from yellow to red indicate ASIL levels A to D. Red is the highest ASIL level, assigned when there are high impacts, common exposures and low controllability.





6.3 ASIL classification examples







ASIL D: Systems such as the airbag and the anti-lock braking system (ABS) fall into this category, because failures here can lead to life-threatening situations, such as unexpected airbag deployment or loss of full braking power at a key moment.

ASIL C to D: Engine management and Adaptive Cruise Control belong here, due to the risks of unwanted acceleration or braking, which can cause major safety problems.

ASIL B: Problems with the instrument cluster or headlights are less serious, but can still be dangerous, for example due to the loss of important information or lighting.

ASIL A : Rear lights have a lower risk, as the failure of both lights reduces visibility but does not immediately lead to serious accidents.



7. ISO 26262-5

7.1 Scope ISO 26262-5 
The scope of ISO 26262-5 focuses on the hardware side of safety-related electrical and electronic systems (E/E-systems) in series-produced vehicles, excluding mopeds. This part of the standard provides guidance on functional safety and helps companies to incorporate safety measures into their development processes.

The document deals with the possible risks that arise from the failure of E/E systems at hardware level and the interaction between these systems. However, it does not focus on hazards such as electric shock, fire or smoke and similar hazards. unless these are directly caused by failures in the E/E systems.

ISO 26262-5 provides clear guidelines for developing hardware, such as how to establish safety requirements, design hardware and check whether the hardware is reliable in the event of unexpected failures. In addition, the standard describes how to ensure that safety objectives are achieved by properly integrating and testing the hardware.



7.2 Main objectives of ISO 26262-5 
Part 5 of the ISO 26262 standard focuses on hardware development and explains how to make hardware, such as sensors in autonomous vehicles, safe. This is important because these sensors collect crucial data for decisions during driving. The main topics are:

7.2.1 Specification of hardware security requirements (Chapter 6):

This explains how to derive safety requirements for hardware from the technical safety plan of the vehicle. It also explains how safety mechanisms work

Safety mechanisms 
Safety mechanisms are systems or functions that ensure that a vehicle continues to operate safely, even if faults occur. They are important for the safety of electrical and electronic systems in cars.

Detection : They can detect errors or problems, such as when a sensor gives an incorrect measurement. This can be done by self-diagnosis or by using additional, redundant systems.

Control : Once a problem is discovered, the safety mechanism ensures that the system enters a safe state. This means, for example, that a faulty system can be shut down or that it can switch to a safe mode.

Prevention : Some mechanisms are designed to prevent errors in the first place, for example by ensuring that important parts in the system are duplicated (such as two sensors measuring the same thing).



7.2.2 Hardware Design (Chapter 7):

The hardware design must meet the required safety requirements. For sensors this means that they must work reliably, even in harsh conditions such as heat, vibrations or interfering signals.

This chapter emphasizes that a simple hardware structure is important. For sensors, this means that their design should be easy to test and maintain, and that errors can be easily found.



These topics show which aspects are important for safe and secure hardware. For Each ASIL level (A, B, C, and D) it is indicated to what extent each aspect is recommended.

Tabel 3: Meaning [ ++] [+] [o]



This table describes security analysis methods used in hardware development and validation. The two primary methods are:

Deductive Analysis - This is a top-down approach where potential failure events are analyzed to derive possible causes. Techniques such as Fault Tree Analysis (FTA) fall under this.

ASIL A : Not necessary (indicated by "o").

ASIL B to D : Recommended with increasing intensity (++ for D means high need).

Inductive Analysis - This is a bottom-up approach where potential failures are analyzed at the component level to see how they might affect the system. FMEA (Failure Modes and Effects Analysis) is a example of an inductive method.

ASIL A to D : Highly recommended all levels (++ for all ASIL levels).

This table lists the verification methods that are intended to ensure that the hardware design meets the safety requirements. Walk- throughs and inspections help detect design flaws early, while simulation and prototyping allow testing under realistic conditions.

7.2.3 Evaluation of hardware architectural metrics (Chapter 8):

This section looks at whether the hardware architecture is secure enough. Two important measurement methods are the Single-Point Fault Metric (SPFM) and the Latent Fault Metric (LFM) .

SPFM measures the probability that a single failure in the system will lead directly to a hazardous situation, without a mechanism to detect or correct this failure. The goal is to minimize the occurrence of such failures as much as possible in order to achieve the stated safety requirements.

These percentages indicate the degree to which the system must be protected against single-point failures (errors that could lead directly to danger without any error detection mechanism intervening) per assigned ASIL.

LFM looks at errors in a system that initially go unnoticed and do not pose an immediate danger at that time. However, if a second error occurs later, these errors together can cause problems. It is therefore important that these types of errors are detected in time, so that they do not lead to unsafe situations in the long term. Although the first error may not be immediately dangerous, it can have serious consequences over time if nothing is done about it.



7.2.4 Safety goals and random hardware faults (Chapter 9):

This chapter is about preventing random errors in the hardware from leading to dangerous situations. For sensors this means that the design must ensure that errors such as incorrect or missing measurements are limited as much as possible, because this can lead to dangerous situations. To ensure the safety of systems, the FIT rate ( Failures In Time) is used ,

ASIL D is the most stringent level. At ASIL D, a maximum of one failure per 100 million hours may occur ( failures per hour).

ASIL C allows a maximum of one failure per 10 million hours ( failures per hour).

ASIL B has the same failure requirement as ASIL C ( failures per hour).



### 3.2.5 Hardware integration and verification (Chapter 10):

This part focuses on integrating the hardware, such as sensors, into the system and verifying that they meet safety standards. Methods such as testing and simulation are essential to verify that the sensors function properly and can detect faults before they are built in.

This table describes methods for setting up test cases that are required for hardware integration testing. These test cases help to ensure that the hardware meets security requirements. The methods in this table focus on testing different aspects of the hardware.

This table provides methods to verify that the hardware implementation meets the security requirements. The focus is on testing the correct operation of the hardware, error detection and protection against malfunctions.

Functional testing: Verifies that the hardware is performing according to specifications under operating conditions.

Fault injection testing: Simulates failures to see how the hardware responds and whether faults are correctly detected and managed.

Electrical testing: Verifies that the hardware meets electrical specifications, such as voltage and signal integrity.





Table 10: Hardware Integration Tests - Durability, Robustness, and Operation Under Stress

This table covers methods to test the hardware for durability and reliability under harsh conditions. The methods focus on verifying that the hardware can withstand a variety of environmental and operational challenges.

8. Safety-oriented Design and Validation of a Radar Sensor according to ISO 26262

Below is an example of the development procedure of a radar sensor according to ISO 26262. Here the process is taken from determining safety goals to verifying the final hardware.

Note: These are not real specifications or requirements; they are provided only as an example.

Step 1: Determine the Safety Goals  ISO 26262- Part 3

Example of safety goals:

Detecting objects within a certain range (for example 200 meters).

Accurate measurement of the distance and speed of objects with minimal margin of error.

Fast response time to identify rapidly changing traffic situations.

Step 2: Safety Requirements​  ISO 26262- Part 4

Functional and technical safety requirements are drawn up on the basis of the safety objectives.

Functional Safety Requirements

Functional safety requirement define the necessary behaviors for the sensor to ensure overall safety in operation and meet the safety goals.

Examples of functional safety requirements:

Error detection: The sensor must be able to detect errors in distance measurement within 0.1 seconds.

Signal processing: The sensor must send and receive a signal every 50 milliseconds.

Interference Management: The sensor must be able to handle interference from other radar systems in nearby vehicles.

Technical Safety Requirements

These are more detailed requirements that determine how the sensor must meet the functional requirements.

Examples of technical safety requirements:

Accuracy: The system must be able to measure the distance to an object with an accuracy of 1 meter at a distance of 200 meters.

Processing capacity: The sensor must have sufficient processing capacity to distinguish objects on the road (for example, a minimum of 5 objects within range).

Redundancy: For important safety functions, there should be duplicate sensors so that if one sensor fails, the other will still work.



Step 3: Hardware Design Specifications ISO 26262- Part 5

The hardware design specifications describe how the radar sensor will be constructed and what components are needed to meet safety requirements.

Examples of hardware design specifications:

Signal Processor : A signal processor that can process received signals in real time to calculate distance and speed.

Microcontroller : A robust microcontroller with built-in error checking to process the data from the radar antennas and forward it to the ADAS/ADS system.

Temperature Control : Since the sensor is mounted on the outside of the vehicle, it must be able to withstand extreme temperatures ( for example: from -40°C to 85°C).

Step 4: Error detection and management ISO 26262- Part 5

In ISO 26262-5 a strategy must be developed to detect and control possible errors in the system.

Examples of fault detection and management for the radar sensor:

Self-Diagnosis : The sensor should perform periodic self-tests to verify that all antennas and signal processing are working properly.

Warnings : If the radar sensor fails or provides abnormal data, the system must provide a warning to the ADAS system to inform the driver.

Fail -safe mode : In the event of serious errors, the sensor can switch itself to a safe mode, in which the ADAS system automatically distances itself from the vehicle in front.

Step 5: Hardware Metrics ISO 26262- Part 5

ISO 26262 requires that the probability of failure be assessed to ensure that the hardware is safe. The following methods are used for this:

FIT rate (Failure In Time)

LFM (Latent Fault Metric ):

SPFM (Single-Point Fault Metric)



Step 6: Hardware Verification and Validation ISO 26262- Part 5

After designing and building the radar sensor, we must perform thorough testing to verify that it meets the stated safety requirements.

Examples of verification and validation tests:

Fault injection testing : Introducing artificial faults to test whether fault detection is working correctly.

Environmental Simulations : Test the radar sensor in different weather conditions (rain, fog, snow) to ensure the reliability of object detection.

Interference Check : Testing whether the sensor functions properly in situations where there may be interference from other radar systems.

Temperature fluctuations : Testing whether the radar sensor can withstand extreme temperatures and temperature fluctuations without affecting the measurements.

This example shows how to develop a safe radar sensor using ISO 26262-5 step by step, including defining safety goals, functional and technical requirements, hardware specifications, fault management, reliability calculations, and finally verification. Following these guidelines ensures that the radar sensor is reliable and safe for use in a vehicle, which promotes the safety of the driver, occupants and other road users.

9. Contributing to the functional safety of sensors:

Error detection safety mechanisms: Sensor mechanisms must be able to detect and correct both internal (within the sensor) and external (such as communication problems) errors.

Diagnostic coverage: The standard sets strict requirements for fault detection, especially for sensors with a high ASIL value (ASIL D) in autonomous vehicles. These sensors must be able to quickly recognize and correct problems so that they do not lead to dangerous situations.

Environmental Conditions: Sensor design must be robust and able to operate in a variety of conditions, such as vibration, extreme temperatures, and electromagnetic fields that can cause interference, which are common in autonomous vehicles.

Relevance for autonomous vehicles:

Autonomous vehicles rely heavily on sensors (such as cameras, LIDAR, radar, and ultrasonic sensors) to drive safely. Part 5 of the ISO 26262 standard ensures that these sensors:

Continue working reliably, even under different conditions.

Have mechanisms to detect and respond to errors.

Comply with strict safety standards to minimize the risk of accidents caused by defective sensors.

In summary, ISO 26262-5 ensures that sensors in autonomous vehicles operate safely and reliably by imposing strict requirements on design, fault detection and testing. This contributes to the functional safety of these vehicles.







Bibliography



International Organization for Standardization. (2018). ISO 26262: Road vehicles – Functional safety: Part 1: Vocabulary (ISO 26262-1:2018). ISO.

International Organization for Standardization. (2018). ISO 26262: Road vehicles – Functional safety: Part 2: Management of functional safety (ISO 26262-2:2018). ISO.

International Organization for Standardization. (2018). ISO 26262: Road vehicles – Functional safety: Part 3: Concept phase (ISO 26262-3:2018). ISO.

International Organization for Standardization. (2018). ISO 26262: Road vehicles – Functional safety: Part 4: System development (ISO 26262-4:2018). ISO.

International Organization for Standardization. (2018). ISO 26262: Road vehicles – Functional safety: Part 5: Hardware development (ISO 26262-5:2018). ISO.

International Organization for Standardization. (2018). ISO 26262: Road vehicles – Functional safety: Part 6: Software development (ISO 26262-6:2018). ISO.

International Organization for Standardization. (2018). ISO 26262: Road vehicles – Functional safety: Part 7: Production and operation (ISO 26262-7:2018). ISO.

International Organization for Standardization. (2018). ISO 26262: Road vehicles – Functional safety: Part 8: Supporting processes (ISO 26262-8:2018). ISO.

International Organization for Standardization. (2018). ISO 26262: Road vehicles – Functional safety: Part 9: Functional safety management (ISO 26262-9:2018). ISO.

International Organization for Standardization. (2018). ISO 26262: Road vehicles – Functional safety: Part 10: Concept of the assessment of functional safety (ISO 26262-10:2018). ISO.

International Organization for Standardization. (2018). ISO 26262: Road vehicles – Functional safety: Part 11: Guidelines on application of ISO 26262 to semiconductors (ISO 26262-11:2018). ISO.

International Organization for Standardization. (2018). ISO 26262: Road vehicles – Functional safety: Part 12: Adaptation of ISO 26262 for motorcycles (ISO 26262-12:2018). ISO.

Kochanthara, S., Rood, N., Saberi, A. K., Cleophas, L., Dajsuren, Y., & Van Den Brand, M. (2021). A functional safety assessment method for cooperative automotive architecture. Journal of Systems and Software, 179, 110991.

Mao, L. (2022, April 8). Functional Safety decomposition [Image]. Lei Mao’s Log Book.
