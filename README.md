# 📘 Student API Testing Project

This project demonstrates API testing for a student-level application using industry-standard tools such as **Postman**, **Visual Studio Code**, **GitHub Actions**, and **Jira**. The goal is to understand how to structure, automate, and manage an API testing workflow in a professional environment.

---

## 🚀 Project Overview

- 🧪 Test RESTful APIs using Postman collections
- 🖥️ Develop and manage the project using Visual Studio Code
- 🔁 Automate testing via GitHub Actions (CI/CD)
- 🗂️ Track tasks and bugs with Jira
- 📊 Generate test reports with Newman

---

## 🧰 Tools & Technologies

| Tool              | Purpose                                |
|-------------------|----------------------------------------|
| Visual Studio Code| Code editing and project structure     |
| Postman           | API testing and request design         |
| Newman            | Command-line runner for Postman tests  |
| GitHub Actions    | CI pipeline for automated testing      |
| Jira              | Issue and task tracking                |
| Git / GitHub      | Version control                        |

---

## 📁 Project Structure

api-testing-project/  
│  
├── .github/  
│ ├── workflows/  
│ └── ci.yml   
│  
├── postman/  
│ ├── Airport_Gap.json    
│  
├── reports/  
│ └── newman-report.html   
│  
├── .gitignore  
├── README.md  
├── testCases.md  
├── package.json   
└── jira_Board.md 


## 📦 Setup Instructions

1. **Clone the Repository**
```bash
git clone https://github.com/Aura-Lem/Airport_Gap.git
cd api-testing-project
```

2. **Install Dependencies**
Ensure you have Node.js installed

```bash
npm install -g newman
```

3. **Run Tests with Newman**
```bash
npm run test
```

## 🧑‍💼 Project Management with Jira

All tasks, bugs, and milestones are tracked via Jira.
👉 [Jira Board Link](https://apozeraite.atlassian.net/jira/software/c/projects/AG/boards/67)

Example workflow:

- To-do
- In Progress
- Done

## 📈 Reporting

Test reports are generated automatically using Newman. These reports include:

- Request/response status
- Assertion results
- Pass/fail summary

## 📃 License

This project is intended for educational use only.

## 🙏 Acknowledgements

Tools: Postman, Newman, GitHub Actions, Jira  
IDE: Visual Studio Code