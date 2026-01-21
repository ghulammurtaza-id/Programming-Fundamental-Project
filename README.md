# Secure Vote Project

[![Version](https://img.shields.io/badge/version-1.0.0-blue)](https://github.com/)
[![License](https://img.shields.io/badge/license-MIT-green)](https://opensource.org/licenses/MIT)
[![C Language](https://img.shields.io/badge/language-C-brightgreen)](https://www.iso-9899.info/)

---

## Table of Contents

* [Introduction](#introduction)
* [Features](#features)
* [Installation](#installation)
* [Usage](#usage)
* [Architecture](#architecture)
* [Tech Stack & Dependencies](#tech-stack--dependencies)
* [Contribution Guidelines](#contribution-guidelines)
* [Roadmap](#roadmap)
* [License](#license)
* [Credits](#credits)

---

## Introduction

**Secure Vote Project** is a console-based **electronic voting system** implemented in C. Designed as a university-level project, it simulates real-world voting scenarios with security, authentication, and automated result generation.

This system ensures that voter credentials are encrypted, voting sessions are time-bound, and results are generated automatically, providing a **safe and reliable voting simulation**.

---

## Features

* **Admin Dashboard**: Manage elections, candidates, and voter data.
* **Voter Authentication**: Validates ID and password before voting.
* **Encrypted Passwords**: Basic XOR-based encryption for security.
* **Time-Bound Voting**: Voting session ends automatically after a specified duration.
* **Automated Results**: Generates result files in CSV format.
* **Data Storage**: Uses CSV files for voter info, candidates, and results.
* **Forget Password Handling**: Security questions for recovery.

---

## Installation

### Requirements

* **OS**: Windows
* **Compiler**: Dev-C++ or any C compiler (GCC)
* **Terminal**: Command Line / PowerShell

### Steps to Run

1. **Clone the repository:**

   ```bash
   git clone [https://github.com/yourusername/secure-vote-project.git](https://github.com/yourusername/secure-vote-project.git)
   cd secure-vote-project
   ```

2. **Compile the code:**

   ```bash
   gcc main.c -o securevote.exe
   ```

3. **Run the executable:**

   ```bash
   ./securevote.exe
   ```

---

## Usage

### Admin Login

Use the default admin credentials (set in `config.csv`) to access the dashboard. From here, you can define candidates and upload voter credentials.

### Voting Process

1. Users log in with their ID.
2. The remaining time for the election is displayed.
3. Users cast their vote for their preferred candidate.

### Result Generation

After the voting session ends, results are automatically compiled and saved in the `results/` folder as a CSV file.

#### Example Session:

```text
Welcome to Secure Vote
1. Login
2. Forget Password
Enter choice: 1
Enter ID: 101
Enter Password: ****

Voting Menu:
1. Candidate A
2. Candidate B
Enter your vote: 1
Thank you for voting!
```

---

## Architecture

```text
+------------------+
|    Main Program  |
+------------------+
        |
        v
+------------------+
| Admin Dashboard  |
| - Setup Voting   |
| - Manage CSVs    |
+------------------+
        |
        v
+------------------+
| Voting Engine    |
| - Authenticate   |
| - Record Vote    |
| - Track Time     |
+------------------+
        |
        v
+------------------+
| Result Generator |
| - CSV Output     |
| - Summary        |
+------------------+
```

---

## Tech Stack & Dependencies

* **Language**: C (ANSI C)
* **Compiler**: GCC (via Dev-C++)
* **Data Storage**: CSV (Comma Separated Values)
* **Libraries**: `<stdio.h>`, `<stdlib.h>`, `<string.h>`, `<time.h>`

---

## Contribution Guidelines

1. **Fork** the repository.
2. **Create a new branch**: `git checkout -b feature/your-feature`.
3. **Commit your changes**: `git commit -m "Add some feature"`.
4. **Push to the branch**: `git push origin feature/your-feature`.
5. **Open a Pull Request**.

---

## Roadmap

* [ ] Implement a Graphical User Interface (GUI).
* [ ] Integrate SHA-256 for advanced password hashing.
* [ ] Add support for multiple concurrent elections.
* [ ] Real-time vote count visualization.

---

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

---

## Credits

* **Ghulam Murtaza**  Developer
* **Fast NU University**  Student

