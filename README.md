# CS384 Attendance Tracker

## 📋 Project Overview
This project automates **attendance tracking** and **Excel report generation** for the CS384 course. Using **QR code-based attendance records**, the script processes timestamps to mark attendance and generates a **highlighted Excel report** showing attendance status.

The project ensures:
- Accurate tracking of attendance.
- Detection of invalid/false attendance entries.
- Highlighting of attendance status in Excel (absent, partial, or full).
- Handling of students who add/drop the course dynamically.

---

## 🚀 Features
- **Timestamp-based Attendance Tracking** (6-8 PM window).  
- **False Attendance Detection**: Identifies timestamps outside the lecture hours.  
- **Excel Report Generation** with color-coded attendance:
  - **Red**: Absent (0)  
  - **Yellow**: Partial Attendance (1)  
  - **Green**: Full Attendance (2)  
- Calculates **extra attendance** and **net attendance percentage**.  
- Easy configuration via input files (student list, attendance data, and class dates).

---

## 📂 Folder Structure
### 📄 Input Files
- **input_attendance.csv**: Contains raw attendance data from QR code scans.
- **stud_list.txt**: List of enrolled students with their roll numbers and names.
- **dates.txt**: Record of dates when classes were held.

### 📄 Output Files
- **output_attendance.csv**: Processed attendance data in CSV format.
- **styled_attendance.xlsx**: Final attendance report with highlighting in Excel format.
- **attendance_script.py**: Python script that processes the attendance data.

---

## 🛠️ How to Run

### Prerequisites
Make sure you have **Python 3.x** installed. Install the required libraries using:
```bash
pip install pandas openpyxl matplotlib seaborn
```
## Running the Notebook

### Clone the Repository:
```bash
git clone https://github.com/AyushSoni14/CS384-Attendance-Tracker.git
cd CS384-Attendance-Tracker
```
### Place input files (stud_list.txt, dates.txt, input_attendance.csv) in the project directory.
### Open and Run the Notebook
Use the following command to open the Jupyter Notebook:
```bash
jupyter notebook Mid_Sem_Mini_Project.ipynb
```
### Check the outputs:
- output_attendance.csv: Intermediate output.
- styled_attendance.xlsx: Final report with highlighted attendance status.
## 📄 Input File Formats

### 1. **stud_list.txt**
This file contains the roll number and name of students, separated by a space.  
**Example**:
```plaintext
2201ME22 Ayush Soni
```
### 2. **dates.txt**
```plaintext
classes_taken_dates = ["10/10/2024", "17/10/2024"]
```
### 3. **input_attendance.csv**
This file contains the attendance data with timestamps and roll numbers along with student names.
```plaintext
Timestamp,Roll
06/08/2024 18:18:23,2201MM26 Rudra Goyal
06/08/2024 18:18:26,2201CE30 Lakshya Pratap Singh
06/08/2024 18:18:26,2201CB19 Chhavi Bamoriya
06/08/2024 18:18:28,2201CE31 Mayank Kumar
06/08/2024 18:18:31,2201CB35 Nakka Supraja
```
## 📊 Output Excel File
The generated styled_attendance.xlsx contains:
- Roll Number and Name
- Attendance for Each Date within the 6-8 PM window.
- False Attendance Count
- Total Attendance Marked
- Extra Attendance Detected
- Net Attendance Percentage
## 📅 Lecture Details
- **Time:** Every Tuesday, 6:00 PM - 8:00 PM
- **Attendance Tracking:** Two consecutive lectures, allowing two attendance entries per student per session.

## 🧑‍💻 Code Highlights
- **Reading Input Files:** Uses pandas for handling CSV and text files.
- **Timestamp Validation:** Checks if attendance falls between 6-8 PM.
- **False Attendance Detection:** Marks attendance outside allowed hours.
- **Excel Styling:** Uses pandas and openpyxl to color-code attendance status.
