# 🖥️ CPU Scheduling Visualizer

<div align="center">

![OS Mini Project](https://img.shields.io/badge/OS%20Mini%20Project-DGCT%202024-00d4ff?style=for-the-badge)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![No Dependencies](https://img.shields.io/badge/Dependencies-None-10b981?style=for-the-badge)

<br/>

**A fully self-contained, single-file web app to simulate and visualize all major CPU Scheduling Algorithms — with interactive Gantt charts and detailed performance metrics.**

<br/>

> ⚡ **Zero setup. No installation. No server. Just open and use.**

<br/>

| 🏫 College | DGCT |
|---|---|
| 📚 Department | B.E Computer Science & Engineering |
| 📅 Semester | 4th Semester |
| 📖 Subject | Operating Systems (OS) |
| 👨‍💻 Student | Nithishkumar S |
| 🎫 Register No | 610524021071 |
| 📆 Academic Year | 2024 |

</div>

---

## 📌 About This Project

**CPU Scheduling** is a core concept in Operating Systems. The OS decides which process in the **Ready Queue** gets CPU time next — this is done by the CPU Scheduler.

This project is an **Operating Systems Mini Project** that implements and visualizes **6 CPU Scheduling Algorithms** in a single HTML file. Everything — the UI, the algorithms, the Gantt chart rendering — runs entirely in the browser using **Vanilla HTML, CSS, and JavaScript**. No frameworks, no libraries, no backend.

---

## ✨ Features

| Feature | Details |
|---------|---------|
| 🎯 **6 Algorithms** | FCFS, SJF, SRTF, Round Robin, Priority (NP & Preemptive) |
| 📊 **Gantt Chart** | Color-coded, proportional blocks with hover tooltips |
| 📈 **Metrics Table** | CT, TAT, WT, RT for every process |
| 📉 **Summary Stats** | Avg Turnaround Time, Avg Waiting Time, Total Processes |
| 📝 **Algorithm Info** | Live description panel for selected algorithm |
| ⊞ **Sample Loader** | One-click preset data for quick testing |
| 🎨 **Dark UI** | Animated grid, glassmorphism cards, glow effects |
| 📱 **Responsive** | Works on desktop and mobile browsers |
| ⚡ **Zero Dependencies** | Pure HTML + CSS + JS — no npm, no pip, no server |

---

## 🚀 How to Run

### Just open the file in your browser!

```
Double-click → CPUSCHEDULING.HTML
```

That's it. No installation, no terminal, no internet required.

> ✅ Works in Chrome, Firefox, Edge, Safari — any modern browser.

---

## 🧠 Algorithms Implemented

### 📖 What is CPU Scheduling?

In a multiprogramming OS, when the CPU is free, the scheduler picks one process from the **Ready Queue** to execute. The goal is to:

- **Maximize** CPU utilization & throughput
- **Minimize** Waiting Time, Turnaround Time & Response Time

---

### 1️⃣ FCFS — First Come First Served

| | |
|--|--|
| **Type** | Non-Preemptive |
| **Strategy** | Processes execute in the order they arrive |
| **Advantage** | Simple, fair, no starvation |
| **Disadvantage** | Convoy Effect — short jobs stuck behind long ones |

---

### 2️⃣ SJF — Shortest Job First

| | |
|--|--|
| **Type** | Non-Preemptive |
| **Strategy** | Always pick the process with the shortest Burst Time |
| **Advantage** | Minimum average Waiting Time among all NP algorithms |
| **Disadvantage** | Starvation of longer processes |

---

### 3️⃣ SRTF — Shortest Remaining Time First

| | |
|--|--|
| **Type** | Preemptive |
| **Strategy** | Always run the process with the least remaining time; preempts on new arrival |
| **Advantage** | Globally optimal average Waiting Time |
| **Disadvantage** | High context-switch overhead; possible starvation |

> SRTF is the **preemptive version of SJF**.

---

### 4️⃣ Round Robin

| | |
|--|--|
| **Type** | Preemptive |
| **Strategy** | Each process gets a fixed **Time Quantum (q)** in circular order |
| **Advantage** | Fair — no starvation; ideal for time-sharing systems |
| **Disadvantage** | High overhead if `q` is too small; poor TAT if `q` is too large |

> Set the **Time Quantum** in the app when selecting Round Robin.

---

### 5️⃣ Priority Scheduling — Non-Preemptive

| | |
|--|--|
| **Type** | Non-Preemptive |
| **Strategy** | Highest priority process (lowest number) runs first from ready queue |
| **Advantage** | Critical processes handled first |
| **Disadvantage** | **Starvation** of low-priority processes |

---

### 6️⃣ Priority Scheduling — Preemptive

| | |
|--|--|
| **Type** | Preemptive |
| **Strategy** | Preempts current process if a higher-priority process arrives |
| **Advantage** | Highly responsive for critical tasks |
| **Disadvantage** | More context switches; starvation risk |

> ℹ️ **Lower priority number = Higher priority** (e.g., Priority 1 runs before Priority 2)

---

## 📐 Metrics Computed

| Metric | Full Form | Formula |
|--------|-----------|---------|
| **CT** | Completion Time | Time when process finishes |
| **TAT** | Turnaround Time | CT − Arrival Time |
| **WT** | Waiting Time | TAT − Burst Time |
| **RT** | Response Time | First CPU Time − Arrival Time |
| **Avg TAT** | Average Turnaround Time | Σ TAT ÷ n |
| **Avg WT** | Average Waiting Time | Σ WT ÷ n |

---

## 💡 How to Use

```
1. Open CPUSCHEDULING.HTML in your browser
2. Select an algorithm from the tab buttons
3. Click "⊞ Load Sample" to auto-fill test processes
   — OR click "+ Add Process" to enter your own data
4. Fill in Arrival Time, Burst Time, and Priority
5. (Round Robin only) Set the Time Quantum
6. Click "▶ Simulate"
7. View the Gantt Chart and Metrics Table
8. Click "↺ Reset" to try another algorithm
```

---

## 📋 Sample Test Data

The app auto-loads this sample on start. You can also load it anytime via **"⊞ Load Sample"**:

| Process | Arrival Time | Burst Time | Priority |
|:-------:|:-----------:|:----------:|:--------:|
| P1 | 0 | 6 | 2 |
| P2 | 1 | 4 | 1 |
| P3 | 2 | 2 | 3 |
| P4 | 4 | 3 | 2 |

> 💡 Try the same data with FCFS, SJF, SRTF, and Round Robin (q=2) — observe how the Gantt chart and average waiting times change!

---

## 🔍 Algorithm Comparison

| Algorithm | Preemptive | Starvation | Avg WT | Best Use Case |
|-----------|:----------:|:---------:|:------:|---------------|
| FCFS | ❌ | ❌ | High | Simple batch processing |
| SJF | ❌ | ✅ Risk | Low | Batch with known burst times |
| SRTF | ✅ | ✅ Risk | Optimal | Time-sharing, known burst times |
| Round Robin | ✅ | ❌ | Medium | Interactive & time-sharing OS |
| Priority NP | ❌ | ✅ Risk | Varies | Priority-based batch jobs |
| Priority P | ✅ | ✅ Risk | Varies | Real-time critical systems |

---

## 🛠️ Tech Stack

| | Technology |
|--|-----------|
| **Structure** | HTML5 — semantic markup |
| **Styling** | Vanilla CSS3 — custom properties, keyframe animations, glassmorphism |
| **Logic** | Vanilla JavaScript (ES6+) — all 6 algorithms, Gantt rendering, metrics |
| **Fonts** | JetBrains Mono + Syne (Google Fonts) |
| **Backend** | None — everything runs in the browser |

---

## 📁 File Info

| File | Size | Description |
|------|------|-------------|
| `CPUSCHEDULING.HTML` | ~37 KB | Complete self-contained app — HTML + CSS + JS in one file |

---

## 📄 Academic Information

```
Subject        :  Operating Systems (OS)
Project Type   :  Mini Project
Topic          :  CPU Scheduling Algorithms — Simulation & Visualization
College        :  DGCT
Department     :  B.E Computer Science & Engineering
Semester       :  4th Semester
Academic Year  :  2025-26
Student        :  Nithishkumar S
Register No    :  610524021071
```

---

## 📄 License

This project is submitted as an academic mini project for the **Operating Systems** course (DGCT, 2024).
Licensed under the [MIT License](LICENSE) — free to use for learning and educational purposes.

---

<div align="center">

**DGCT** · B.E CSE · Semester 4 · Operating Systems Mini Project

Made with ❤️ by **Nithishkumar S** · Reg No: 610524021071

⭐ Star this repo if it helped you understand CPU Scheduling!

</div>
