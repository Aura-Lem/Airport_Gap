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
│ ├── api-tests.postman_collection.json  
│ └── dev_environment.postman_environment.json  
│  
├── reports/  
│ └── newman-report.html   
│  
├── .gitignore  
├── README.md 
├── testCases.md 
├── package.json   
└── Jira-Board-Link.md 


## 📦 Setup Instructions

1. **Clone the Repository**
```bash
git clone https://github.com/your-username/api-testing-project.git
cd api-testing-project
```

2. **Install Dependencies**
Ensure you have Node.js installed

```bash
npm install -g newman
```

3. **Run Tests with Newman**
```bash
newman run postman/api-tests.postman_collection.json \
  -e postman/dev_environment.postman_environment.json \
  -r cli,html \
  --reporter-html-export reports/newman-report.html
```

4. **Open Report**
Open the reports/newman-report.html file in your browser to view the test results.

## 🧑‍💼 Project Management with Jira

All tasks, bugs, and milestones are tracked via Jira.
👉 [Jira Board Link](https://apozeraite.atlassian.net/jira/software/c/projects/AG/boards/67)

Example workflow:

- To-do
- In Progress
- Done

## 📈 Reporting

Test reports are generated automatically using Newman and exported to reports/ folder. These reports include:

- Request/response status
- Assertion results
- Pass/fail summary

## 📃 License

This project is intended for educational use only.

## 🙏 Acknowledgements

Instructor: [Instructor Name]  
Tools: Postman, Newman, GitHub Actions, Jira  
IDE: Visual Studio Code