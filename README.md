
# Project Tracking Dashboard: Real-Time Team Performance Monitoring

## 📋 Project Overview

An Excel-based **Project Tracking Dashboard** designed to provide managers with real-time visibility into team workload and task completion rates.

This tool transforms raw task data into actionable reporting-ready charts by using pivot tables, interactive slicers and dynamic chart.

---

## 🎯 Business Context

### The Problem

**Scenario:**  
A operations team takes over 100 cost centers from a legacy team. This takeover is scheduled in 8 phases and 8 employees take part. Managers need to answer critical questions:
- Which cost center has been migrated by a certain time... by a certain time ?
- Which cost center is still on hold ... by a certain time ?
- How is the workload distributed ... by a certain time ?

**Traditional approach:**
- Weekly status meetings (time-consuming)
- Manual email updates (inconsistent)
- Manual Excel with inconsistent input (different people are using it)
- Spreadsheets with no structure (hard to analyze)

---

### The Solution

Created a **self-service dashboard** where:
1. **Team members** log tasks in a simple "Data Input" sheet via drop downs (no training required)

<img width="990" height="457" alt="image" src="https://github.com/user-attachments/assets/8ee3db7a-9016-4c06-9a3a-88678cd4f007" />
<img width="985" height="451" alt="image" src="https://github.com/user-attachments/assets/fb3ac460-655e-4836-9651-4c4dfb412eb0" />


2. **Managers** access a "Reporting" sheet with **interactive filters** (employee, date range)
![capture_20260219_202037](https://github.com/user-attachments/assets/2d4f8bb6-b40a-4fad-b0b5-2118434a5dcf)


3. **Automated pivot tables** calculate completion rates and workload distribution.

**Result:**  
Managers get instant answers to "Who is doing what?" and "Are we on track?" without status meetings.

---

## 🔍 Methodology

### Four-Sheets Architecture

#### **1. Data Input Sheet (Team-Facing)**

**Purpose:**  
Simple, user-friendly interface for team members to log tasks.

**Columns:**
- Cost center
- Employee drop down (Mr. A, Mr. B, Mr. C)
- Status dropdown (Complete, On Hold, Planned)
- Date

** Key Features:**
- **Data validation** (dropdowns to prevent typos)
- **Simple layout** (no complex formulas visible to users)

**User Experience:**
- Team members open the sheet, add a row, fill in task details (2 minutes)
- No training required (intuitive dropdowns)

---

#### **2. 2 Reporting Sheets (Manager-Facing)**

**Purpose:**  
Interactive dashboard for managers to analyze team performance.
No training required.

**A. Workload by Employee**
<img width="524" height="401" alt="image" src="https://github.com/user-attachments/assets/b9ec77b1-e574-4e85-81fd-f1a7cd6c4fb5" />

**B. Completion Status**

<img width="696" height="353" alt="image" src="https://github.com/user-attachments/assets/1b85fae3-d7da-4440-a8d2-ab30b74b13a5" />

---

#### **3. Tech Sheet (Backend)**

**Purpose:**  
Hidden sheet that stores dropdown lists and reference data.

**Why a separate sheet?**
- Keeps Data Input sheet clean (no clutter)
- Easy to update (add new employees, categories, etc.)
- Centralized reference (all dropdowns pull from one source)

---

## 💡 Key Features

**Before:**
- Manager asks: "How many tasks did Mr. A took over as of XYZ month?"
- Analyst manually filters data, counts rows, correct inconsistent data input, sends email (15 minutes)

**After:**
- Manager opens Reporting sheet, clicks "Mr. A" slicer, sees answer instantly (10 seconds)

**Impact:**  
- Saves 2+ hours per week 
- Reportings can be sent directly to a manager without formally planning a meeting

---

## 🛠️ Technical Implementation

### Excel Features Used

#### **1. Pivot Tables**

**Purpose:**  
Automatically summarize task data by employee and status.

**Configuration:**
- **Rows:** Employee Name
- **Columns:** Status
- **Values:** Count of Task ID
- **Filters:** Start Date (for time slicer)

**Benefit:**  
No formula, no manual counting (pivot table updates automatically when data changes)
