# MediCare Hospital Patient Admission System

**Module:** PROG6112  
**Student Number:** ST10476298  
**Institution:** IIE Varsity College

## Project Overview
MediCare Hospital is replacing its paper-based patient admission process with this console-based Java application. This system allows administrative staff to manage patient records and hospital bed allocations efficiently. 

This project demonstrates the application of Object-Oriented Programming (OOP) principles, including encapsulation, inheritance, polymorphism, array management, and unit testing.

## Features Implemented

### 1. Patient Management
* **Registration:** Captures patient details (ID, Name, Age, Gender, Medical Condition).
* **Validation:** Prevents the registration of duplicate Patient IDs.
* **Search & Delete:** Allows staff to find and safely remove patient records.

### 2. Bed Management (2D Arrays)
* **Ward Layout:** Simulates a 20-bed hospital ward using a `4 x 5` Two-Dimensional Array.
* **Allocation:** Assigns available beds exclusively to `Inpatient` categories. Prevents allocation if the ward is at 100% capacity.
* **Release:** Frees up beds when patients are discharged or deleted.
* **Visual Display:** Prints a visual grid showing available `[ ]` and occupied `[X]` beds.

### 3. Patient Categories (Inheritance & OOP)
* **Base Class:** Utilizes a `Patient` superclass with fully encapsulated attributes.
* **Subclass:** Contains an `Inpatient` class that extends `Patient` using `super()` for constructor chaining.
* **Method Overriding:** Overrides the `displayDetails()` method to include ward and bed tracking.
* **Enums:** Uses a `PatientCategory` enum (INPATIENT, OUTPATIENT, EMERGENCY).

### 4. Reports & Sorting
* Generates real-time statistics including total registered patients, available beds, and overall ward occupancy percentage.
* Sorts the patient registry alphabetically by surname.

### 5. Unit Testing (JUnit 5)
Comprehensive automated testing ensures system reliability. Tests include:
* Successful patient registration and duplicate ID prevention.
* Successful bed allocation and release.
* Boundary testing (preventing bed allocation when all 20 beds are occupied).

## Project Structure
```text
MediCareSystem/
│
├── Main.java                 # Entry point and Console UI
├── PatientCategory.java      # Enum for patient types
├── Patient.java              # Superclass
├── Inpatient.java            # Subclass extending Patient
├── HospitalManager.java      # Core logic and 2D Array management
├── HospitalManagerTest.java  # JUnit 5 Unit Tests
└── README.md                 # Project documentation