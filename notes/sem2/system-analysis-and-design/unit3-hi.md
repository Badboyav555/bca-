# SYSTEM ANALYSIS AND DESIGN (SAD)

# UNIT – TOOLS OF STRUCTURED ANALYSIS

---

# Introduction to Structured Analysis

Structured Analysis:
```text
Ek systematic method hai jisse kisi system ko analyze aur design kiya jata hai
```

Iska main purpose hota hai:
- system ko properly samajhna
- problems identify karna
- better solution develop karna

Structured analysis mein different:
```text
Tools aur techniques
```
use hoti hain jo system ko easily explain karti hain.

Ye tools help karte hain:
- data flow samajhne mein
- system structure dekhne mein
- processing identify karne mein
- decisions analyze karne mein

---

# Objectives of Structured Analysis Tools

1. Complex system ko simple banana
2. Better understanding provide karna
3. Communication improve karna
4. Documentation maintain karna
5. Error detection easy banana

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
10. Pseudo Codes
11. Flow Charts
12. Decision Tree
13. Decision Table
14. Data Validation

---

# LOGICAL AND PHYSICAL MODELS

# Introduction

System ko samajhne ke liye:
```text
Logical aur Physical Models
```
use kiye jate hain.

---

# Logical Model

Logical Model explain karta hai:
```text
System kya karta hai
```

Ye mainly:
- business process
- data flow
- functions

par focus karta hai.

---

# Real Life Example

Library Management System:
- book issue
- book return
- fine calculation

Logical model explain karega:
```text
Ye kaam kaise perform hote hain
```

---

# Physical Model

Physical Model explain karta hai:
```text
System practically kaise implement hoga
```

Ye focus karta hai:
- hardware
- software
- database
- devices

par.

---

# Example

Library system mein:
- barcode scanner
- printer
- computers

Physical model ka part hain.

---

# Difference Between Logical and Physical Model

| Logical Model | Physical Model |
|---|---|
| System kya karta hai | System kaise implement hoga |
| Business oriented | Technical oriented |
| Abstract view | Real implementation |

---

# CONTEXT DIAGRAM

# Introduction

Context Diagram:
```text
Highest level DFD
```
hota hai.

Ye:
```text
Pure system ko ek single process ke form mein represent karta hai
```

---

# Purpose of Context Diagram

1. System boundary define karna
2. External entities identify karna
3. Inputs aur outputs show karna

---

# Components

1. System Process
2. External Entity
3. Data Flow

---

# Real Life Example

ATM System mein:
- Customer
- Bank Server

external entities hain.

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

# Advantages

1. Easy understanding
2. Simple overview
3. System boundary clear hoti hai

---

# DATA DICTIONARY

# Introduction

Data Dictionary:
```text
Data elements ki information ka collection
```
hota hai.

Ye:
- field names
- data types
- sizes
- meanings

store karta hai.

---

# Example

| Field Name | Type | Size |
|---|---|---|
| Student_ID | Integer | 10 |
| Name | Text | 50 |

---

# Importance

