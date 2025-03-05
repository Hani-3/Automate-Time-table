# Project Document: Automatic Time-Table System

## 1. Introduction
The **Automatic Time-Table System** is designed to generate academic timetables efficiently by processing course data from an Excel file. It provides a user-friendly interface to upload data, configure scheduling preferences, and view or download the generated timetables. The system also ensures optimal workload distribution for teachers while resolving scheduling conflicts.

---

## 2. Features
- **User Authentication**: Secure login using email ID and password.
- **Excel File Upload**: Supports an Excel file containing multiple sheets:
  - Courses
  - Time Slots
  - Teachers
  - Credit Points
  - Subject-Teacher Assignments
  - Rooms & Labs
- **Session Selection for Practical Subjects**: Allows users to assign practical sessions for each semester.
- **Teacher Assignment Methods**:
  - **Ratio-wise**: Distributes lectures between two teachers based on credit points.
  - **Workload-wise**: Allocates teachers based on pre-defined workloads while considering subject constraints.
- **Automatic Timetable Generation**: Uses credit points and session constraints to create optimized schedules.
- **Semester Selection for Viewing**: Users can choose which semester’s timetable to display.
- **Teacher Workload Management**: Displays workload distribution for all assigned teachers.
- **Conflict Resolution**:
  - Teacher scheduling conflicts.
  - Subject-practical duration constraints.
  - Recess time handling.
- **Download Functionality**: Allows downloading of generated timetables.

---

## 3. System Workflow
1. **User Login**:
   - The system prompts users to enter an email ID and password.
   - Upon successful authentication, the user is redirected to the file upload page.
2. **Excel File Upload & Data Extraction**:
   - The user uploads an Excel file containing all necessary data.
   - The system extracts data from sheets and validates it.
3. **Session Selection for Practical Subjects**:
   - Users assign practical sessions to different semesters.
   - Example: Semester 1: Sessions 2 & 3, Semester 2: Sessions 5 & 6.
4. **Teacher Assignment Method Selection**:
   - **Ratio-wise**: Lectures are divided based on credit points.
   - **Workload-wise**: Assigns teachers based on their pre-defined workload constraints.
5. **Timetable Generation**:
   - The system processes the input data and generates semester-wise schedules.
   - Ensures no conflicts in teacher assignments.
   - Manages subject-practical durations.
   - Allocates recess times appropriately.
6. **Timetable Selection & Viewing**:
   - The system displays checkboxes for each semester.
   - Users select the semesters they want to view.
   - The selected semester-wise timetables are displayed.
7. **Additional Views**:
   - Button to view teacher workload distribution.
   - Button to download the generated timetables.

---

## 4. Technical Requirements
- **Frontend**:
  - HTML, CSS
- **Backend**:
  - Python (Flask)
- **File Handling**:
  - Use libraries like `pandas` for Excel file parsing in Python.

---

## 5. Timetable Generation Algorithm
1. Extract course, time slots, teacher, credit points, and room data from Excel.
2. Assign practical sessions based on user input.
3. Distribute lectures according to the selected method (Ratio-wise or Workload-wise).
4. Schedule lectures, ensuring no teacher overlaps.
5. Allocate subjects to rooms while considering lab requirements.
6. Implement recess time constraints.
7. Optimize timetable layout and ensure fair workload distribution.
8. Generate the final timetable output.

---

## 6. Conflict Handling Strategies
- **Teacher Overlap**: Ensures a teacher is not scheduled for multiple subjects at the same time.
- **Subject-Practical Duration**: Adjusts the time slots to maintain practical duration consistency.
- **Room Availability**: Ensures no room is double-booked for lectures or labs.
- **Workload Balancing**: Ensures teachers get an appropriate number of classes.
- **Recess Management**: Distributes break times without disrupting schedules.

---

## 7. Expected Outputs
- **Timetable Display**:
  - Semester-wise timetable in tabular format.
- **Workload Report**:
  - Detailed workload distribution per teacher.
- **Downloadable Timetable**:
  - Export options: PDF, Excel, or Printable View.

---

## 8. Conclusion
The **Automatic Time-Table System** is designed to simplify academic scheduling by automating timetable generation based on predefined constraints and user inputs. It ensures fair workload distribution, avoids conflicts, and provides an easy-to-use interface for managing schedules efficiently.
