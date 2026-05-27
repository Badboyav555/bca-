# SYSTEM ANALYSIS AND DESIGN (SAD)

# UNIT – TOOLS OF STRUCTURED ANALYSIS

---

# Introduction to Structured Analysis

Structured Analysis:
```text
A systematic way of analyzing and designing an information system
```
hai.

Iska main purpose:
- system ko properly understand karna
- problems identify karna
- better solution develop karna

hota hai.

Structured analysis mein different:
```text
Tools and techniques
```
use ki jati hain.

Ye tools:
- data flow
- processing
- system structure
- decision making

ko easily explain karte hain.

---

# Objectives of Structured Analysis Tools

1. System ko easily understand karna
2. Complex problems ko simplify karna
3. Better communication provide karna
4. Proper documentation maintain karna
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

System ko understand karne ke liye:
```text
Logical aur Physical models
```
use kiye jate hain.

---

# Logical Model

Logical model:
```text
System kya karta hai
```
ye describe karta hai.

Ye:
- business process
- data flow
- system functions

par focus karta hai.

---

# Example

Library system:
- book issue
- return
- fine calculation

Logical model explain karega:
```text
Kaam kaise hota hai
```

---

# Physical Model

Physical model:
```text
System kaise implement hoga
```
ye explain karta hai.

Ye:
- hardware
- software
- database
- devices

par focus karta hai.

---

# Example

Library system mein:
- barcode scanner
- computer
- printer

physical model ka part hain.

---

# Difference Between Logical and Physical Model

| Logical Model | Physical Model |
|---|---|
| What system does | How system works |
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
Entire system ko single process ke form mein show karta hai
```

---

# Purpose

1. System boundary define karna
2. External entities identify karna
3. Input and output show karna

---

# Components

1. System Process
2. External Entities
3. Data Flow

---

# Example

ATM System:
- customer
- bank server

external entities hain.

---

# Context Diagram Representation

```md
![Context Diagram](images/context-diagram.png)
```

Suggested Image Link:
https://upload.wikimedia.org/wikipedia/commons/7/75/Context_diagram_example.svg

---

# Advantages

1. Easy to understand
2. Simple overview provide karta hai
3. System boundary clear karta hai

---

# DATA DICTIONARY

# Introduction

Data Dictionary:
```text
Collection of information about data elements
```
hota hai.

Ye database ke:
- data names
- types
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

Ye:
- data input
- processing
- storage
- output

ko graphical form mein represent karta hai.

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

Outside user/system show karta hai.

---

# Example

Bank System:
- customer data
- transaction processing
- database storage

DFD mein show hote hain.

---

# DFD Representation

```md
![Data Flow Diagram](images/data-flow-diagram.png)
```

Suggested Image Link:
https://upload.wikimedia.org/wikipedia/commons/3/3d/Data-flow-diagram-example.svg

---

# Advantages of DFD

1. Easy system understanding
2. Better communication
3. Helps in system analysis

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

School admission forms analyze karke:
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
- input data
- processing steps
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

1. Simple understanding
2. Better documentation
3. Easy system planning

---

# HIPO CHART

# Introduction

HIPO:
```text
Hierarchy plus Input Process Output
```
hai.

Ye:
- hierarchy structure
- module details
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

Ye:
- tasks
- starting date
- ending date
- project progress

show karta hai.

---

# Example

Software Development Project:
- planning
- coding
- testing
- implementation

timeline mein show hote hain.

---

# Gantt Chart Representation

```md
![Gantt Chart](images/gantt-chart.png)
```

Suggested Image Link:
https://upload.wikimedia.org/wikipedia/commons/3/37/GanttChartAnatomy.png

---

# Advantages

1. Project management easy
2. Time tracking
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

# Types of Models

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
2. Programming logic clear hota hai
3. Coding easy hoti hai

---

# FLOW CHARTS

# Introduction

Flowchart:
```text
Graphical representation of program logic
```
hota hai.

Ye symbols use karke:
- steps
- decisions
- process flow

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

# Example

Even/Odd checking flowchart.

---

# Flowchart Representation

```md
![Flowchart Example](images/flowchart-example.png)
```

Suggested Image Link:
https://upload.wikimedia.org/wikipedia/commons/5/57/Flowchart_example.png

---

# Advantages

1. Logic understanding easy
2. Error detection easy
3. Better communication

---

# SYSTEM FLOW CHART

# Introduction

System Flowchart:
```text
Entire system ka flow
```
show karta hai.

Ye:
- input
- processing
- output
- storage

sab show karta hai.

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
Graphical representation of decision making process
```
hai.

Ye:
- conditions
- alternatives
- possible results

show karta hai.

---

# Example

Loan Approval System:
- salary check
- age check
- loan approval

decision tree se represent kiya ja sakta hai.

---

# Decision Tree Representation

```md
![Decision Tree](images/decision-tree.png)
```

Suggested Image Link:
https://upload.wikimedia.org/wikipedia/commons/f/f3/CART_tree_titanic_survivors.png

---

# Advantages

1. Easy decision analysis
2. Complex conditions simplify karta hai
3. Better understanding

---

# DECISION TABLE

# Introduction

Decision Table:
```text
Conditions aur actions ko tabular form mein represent karna
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
2. Easy documentation
3. Better decision analysis

---

# DATA VALIDATION

# Introduction

Data Validation:
```text
Input data ko check karna ki wo correct aur valid hai ya nahi
```
hai.

---

# Example

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

Input ki length check hoti hai.

Example:
```text
Mobile number 10 digits ka hona chahiye
```

---

# 4. Format Check

Specific format follow hona chahiye.

Example:
```text
Email format
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
| Easy visualization | Compact representation |
| Complex diagrams possible | Better for multiple conditions |

---

# Important Points to Remember

- Structured analysis system ko analyze karne ki systematic approach hai.
- Logical model system functions show karta hai.
- Physical model implementation details show karta hai.
- Context diagram highest level DFD hota hai.
- Data dictionary data information store karta hai.
- DFD data flow represent karta hai.
- IPO input-process-output show karta hai.
- HIPO hierarchy show karta hai.
- Gantt chart project scheduling ke liye use hota hai.
- Pseudo code programming logic explain karta hai.
- Flowchart graphical logic representation hota hai.
- Decision tree decision making show karta hai.
- Data validation incorrect data ko prevent karti hai.

---

# Conclusion

Tools of Structured Analysis:
```text
System ko properly understand aur design karne mein help karte hain
```

Ye tools:
- analysis
- documentation
- planning
- communication

ko easy banate hain.

Using structured analysis tools:
```text
Developers better, accurate aur efficient systems create kar sakte hain
```
