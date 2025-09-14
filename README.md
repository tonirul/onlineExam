# 📝 Exam Web App

A lightweight **browser-based exam platform** with an **admin panel**, **student exam interface**, and **result dashboard**.  
Everything runs **locally in the browser** using **HTML, CSS, and JavaScript**, with no backend server required.  
Questions and exam settings are saved in **LocalStorage**, making it easy to test and deploy on any static hosting service.

---

## 🚀 Features

### 👩‍🏫 Admin Panel (`admin.html`)
- Upload questions via **CSV file**.
- Configure exam:
  - Exam name  
  - Duration (minutes)  
  - Marks for correct/wrong answers
- Edit questions directly in the interface.
- Save exam data to **LocalStorage** for students to attempt.

### 👨‍🎓 Exam Interface (`index.html`)
- Candidate name prompt before starting.
- Section-wise tabs and palette for navigation.
- Options:
  - Save Answer  
  - Mark & Review  
  - Clear Response  
  - Save & Next  
- Question palette with color-coded states:
  - **Green** → Answered  
  - **Orange** → Marked for Review  
  - **Grey** → Not Visited  
- **Question Paper View**: quick navigation to any question.
- **Timer** (auto-submit when time expires).
- **Anti-Cheating Measures**:
  - Warns if the user switches tabs / refreshes.
  - Auto-submits after 3 violations.
- **Analysis Page** after submission:
  - Summary (Correct, Wrong, Unattempted, Total Score).
  - Pie chart visualization (Chart.js).
  - Section-wise detailed table.
  - Option to restart exam with same data.

### 📊 Results Dashboard (`result.html`)
- Lists all student attempts stored in LocalStorage.
- Displays:
  - Student name  
  - Exam name  
  - Date  
  - Score  
  - Violations  
  - Section-wise stats
- **Export to CSV** option for reports.

---

## 🛠️ Installation & Setup

1. Clone or download this repository.
2. Open `admin.html` in a browser to **upload exam questions** and save settings.
   - CSV format should include headers:  
     ```
     id,section,question,options,answer
     1,Math,What is 2+2?,2|3|4|5,4
     2,Science,Water formula?,H2O|O2|CO2,H2O
     ```
   - Options must be separated with `|`.
3. Open `exam.html` to **attempt the test**.
4. After submission, reports are available in `result.html`.

---

## 📦 Tech Stack

- **Frontend**: HTML, CSS, JavaScript  
- **Parsing**: [PapaParse](https://www.papaparse.com/) for CSV import  
- **Charts**: [Chart.js](https://www.chartjs.org/) for analysis visualization  
- **Storage**: LocalStorage for saving exam data and results  

---

## 📸 Screenshots (Concept)

- `admin.html`: Upload CSV & configure exam  
- `exam.html`: Student exam interface with palette and timer  
- `result.html`: Student reports table  

---

## ⚠️ Limitations

- Runs only on the client (no server/database).
- Results stored locally → clearing browser storage removes data.
- Not secure for high-stakes exams (for demos/mock practice only).

---

## 📌 Future Enhancements

- ✅ CSV download of detailed student responses  
- ✅ Randomized question order & shuffling options  
- ✅ Authentication for admin/student  
- ✅ Backend integration with database  

---

## 👨‍💻 Author

Developed as a **mock exam platform** demo project.  
Feel free to fork and improve! 🎉
