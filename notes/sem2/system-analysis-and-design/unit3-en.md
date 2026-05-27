# SYSTEM ANALYSIS AND DESIGN (SAD)

# UNIT – TOOLS OF STRUCTURED ANALYSIS

---

# Introduction to Structured Analysis

Structured Analysis is:
```text
A systematic approach used to analyze and design an information system
```

It helps developers:
- understand system requirements
- identify problems
- improve communication
- create better system designs

Structured analysis uses different:
```text
Tools and techniques
```
to represent the working of a system in a simple and organized way.

These tools help in:
- understanding data flow
- understanding processes
- identifying system structure
- simplifying complex systems

---

# Objectives of Structured Analysis Tools

1. Simplify complex systems
2. Improve system understanding
3. Enhance communication
4. Maintain proper documentation
5. Detect errors easily

---

# Main Tools of Structured Analysis

1. Logical and Physical Models
2. Context Diagram
3. Data Dictionary
4. Data Flow Diagram (DFD)
5. Form Driven Methodology
6. IPO Chart
7. HIPO Chart
8. Gantt Chart
9. System Model
10. Pseudo Code
11. Flowcharts
12. Decision Tree
13. Decision Table
14. Data Validation

---

# LOGICAL AND PHYSICAL MODELS

# Introduction

Logical and Physical Models are used to:
```text
Understand and represent the system properly
```

---

# Logical Model

Logical Model describes:
```text
What the system does
```

It focuses on:
- business activities
- data flow
- processing logic

without discussing technical implementation.

---

# Example

In a Library Management System:
- book issue
- return process
- fine calculation

are explained in the logical model.

---

# Physical Model

Physical Model describes:
```text
How the system will be implemented
```

It focuses on:
- hardware
- software
- database
- devices

used in the actual system.

---

# Example

In Library System:
- barcode scanner
- printer
- computers

are part of the physical model.

---

# Difference Between Logical and Physical Model

| Logical Model | Physical Model |
|---|---|
| Describes what system does | Describes how system works |
| Business oriented | Technical oriented |
| Abstract representation | Real implementation |

---

# CONTEXT DIAGRAM

# Introduction

Context Diagram is:
```text
The highest level Data Flow Diagram (DFD)
```

It represents:
```text
Entire system as a single process
```

---

# Purpose of Context Diagram

1. Define system boundaries
2. Identify external entities
3. Show input and output flow

---

# Components of Context Diagram

1. Process
2. External Entity
3. Data Flow

---

# Example

In ATM System:
- customer
- bank server

are external entities.

---

# Context Diagram Representation

```md
![Context Diagram](images/context-diagram.png)
```

Suggested Image Path:
```text
images/context-diagram.png
```

---

# Advantages of Context Diagram

1. Easy to understand
2. Provides overall system overview
3. Defines system boundaries clearly

---

# DATA DICTIONARY

# Introduction

Data Dictionary is:
```text
A collection of information about data elements used in a system
```

It stores:
- field names
- data types
- sizes
- meanings

---

# Example

| Field Name | Type | Size |
|---|---|---|
| Student_ID | Integer | 10 |
| Name | Text | 50 |

---

# Importance of Data Dictionary

1. Maintains data consistency
2. Improves documentation
3. Helps developers understand data structure

---

# Advantages

1. Better data management
2. Easy maintenance
3. Reduced confusion

---

# DATA FLOW DIAGRAM (DFD)

# Introduction

DFD:
```text
Represents the flow of data inside a system
```

It shows:
- input
- processing
- storage
- output

in graphical form.

---

# Components of DFD

1. Process
2. Data Flow
3. Data Store
4. External Entity

---

# 1. Process

Represents data processing activity.

---

# 2. Data Flow

Represents movement of data.

---

# 3. Data Store

Represents storage location of data.

---

# 4. External Entity

Represents external user or system.

---

# Example

In Bank System:
- customer data
- transaction processing
- database storage

are represented using DFD.

---

# DFD Representation

```md
![Data Flow Diagram](images/data-flow-diagram.png)
```

Suggested Image Path:
```text
images/data-flow-diagram.png
```

---

# Advantages of DFD

1. Easy system understanding
2. Better communication
3. Helps in analysis

---

# FORM DRIVEN METHODOLOGY

# Introduction

Form Driven Methodology means:
```text
Analyzing existing forms and documents to develop a new system
```

---

# Example

School admission forms are analyzed to develop:
```text
Admission Management System
```

---

# Advantages

1. Easy understanding of workflow
2. Easy identification of data requirements

---

# IPO CHART

# Introduction

IPO stands for:
```text
Input Process Output
```

It shows:
- input data
- processing steps
- output information

---

# Example

Student Result System:

| Input | Process | Output |
|---|---|---|
| Marks | Calculate Total | Result |

---

# Advantages of IPO Chart

1. Simple understanding
2. Better documentation
3. Easy planning

---

# HIPO CHART

# Introduction

HIPO stands for:
```text
Hierarchy plus Input Process Output
```

It represents:
- hierarchy structure
- modules
- input/process/output details

---

# Example

Online Shopping System:
- login module
- payment module
- order module