1. Data consistency maintain karta hai
2. Documentation improve karta hai
3. Developers ko help karta hai

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
System mein data ka flow show karta hai
```

Ye represent karta hai:
- input
- processing
- storage
- output

---

# Components of DFD

1. Process
2. Data Flow
3. Data Store
4. External Entity

---

# 1. Process

Data processing activity show karta hai.

---

# 2. Data Flow

Data movement show karta hai.

---

# 3. Data Store

Data storage location show karta hai.

---

# 4. External Entity

Outside user/system represent karta hai.

---

# Real Life Example

Bank System:
- customer input
- transaction processing
- database storage

DFD mein show hote hain.

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

Form Driven Methodology:
```text
Existing forms aur documents ko analyze karke system develop karna
```
hai.

---

# Example

School admission forms ko analyze karke:
```text
Admission Management System
```
develop karna.

---

# Advantages

1. Existing workflow samajhna easy
2. Data requirements identify karna easy

---

# IPO CHART

# Introduction

IPO ka full form:
```text
Input Process Output
```
hai.

Ye:
- input
- processing
- output

show karta hai.

---

# Example

Student Result System:

| Input | Process | Output |
|---|---|---|
| Marks | Calculate Total | Result |

---

# Advantages

1. Easy understanding
2. Better documentation
3. Simple planning

---

# HIPO CHART

# Introduction

HIPO ka full form:
```text
Hierarchy plus Input Process Output
```
hai.

Ye:
- hierarchy structure
- modules
- input/process/output

show karta hai.

---

# Example

Online Shopping System:
- login module
- payment module
- order module

HIPO chart mein show hote hain.

---

# Advantages

1. Better system structure
2. Easy module understanding
3. Good documentation

---

# GANTT CHART

# Introduction

Gantt Chart:
```text
Project scheduling chart
```
hai.

Ye show karta hai:
- tasks
- starting date
- ending date
- project progress

---

# Real Life Example

Software Development Project:
- planning
- coding
- testing
- implementation

timeline ke form mein show hote hain.

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

# Advantages

1. Time management easy
2. Project tracking possible
3. Better scheduling

---

# SYSTEM MODEL

# Introduction

System Model:
```text
System ka simplified representation
```
hota hai.

Ye:
- structure
- working
- components

show karta hai.

---

# Types of System Models

1. Logical Model
2. Physical Model
3. Mathematical Model

---

# Importance

1. Better understanding
2. Easy planning
3. Problem solving

---

# PSEUDO CODES

# Introduction

Pseudo Code:
```text
Programming logic ko simple English statements mein likhna
```
hai.

Ye actual programming language nahi hoti.

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

# Advantages

1. Easy to understand
2. Logic clear hota hai
3. Coding easy hoti hai

---

# FLOW CHARTS

# Introduction

Flowchart:
```text
Program ya system logic ka graphical representation
```
hota hai.

Ye symbols use karke:
- process
- decisions
- flow direction

show karta hai.

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

# Advantages

1. Logic easy samajh aata hai
2. Error detection easy hoti hai
3. Better communication

---

# SYSTEM FLOW CHART

# Introduction

System Flowchart:
```text
Complete system ka flow
```
show karta hai.

Ye include karta hai:
- input
- process
- output
- storage

---

# Example

Bank transaction process flow.

---

# RUN FLOW CHART

# Introduction

Run Flowchart:
```text
Program execution sequence
```
show karta hai.

Ye:
- modules
- execution order
- control flow

represent karta hai.

---

# DECISION TREE

# Introduction

Decision Tree:
```text
Decision making process ka graphical representation
```
hai.

Ye:
- conditions
- alternatives
- possible results

show karta hai.

---

# Real Life Example

Loan Approval System:
- salary check
- age check
- approval/rejection

Decision tree se represent kiya ja sakta hai.

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

# Advantages

1. Complex decisions simplify karta hai
2. Better understanding
3. Easy analysis

---

# DECISION TABLE

# Introduction

Decision Table:
```text
Conditions aur actions ko table form mein represent karna
```
hai.

---

# Example

| Condition | Action |
|---|---|
| Marks > 40 | Pass |
| Marks < 40 | Fail |

---

# Advantages

1. Complex logic simplify karta hai
2. Better documentation
3. Easy decision analysis

---

# DATA VALIDATION

# Introduction

Data Validation:
```text
Input data ko check karna ki wo correct aur valid hai ya nahi
```
hai.

---

# Real Life Example

Age field:
```text
Negative value allow nahi honi chahiye
```

---

# Types of Validation

1. Range Check
2. Type Check
3. Length Check
4. Format Check

---

# 1. Range Check

Value fixed range mein honi chahiye.

Example:
```text
Marks 0 se 100 ke beech hone chahiye
```

---

# 2. Type Check

Correct data type required hota hai.

Example:
```text
Age numeric honi chahiye
```

---

# 3. Length Check

Input length check hoti hai.

Example:
```text
Mobile number 10 digits ka hona chahiye
```

---

# 4. Format Check

Specific format follow hona chahiye.

Example:
```text
Email proper format mein hona chahiye
```

---

# Advantages of Data Validation

1. Errors reduce hote hain
2. Data accuracy improve hoti hai
3. System reliability improve hoti hai

---

# Difference Between Decision Tree and Decision Table

| Decision Tree | Decision Table |
|---|---|
| Graphical form | Tabular form |
| Visualization easy | Compact representation |
| Large diagrams possible | Better for multiple conditions |

---

# Important Points to Remember

- Structured analysis system understanding ka systematic method hai.
- Logical model system functions explain karta hai.
- Physical model implementation explain karta hai.
- Context diagram highest level DFD hota hai.
- Data dictionary data information store karta hai.
- DFD data movement show karta hai.
- IPO chart input-process-output explain karta hai.
- HIPO hierarchy structure show karta hai.
- Gantt chart scheduling ke liye use hota hai.
- Pseudo code programming logic explain karta hai.
- Flowchart graphical logic representation hota hai.
- Decision tree decisions show karta hai.
- Data validation incorrect data ko prevent karti hai.

---

# Conclusion

Tools of Structured Analysis:
```text
System ko properly analyze aur design karne mein help karte hain
```

Ye tools:
- planning
- documentation
- communication
- analysis

ko easy aur efficient banate hain.

Structured analysis tools use karke:
```text
Developers better aur more reliable systems create kar sakte hain
```