can be represented using HIPO chart.

---

# Advantages

1. Better system structure
2. Easy module understanding
3. Good documentation

---

# GANTT CHART

# Introduction

Gantt Chart is:
```text
A project scheduling chart
```

It shows:
- tasks
- start date
- end date
- project progress

---

# Example

Software Development Project:
- planning
- coding
- testing
- implementation

are represented in timeline form.

---

# Gantt Chart Representation

```md
![Gantt Chart](images/gantt-chart.png)
```

Suggested Image Path:
```text
images/gantt-chart.png
```

---

# Advantages of Gantt Chart

1. Better project management
2. Easy time tracking
3. Proper scheduling

---

# SYSTEM MODEL

# Introduction

System Model is:
```text
A simplified representation of a system
```

It helps in understanding:
- structure
- components
- working process

---

# Types of System Models

1. Logical Model
2. Physical Model
3. Mathematical Model

---

# Importance of System Model

1. Better understanding
2. Easy planning
3. Problem solving

---

# PSEUDO CODE

# Introduction

Pseudo Code is:
```text
Writing program logic using simple English statements
```

It is not an actual programming language.

---

# Example

```text
START
Input Number
If Number > 0
Print Positive
Else
Print Negative
STOP
```

---

# Advantages of Pseudo Code

1. Easy to understand
2. Program logic becomes clear
3. Coding becomes easier

---

# FLOWCHARTS

# Introduction

Flowchart is:
```text
A graphical representation of program or system logic
```

It uses symbols to represent:
- process
- decision
- flow direction

---

# Basic Symbols

| Symbol | Meaning |
|---|---|
| Oval | Start/Stop |
| Rectangle | Process |
| Diamond | Decision |
| Arrow | Flow Direction |

---

# Flowchart Representation

```md
![Flowchart Example](images/flowchart-example.png)
```

Suggested Image Path:
```text
images/flowchart-example.png
```

---

# Advantages of Flowcharts

1. Easy understanding of logic
2. Easy error detection
3. Better communication

---

# SYSTEM FLOWCHART

# Introduction

System Flowchart:
```text
Represents the complete flow of a system
```

It shows:
- input
- processing
- output
- storage

---

# Example

Bank transaction process.

---

# RUN FLOWCHART

# Introduction

Run Flowchart:
```text
Represents execution sequence of a program
```

It shows:
- modules
- execution order
- control flow

---

# DECISION TREE

# Introduction

Decision Tree is:
```text
A graphical representation of decision making process
```

It shows:
- conditions
- alternatives
- possible outcomes

---

# Example

Loan Approval System:
- salary check
- age check
- loan approval/rejection

can be represented using decision tree.

---

# Decision Tree Representation

```md
![Decision Tree](images/decision-tree.png)
```

Suggested Image Path:
```text
images/decision-tree.png
```

---

# Advantages of Decision Tree

1. Simplifies complex decisions
2. Easy understanding
3. Better analysis

---

# DECISION TABLE

# Introduction

Decision Table is:
```text
A tabular representation of conditions and actions
```

---

# Example

| Condition | Action |
|---|---|
| Marks > 40 | Pass |
| Marks < 40 | Fail |

---

# Advantages of Decision Table

1. Simplifies complex logic
2. Better documentation
3. Easy decision analysis

---

# DATA VALIDATION

# Introduction

Data Validation is:
```text
The process of checking whether input data is correct and valid or not
```

---

# Example

Age field:
```text
Negative values should not be allowed
```

---

# Types of Data Validation

1. Range Check
2. Type Check
3. Length Check
4. Format Check

---

# 1. Range Check

Checks whether value lies within fixed range.

Example:
```text
Marks should be between 0 and 100
```

---

# 2. Type Check

Checks correct data type.

Example:
```text
Age must be numeric
```

---

# 3. Length Check

Checks length of input data.

Example:
```text
Mobile number should contain 10 digits
```

---

# 4. Format Check

Checks whether data follows proper format.

Example:
```text
Email format validation
```

---

# Advantages of Data Validation

1. Reduces errors
2. Improves data accuracy
3. Improves system reliability

---

# Difference Between Decision Tree and Decision Table

| Decision Tree | Decision Table |
|---|---|
| Graphical representation | Tabular representation |
| Better visualization | Compact representation |
| Can become large and complex | Better for multiple conditions |

---

# Important Points to Remember

- Structured analysis helps in proper system analysis and design.
- Logical model describes system functions.
- Physical model describes implementation.
- Context diagram is highest level DFD.
- Data dictionary stores information about data.
- DFD represents data movement.
- IPO chart shows input-process-output relationship.
- HIPO chart represents hierarchy and module structure.
- Gantt chart helps in project scheduling.
- Pseudo code explains program logic.
- Flowcharts represent logic graphically.
- Decision tree represents decision making process.
- Data validation prevents incorrect data entry.

---

# Conclusion

Tools of Structured Analysis:
```text
Help developers analyze, understand and design systems effectively
```

These tools improve:
- planning
- communication
- documentation
- system understanding

Using structured analysis tools:
```text
Developers can create better, accurate and reliable information systems
```
